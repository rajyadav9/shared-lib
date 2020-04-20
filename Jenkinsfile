//@Library('my-shared-library') _
pipeline {
    agent any

    stages {
    stage ('Example') {
                steps {
                    // log.info 'Starting'
                    sh """
                    cd /Users/raj.yadav/.jenkins/workspace/shared-lib-demo@libs/my-shared-library
                    cp -r jenkins/vars .
                   """
                    }
                }

        @Library('my-shared-library') _
        stage ('Example') {
            steps {
                // log.info 'Starting' 
                script {

             type= "warning"
             message = "This is a log msg"
             echo "abcxeyjkdbj"
             log.info 'Starting'
             log.warning 'Nothing to do!'
                }
            }
    }
}
}