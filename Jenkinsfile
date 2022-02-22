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
	    sleep(90)
            echo 'This step will never be run'
         }
      }
      
      // Execute when branch = 'feature'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'feature/new_card_development'
	 }
         steps {
	    sleep(90)
            echo 'BASIC WHEN - Feature Branch!'
         }
      }
	// Execute when branch = 'feature'
      stage("Deploy") {
         steps {
	    sleep(10)
            echo 'Deploy'
         }
      }
      stage("Move To QA") {
         steps {
	    sleep(10)
            echo 'Moved To QA'
         }
      }
      stage("Move To UAT") {
         steps {
	    sleep(10)
            echo 'Moved To UAT'
         }
      }
   }
}
