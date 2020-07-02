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
            sh "mvn clean package"
        }
    }
        stage("deploy-to-tomcat"){
            steps {
                echo "welcome to deployment"
               sshagent(['root']) {
                sh ' ssh -o StrictHostKeyChecking=no target/*.war root@35.223.144.233:/opt/tomcat8/webapps'
}


            }
        }
       
}
}
