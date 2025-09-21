# Techsaksham_project
# Healthcare Cloud Solution: Secure Patient Record Delivery with AWS SNS, Lambda, and VPC

## 📝 Project Overview
In the healthcare industry, safeguarding patient data and ensuring the confidentiality of medical records is paramount. This project addresses the need for secure, real-time access to patient records by leveraging AWS cloud services to build a scalable and secure platform for delivering medical reports via mobile push notifications.

The platform ensures that sensitive patient data is transmitted securely, leveraging **AWS VPC**, **SNS**, **Lambda**, and other AWS services to create a robust solution for patient record management.

## 🔐 Key Features

- ✅ **AWS CloudFormation for Infrastructure as Code**:
  - Deployed the entire infrastructure using **AWS CloudFormation**, allowing for easy replication, version control, and management of resources. The CloudFormation template provisions all necessary components for the secure delivery of medical reports.

- 🌐 **VPC Configuration for Secure Networking**:
  - Created a **VPC** (Virtual Private Cloud) with a **custom subnet**, **Internet Gateway (IGW)**, and **Route Table** to ensure secure networking. This isolated environment allows for safe communication between resources, enhancing security and reducing exposure to external threats.
  - **Security Groups**: Configured **Security Groups** for **EC2 instances** and other components, restricting access to internal communication within the VPC and SSH traffic from anywhere.

- 📩 **SNS Topics for Messaging**:
  - Configured two **SNS topics** (Simple Notification Service) to handle secure report publishing and notifications.
  - **SNS Endpoint**: Established private **VPC Endpoints** for SNS to avoid traffic exposure to the public internet, ensuring message privacy and secure delivery.

- 🖥️ **EC2 Instance for Hosting Logic**:
  - Deployed an **EC2 instance** inside the VPC, responsible for running the logic to handle medical report generation and messaging.
  - **Security Group** settings were fine-tuned to allow traffic only within the VPC and secure **SSH** access from anywhere, ensuring that only authorized users can interact with the instance.

- 🔄 **AWS Lambda for Report Handling**:
  - Created a **Lambda function** that listens to one SNS topic, processes incoming messages, formats them into structured medical reports, and forwards them to another SNS topic for patient notifications.
  - The Lambda function integrates seamlessly with the SNS system to trigger workflows, ensuring real-time, event-driven data processing.

- 🔑 **IAM Roles for EC2 and Lambda**:
  - Defined **IAM roles** to grant **EC2 instances** and **Lambda functions** the necessary permissions to interact with AWS services securely, following the principle of least privilege to minimize potential attack vectors.

- 🔒 **Private SNS with VPC Endpoint**:
  - Implemented a **VPC endpoint** for SNS, ensuring that all SNS messages are securely transmitted within the VPC, avoiding exposure to the public internet. This setup ensures secure communication between SNS and Lambda, enhancing the confidentiality and integrity of medical data.

## 🛠️ Technologies & Services Used

- **AWS CloudFormation**: Automating infrastructure provisioning and management.
- **Amazon VPC**: Securing network infrastructure with custom subnets, route tables, and internet gateways.
- **Amazon EC2**: Hosting the logic for processing and generating medical reports.
- **Amazon SNS**: Messaging service for securely publishing and delivering medical reports.
- **AWS Lambda**: Event-driven processing of incoming messages and report formatting.
- **IAM (Identity and Access Management)**: Secure permissions and access controls.
- **VPC Endpoints**: Ensuring private and secure message delivery without public internet exposure.
- **Security Groups**: Fine-tuning access control for EC2 and other resources.

## 🔒 Security & Privacy Considerations

This solution ensures the following:

- **Data Privacy**: By using private **SNS VPC Endpoints** and **VPC** networking, the system minimizes exposure to the internet and ensures data is only accessible within the secure network.
- **HIPAA Compliance**: The solution aligns with HIPAA-like privacy standards for handling sensitive healthcare data.
- **Least Privilege**: **IAM roles** are configured with minimal permissions, ensuring that only authorized entities can access the services.
- **Scalability**: The system is built to scale with patient volume, leveraging **AWS Lambda** for event-driven processing and **SNS** for high-throughput message delivery.

## 🤝 Contact

Feel free to reach out if you have any questions, suggestions, or would like to discuss this project further:

- **Email**: thatharohith062@gmail.com
- **LinkedIn**: https://www.linkedin.com/in/thatha-rohith/


I'm always open to collaborating or discussing improvements on this project. Let's connect!
