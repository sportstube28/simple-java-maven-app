podTemplate(containers: [
    containerTemplate(
        name: 'jnlp', 
        image: 'maven:3.8.1-adoptopenjdk-11'
        )
    ]) {

    node(POD_LABEL) {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
