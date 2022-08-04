# Creating a release

You will need to have the project on your computer and NPM installed.

## How to create a release?

The whole process summarized 

- Get all the PRs since last release.
- Create a new branch with the updated version and changelog for the team to review.
- Create Github release.
- Release it 🎉

### Get the PRs
We are using [auto-changelog](https://github.com/cookpete/auto-changelog) to gather all the changes made from release to release.

First we will need to update the version in the `/package.json` (the one in root directory) to corresponding version.

Then get the name of the Stooa's remote repo in your config. In our case is `upstream` because this is how we named it.

To check yours run
```batch
git remote -v
```
And make sure you use the Stooa repo, not your fork.


Then, once we know the remote name, we get all the PRs since last release and update the `changelog.md` in the project just running

```batch
npx auto-changelog --remote=[name_of_your_remote]
```

This command will output our updated `CHANGELOG.md`

### Create new Release branch

Now create the new branch to push all the changes made to the changelog. This way the team could review that everything is correct to approve it!

### Create Github release

With the approved branch, we head to [github releases](https://github.com/Stooa/Stooa/releases) to create a new one with the same number in the tag release we previously used in the `package.json`. 

The content of the release will be the last changes in the `CHANGELOG.md`

### Release 🎉
You can save a draft to further revision or just release it!

Well done, you've made a Stooa release 😄
