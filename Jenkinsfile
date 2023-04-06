node {
        stage("Git Checkout"){
            git url:'https://github.com/BhaskarLodhi-impressico/NewDemoProject.git'
        }
        stage("Code Build") {
            sh 'mvn clean install'
        }
        stage("Tesing Code") {
            echo 'Running test cases'
        }
        stage("Deploying Application") {
            echo 'Deploying  Application on server'
        }
        stage("Cleaning Workspace"){
            cleanWs()
        }
    }
