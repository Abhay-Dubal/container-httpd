pipeline{
	agent {
		node {
			label "master"
			customWorkspace "/mnt/docker/22q3"
		}
	}	
		stages {
			stage ('create container') {
				steps {
			
				sh "docker run --name container3 -itdp 8080:80 httpd"
				}
			}
			
			
			stage {
				steps {
				dir ('/mnt/docker/22q3') {
					
					sh "docker cp index.html container3:/usr/local/apache2/htdocs"
					
					}
				}	
			}
		}
}
