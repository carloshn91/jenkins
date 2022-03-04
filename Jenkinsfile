pipeline {
    agent any

    tools {nodejs "node"}

    stages {
       stage('Removing files') {
           steps {
                sh 'rm -rf /var/jenkins_home/workspace/Jenkins/website'
               }
            }
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
                sh 'cd website/ && npm run build'
            }
        }
   }
}

def notifyBuild(String buildStatus = 'STARTED') {
  buildStatus = buildStatus ?: 'SUCCESSFUL'
  def colorName = 'RED'
  def colorCode = '#FF0000'
}