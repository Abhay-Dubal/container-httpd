pipeline{
	agent {
		node {
			label"label"
			customWorkspace "/mnt/docker"
		}
		stages {
			stage ('create container'){
				steps {
				sh "docker run --name container-1 -itdp 80:80 httpd"
				sh "docker run --name container-2 -itdp 90:80 httpd"
				sh "docker run --name container-3 -itdp 8080:80 httpd"
				}
			}
			stage {
				steps {
				dir ('/mnt/docker/22q1') {
					sh "docker cp index.html container-1:/usr/local/apache2/htdocs"
					
					}
				}	
			}
			stage {
				steps {
				dir ('/mnt/docker/22q2') {
					
					sh "docker cp index.html container-2:/usr/local/apache2/htdocs"
					
					}
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
