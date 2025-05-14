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
			  	git branch: 'main', credentialsId: 'GitHub', url:https://github.com/Rchandrakanth/devpractice.git'
					
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

