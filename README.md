# github-node-pkg

## How can I update this package:

  1. Authenticate your npm inside the github registry

    ```
      npm login --scope=@<ORGANIZATION-NAME> --registry=https://npm.pkg.github.com
    ```

    After be running the command, the cli will ask you about your username and password, for the username use the same you use in the scope, and
    to the password you need to use a Github personal access token which grant access to package read/write.
  
  2. After your changes and commits, execute the command 

    ```
      npm release
    ```
  
