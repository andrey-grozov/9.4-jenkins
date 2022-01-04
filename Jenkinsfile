pipeline {
    agent any
    stages {
        stage('Git') {
            steps {
                git branch: '1011', credentialsId: 'git', url: 'https://github.com/andrey-grozov/mnt-homeworks-ansible.git'
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
