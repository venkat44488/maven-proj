

pipeline {
    agent any
    stages {
        stage("welcome") {
            steps {
                echo "welcome to jenkinsfile"

}
}
        stage("MAVEN-BUILD") {
        steps {
            sh "mvn clean install package"
        }
    }
}
}
