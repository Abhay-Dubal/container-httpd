pipeline{
	agent {
		node {
			label"label"
			customWorkspace "/mnt/docker"
		}
	}	
		stages {
			stage ('create container-2'){
				steps {
				
				sh "docker run --name container-2 -itdp 90:80 httpd"
				
				}
			}
			
				
			stage {
				steps {
				dir ('/mnt/docker/22q2') {
					
					sh "docker cp index.html container-2:/usr/local/apache2/htdocs"
					
					}
				}	
			}
			
		}
}
