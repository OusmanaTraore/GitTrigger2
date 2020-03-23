pipeline {
    
  //  agent {
    //    docker {
      //       image: 'nginx:latest'
        //     args '-p 8081:8081'}
    //}node('agent any') {
    // some block
}//
    node('agent any') {
    // some block
    }
    stages {
        stage ('Clone') {
            steps {
                sh " rm -rf * " 
                sh "git clone https://github.com/OusmanaTraore/GitTrigger2.git "
            }
        }
        stage ('Build') {
            steps {
                sh "cd /var/lib/jenkins/workspace/JenkinsPipeline/GitTrigger2/MvnProject/mon-appli/src/main/java/ && javac org/example/demo/App.java"
                

            }
        }
        stage ('Run') {
            steps {
                sh " cd /var/lib/jenkins/workspace/JenkinsPipeline/GitTrigger2/MvnProject/mon-appli/src/main/java/  && java org/example/demo/App  "
            }
        }
    }
}
