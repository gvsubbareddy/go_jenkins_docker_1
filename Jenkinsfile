pipeline {
  environment {
    customImage = ''
	
  }
  agent {
    dockerfile {
		 filename 'Dockerfile'
	         args '-v "$PWD":/usr/src/myapp -w /usr/src/myapp'
		 reuseNode false
	 }
  }
  
  stages {
    stage('plan') {
	   steps {
		//sh 'docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.14 go build -v'
		sh 'docker build -t my-golang-app .'
		sh 'docker run -it --rm --name my-running-app my-golang-app'
			
		}
	}
   
    stage('deploy') {
	   steps {
			sh 'echo completed'			
		}
	}
  }
}
