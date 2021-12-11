pipeline {
  agent any 
  stages {
    stage("Delete Workspace"){
      steps {
        cleanWs deleteDirs: true
        checkout scm
      }
    }
    stage("Build Application"){
      steps  {
        bat '''
        mvn clean package 
        '''
      }
    }
  }
