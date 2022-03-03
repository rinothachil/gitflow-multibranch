#!/usr/bin/env groovy
pipeline {
   agent any
    
   stages {
      // Execute when branch = 'feature'
      stage("BASIC WHEN - Branch") {
         when {
            branch 'feature/paralell-pipeline'
	 }
         steps {
	    sleep(2)
            echo 'BASIC WHEN - Feature Branch!'
         }
      }
	// Execute when branch = 'feature'
      stage("Checkout Code") {
         steps {
	    sleep(2)
            echo 'Code Checkout Completed'
         }
      }
      stage("Unit Test") {
         steps {
	    sleep(5)
            echo 'Unit Test Completed'
         }
      }
      stage("ArchUnit Test") {
         steps {
	    sleep(5)
            echo 'ArchUnit Test Completed'
         }
      }
      stage("Isolation Test") {
         steps {
	    sleep(5)
            echo 'Isolation Test Completed'
         }
      }
      stage("OWASP Check") {
         steps {
	    sleep(5)
            echo 'OWASP Check Completed'
         }
      }
      stage("Sonar Check") {
         steps {
	    sleep(5)
            echo 'Sonar Check Completed'
         }
      }
     stage("Merge To Develop") {
         steps {
	    sleep(2)
            echo 'Merge the Source with Develop'
         }
      }
   }
}
