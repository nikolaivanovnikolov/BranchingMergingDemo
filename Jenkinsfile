#!groovy
/** @Library('pipeline') _ **/

/**
 * This is the pipeline for developing BWC.
 *
 * You can find the shared library 'pipeline' code here:
 *
 * https://sqbu-github.cisco.com/Broadsoft/pipeline
 **/

stages {
 stage('checkout') {
  checkout scm
 }
 stage('deploy') {
  echo 'branch name ' + env.BRANCH_NAME
 
  if (env.BRANCH_NAME.startsWith("Feature_")) {
   echo "Deploying to Dev environment after build"
  } else if (env.BRANCH_NAME.startsWith("Release_")) {
   echo "Deploying to Stage after build and Dev Deployment"
  } else if (env.BRANCH_NAME.startsWith("master")) {
   echo "Deploying to PROD environment"
  }
 
  sh ""
  "chmod +x HelloWorld.sh 
  . / HelloWorld.sh ""
  "
 
 }
}
