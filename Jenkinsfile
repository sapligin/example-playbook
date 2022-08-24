pipeline {
    agent any
    stages {
        stage('Get code from GitHub') {
            steps {
                git 'https://github.com/sapligin/example-playbook.git'
            }
        }
        stage('Run ansible') {
            steps {
                sh 'ansible-playbook site.yml -i inventory/prod.yml'
            }
        }
    }
}