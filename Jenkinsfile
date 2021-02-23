node
{
    def app
    stage('Clone repository') {
        checkout scm
        }
    stage("Build Image") {
        app = docker.build('example-app')
        }
    stage("Push Image") {
        app = docker.withRegistry("https://registry.hub.docker.com", 'Dockerhublogin'){
            app.push('latest')
        }
    }
}
