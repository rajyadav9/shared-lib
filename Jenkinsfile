@Library('my-shared-library') _
pipeline {
    agent any

    stages {
    stage('Set environment variables')
            {
                steps {
                    script{
                        env.REGION = "us-west-2"
                        env.PROJECT_NAME = 'admin-core-web'
                        env.SERVICE_PATH = ""
                        env.ECS_SERVICE_NAME = "hrx-admin-core-web-service"
                        env.SSM_PARAM_PREFIX = "hrx-core-web"
                    }
                }
            }

        stage ('Example') {
            steps {
                // log.info 'Starting' 
                script {

//              type= "warning"
//              message = "This is a log msg"
//              echo "abcxeyjkdbj"
//              log.info 'Starting'
//              log.warning 'Nothing to do!'

                 abc(
                 REGION: "${REGION}",
                 PROJECT_NAME: "${PROJECT_NAME}",

                 )

                }
            }
    }
}
}