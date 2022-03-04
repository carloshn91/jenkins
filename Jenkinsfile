pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 14.x', configId: '<config-file-provider-id>') {
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