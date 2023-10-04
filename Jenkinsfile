node {
    def mvnHome
    stage('Clone source code') { // for display purposes
        withCredentials([file(credentialsId: 'ssh-key', variable: 'ssh_key_file')]) {
            sh "cat $ssh_key_file > key"
            sh "chmod 400 key"
            sh "ssh -o StrictHostKeyChecking=no -i key cicd@35.187.231.94 'git clone https://github.com/devopsway/devops-project-application-cowsay-frontend.git'"
        }
    }
    stage('Build') {
        withCredentials([file(credentialsId: 'ssh-key', variable: 'ssh_key_file')]) {
            sh "cat $ssh_key_file > key"
            sh "chmod 400 key"
            sh "ssh -o StrictHostKeyChecking=no -i key cicd@35.187.231.94 'cd devops-project-application-cowsay-frontend && npm install'"
        }
    }
    stage('Results') {
        println("Preparation")
        aloha()
    }
}

def aloha() {
    println("This is aloha method")
}
