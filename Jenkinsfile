// pipeline {
//      agent any
//      stages {
//         stage('Installing dependencies') {
//             steps {
//                 bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/node_modules'
//                 bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/package-lock.json'
//                 bat 'npm cache clean --force'
//                 bat 'npm i'
//             }
//         }
//      }
//     stages {
//         stage('Build') { 
//             steps {
//                 bat 'npm start' 
//             }
//         }
//     }
// }

pipeline {
    agent any

    stages {
        stage('Installing dependencies') {
            steps {
                // bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/node_modules'
                // bat 'rm -rf /var/lib/jenkins/workspace/TML_Drishit/package-lock.json'
                bat 'npm cache clean --force'
                bat 'npm i'
            }
        }
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
//         stage('Deploy') {
//             steps { 
//                 sh 'sudo rm -rf /home/sankey/design-mvp1/CVP_FMS_Design/dist'
//                 sh 'sudo cp -r /var/lib/jenkins/workspace/dev/CVP_FMS_Design/dist /home/sankey/design-mvp1/CVP_FMS_Design'
//                 sh 'sudo service nginx restart'
//             }
//         }
    }
}


