## Master Account
1. RAM => Settings => Enable Sharing with AWS ORG

054223747689

kiwonyoon101@gmail.com
664695030410
kiwonyoon0701@gmail.com
054223747689

10.0.0.7

### Source account
1. Create TGW
   1. auto accept : no
2. Service : RAM
   1. Create resource share
      1. Resources : TGW
      2. Principals 
         1. Allow external accounts : check
         2. Add aws account number 0542XXXXXXXX


### Target account
1. RAM => Shared with me check


### Source account
1. VPC -> Transit gateway attachments

2. Create Transit Gateway Attachment
   1. Transit gateway ID : tgw-0349xxxxxxxxxxxx
   2. Attachment name tag : seoulvpc
   3. DNS support : enable
   4. VPC ID : SeoulVPC
   5. Click Create

3. VPC -> Transit Gateway Route Tables

4. Create Transit Gateway Route Table
5. 


