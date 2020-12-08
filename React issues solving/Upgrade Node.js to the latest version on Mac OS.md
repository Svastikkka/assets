Here's how I successfully upgraded from v0.8.18 to v0.10.20 without any other requirements like brew etc, (type these commands in the terminal):

``` sudo npm cache clean -f``` (force) clear you npm cache
```sudo npm install -g n``` install n (this might take a while)
```sudo n stable``` upgrade to the current stable version
Note that sudo might prompt your password.

Additional note regarding step 3: stable can be exchanged for latest, lts (long term support) or any specific version number such as 0.10.20.

If the version number doesn't show up when typing node -v, you might have to reboot.

These instructions are found here as well: davidwalsh.name/upgrade-nodejs
More info about the n package found here: npmjs.com/package/n
More info about Node.js' release schedule: github.com/nodejs/Release
