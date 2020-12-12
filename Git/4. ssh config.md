Please follow the steps to add ssh key into bitbucket account to solve your issue.

1. Open git bash terminal and enter the command ```ssh-keygen -t rsa -C "your email address"```
2. Enter passphrase (leave it blank) and enter
3. Enter the same phrase again (leave it blank) and enter
Copy the ```id_rsa.pub``` file content from where it is residing in your system (C:\Users\username\.ssh)
Login to bitbucket account and click top right most user icon ->bitbucket settings->ssh keys under security menu then paste into key field and save it. 
6.Restart your git bash terminal and enter git init command and add ssh git repository location ```git@bitbucket.org:username/repository_name.git``` which is present in your bitbucket repository.
Enjoy!
