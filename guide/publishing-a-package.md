# Publishing a package

Publishing a package is only supported for git repositories. Preferably hosted on GitHub.

### Log in

To publish a package you need to log in through the CLI with an access token. You can find your access token [here](https://grillpm.vercel.app/settings). Log in or create an account if you haven't already. Then go to the Authorization tab and copy your token. If you haven't generated a token before, click New.

To login with the CLI, run this command and paste your access token:

```
$ grill login
? paste your token here (found on Account > Settings > Authorization)
 › *paste token here*
```

### Publish

You are now ready to publish your package. To do so, run the [publish](../commands/publish.md) command. The output might look something like this:

```
$ grill publish
     Package MyProject
     Version 0.1.0
      Commit dc50795202dc73c3b0726ae1748f5779dc8d3f88
             " initial commit "

? Publish? (y/n) ›
```

Hit the `Y` key to confirm the version and commit to be published. If you have uncommitted changes, <mark style="color:red;">`(dirty)`</mark> will be displayed before the commit message. If the version already exists or if the commit does not exist on the remote, the command will fail.

When publishing a package for the first time, you will be prompted to select a remote url for the package.

### Done

Your package is now available to everyone and can be found on the [website](https://grillpm.vercel.app/).

