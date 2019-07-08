#!/usr/bin/env groovy

/**
@Author 
SridharKumar
**/

node {
   def mvnHome
   stage('SCM Checkout') { // for display purposes
      // Get some code from a GitHub repository
             git'https://github.com/galamsiva2020/mqwebservice-simple-file.git'

   }
  
stage('Maven Build') {
      // Run the maven build
	  
      withEnv(["MVN_HOME=C:/Users/raju_/Downloads/apache-maven-3.6.1"]) {
         if (isUnix()) {
            sh '"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package'
         } else {
            bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/)
         }
      }
   }
   stage('TestResults') {
	   archive "target/**/*"
	   //archiveArtifacts 'target/*.jar'
      junit 'target/surefire-reports/*.xml'
      //archiveArtifacts 'target/*.jar'
   }
}

