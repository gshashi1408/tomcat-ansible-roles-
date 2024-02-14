pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf tomcat'
                sh 'git clone https://github.com/gshashi1408/tomcat-ansible-roles-.git'
            }
        }
        stage('Deploy tomcat') {
            steps {
                sh 'ansible-playbook tomcat.yml -i inventory/hosts'
            }
        }
    }
}
