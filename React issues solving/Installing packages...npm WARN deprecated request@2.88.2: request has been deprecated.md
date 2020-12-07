# see https://github.com/request/request/issues/3142 
Here is the solution:

Open your command prompt and uninstall angular/cli by using

```npm uninstall -g angular-cli``` command.

Remove node_modules directory and then clear the cache by using
```npm cache clear --force`` command.

Remove
C:\Users<username>\AppData\Roaming\npm\
you can remove the folder this way
rmdir C:\Users<username>\AppData\Roaming\npm\ /s
and
C:\Users<username>\AppData\Roaming\npm-cache.
you can remove the folder this way
rmdir C:\Users<username>\AppData\Roaming\npm-cache /s

Now try to install the angular/cli@latest by using npm install -g @angular/cli@latest command.
