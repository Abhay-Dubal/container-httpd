pipeline{
	agent {
		node {
			label "master"
			customWorkspace "/mnt/docker/22q1"
		}
	}	
		stages {
			stage ('create container') {
				steps {
				sh "docker run --name container1 -itdp 80:80 httpd"
				
				}
			}
			stage {
				steps {
				
					sh "docker cp index.html container1:/usr/local/apache2/htdocs"
					
				}	
			}
				
		
		}
}
