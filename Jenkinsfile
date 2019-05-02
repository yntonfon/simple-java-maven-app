pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
	}
		tool name: 'Docker-Master', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'		
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
