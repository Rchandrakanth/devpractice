pipeline {
		agent {  label 'jenkin-agent' } 
		tools { 
			jdk 'java17'
			maven 'maven3'
		}
		stages{
			stage("cleanup workspace"){
				  steps {
			  	clenws()
				}
			}
			stage ("checkout form SCM"){
			  	steps {
			  	git branch: 'master', credentialsId: 'github', url: 'https://github.com/Rchandrakanth/devpractice'
					
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

