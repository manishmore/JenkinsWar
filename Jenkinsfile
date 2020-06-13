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
        stage("Determine build file") {
            String jenkinsFile = ParamsFile.groovy
        }
    }

    // Here the Jenkins build file is loaded and executed
    load jenkinsFile
}

def showMavenVersion(String a) {
    echo a
}
