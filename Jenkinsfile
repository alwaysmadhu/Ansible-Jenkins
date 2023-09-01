pipeline {
    agent any
    stages {
        stage ('clone repo'){
            steps {
                sh ""git clone https://github.com/alwaysmadhu/Ansible-Jenkins.git""
            }
        }
        stage ('Execute Playbook') {
            steps {
            ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            }
        }
        stage ('restart web server') {
            steps {
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
