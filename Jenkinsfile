pipeline {
		
		tools { 
			jdk 'java17'
			maven 'maven3'
		}
		stages{
			stage("cleanup workspace"){
				  steps {
			  	clenWs()
				}
			}
			stage ("checkout form SCM"){
			  	steps {
			  	git branch: 'master', credentialsId: 'github', url: 'https://github.com/Rchandrakanth/devpractice.git'
					
				}
			}
			stage("build application "){
				steps {
					sh  "mvn clean package"
				}
			}
			stage("test application "){
				steps {
					sh "mvn test "                                  
				}

			}
			
		}	
	}

