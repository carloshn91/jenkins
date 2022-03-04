pipeline {
    agent none
    stages {
        stage('Select micro services') {
            input {
                message "Select all micro services to deploy"
                ok "All selected!"
            }
        }
        stage('Select single service') {
            input {
                message "Select single micro services to deploy?"
            }
        }
    }
}