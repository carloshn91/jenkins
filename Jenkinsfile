pipeline {
    agent docker { image 'node:14' }
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