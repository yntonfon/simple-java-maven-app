node {
    def dockerHome = tool name: 'docker', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
    env.PATH = "${dockerHome}/bin:${env.PATH}"

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3-alpine' 
                    args '-v /root/.m2:/root/.m2' 
                }
            }
            steps {
                h 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
