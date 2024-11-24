pipeline {
    agent any

    stages {
        // Stage 1: Clone GitHub Repository
        stage('Clone GitHub Repository') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/Jasvanth-30/practice-repo.git' // Replace with your repo URL
            }
        }

        // Stage 2: Execute Java Program
        stage('Run Java Program') {
            steps {
                echo 'Running Java Program...'
                script {
                    sh '''
                    cd java_program
                    javac HelloWorld.java
                    java HelloWorld
                    '''
                }
            }
        }

        // Stage 3: Execute Python Program
        stage('Run Python Program') {
            steps {
                echo 'Running Python Program...'
                script {
                    sh '''
                    cd python_program
                    python3 hello_world.py
                    '''
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed!'
        }
    }
}
