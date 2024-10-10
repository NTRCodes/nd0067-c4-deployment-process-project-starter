## Continuous Integration
#### GitHub
When developers commit and push their code to the GitHub repository that is linked to the CircleCI platform, CircleCI listens to changes on GitHub and a build commences.

#### CircleCI
CircleCI is configured via the .circleci/config.yml. Udagram, has 2 jobs: frontend & backend.

- Frontend: Runs the build script given in the package.json file. Then uses AWS CLI to upload assets to S3.
- Backend: Runs the build script, exports all environment variables from CircleCI configuration to a .env file, then runs the archive script. Then uses AWS CLI to upload archive to S3.