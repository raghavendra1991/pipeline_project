pipeline {
  agent any
  environment {
          Name="duvva_raghavendra"
  }
  triggers {
       cron '1 * * * *'
  }
  stages {
    
    stage ('trigger') {
      steps {
        build('Build')
        build('Test')
      }
    }
        
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
