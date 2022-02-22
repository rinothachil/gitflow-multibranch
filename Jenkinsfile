#!/usr/bin/env groovy
pipeline {
   agent any
    
   stages {
   
      // skip a stage while creating the pipeline
      stage("A stage to be skipped") {
         when {
            expression { false }  //skip this stage
         }
         steps {
	    sleep(45)
            echo 'This step will never be run'
         }
      }
      // Execute when branch = 'develop'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'develop'
	 }
         steps {
	    sleep(45)
            echo 'BASIC WHEN - Develop Branch!'
         }
      }
   }
}
