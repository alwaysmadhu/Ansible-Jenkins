pipeline {
    agent any
    stages {
        stage ('Execute Playbook') {
            steps {
            ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            }
        }
    }
}
