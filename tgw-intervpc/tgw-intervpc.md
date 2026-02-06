1. Create TGW

Name : TGW1
State : Available

2. Creat Traisit Gateway Attachement - OnPrem

Transit Gateway ID : TGW1
Attachment type : VPC

Attachment name tag : TGW1-OnPREM
VPC ID : OnPrem

3. Creat Traisit Gateway Attachement - AWSDC

Transit Gateway ID : TGW1
Attachment type : VPC

Attachment name tag : TGW1-AWSDC
VPC ID : AWSDC

4. Add route entry into VPC route table

OnPREM-Public-rt
OnPREM-Private-rt1
OnPREM-Private-rt2
AWSDC-Public-rt
AWSDC-Private-rt1
AWSDC-Private-rt2

```

aws ec2 create-route --route-table-id rtb-0d8886b1cf563e01e --destination-cidr-block 10.0.0.0/16 --transit-gateway-id tgw-03d795c518d2789ec

kiwony@kiwonymac.com:/Users/kiwony/temp> cat route.sh
for ((i=1; i<150; i++)); do
        aws ec2 create-route --route-table-id rtb-0d8886b1cf563e01e --destination-cidr-block 10.$i.0.0/16 --transit-gateway-id tgw-03d795c518d2789ec|jq
done
```
