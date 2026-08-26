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
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Test'){
            steps{
                echo "Running Test"
                sh 'python3 -m pytest'
            }
        }

        stage('Build'){
            steps{
                echo "Building the application"
                sh 'python3 app.py'
            }
        }
    }


}
