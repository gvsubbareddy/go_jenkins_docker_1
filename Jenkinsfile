pipeline {
  agent any
  
  stages {
    
    stage ('dockerization') {
      steps {
        sh '''
        docker build -t my-golang-app .        
        '''
      }
    }
	
	stage ('Building') {
      steps {
        sh '''
        docker run -i --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp --name my-running-app my-golang-app
        '''
      }
    }
  }
}
