@Library('my-shared-library') _
pipeline {
    agent none
    stages {
        stage ('Example') {
            steps {
                // log.info 'Starting' 
                script { 
                     type= "warning"
		     message = "This is a log msg"
                     log.info 'Starting'
                    log.warning 'Nothing to do!'
                }
            }
        }
    }
}
