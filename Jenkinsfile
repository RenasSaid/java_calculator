pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        echo 'Buildning...'
      }
    }
    stage ('Build Test') {
      when {
        anyOf {
          branch 'develop';
          branch 'main'
        }
      }
      steps {
        echo 'Testing...'
      }
    }
    stage ('Deploy') {
      when {
        branch 'main'
      }
      steps {
        echo 'Deploy...'
      }
    }
  }
}
