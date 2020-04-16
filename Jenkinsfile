pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
@Library('my-shared-library') _
stages{
	stage ("Shared Library Test") {
  	log {
    		type = "warning"
   	         message = "This is a log message!"
            }
      }
}
}
