# Heroku

## Deploy commands
- Deploy a local branch to heroku
```bash
git push -f heroku local_branch_name:main
```

## Setup for vite
- Setting -> Buildpacks: add `heroku/nodejs` to the top

```
heroku/nodejs
heroku/ruby
```