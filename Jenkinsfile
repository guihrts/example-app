node
{
    def app
    stage('Clone repository') {
        checkout scm
        }
    stage("Build Image") {
        app = docker.build('guihrts/example-app')
        }
    stage("Push Image") {
        app = docker.withRegistry("https://registry.hub.docker.com", 'docker-hub-credentials'){
            app.push('latest')
        }
    }
}
