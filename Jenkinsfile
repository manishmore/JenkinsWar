pipeline {
    agent any
  try {
    stages {
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
    } finally {
        echo "IN finally stage..."
        //emailext subject: "${env.JOB_NAME} - Build # ${env.BUILD_NUMBER} - FAILURE (${e.message})!", to: "me@me.com",body: "..."
        //throw e; // rethrow so the build is considered failed
    }
}
