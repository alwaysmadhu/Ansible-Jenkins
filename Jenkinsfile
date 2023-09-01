pipeline {
    ageny any
    stages {
        stage ('Execute Playbook') {
            ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            
        }
    }
}
