pipeline{
	agent {
		node {
			label "master"
			customWorkspace "/mnt/docker"
		}
	}	
		stages {
			stage ('create container'){
				steps {
			
				sh "docker run --name container-3 -itdp 8080:80 httpd"
				}
			}
			
			
			stage {
				steps {
				dir ('/mnt/docker/22q3') {
					
					sh "docker cp index.html container-3:/usr/local/apache2/htdocs"
					
					}
				}	
			}
		}
}
