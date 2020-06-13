pipeline {
    agent any
    stages {
        stage("Run unit tests"){
          steps {
            script {
              try {
              echo "Hello, CONDITIONAL----"
              } finally {
                junit 'nosetests.xml'
              }
            }
          }
        }
        stage ('Speak') {
            steps{
              echo "Hello, CONDITIONAL"
            }
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
        stage('build-test') {
            steps {
                sh "docker --version"
                echo "test:color"
            }
        }
}
