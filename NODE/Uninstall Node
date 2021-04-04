How do I completely uninstall Node.js, and reinstall from beginning (Mac OS X)
- Apparently, there was a /Users/myusername/local folder that contained a include with node and lib with node and node_modules. How and why this was created instead of in my /usr/local folder, I do not know.

- Deleting these local references fixed the phantom v0.6.1-pre. If anyone has an explanation, I'll choose that as the correct answer.
  
- You may need to do the additional instructions as well:
  `sudo rm -rf /usr/local/{lib/node{,/.npm,_modules},bin,share/man}/{npm*,node*,man1/node*}`
  which is the equivalent of (same as above)...
  `sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node* /usr/local/lib/dtrace/node.d ~/.npm ~/.node-gyp `
  or (same as above) broken down...
  
  To completely uninstall node + npm is to do the following:
    1. go to /usr/local/lib and delete any node and node_modules
    2. go to /usr/local/include and delete any node and node_modules directory
    3. if you installed with brew install node, then run brew uninstall node in your terminal
    4. check your Home directory for any local or lib or include folders, and delete any node or node_modules from there
    5. go to /usr/local/bin and delete any node executable
- You may also need to do:
  `sudo rm -rf /opt/local/bin/node /opt/local/include/node /opt/local/lib/node_modules`
  `sudo rm -rf /usr/local/bin/npm /usr/local/share/man/man1/node.1 /usr/local/lib/dtrace/node.d`
  
Source:- [How do I completely uninstall Node.js, and reinstall from beginning (Mac OS X)](https://stackoverflow.com/questions/11177954/how-do-i-completely-uninstall-node-js-and-reinstall-from-beginning-mac-os-x)
