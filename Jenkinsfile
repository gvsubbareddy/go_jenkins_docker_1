pipeline {
  environment {
    customImage = ''
	
  }
  agent {
    dockerfile {
		 filename 'Dockerfile'
		 reuseNode false
	 }
  }
  
  stages {
    stage('plan') {
	   steps {
		sh 'docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.14 go build -v'
			
		}
	}
   
    stage('deploy') {
	   steps {
			sh 'echo completed'			
		}
	}
  }
}
