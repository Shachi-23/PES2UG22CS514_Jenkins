pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([[$class: 'GitSCM',
        //         branches: [[name: '*/main']],
        //         userRemoteConfigs: [[url: 'https://github.com/Shachi-23/PES2UG22CS514_Jenkins.git']]
        //         ])
        //     }
        // }
        stage('Build') {
            steps {
                build 'PES2UG19CS514-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
