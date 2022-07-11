pipeline {
    agent any
    tools {
        go 'go-1.17'
    }
    environment{
        GO111MODULE='on'

    }
    stages {
        stage('Build or Compile') {
            steps {
               sh 'go build .'
            }
        }

        stage('Test') {
            steps {
                sh 'go test ./...'
            }
        }
        stage('Run') {
            steps {
               sh 'cd /var/lib/jenkins/workspace/GOLang_Project/Pipeline5 && go-webapp-sample &'
            }
        }
    }
}
