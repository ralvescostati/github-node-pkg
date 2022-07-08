# github-node-pkg

## How can I update this package?

  1. Authenticate your npm inside the github registry

  ```bash
    npm login --scope=ralvescostati --registry=https://npm.pkg.github.com
  ```

  After be running the command, the cli will ask you about your username and password, for the username use the same you use in the scope, and
  to the password you need to use a Github Personal Access Token which grant access to package read/write.
  
  2. After your changes and commits, execute the command 

  ```bash
    npm run release
  ```

## How can i use this package in other projects?
  
  1. Create a .npmrc file, and inside the file copy this content:

    @ralvescostati:registry=https://npm.pkg.github.com
    //npm.pkg.github.com/:_authToken=${NPM_TOKEN}

  NPM_TOKEN is the token required to use your package in another project. NPM_TOKEN will be stored in your environment variable in production, while in development you want to store that in a .bashrc file or similar depending on your OS; that way you can use the same token to authenticate multiple projects without having an .env file in each of them.

  You can use the same Github Access Token you already created in the previous step.

  ```bash
    export NPM_TOKEN=<GA_PERSONAL_TOKEN>

    npm install @ralvescostati/githubjs
  ```