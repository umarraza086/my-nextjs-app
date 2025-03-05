pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/umarraza086/my-nextjs-app.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                dir('my-nextjs-app') {  // Move into the project folder
                    sh 'npm install'
                }
            }
        }
        
        stage('Build') {
            steps {
                dir('my-nextjs-app') {  
                    sh 'npm run build'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                dir('my-nextjs-app') {  
                    sh 'npm start &'
                }
            }
        }
    }
}
     
