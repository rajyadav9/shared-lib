//@Library('my-shared-library') _
pipeline {
    agent any
    stages {
        stage ('Example') {
            steps {
                // log.info 'Starting' 
                script {
                checkout scm
            sh('cd jenkins && git init && git add --all . && git commit -m init &> /dev/null')
            def repoPath = sh(returnStdout: true, script: 'pwd').trim() + "/jenkins"
            library identifier: 'local-lib@master', retriever: modernSCM([$class: 'GitSCMSource', remote: repoPath])
@Library('my-shared-library') _

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