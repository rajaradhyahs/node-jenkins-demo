pipeline {

    agent any

    stages {

        stage('Tests') {

            steps {

//                 script {

//                    docker.image('node:10-stretch').inside { c ->

                        echo 'Building..'

                        sh 'npm install'

                        echo 'Testing..'

                        sh 'npm test'

//                         sh "docker logs ${c.id}"

//                    }

//                 }

            }

        }

        stage('Build and push docker image') {

            steps {

                script {
<<<<<<< HEAD

                    def dockerImage = docker.build("rajaradhyahs/node-demo:master")

=======
                    def dockerImage = docker.build("rajaradhyahs/node-demo:master")
>>>>>>> 567222d9f24e9917b8288b2a1b17f5a41f67be20
                    docker.withRegistry('', 'demo-docker') {

                        dockerImage.push('master')

                    }

                }

            }

        }

        stage('Deploy to remote docker host') {

            environment {

                DOCKER_HOST_CREDENTIALS = credentials('demo-docker')

            }

            steps {

                script {

//                     sh 'docker login -u $DOCKER_HOST_CREDENTIALS_USR -p $DOCKER_HOST_CREDENTIALS_PSW 127.0.0.1:2375'
<<<<<<< HEAD

                    sh 'docker pull rajaradhyahs/node-demo:master'

=======
                    sh 'docker pull rajaradhyahs/node-demo:master'
>>>>>>> 567222d9f24e9917b8288b2a1b17f5a41f67be20
                    sh 'docker stop node-demo'

                    sh 'docker rm node-demo'
<<<<<<< HEAD

                    sh 'docker rmi rajaradhyahs/node-demo:current'

                    sh 'docker tag rajaradhyahs/node-demo:master rajaradhyahs/node-demo:current'

                    sh 'docker run -d --name node-demo -p 80:3000 rajaradhyahs/node-demo:current'

=======
                    sh 'docker rmi rajaradhyahs/node-demo:current'
                    sh 'docker tag rajaradhyahs/node-demo:master rajaradhyahs/node-demo:current'
                    sh 'docker run -d --name node-demo -p 80:3000 rajaradhyahs/node-demo:current'
>>>>>>> 567222d9f24e9917b8288b2a1b17f5a41f67be20
                }

            }

        }

    }
<<<<<<< HEAD

=======
>>>>>>> 567222d9f24e9917b8288b2a1b17f5a41f67be20
}
