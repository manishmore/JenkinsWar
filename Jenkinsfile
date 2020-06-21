import jenkins.model.*


pipeline {
    agent any
    stages {
        stage("Run unit tests"){
          steps {
            script {
              try {
              echo "Hello, CONDITIONAL----"
              test
              }catch(Exception ex) {
                println("Catching the exception");
                currentBuild.result = 'UNSTABLE'
              } finally {
                echo "finally..."
                echo currentBuild.result
              }
            }
          }
        }
        stage ('Speak') {
            steps{
              echo "Hello, CONDITIONAL"
              showMavenVersion("--maven")
            }
          }
        stage('build') {
                steps {
                    echo "Size ${params.size}"
                }
        }
        stage('deploy') {
                steps {
                    echo "Color ${params.color}"
                }
        }
    }
}

def pipeline
node {
  pipeline = load 'pipeline.groovy'
      stage('end of the file') {
            echo "===== ${WORKSPACE}"
            sh 'pwd'
            sh 'ls -al'
            sh 'env'
            print "Result " + pipeline.testMethod()
      }
}


def showMavenVersion(String a) {
     try {
     def tmpHM = ['test','test2','test3','tests6']
     tmpHM.each{
      try {
        echo "TEST:"+it
         test090
       } catch(Exception e2) {
        echo "Error:" + e2
      }
    }
      } catch (Exception e) {
       echo "Error" + e
       throw new Exception(e);
     } finally {
     echo "finally::" + a
     }
}
