pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                sh 'git clone https://github.com/alwaysmadhu/Ansible-Jenkins.git'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook httpd.yaml'
            }
        }
        stage('Restart Apache HTTPD') {
            steps {
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
