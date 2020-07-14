pipeline
{
  agent any 
  stages{
    stage('clone'){
      git 'https://github.com/devops-vamshi/simple_maven.git'
      }
      stage('build'){
      sh "mvn clean package"
      }
    }
 }
