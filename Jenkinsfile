pipeline {
  environment {
    customImage = ''
	
  }
  agent {
    dockerfile {
		 filename 'Dockerfile'
	         args '-v "$PWD":/usr/src/myapp -w /usr/src/myapp'
		 reuseNode true
	 }
  }
  
  stages {
    stage('plan') {
	   steps {
		//sh 'docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.14 go build -v'
		//sh 'docker build -t my-golang-app .'
		//sh 'docker run -it --rm --name my-running-app my-golang-app'
		   sh 'echo `pwd`'
			
		}
	}
   
    stage('deploy') {
	   steps {
			sh 'echo completed'			
		}
	}
  }
}
