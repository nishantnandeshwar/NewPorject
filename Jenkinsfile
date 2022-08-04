pipeline {
     agent any
     stages {
        stage('Installing dependencies') {
            steps {
                bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/node_modules'
                bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/package-lock.json'
                bat 'npm cache clean --force'
                bat 'npm i'
            }
        }
     }
    stages {
        stage('Build') { 
            steps {
                bat 'npm start' 
            }
        }
    }
}
