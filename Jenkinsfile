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
                            env.bb = currentBuild.getPreviousBuildInProgress()
                            env.cc = currentBuild.getPreviousBuild()
                            echo "${env.bb}"
                            echo "full build"
                                                        echo "${env.bb}"

                            echo "current tag"
                            echo "${tag}"
         // if(currentBuild.getPreviousBuildInProgress()){
 env.aa = currentBuild.getPreviousBuild().getRawBuild().actions.find{ it instanceof ParametersAction }?.parameters.find{it.name == 'tag'}?.value
                            echo "previous tag"
                            echo "${env.aa}"
                            echo "jai shrree ram"
//                             echo "${env.aa[10]}


                            echo "hahahah"
                            env.BUILD_CAUSE = currentBuild.getBuildCauses()[0].shortDescription.contains("push by") ? 'push' : 'manual'
                            env.BUILD_CAUSE11 = currentBuild.getBuildCauses()
                            echo "${env.BUILD_CAUSE}"
                            echo"nananana"
                            echo "${env.BUILD_CAUSE11}"

//}

                            }
                        }
                    }
            }
      }