#!/usr/bin/env groovy
pipeline {
   agent any
    
   environment {
      VALUE_ONE = '1'
      VALUE_TWO = '2'
      VALUE_THREE = '3'
   }
    
   stages {
   
      // skip a stage while creating the pipeline
      stage("A stage to be skipped") {
         when {
            expression { false }  //skip this stage
         }
         steps {
            echo 'This step will never be run'
         }
      }
      
      // Execute when branch = 'main'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'main'
	 }
         steps {
            echo 'BASIC WHEN - Main Branch!'
         }
      }
             // Execute when branch = 'develop'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'develop'
	 }
         steps {
            echo 'BASIC WHEN - Develop Branch!'
         }
      }
   }
}
