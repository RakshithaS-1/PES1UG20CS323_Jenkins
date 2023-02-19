pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output 1.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') { 
            steps {
                sh './output'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') { 
            steps {
                //sh 'cat 1.cpp'
                error 'Pipeline Stage Error'
                echo 'Deployment Stage Succeddful'
            }
        }
    }
    post{
        success{
          echo 'Pipeline Success'
        }
    	  failure{
    		  echo 'Pipeline Failed'
    	  }
    }
}
