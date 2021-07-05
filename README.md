# loop-ansible-aws-ecr
This is repository which is Ansible loop value for create multiple ECR


![image](https://user-images.githubusercontent.com/70093183/124305489-04237f80-db1a-11eb-82d3-c8609abb5570.png)
            

####Install collection AWS


####Install if have problem with boto3 and botocore    
python3 -m pip install --user --upgrade pip

python3 -m pip install ansible boto3 botocore

####Use with_dict to loop

####If you get error Failed to import the required Python library (botocore or boto3) on 's Python /usr/bin/python2
  - name: install pip2 dependencies

    pip:
  
      name: ['boto3', 'botocore']
    
      executable: /usr/bin/pip2
      
      
####Upload Docker Image to ECR

aws ecr get-login-password --region us-east-1| docker login --username AWS --password-stdin 108131037450.dkr.ecr.us-east-1.amazonaws.com

docker tag redis:latest 108131037450.dkr.ecr.us-east-1.amazonaws.com/helloworlds

docker push 108131037450.dkr.ecr.us-east-1.amazonaws.com/helloworlds
