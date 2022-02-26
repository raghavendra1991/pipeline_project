pipeline {
  agent any
  environment {
          Name="duvva_raghavendra"
  }
  stages {
    stage ('Build') {
      agent { label 'slave'}
      steps {
        echo 'agent successfull installation'
      }
    }
    stage ('Test') {
      steps {
        echo "My name is $Name"
      }
    }
    stage ('triggerjob') {
      steps {
          build('Build')
          build('Test')
      }
    }
  }
}
