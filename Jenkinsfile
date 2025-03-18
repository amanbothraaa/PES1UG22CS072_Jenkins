pipeline {
    agent any

        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploy'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
