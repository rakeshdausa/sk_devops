pipeline {
  agent any
  stages {
    stage("Hello") {
      steps {
        sh 'echo \'Hello Shravan\''
      }
    }
  
    stage("Upload to AWS") {
      steps {
        withAWS(region:'us-east-1',credentials:'sk_devops_creds') {
          s3Upload(file:'index.html', bucket:'skuchkuladata')
        }
      }
    }
  }
}

