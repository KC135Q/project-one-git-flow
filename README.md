Day to day team git workflow
===

> This assumes that you have already created or cloned the project repo to your local development machine.  And, that you are currently in that (project-one) repo.

1. Development (coding) prep
- `git pull origin master`
- `git checkout -b branch-name`
- // Write some code
- `git add -A`
- `git commit -m "Message to Self"`
- `git pull origin master`
  (This is an optional step but helps reduce merge conflicts during the GitHub pull request)
- // Check for merge conflicts
- `git push origin branch-name`

2. Pull Request Review (PRR)
- On GitHub.com go to the branch you just pushed up
- Create a Pull Request
- Repo Admin reviews and approves (or denies) Pull Request
- Once merge is complete, delete the branch on GitHub.com 
- // Slack the team to inform them that there is a new Mast Branch

3. Recover (local)
- `git checkout master`
- `git pull origin master`
- `git branch -D branch-name`
- // Go back to 1. Development and start again with a new branch-name

## branch-name tips
- lowercase with dashes
- use initials then issue or task
- Examples
> `dk-initial`

> `aa-db-setup`

> `kk-html-css-setup`

> `dk-pseudocode`

> `aa-db-models`

> `kk-start-jquery`

Next will be deploying an app through firebase as shown [here](https://firebase.google.com/docs/hosting/deploying)