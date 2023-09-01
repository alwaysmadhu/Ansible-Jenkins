pipeline {
    agent any
    stages {
        stage ('clone repo'){
            steps {
              sh "git clone https://github.com/alwaysmadhu/Ansible-Jenkins.git"
            }
        }
        stage ('Execute Playbook') {
            steps {
              ansiblePlaybook credentialsId: 'ApacheWeb', disableHostKeyChecking: true, installation: 'ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/httpd.yaml'
            }
        }
        stage('Restart Apache2') {
            steps {
              sshagent(['ApacheWeb']) {
                ssh -A ubuntu@16.171.253.118 "sudo service apache2 restart"
              }
            }
        }
    }
}
