pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo "This Should run for the Feature Branch only"
        docker build -t myimage -f Dockerfile.dev .
       }
      }
    stage('Test') {
      steps {
          echo "This is Without The Steps"
          docker run myimage npm run test -- --coverage
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
