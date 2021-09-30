pipeline {
    agent any
    environment {
    AWS_ACCESS_KEY_ID     = "AKIA3LSDZ55XTGE6PEQV"
    AWS_SECRET_ACCESS_KEY = "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"
   }
    stages {
        stage('Create Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name s3bucket13 --parameters ParameterKey=Applications,ParameterValue=1 --template-body file://simplests3cft.json --region 'us-east-1'"
              }
            }
        }
     }
