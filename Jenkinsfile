pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
	stage('Initialize') {
	    def dockerHome = tool 'Docker-Master'
	    env.PATH = "${dockerHome}/bin:${env.PATH}"	    	
	}
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
