pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Cloning the repository...'
                git branch: 'main', url: 'https://github.com/abhyudaya13/pes2ug22cs022_jenkins'
                
                script {
                    // Replace 'hello.cpp' with the actual filename in your repo
                     sh 'g++ -o output_file main/hello.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    sh './output_file'  // Run the compiled C++ program
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment commands here if needed
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline execution failed!'
        }
    }
}
