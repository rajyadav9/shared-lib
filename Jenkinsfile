// import hudson.model.Result
// import hudson.model.Run
// import jenkins.model.CauseOfInterruption.UserInterruption
// import com.cloudbees.groovy.cps.NonCPS
import hudson.model.Result
import jenkins.model.CauseOfInterruption
@Library('my-shared-library') _
pipeline {
    agent any

    stages {
            stage('Stop Old Build') {
                        steps {
//                             milestone label: '', ordinal:  Integer.parseInt(env.BUILD_ID) - 1
//                             milestone label: '', ordinal:  Integer.parseInt(env.BUILD_ID)
                            script{
                            env.cls = currentBuild.getBuildCauses()
                            echo "${env.cls}"
                            echo "${tag}"
         // if(currentBuild.getPreviousBuildInProgress()){
          env.aa =currentBuild.getPreviousBuild().actions.find{ it instanceof ParametersAction }?.parameters.contains("${tag}")
                            echo "${env.aa}"
                            echo "jai shrree ram"
//                             echo "${env.aa[10]}"
                            echo "${tag}"

                            echo "hahahah"
                            env.BUILD_CAUSE = currentBuild.getBuildCauses()[0].shortDescription.contains("push by") ? 'push' : 'manual'
                            env.BUILD_CAUSE11 = currentBuild.getBuildCauses()
                            echo "${env.BUILD_CAUSE}"
                            echo"nananana"
                            echo "${env.BUILD_CAUSE11}"
                            delay(10000)

//}

                            }
                        }
                    }
            }
      }