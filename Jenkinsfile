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
                    id: "central",
		    url: 'http://localhost:8081/artifactory/project_maven',
		    // If you're using username and password:
		    username: 'admin',
		    password: 'devops@890',
                )

		rtUpload (
	    serverId: 'central',
	    specPath: '/home/vamshi/.jenkins/workspace/file1/target/spec.jar',	 
	   // buildName: 'holyFrog',
	    
		)
		}
	}
   }
 }
