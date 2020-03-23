pipeline {
    agent any
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
