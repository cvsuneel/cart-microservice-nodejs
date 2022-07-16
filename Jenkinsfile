#! groovy
node {
    stage('code') {
        git branch: 'main', url: 'https://github.com/cvsuneel/cart-microservice-nodejs.git' "
    }
    stage('Build') {
        sh 'docker build -t cart .'
    }
    stage('Deploy') {
        sh 'sudo docker run -d -p 1004:1004 --restart unless-stopped --name cart cart'
    }
}
