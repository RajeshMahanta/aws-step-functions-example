pipeline {
    agent any
    stages {
        stage('create Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name example --template-body file://template.yml --capabilities CAPABILITY_IAM"
              }
             }
        stage('wait stack') {
            steps {
            sh "aws cloudformation wait stack-create-complete --stack-name example"
            }
            }
            }
            }
