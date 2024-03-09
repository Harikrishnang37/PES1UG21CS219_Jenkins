pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is Build stage."
                build 'PES1UG21CS219-1'
                sh 'g++ ./new_hello.cpp -o output'
                echo "Build Stage Successful. Yay"
            }
        }
        stage('Test') { 
            steps {
                echo "This is Test stage." 
                sh './output'
                echo "Test Stage Successful. Yippee"
            }
        }
        stage('Deploy') { 
            steps {
                echo "This is Deploy stage."
                echo "Deployment Success. OMG wow!"
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}
