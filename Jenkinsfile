pipeline {
    agent any
    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/parkchanbin54/demotest.git'
            }
        }
        stage('BE-Build') {
            steps {
                    sh '''
                    cd demotest
                    ./gradlew clean build --exclude-task test
                    '''
                   }
        }
        stage('Deploy') {
            steps {
                echo "Deploy Start"
            }
        }
    }
}
