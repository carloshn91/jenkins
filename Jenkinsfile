pipeline {
    agent { 
        docker { 
            image 'node:14'
        }
    }
    stages {
        stage('Install') {
            steps {
                npx 'create-docusaurus@latest website classic'
            }
        }
        stage('Build') {
            steps {
                npm 'run build'
            }
        }
    }
}