pipeline {
  agent any
  environment {
          Name="duvva_raghavendra"
  }
  triggers {
       crons '1 * * * *'
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
  }
}
