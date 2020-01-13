### Utworzenie VPC HomeWork04 10.1.0.0/16
```
aws2 ec2 create-vpc --cidr-block 10.1.0.0/16

aws2 ec2 create-tags --resources vpc-08cf2e289b2c8ec93 --tags Key=Name,Value=HomeWork04

```
hint: aws2 ec2 describe-vpcs
vpc="vpc-08cf2e289b2c8ec93"

### Utworzenie subnet Public01 10.1.1.0/24

```
aws2 ec2 create-subnet \
    --vpc-id vpc-08cf2e289b2c8ec93 \
    --availability-zone eu-west-1a \
    --cidr-block 10.1.1.0/24

aws2 ec2 create-tags --resources subnet-0a8c311c1e696fe9d \
    --tags Key=Name,Value=Public01

```
public01="subnet-0a8c311c1e696fe9d"

### Utworzenie subnet Public02 10.1.2.0/24

```
aws2 ec2 create-subnet \
    --vpc-id vpc-08cf2e289b2c8ec93 \
    --availability-zone eu-west-1b \
    --cidr-block 10.1.2.0/24

aws2 ec2 create-tags --resources subnet-0164f2b1ae47d4b2e \
    --tags Key=Name,Value=Public02

```
public02="subnet-0164f2b1ae47d4b2e"

##################
### Utworzenie subnet Private01 10.1.3.0/24

```
aws2 ec2 create-subnet \
    --vpc-id vpc-08cf2e289b2c8ec93 \
    --availability-zone eu-west-1a \
    --cidr-block 10.1.3.0/24

aws2 ec2 create-tags --resources subnet-0081f258d37261cac \
    --tags Key=Name,Value=Private01

```
private01="subnet-0081f258d37261cac"

### Utworzenie subnet Private02 10.1.2.0/24

```
aws2 ec2 create-subnet \
    --vpc-id vpc-08cf2e289b2c8ec93 \
    --availability-zone eu-west-1b \
    --cidr-block 10.1.4.0/24

aws2 ec2 create-tags --resources subnet-08689551c0b507387 \
    --tags Key=Name,Value=Private02

```
public02="subnet-08689551c0b507387"
#### hint: aws ec2 create-vpc --cidr-block 10.0.0.0/16 --output text | awk '{print $NF}' | xargs aws ec2 create-tags --tags Key=Name,Value=MyVPC --resources
