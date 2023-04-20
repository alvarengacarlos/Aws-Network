# Aws Network

## Deploy
Follow this steps to create a simple network:

- Create vpc stack:
```bash
aws cloudformation create-stack --stack-name simple-network-vpc --template-body file://$(pwd)/vpc.yaml
```
- Create internet gateway stack:
```bash
aws cloudformation create-stack --stack-name simple-network-internet-gateway --template-body file://$(pwd)/internet-gateway.yaml
```

- Create subnets stack:
```bash
aws cloudformation create-stack --stack-name simple-network-subnets --template-body file://$(pwd)/subnets.yaml
```

- Create acls stack:
```bash
aws cloudformation create-stack --stack-name simple-network-acls --template-body file://$(pwd)/acls.yaml
```

- Create route tables stack:
```bash
aws cloudformation create-stack --stack-name simple-network-route-tables --template-body file://$(pwd)/route-tables.yaml
```

- Create security groups stack:
```bash
aws cloudformation create-stack --stack-name simple-network-security-groups --template-body file://$(pwd)/security-groups.yaml
```

- Create security groups stack:
```bash
aws cloudformation create-stack --stack-name simple-network-ec2-instances --template-body file://$(pwd)/ec2-instances.yaml
```