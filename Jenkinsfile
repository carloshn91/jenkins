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
                sh 'cd website/ && npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'cd website / && npm run build'
            }
        }
    }
}