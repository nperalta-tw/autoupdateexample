# autoupdateexample
electron auto update example

# Getting started
1. You will need the latest version of node and npm.
2. Clone this repo `git clone https://github.com/nperalta-tw/autoupdateexample.git`
3. In your preferred terminal, navigate to the project notification-module.
4.  Execute `npm ci`.  If there is an error with this command, you likely need to update your npm via `npm install -g npm`. If neither works, just use `npm install`.
5. Create a new repo, example `autoupdateexample`, and create a token with repo permissions.
6. At the root of the project, create a file called `electron-builder.yml`, and fill out the config.
- `appId: com.example.app`
- `publish:` 
	- `provider: github`
	- `token: < github project token >`
7. `git remote add origin https://github.com/nperalta-tw/autoupdateexample.git`
8. Stage your project for release, `npm run deploy`
9. Navigate to releases in your github repo, and publish the release.
10. Download the executable, and run the program. Pay attention to the version number.
11. In your local project, in package.json, change the version number, save the project, add, commit, and push.  Then `npm run deploy` one last time.
12. Navigate to releases in your github repo again, and publish the latest release.
13. Quit the app.  Reopen it, and the updater will trigger.  
