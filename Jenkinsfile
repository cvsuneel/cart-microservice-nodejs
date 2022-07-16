#! groovy
node {
    stage('code') {
        git branch: 'main', url: 'https://github.com/cvsuneel/cart-microservice-nodejs.git' "
    }
    stage('Build') {
        sh 'docker build -t cart .'
    }
    stage('Deploy') {
        sh 'sudo docker run -d -p 3200:8080 --restart unless-stopped --name cart cart'
    }
}
