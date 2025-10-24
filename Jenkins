pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // If you have a Git repo, you can pull it here
                // git 'https://github.com/your-repo/DevOpsPython.git'
                echo 'Assuming code is already on Jenkins workspace'
            }
        }

        stage('Run BMI Python Script') {
            steps {
                // Run the Python script
                sh 'python3 bmi.py'  // Use 'python bmi.py' if Python 3 is default
            }
        }
    }

    post {
        success {
            echo 'BMI Script ran successfully!'
        }
        failure {
            echo 'Something went wrong while running the BMI script.'
        }
    }
}
