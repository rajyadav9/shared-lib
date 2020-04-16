@Library('my-shared-library') _
pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
stages{
	stage ("Shared Library Test") {
  	log {
    		type = "warning"
   	         message = "This is a log message!"
            }
      }
}
}
