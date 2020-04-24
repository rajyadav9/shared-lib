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
                            milestone label: '', ordinal:  Integer.parseInt(env.BUILD_ID) - 1
                            milestone label: '', ordinal:  Integer.parseInt(env.BUILD_ID)
                            env.cls = currentBuild.getBuildCauses()
                            echo "${env.cls}"
                        }
                    }
            }
      }