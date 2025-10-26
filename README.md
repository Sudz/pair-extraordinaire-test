# pair-extraordinaire-test
## Purpose
This repository is created to unlock the 'Pair Extraordinaire' achievement on GitHub by creating a co-authored commit.

## Process for Unlocking Pair Extraordinaire Achievement
### Steps:
1. Create a new repository or use an existing one
2. Create a new branch for your changes
3. Make changes to a file (e.g., README.md)
4. Create a commit with a co-author using the 'Co-authored-by' trailer
5. Open a pull request from the feature branch to the main branch
6. Merge the pull request

### Co-authored-by Format
In the commit message, add the following at the end:
```
Co-authored-by: Name <email@example.com>
```

### Example Commit Message:
```
Add documentation for Pair Extraordinaire achievement

Co-authored-by: GitHub User <noreply@github.com>
```

## Automation Notes
- Use Git CLI or GitHub API to create co-authored commits programmatically
- The Co-authored-by trailer must be in the commit message body (not the title)
- Multiple co-authors can be added by including multiple Co-authored-by lines
- Achievement is unlocked when the co-authored PR is merged

## Process for Unlocking Quickdraw Achievement
### Overview
The Quickdraw achievement is earned by closing an issue within 5 minutes of opening it.

### Steps:
1. Navigate to the repository's Issues tab
2. Click "New issue" button
3. Enter issue title: "Practice Quickdraw Achievement"
4. Add description noting the issue will be closed within 5 minutes for automation practice
5. Click "Create" to submit the issue
6. Immediately click "Close issue" button (must be within 5 minutes of creation)

### Automation Notes
- Can be automated using GitHub API or CLI
- Issue must be closed within 5 minutes of creation time
- The close action should be performed as quickly as possible after creation
- This is replicable and can be done multiple times for testing automation workflows
- Example API workflow:
  ```bash
  # Create issue
  ISSUE_URL=$(gh issue create --title "Practice Quickdraw Achievement" --body "This issue will be closed within 5 minutes for automation practice.")
  
  # Extract issue number
  ISSUE_NUM=$(echo $ISSUE_URL | grep -o '[0-9]*$')
  
  # Close issue immediately
  gh issue close $ISSUE_NUM
  ```
