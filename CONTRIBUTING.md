# Contributing to Steel Evolution

Thank you for your interest in contributing to Steel Evolution! 🎮🤖

This document provides guidelines for contributing to the project. Following these guidelines helps maintain code quality and makes the contribution process smooth for everyone.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)

---

## Code of Conduct

This project follows a simple code of conduct:
- Be respectful and considerate
- Welcome newcomers and help them learn
- Focus on what's best for the community and the game
- Provide constructive feedback

## How Can I Contribute?

### 🐛 Reporting Bugs

Found a bug? Help us fix it!

1. **Check existing issues** - Someone might have already reported it
2. **Use the Bug Report template** - It helps us gather all needed info
3. **Include details:**
   - Clear description
   - Steps to reproduce
   - Expected vs actual behavior
   - Platform (Android/iOS)
   - Device info
   - Game version
   - Screenshots if applicable

[Create a Bug Report →](https://github.com/matt729/Steel-Evolution/issues/new?template=bug_report.md)

### 💡 Suggesting Features

Have an idea? We'd love to hear it!

1. **Check existing issues** - Might already be planned
2. **Use the Feature Request template**
3. **Explain:**
   - What problem it solves
   - How it would work
   - Impact on players
   - Estimated effort

[Suggest a Feature →](https://github.com/matt729/Steel-Evolution/issues/new?template=feature_request.md)

### ⚖️ Balance Feedback

Think something's too strong/weak?

1. **Use the Balance Issue template**
2. **Include data:**
   - Current stats
   - Win rates
   - Player feedback
   - Proposed changes
   - Expected impact

[Report Balance Issue →](https://github.com/matt729/Steel-Evolution/issues/new?template=balance_issue.md)

### 🔧 Contributing Code

Ready to code? Awesome!

1. **Pick an issue** - Check [Issues](../../issues) or [Project Board](../../projects)
2. **Comment** - Let others know you're working on it
3. **Fork & Branch** - Create a feature branch
4. **Code** - Follow our coding standards
5. **Test** - Make sure it works
6. **PR** - Submit a pull request
7. **Review** - Address feedback
8. **Merge** - Celebrate! 🎉

---

## Development Workflow

### 1. Setup Development Environment

```bash
# Fork the repo on GitHub, then clone YOUR fork
git clone https://github.com/YOUR_USERNAME/Steel-Evolution.git
cd Steel-Evolution

# Add upstream remote
git remote add upstream https://github.com/matt729/Steel-Evolution.git

# Install dependencies (if Unity)
# Open in Unity Hub 2022.3 LTS

# OR if Flutter
cd client/flutter
flutter pub get
```

### 2. Create a Branch

```bash
# Always branch from develop
git checkout develop
git pull upstream develop

# Create feature branch
git checkout -b feature/your-feature-name
```

**Branch naming convention:**
- `feature/` - New features
- `bugfix/` - Bug fixes
- `balance/` - Balance changes
- `ui/` - UI improvements
- `docs/` - Documentation

### 3. Make Changes

- Write clean, readable code
- Follow coding standards (see below)
- Add comments for complex logic
- Write/update tests
- Update documentation

### 4. Commit Your Changes

```bash
git add .
git commit -m "feat(combat): implement critical hit system"
```

See [Commit Messages](#commit-messages) for convention.

### 5. Push to Your Fork

```bash
git push origin feature/your-feature-name
```

### 6. Create Pull Request

1. Go to your fork on GitHub
2. Click "New Pull Request"
3. Base: `matt729/Steel-Evolution` `develop`
4. Compare: `your-fork` `feature/your-feature-name`
5. Fill out the PR template
6. Submit!

---

## Coding Standards

### C# (Unity)

Follow [Microsoft C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)

**Key Points:**
```csharp
// PascalCase for public members
public class CombatSystem
{
    public int MaxHealth { get; set; }
    
    // camelCase for private members
    private float attackSpeed;
    
    // Use explicit types when clear
    public void CalculateDamage(int baseDamage)
    {
        float modifier = 1.5f;
        int finalDamage = (int)(baseDamage * modifier);
    }
    
    // XML comments for public APIs
    /// <summary>
    /// Calculates critical hit damage
    /// </summary>
    /// <param name="baseDamage">Base damage value</param>
    /// <returns>Damage with crit multiplier</returns>
    public float CalculateCritDamage(float baseDamage)
    {
        return baseDamage * 1.5f;
    }
}
```

### Dart (Flutter)

Follow [Effective Dart](https://dart.dev/guides/language/effective-dart)

**Key Points:**
```dart
// lowerCamelCase for variables and functions
class CombatSystem {
  final int maxHealth;
  double _attackSpeed;
  
  // Use var for obvious types
  void calculateDamage(int baseDamage) {
    var modifier = 1.5;
    var finalDamage = (baseDamage * modifier).toInt();
  }
  
  // Doc comments with ///
  /// Calculates critical hit damage
  /// 
  /// Returns damage with 1.5x crit multiplier
  double calculateCritDamage(double baseDamage) {
    return baseDamage * 1.5;
  }
}
```

### General Rules

✅ **DO:**
- Write self-documenting code
- Keep functions small and focused
- Use meaningful variable names
- Add comments for complex logic
- Follow DRY (Don't Repeat Yourself)
- Handle errors gracefully
- Write tests for new features

❌ **DON'T:**
- Commit commented-out code
- Leave TODO without issue number
- Use magic numbers (define constants)
- Ignore warnings
- Commit unformatted code
- Push broken code

### Code Formatting

**Unity (C#):**
- Use Visual Studio default formatting
- Or run: Tools → Format Document

**Flutter (Dart):**
```bash
# Auto-format before committing
flutter format .
```

---

## Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/) for clear history.

### Format

```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

### Types

- `feat:` - New feature
- `fix:` - Bug fix
- `balance:` - Game balance change
- `ui:` - UI/UX improvement
- `perf:` - Performance improvement
- `refactor:` - Code refactoring
- `test:` - Adding tests
- `docs:` - Documentation
- `build:` - Build system
- `ci:` - CI/CD changes
- `chore:` - Maintenance

### Scope

Component affected: `combat`, `gacha`, `equipment`, `ui`, `backend`, etc.

### Examples

```bash
# Feature
git commit -m "feat(combat): implement auto-battle system"

# Bug fix
git commit -m "fix(gacha): correct pity counter reset bug"

# Balance change
git commit -m "balance(proto): reduce starting ATK from 12 to 10"

# UI improvement
git commit -m "ui(main-hub): redesign character display"

# With body
git commit -m "feat(fusion): add fusion system

- Implement fusion stat calculation
- Add fusion UI screens
- Create fusion animation

Closes #42"
```

### Rules

- Use present tense ("add" not "added")
- Use imperative mood ("move" not "moves")
- Don't capitalize first letter
- No period at the end
- Limit first line to 72 characters
- Reference issues with `Closes #XX`

---

## Pull Request Process

### Before Submitting

- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] No new warnings/errors
- [ ] Tests pass
- [ ] Build succeeds

### PR Template

When you create a PR, fill out all sections:

1. **Description** - What does this PR do?
2. **Type of Change** - Feature, bugfix, etc.
3. **Related Issues** - Link issues
4. **Changes Made** - List changes
5. **Testing** - How you tested
6. **Screenshots** - If UI changes
7. **Checklist** - Complete all items

### Review Process

1. **Automated Checks** - CI/CD runs
2. **Code Review** - Maintainer reviews
3. **Feedback** - Address comments
4. **Approval** - PR approved
5. **Merge** - Merged to develop

**Timeline:**
- Initial review: Within 48 hours
- Follow-up reviews: Within 24 hours

### After Merge

```bash
# Update your fork
git checkout develop
git pull upstream develop
git push origin develop

# Delete feature branch
git branch -d feature/your-feature-name
git push origin --delete feature/your-feature-name
```

---

## Testing Guidelines

### Manual Testing

- Test on at least one device (Android or iOS)
- Test happy path (normal usage)
- Test edge cases
- Test error scenarios
- Verify no performance regression

### Unit Tests (if applicable)

```csharp
// Unity (C#)
[Test]
public void CalculateDamage_WithCrit_Returns150Percent()
{
    var combat = new CombatSystem();
    float baseDamage = 100f;
    
    float result = combat.CalculateCritDamage(baseDamage);
    
    Assert.AreEqual(150f, result);
}
```

---

## Project Structure

```
Steel-Evolution/
├── client/                 # Game client
│   ├── Assets/            # Unity assets
│   └── lib/               # Flutter code
├── backend/                # Backend services
│   ├── supabase/          # Database, auth
│   └── n8n-workflows/     # Automation
├── docs/                   # Documentation
├── assets-source/          # Source assets
└── tools/                  # Development tools
```

---

## Questions?

- 💬 [GitHub Discussions](https://github.com/matt729/Steel-Evolution/discussions)
- 🐛 [Report Issues](https://github.com/matt729/Steel-Evolution/issues)
- 📧 Email: [via GitHub profile]

---

## Recognition

Contributors will be recognized in:
- README credits section
- Release notes
- In-game credits (for significant contributions)

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to Steel Evolution! 🚀🤖**

Your efforts help make this game better for everyone.
