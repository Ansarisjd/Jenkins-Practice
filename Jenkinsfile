pipeline{
    agent any

    stages{
        stage('Checkout Code'){
            steps{
                echo 'Checking out code from github....'
                checkout scm
                }
        }
        stage('Install Dependencies'){
            steps{
                echo "Installing Dependencies"
                sh 'python3 -m pip install requirements.txt'
            }
        }

        stage('Run Test'){
            steps{
                echo "Running Test"
                sh 'pytest'
            }
        }

        stage('Build'){
            steps{
                echo "Building the application"
                sh 'python app.py'
            }
        }
    }


}
