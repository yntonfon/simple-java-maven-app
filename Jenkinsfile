node('master') {
    def dockerHome = tool name: 'docker', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
    env.PATH = "${dockerHome}/bin:${env.PATH}"
}
