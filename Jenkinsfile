import hudson.model.Result
import hudson.model.Run
import jenkins.model.CauseOfInterruption.UserInterruption
import com.cloudbees.groovy.cps.NonCPS
@Library('my-shared-library') _
pipeline {
    agent any

    stages {
           stage('Set environment variables')
            {
                steps {
//                     script{
//                     def buildNumber = env.BUILD_NUMBER as int
//                     if (buildNumber > 1) milestone(buildNumber - 1)
//                     milestone(buildNumber)
                    abortPreviousRunningBuilds()
                     }
              }

         }


    def abortPreviousRunningBuilds() {
      def hi = Hudson.instance
      def pname = env.JOB_NAME.split('/')[0]

      hi.getItem(pname).getItem(env.JOB_BASE_NAME).getBuilds().each{ build ->
        def exec = build.getExecutor()

        if (build.number != currentBuild.number && exec != null) {
          exec.interrupt(
            Result.ABORTED,
            new CauseOfInterruption.UserInterruption(
              "Aborted by #${currentBuild.number}"
            )
          )
          println("Aborted previous running build #${build.number}")
        } else {
          println("Build is not running or is current build, not aborting - #${build.number}")
        }
      }

 }





























//                         env.REGION = "us-west-2"
//                         env.PROJECT_NAME = 'admin-core-web'
//                         env.SERVICE_PATH = ""
//                         env.ECS_SERVICE_NAME = "hrx-admin-core-web-service"
//                         env.SSM_PARAM_PREFIX = "hrx-core-web"
//                         env.aaa = "my name is raj"
//                         echo "racnckcknckncksnc"

//                         env.build_disp=currentBuild.rawBuild.getPreviousBuildInProgress()
//                         echo "buildaaaaaa"
//                         echo "${env.build_disp}"
                    }
                }
            }
// stage ('env') {
//             steps {
//             script{
//             env.XYZ= "ABCABCABC"
//                                 zzz()
//
//             }
//     }
//     }
//         stage ('Example') {
//             steps {
//                 // log.info 'Starting'
//                  abc(
//                  REGION: "${REGION}",
//                  PROJECT_NAME: "${PROJECT_NAME}",
//                  )
//                  echo "jai shree ram"
//                 echo "${env.XYZ}"
//
//             }
//     }
// //     stage('Set variables')
// //                 {
// //                     steps {
// //                             aws1 = abc(
// //                                                    REGION: "${REGION}",
// //                                                    PROJECT_NAME: "${PROJECT_NAME}",
// //                                                    ).aws
// // //                          zzz(
// // //                                 aws: "${aws1}"
// // //                             )
// //
// //                     }
// //                // }
// }
// }