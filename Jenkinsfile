pipeline
{
  agent any 
  stages{
    stage('clone'){
      steps{
      git 'https://github.com/devops-vamshi/simple_maven.git'
      }
      }
      stage('build'){
      
        steps{
        sh "mvn clean package"
        }
      }
    }
 }
