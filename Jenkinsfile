#!/usr/bin/env groovy
pipeline {
   agent any
    
   stages {
      // Execute when branch = 'feature'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'feature/new_card_development'
	 }
         steps {
	    sleep(5)
            echo 'BASIC WHEN - Feature Branch!'
         }
      }
	// Execute when branch = 'feature'
      stage("Unit Test") {
         steps {
	    sleep(5)
            echo 'Unit Test Completed'
         }
      }
      stage("Isolation Test") {
         steps {
	    sleep(5)
            echo 'Isolation Test Completed'
         }
      }
      stage("Sonar Check") {
         steps {
	    sleep(5)
            echo 'Sonar Check Completed'
         }
      }
   }
}
