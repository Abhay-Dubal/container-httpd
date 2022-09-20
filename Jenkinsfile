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
					/*sh  "docker kill container3"
					sh "docker rm container3"*/
				sh "docker run --name container3 -itdp 300:80 httpd"
				
				}
			}
			stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container2:/usr/local/apache2/htdocs"
					
				}	
			}
				
		
		}
}
