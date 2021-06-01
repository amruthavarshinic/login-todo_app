pipeline {
  agent any

  stages {

    stage('Prepare Artifacts') {
      steps {
        sh '''
          zip ../login.zip *
        '''
      }
    }

    stage('Upload Artifact') {
      steps {
        sh '''
         curl -v -u admin:admin123 --upload-file /var/lib/jenkins/workspace/TODO_CI-Pipelines/login.zip http://172.31.52.12:8081/repository/login/login.zip
        '''
      }
    }
  }

}