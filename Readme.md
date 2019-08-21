```
packer validate -var-file=./aws.json packer.json
packer inspect  packer.json
packer build -var-file=./aws.json packer.json
```

```
aws ec2 run-instances --image-id ami-0160824deef7cd4d5
    --count 1 --instance-type t2.micro
    --key-name vivek 
    --region us-east-1
    --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=demo}]'
```