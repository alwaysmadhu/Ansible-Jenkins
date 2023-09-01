pipeline {
    agent any
    stages {
        stage ('git clone'){
            steps {
                sh "git clone
        stage ('Execute Playbook') {
            steps {
            ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            }
        }
    }
}
