pipeline {
    agent any 
    stages {
        steps {
            withCredentials([usernamePassword(credentialsId: 'eb1092d1-0f06-4bf9-93c7-32e5f7b9ef76', accessKeyVariable: 'AWS_ACCESS_KEY_ID', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
                sh 'echo $AWS_ACCESS_KEY_ID'
                sh 'echo $AWS_SECRET_ACCESS_KEY'
            }
      }
        stage('Create Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name New_project --parameters ParameterKey=Applications,ParameterValue=1 --template-body file://CFT.json --region 'us-east-1'"
              }
            }
         }
