# loop-ansible-aws-ecr

├── hosts
├── main.yaml
└── roles
    ├── common
    │   └── vars
    │       └── main.yaml
    └── ecr
        └── tasks
            └── main.yaml

####Install collection AWS


####Install if have problem with boto3 and botocore    
python3 -m pip install --user --upgrade pip
python3 -m pip install ansible boto3 botocore
