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
      // Run the maven build (compile and tesrting  packaging)
	mvnHome ='C:/Users/raju_/Downloads/apache-maven-3.6.1'  
    }
   stage('TestResults') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
   }
}

