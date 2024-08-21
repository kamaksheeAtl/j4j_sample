pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Cloning the Git repository
                    git 'https://github.com/your-repo.git'
                    
                    // Building the Java application
                    sh 'mvn clean package'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    // Deploying the application to a server
                    sh 'ssh user@server "mkdir /path/to/deploy"'
                    sh 'scp target/your-app.jar user@server:/path/to/deploy'
                }
            }
        }
    }
}
