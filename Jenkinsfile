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
    
      stage('git clone'){
        steps{
         sh '''
           ssh -o StrictHostKeyChecking=no -p 65520 ${host}@${ip} '
           cd /home/ubuntu;
           cd testVersion;
           mkdir '"${version}"';
           cd '"${version}"';
           git clone -b '"${branch}"' https://github.com/ManiramGudla/Keyist-Ecommerce.git
           '
     '''
            }
      }
      
      stage('Ansible playbook'){
        steps{
         sh '''
           ssh -o StrictHostKeyChecking=no -p 65520 ${host}@${ip} '
           cd /home/ubuntu;
           cd testVersion/'"${version}"'/Keyist-Ecommerce;
           ansible-playbook ansibleReplacingIp.yml -e version='"${version}"' -e ip='"{ip}"'
           '
     '''
            }
      }
      
      stage('docker compose'){
        steps{
         sh '''
           ssh -o StrictHostKeyChecking=no -p 65520 ${host}@${ip} '
           cd /home/ubuntu;
           cd testVersion/'"${version}"'/Keyist-Ecommerce;
           sudo su ;
           docker-compose up -d
           '
     '''
            }
      }
      
    
    }


}
