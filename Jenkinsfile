pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage('Creating Files Website') {
            steps {
                sh 'npx create-docusaurus@latest website classic'
               }
            }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}