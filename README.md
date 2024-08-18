# AWS VPC Monitoring with Flow Logs


# Get Ready To Build: 

1. ☁️ Set up two VPCs and test their peering connection.
 
2. 🛶 Set up VPC Flow Logs that collect network traffic data.

3. 🧠 Analyse network traffic using CloudWatch's Log Insights.


# High Level Overview of Project Architecture:

![image](https://github.com/user-attachments/assets/7946687c-710b-4f19-ac36-b150d10c45b7)


# Step 1: Set up  VPCs in Minutes

![image](https://github.com/user-attachments/assets/276cd754-0d88-435d-a528-fe8e0973a80c)


![image](https://github.com/user-attachments/assets/877e2226-36a5-4d2c-bf94-c5afda821d29)


## 1. IPv4 CIDR block muust be 10.1.0.0/16

![image](https://github.com/user-attachments/assets/270875e5-eef2-42c1-be97-2a73d2be8541)

![image](https://github.com/user-attachments/assets/46c34c54-dd21-4738-b87b-05ebac089221)


![image](https://github.com/user-attachments/assets/45c94d6f-d8b5-4bf6-8d08-7e1f0d17eb1b)




# Step 2: Set up VPC 2



![image](https://github.com/user-attachments/assets/fb56a2e5-f09e-4949-a56f-3d71af799ad0)


## 1. IPv4 CIDR block muust be 10.2.0.0/16

## Same as VPC-1



# Step 3: Launch EC2 Instances


![image](https://github.com/user-attachments/assets/d7ed4bd1-f345-472e-8891-e661559e19d0)

1. Select Launch instances.
2. Since your first EC2 instance will be launched in your first VPC, let's name it 
3. For the Amazon Machine Image, select Amazon Linux 2023 AMI.
4. For the Instance type, select t2.micro.
5. For the Key pair (login) panel, select  Proceed without a key pair (not recommended).


![image](https://github.com/user-attachments/assets/6c132a1e-f919-4522-8b35-61059c2ec066)

![image](https://github.com/user-attachments/assets/d5209aae-5d20-412d-a16f-9516d4efda47)



# Step 4: 

1. Select VPC 1 
2. Name your security group 
3. Choose Add security group rule.
4. For the new rule's Type, select All ICMP - IPv4.
5. For the new rule's Source, select 0.0.0.0/0

![image](https://github.com/user-attachments/assets/325013ca-6e4b-4d64-b0e9-aeb4c44340d9)


# Step 5: Launch an instance in VPC 2

1. The Name is 
2. The VPC is NextWork-vpc-2.
3. Make sure you select Enable for Auto-assign public IP here too
4. Name your security group 
5. Allow ICMP traffic from ALL IP addresses.


![image](https://github.com/user-attachments/assets/18d5668d-f19d-4fc7-8fda-99f1c3f2a2b0)



# Step 6: Set Up Flow Logs


![image](https://github.com/user-attachments/assets/f7b2e009-aab9-417c-9507-41e96cfa54e8)


![image](https://github.com/user-attachments/assets/1274c276-843f-44cf-a17d-65ce137a84b6)

![image](https://github.com/user-attachments/assets/156c3119-64a7-4403-9e7b-dfa98a170377)


![image](https://github.com/user-attachments/assets/e727d462-cbfa-43cd-8f7d-5d36c515032f)


![image](https://github.com/user-attachments/assets/39fd7854-bb59-4ac4-b544-e1931d55ec8c)


![image](https://github.com/user-attachments/assets/fc9ece56-64b4-469c-ba7e-03b1be1ffd54)


![image](https://github.com/user-attachments/assets/f103e2f7-f7e8-4612-a115-0279699f005b)





# Step 7: 

1. Head back to your VPC console.
2. Select the Your VPCs page.
3. Select NextWork-1-vpc.
4. Scroll down to the Flow Logs tab, and click on Create flow log.


![image](https://github.com/user-attachments/assets/bd138996-526b-42fb-bedf-7dcec6c7b37a)


![image](https://github.com/user-attachments/assets/3cb18fa3-9e45-4034-a693-c26ac09ffd35)


![image](https://github.com/user-attachments/assets/4eaa1929-391e-42e0-ac07-1aaef0a89ace)


![image](https://github.com/user-attachments/assets/3db0d933-16e0-4695-a658-171b26dd16ac)
