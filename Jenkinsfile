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
	    sleep(60)
            echo 'This step will never be run'
         }
      }
      
      // Execute when branch = 'main'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'main'
	 }
         steps {
	    sleep(60)
            echo 'BASIC WHEN - Main Branch!'
         }
      }
	// Execute when branch = 'feature'
      stage("Build") {
         steps {
	    sleep(10)
            echo 'Build'
         }
      }
      stage("Move To PROD") {
         steps {
	    sleep(10)
            echo 'Deployed To PROD'
         }
      }
   }
}
