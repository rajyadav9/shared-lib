import hudson.model.Result
import hudson.model.Run
import jenkins.model.CauseOfInterruption.UserInterruption
package net.my.jenkins.workflow
import com.cloudbees.groovy.cps.NonCPS
@Library('my-shared-library') _
pipeline {
    agent any

    stages {
    stage('Set environment variables')
            {
                steps {
                    script{
                    zzz()
                        env.REGION = "us-west-2"
                        env.PROJECT_NAME = 'admin-core-web'
                        env.SERVICE_PATH = ""
                        env.ECS_SERVICE_NAME = "hrx-admin-core-web-service"
                        env.SSM_PARAM_PREFIX = "hrx-core-web"
                        env.aaa = "my name is raj"
                        echo "racnckcknckncksnc"
                        echo "${env.XYZ}"

                        env.build_disp=currentBuild.rawBuild.getPreviousBuildInProgress()
                        echo "buildaaaaaa"
                        echo "${build_disp}"
                    }
                }
            }
stage ('env') {
            steps {
            script{
            env.XYZ= "ABCABCABC"
                                zzz()

            }
    }
    }
        stage ('Example') {
            steps {
                // log.info 'Starting' 
                 abc(
                 REGION: "${REGION}",
                 PROJECT_NAME: "${PROJECT_NAME}",
                 )
                 echo "jai shree ram"
                echo "${env.XYZ}"

            }
    }
//     stage('Set variables')
//                 {
//                     steps {
//                             aws1 = abc(
//                                                    REGION: "${REGION}",
//                                                    PROJECT_NAME: "${PROJECT_NAME}",
//                                                    ).aws
// //                          zzz(
// //                                 aws: "${aws1}"
// //                             )
//
//                     }
               // }
}
}