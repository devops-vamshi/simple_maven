pipeline
{
  agent any 
  stages
{
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

	 stage ('Artifactory configuration') {
            steps {
                rtServer (
                    id: "Artifactory Version 7.6.2",
		    url: 'http://localhost:8081/artifactory/project_maven',
		    username: 'admin',
		    password: 'devops@890',
                )

		rtUpload (
	    serverId: 'central',
	    specPath: '/home/vamshi/.jenkins/workspace/file1/target/ *.jar',
	    buildName: 'file1',
	    
		)
		}
	}
   }
 }
