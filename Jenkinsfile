node {
  def app

  stage('Clone repository'){
    checkout scm
  }

  stage('builde image'){
    app = docker.build("heyato/pipeline1")
  }

  stage('Push image'){
    docker.withRegistery('http://registery.hub.docker.com','docker-hub-credentials'){
      app.push("latest")
    }
  }
}
