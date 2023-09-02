pipeline {
    agent any
    
    stages {
        stage ("Git Clone"){
            steps {
                echo "Cloning project from Repo"
                git branch: 'main', url: 'https://github.com/ARGITHUB1950/jenkins1.git'
            }
        }
        stage ("Build"){
            steps {
                echo "Building Docker file"
                sh "docker build -t noteapp ."
            }
        }
        stage ("Deploy"){
            steps {
                echo "Deploying"
                sh "docker run -dt -p 8003:8000 noteapp"
            }
        }
    }
}
