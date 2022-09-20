pipeline{
	agent {
		node {
			label "master"
			customWorkspace "/mnt/docker/22q2"
		}
	}	
		stages {
			stage ('create container-2') {
				steps {
				
				sh "docker run --name container2 -itdp 90:80 httpd"
				
				}
			}
			
				
			stage {
				steps {
				dir ('/mnt/docker/22q2') {
					
					sh "docker cp index.html container2:/usr/local/apache2/htdocs"
					
					}
				}	
			}
			
		}
}
