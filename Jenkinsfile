pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf tomcat'
                sh 'git clone https://github.com/gshashi1408/prometheus.git'
            }
        }
        stage('Deploy Prometheus') {
            steps {
                sh 'ansible-playbook tomcat.yml -i inventory/hosts'
            }
        }
    }
}
