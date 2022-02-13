podTemplate(containers: [
    containerTemplate(
        name: 'jnlp', 
        image: 'jenkins/inbound-agent:latest'
        )
  ]) {

     node(POD_LABEL) {
        stage('Get a Maven project') {
            git 'https://github.com/sportstube28/simple-java-maven-app.git'
            container('maven') {
                stage('Build a Maven project') {
                    sh '''
                    echo "maven build"
                    mvn -B -DskipTests clean package
                    '''
                    }
            }
        }
     }
}
