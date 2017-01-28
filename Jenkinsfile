node("docker") {
    #docker.withRegistry('andreluizkbca/get-start-react', 'docker-hub') {
    
        git url: "git@github.com:andreluizmachado/get-start-react.git", credentialsId: 'github'
    
        sh "git rev-parse HEAD > .git/commit-id"
        def commit_id = readFile('.git/commit-id').trim()
        println commit_id
    
        stage "build"
        def app = docker.build "get-start-react"
    
        stage "publish"
        app.push 'master'
        app.push "${commit_id}"
    #}
}
