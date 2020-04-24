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
           stage('Set environment variables')
            {
                steps {
                        script{
                        //iterate through current project runs
                        build.getProject()._getRuns().iterator().each{ run ->
                          def exec = run.getExecutor()
                          //if the run is not a current build and it has executor (running) then stop it
                          if( run!=build && exec!=null ){
                            //prepare the cause of interruption
                            def cause = { "interrupted by build #${build.getId()}" as String } as CauseOfInterruption
                            exec.interrupt(Result.ABORTED, cause)
                          }
                        }

                       // zzz()
//                               def hi = Hudson.instance
//                               def pname = env.JOB_NAME.split('/')[0]
//
//                               hi.getItem(pname).getItem(env.JOB_BASE_NAME).getBuilds().each{ build ->
//                                 def exec = build.getExecutor()
//
//                                 if (build.number != currentBuild.number && exec != null) {
//                                   exec.interrupt(
//                                     Result.ABORTED,
//                                     new CauseOfInterruption.UserInterruption(
//                                       "Aborted by #${currentBuild.number}"
//                                     )
//                                   )
//                                   println("Aborted previous running build #${build.number}")
//                                 } else {
//                                   println("Build is not running or is current build, not aborting - #${build.number}")
//                                 }
//                               }

                     }
              }

         }

}


}
