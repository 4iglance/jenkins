pipeline {
    agent { node 'master' }
    stages{
        stage('Prepare') {
            steps {
                sh 'git clone https://github.com/4iglance/ansible.git'
            }
        }
    stage('After Checkout') {
            steps {
                sh 'pwd; ls'
            }
        }
    stage('Run Playbook') {
        steps {
            sh 'ansible-playbook ansible/httpd.yaml -u centos -b'
        }
    }
    }
}
