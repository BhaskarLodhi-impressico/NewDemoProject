node {
        stage("Git Checkout"){
            checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/BhaskarLodhi-impressico/NewDemoProject.git']])
        }
        stage("Code Clean") {
            sh 'mvn clean'
        }
        stage("Code Build") {
            sh 'mvn install'
        }
        stage("Running Test Cases") {
            echo 'Running test cases to test code of our application'
        }
        stage("Building Docker Image") {
            sh 'docker build -t bhaskarlodhi9997/my-java-app:latest .'
        }
        stage("Running Docker Container"){
            echo 'Running docker container with image bhaskarlodhi9997/my-java-app:latest'
        }
        stage("Deleting Docker Image"){
            sh 'docker rmi bhaskarlodhi9997/my-java-app:latest'
        }
        stage("Cleaning Workspace"){
            cleanWs()
        }
    }
