pipeline {
    tools{
        maven 'mymaven'
    }
    agent any
    stages{
        stage('Clone a repo'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Compile the code'){
            steps{
                bat 'mvn compile'
            }
        }
        stage('CodeReview'){
		  steps{
		      bat 'mvn pmd:pmd'
             }
         }  
         stage('UnitTest'){
		  steps{
	         bat 'mvn test'
		      }
          }
         stage('Package'){
		  steps{
		      bat 'mvn package'
              }
          }
	     }
}
