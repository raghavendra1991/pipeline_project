pipeline {
  agent any
  environment {
          Name="duvva_raghavendra"
  }
  triggers {
       cron '1 * * * *'
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
    stage ("build") {
      parallel{
        stage('job1'){
           steps{
           echo "job1"
     }
   }
        stage('job2'){
           steps{
           echo "job2"
     }
   }             
  }
}
