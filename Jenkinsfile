pipeline {
    agent node
    stages {
        stage('Install') {
            steps {
                sh 'npm install -g npx && \
                    npx create-docusaurus@latest website classic'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}