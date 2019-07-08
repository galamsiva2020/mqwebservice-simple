#!/usr/bin/env groovy

/**
@Author 
SridharKumar
**/

node {
   def mvnHome
   stage('SCM Checkout') { // for display purposes
      // Get some code from a GitHub repository
             
      //mvnHome = 'C:/Users/raju_/Downloads/apache-maven-3.6.1'
   }
   /**
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
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
   }
}
**/
