pipeline {
    agent any
    stages {
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
