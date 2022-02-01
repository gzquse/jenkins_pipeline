// pipeline{
//     agent any
//     tools{
//         maven 'mvn-3.5.4'
//     }
//     stages{
//         stage('Build'){
//             steps{
//                 sh "mvn clean package spring-boot:repackage"
//                 sh "printenv"
//             }
//         }
//     }
// }
// pipeline{
//     agent any
//     stages{
//         stage('deploy'){
//             steps{
//                 input message: 'start or stop'
//             }
//         }
//     }
// }

pipeline{
    agent any
    // post{
    //     always{
    //         cleanWs()
    //     }
    // }
    stages{
        stage('performance test'){
            steps{
                // script{
                //     def browsers = ['chrome', 'firefox']
                //     for (int i =0; i<browsers.size(); ++i){
                //         echo "Testing the ${browsers[i]} browser"
                //     }
//                     echo "Running ${BUILD_NUMBER} on ${JENKINS_URL}"
                    bzt params: 'blaze_exist_jmeter_config.yml'
                }
            }
        }
    }