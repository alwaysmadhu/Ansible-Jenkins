pipeline {
    agent any
    stages {
        stage ('install httpd') {
            steps {
                ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            }
        }
        stage ('restart httpd'){
            steps {
                ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/restart-apache.yaml'
            }
        }
    }
}
