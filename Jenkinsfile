pipeline {
    agent any

    stages {
        stage('Pull Code') {
            steps {
                // Pull the latest code from the repository
                git branch: 'main', url: 'https://github.com/ghouse80701/Deploying_Job.git'
            }
        }

        stage('execute the ansible playbook') {
            steps {
                script {
                    sh 'cd dev && ansible-playbook deployment.yaml'
                }
            }
        }
    }
}
