pipeline {

      agent any

      stages {

            stage('GIT') {

                  steps {

                        echo 'Hi, this is Satyam from 3Pillar'

                        echo 'We are Starting the Testing'
                        git 'https://github.com/satyam1998/newpipeline.git'

                  }

            }
            stage('COMPILE_packege') {

                  steps {

                        echo 'COMPILE THE FILE'
                        tool name: 'Local_maven', type: 'maven'
                        sh 'mvn -f pom.xml package'
                        


                  }

            }

            stage('Build') {

                  steps {

                        echo 'Building Sample Maven Project'
                        archiveArtifacts '**/*.war'

                  }

            }
             
           


      }

}
