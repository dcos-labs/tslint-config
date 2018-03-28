# tslint-config
Shared tslint config for DCOS projects using typescript

## Commits
You should follow [conventional commit](https://conventionalcommits.org/) formatting rules, as they provide a framework to write explicit messages that are easy to comprehend when looking through the project history and enable automatic change log generation.

These Guidelines were written based on [AngularJS Git Commit Message Conventions](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#-commit-message-guidelines).


```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

## Release / Publishing

After your PR is merged to `master` to cut a release is very simple, assuming you are `on master` branch follow the steps below.

Fetch all git tags
```
git fetch origin --tags
```

Then run the command to automatically update the `package.json`, `changelog.md` and create a new release commit.
```
npm run release
```

Now push the latest commit and the tag created (_run `git tag` to see all tags_).
```
git push origin master && git push origin TAG_VERSION
```

And finally publish to npm.
```
npm publish
```


