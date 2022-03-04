pipeline {
    agent any

    tools {nodejs "node"}

    stages {
        stage('Install') {
            steps {
                sh 'npx create-docusaurus@latest website classic'
               }
            }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}