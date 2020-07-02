



pipeline {
    agent any
    environment{
   PATH="/opt/maven/apache-maven-3.6.3/bin:$PATH"
    }
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
