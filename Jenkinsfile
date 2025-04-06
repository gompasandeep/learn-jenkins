pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'echo "This is Build"'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'echo "This is Test"'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'echo "This is Deploy"'
                   // error "pipeline failed"
                }
            }
        }
    }

    post {
        always{
            echo "This section runs always"
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}
