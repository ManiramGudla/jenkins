pipeline{
  agent any
  environment{
     
    branch="${params.branch}"
    host='ubuntu'
    ip="${params.hostIp}"
    version="${params.version}"
    jenkinsIp='3.110.116.50'
  }
    stages{
    
     
      
      stage('docker compose'){
        steps{
         sh '''
           ssh -o StrictHostKeyChecking=no -p 65520 ${host}@${ip} '
           cd /home/ubuntu;
           cd testVersion/Keyist-Ecommerce;
           sudo su | docker-compose up -d ;
           '
     '''
            }
      }
      
    
    }


}
