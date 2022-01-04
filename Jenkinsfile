pipeline {
    agent any
    stages {
        stage('Git') {
            steps {
                git branch: 'main', credentialsId: 'git', url: 'https://github.com/andrey-grozov/9.4-jenkins.git'
            }
        }
        stage('Run') {
            steps {
                sh 'pip3 install -r test-requirements.txt'
                sh 'molecule test'
            }
        }
    }
}