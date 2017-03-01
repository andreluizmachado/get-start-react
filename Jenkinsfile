#!groovy
import groovy.json.JsonSlurper
import groovy.json.JsonOutput

def dockerHostTesting = "tcp://10.80.29.81:2375"

node('docker') {
    wrap([$class: 'AnsiColorBuildWrapper', 'colorMapName': 'xterm', 'defaultFg': 1, 'defaultBg': 2]) {
        stage ('Checkout') {
            step([$class: 'WsCleanup'])
                checkout scm
        }

        docker.withServer(dockerHostTesting) {
            try {
                stage ('Installing Dependencies') {
                    //installDependencies()
                }


                stage ('Unit Tests') {
                    //runUnitTests()
                }


                stage ('Build Application for Functional Tests') {
                    //buildApplicationTest()
                }


                stage ('Functional Tests') {
                    //runFunctionalTests()
                }

            }
            finally {
                //teardownContainers()
            }
        }
    }
}
