pipeline {
    agent any
   
    stages {
         stage('Clone repository') { 
            steps { 
                script{
                checkout scm
                }
            }
        }

        stage('Build') { 
            steps { 
                 sh 'echo Build'
		 sh 'install npm -y'
		 sh 'npm init -y'
		 sh 'npm install express@4.17.1'
         sh 'node server.js'

            }
        }
        stage('Test'){
            steps {
                 sh 'echo Test'
            }
        }
        stage('Deploy') {
            steps {
               sh 'echo Deploy'
            }
        }
    }
}
