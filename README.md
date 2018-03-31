﻿# angular-cli-docker for AWS-Codebuild
 - This image is meant to shorten the length of time it takes to get the build env configured for building projects on CodeBuild since the billing is by the minute and the free tier only allows for 100 minutes/month. Your mileage may vary for the size of your project but the spinup time for env config should be greatly sped up by this
 - In order to leverage the preloaded node_modules directory you will want to modify your AWS buildspec.yml file for your project to create a symlink to this directory. Or somehow figure out how to instruct AWS CodeBuild to use the `/usr/src` directory as the working directory when it clones and builds the project. You will also find a sample builspec.yml file that works well with this docker
 - It expects a package.json in the working directory and will run an NPM install for those dependecies. 
 - The default directory for this is `/usr/src`
 - python is included
 - The built docker image is based on Alpine(28mb linux install) is 288 MB at the time of writing this with my base project dependencies included. 
 
 
