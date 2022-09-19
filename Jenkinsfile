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
				sh "docker run --name container-1 -itdp 80:80 httpd"
				
				}
			}
			stage {
				steps {
				dir ('/mnt/docker/22q1') {
					sh "docker cp index.html container-1:/usr/local/apache2/htdocs"
					
					}
				}	
			}
				
		
		}
}
