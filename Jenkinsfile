pipeline {
  agent any
  environment {
          Name="duvva_raghavendra"
  }
  triggers {
      cron '2 * * * *'
  }
  stages {
        
    stage ('job1') {
      agent { label 'slave'}
      steps {
        echo 'agent successfull installation'
      }
    }
    stage('based on previous') {
      when {
        expression {
        currentBuild.getPreviousBuild().result==='SUCCESS'
        }
      }
    
    stage ('filesysytem') {
      steps {
        sh "ls -l"
      }
    }
   
    stage ("build") {
      parallel{
        stage('job3'){
           steps{
           echo "job3"
           }
        }
        stage('job4'){
           steps{
           echo "job4"
           }
        }             
      }
    }
  } 	
  post {
      always {
         echo  "Always run, regardless of build status"
      }
    }
  }
}
