#!groovy

/**
 * This is the pipeline for developing BWC.
 *
 * You can find the shared library 'pipeline' code here:
 **/

pipeline {
  agent { 
    master 
  }
  stages {
    stage('Build') {
      steps {
        echo 'Step: Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Step: Testing...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Step: Deploying...'
        sh "chmod +x HelloWorld.sh "
        sh ". / HelloWorld.sh "
      }
    }
  }
}
