productivity-scripts
===================

A git hook for Redmine  integration. Redmine has the functionality that if configured, allows commits
to appear as comments in the story. this is acheived by appending `refs #redmine_id` to the commit message.

The hook reads the Redmine story id from the branch name where it is defined and appends it to the start of every message.

### Instructions

1. Copy this file and paste it into the `.git/hooks` folder of the current project.
2. While in the `.git/hooks` folder, enter the following command `chmod u+x prepare-commit-msg`
3. Congrats you're set!

Branches can now be created with the formats below and once commit messages are entered, the redmine story id will be
prepended to the messages in an automated fashion.

```
git branch st{redmine_story_id}_commit_description_here
git branch feature/st{redmine_story_id}_commit_description_here
git branch hotfix/st{redmine_story_id}_commit_description_here
```
