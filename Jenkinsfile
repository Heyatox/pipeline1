node {
  def app

  stage('Clone repository'){
    checkout scm
  }

  stage('builde image'){
    app = docker.build("Heyato/pipeline1")
  }

  stage('Push image'){
    docker.withRegistery('http://regestery.hub.docker.com','docker-hub-credentials'){
      app.push("latest")
    }
  }
}
