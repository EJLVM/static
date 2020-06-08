pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials: 'aws-static') {
          s3Upload(bucket:'ud-jenkins-s3', file:'index.html', path:'index.html')
        }
      }
    }
  }
}