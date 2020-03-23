pipeline {
    agent {
        docker { 
            image 'obohovyk/node-jenkins:latest'
            args '-u 0:0'
        }
    }
    stages {
        stage('Node version') {
            steps {
                sh 'node --version'
                sh 'npm i'
            }
        }
    }
    post{
        success {
            sh "echo 'Pipeline completed successfully.'"
        }
        failure{
            sh "echo 'Pipeline failed.'"
        }
    }
}
