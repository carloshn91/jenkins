pipeline {
    agent { 
        docker { 
            image 'node'
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