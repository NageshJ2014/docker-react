pipeline {
  agent {
    node {
      label 'My-Vag'
    }
  }
  stages {
    stage('build') {
      steps {
        echo "This Should run for the Feature Branch only"
        sh "docker build -t myimage -f Dockerfile.dev ."
       }
      }
    stage('Test') {
      steps {
          echo "This is Without The Steps"
          sh "docker run myimage npm run test -- --coverage"
        }
      }
    }
  }


  // pipeline {
  //     agent any
  //     stages {
  //         stage('NPM Build') {
  //             steps {
  //               echo "This Should run for the Feature Branch only"
  //               docker build -t myimage -f Dockerfile.dev .
  //             }
  //         }
  //         stage('NPM Test') {
  //             steps {
  //                 echo 'Deploying'
  //             }
  //         }
  //     }
  // }
