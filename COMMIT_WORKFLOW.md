# Commit Workflow Guide

## Committing Changes Without Pushing

When working on features or fixes, it's often useful to commit your changes locally before pushing them to the remote repository. This allows you to:

- Save your work incrementally
- Create a clean history of changes
- Review your commits before sharing with the team
- Make adjustments or squash commits before pushing

### Basic Workflow

1. **Make your changes** to the code or assets

2. **Stage your changes**:
   ```bash
   git add .
   # or for specific files:
   git add path/to/file
   ```

3. **Commit locally** (without pushing):
   ```bash
   git commit -m "Your descriptive commit message"
   ```

4. **Review your commits** (optional):
   ```bash
   git log --oneline
   git show HEAD
   ```

5. **Push when ready**:
   ```bash
   git push origin your-branch-name
   ```

### Best Practices

- **Commit early and often**: Make small, focused commits while working
- **Write clear commit messages**: Describe what changed and why
- **Review before pushing**: Check your commits with `git log` before pushing
- **Test your changes**: Ensure your code works before pushing to remote

### Example: Working on a Feature

```bash
# Make some changes
# ...

# Commit locally
git add Assets/Scripts/PlayerController.cs
git commit -m "Add player jump functionality"

# Make more changes
# ...

# Commit again
git add Assets/Scripts/PlayerController.cs
git commit -m "Adjust jump height and gravity"

# Review your work
git log --oneline -3

# When satisfied, push to remote
git push origin feature/player-movement
```

### When to Push

- When you're ready to share your work with the team
- Before switching to work on a different machine
- At the end of your work session
- When you want to create a backup of your work
- Before creating a pull request

### Unity-Specific Tips

- Always commit after making significant Unity Editor setting changes
- Commit `.meta` files along with their associated assets
- Use meaningful commit messages for scene changes
- Consider committing before and after importing packages

## Questions?

If you have questions about the git workflow, reach out to the team lead or check the main README.md for more information.
