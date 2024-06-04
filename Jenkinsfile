pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }
  stages {
    stage('Hello') {
      steps {
        sh '''
          java -version
        '''
      }
    }
    stage('Hello1') {
      steps {
        sh '''
          mvn -version
        '''
      }
    }
    stage('cat README') {
      when {
        branch "main*"
      }
      steps {
        sh '''
          cat README.md
        '''
      }
    }
  }
}
