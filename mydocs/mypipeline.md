# CICD

## GitHub
+) When code is committed and pushed to the GitHub repository that is linked to the CircleCI platform, it will trigger CircleCI.

## CircleCI
+) CircleCI uses the /udagram/udagram-api/.circleci/config.yml file to determine what needs to be done. The following tasks are performed:

++) Server: The code is built and exported, all environment variables from the CircleCI configuration are written to a .env file, and the code is then archived to a zipfile. Finally, the AWS CLI is used to upload the archive to S3.
++) Frontend: The build script provided in the package.json file is run, and then the AWS CLI is used to upload the resulting assets to S3.

