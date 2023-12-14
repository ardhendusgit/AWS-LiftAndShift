## Table of contents
* [General info](#general-info)
* [Cloud Technologies](#cloud-technologies)
* [Setup](#setup)

## General info
This project facilitates the migration of a locally hosted Multi-Tier Web Application to the AWS Cloud, using a proven strategy known as "Lift and Shift" while taking full advantage of the robust AWS service ecosystem.

## Cloud Technologies
Here's how this project uses AWS services for an efficient migration:
* ## Amazon EC2 Instances
We begin by replicating on-premises/localized servers as Amazon EC2 instances. This provides a virtualized environment to run your application within the AWS Cloud.

* ## Amazon Elastic Load Balancing (ELB)
To enhance the availability and distribution of incoming traffic, Amazon ELB is used to distribute requests across multiple EC2 instances. This ensures high availability and optimal performance.

* ## Amazon S3 for Artifact Storage
Amazon S3 for Artifact Storage: Amazon S3 serves as the ideal repository for storing application artifacts and other critical data. It's a scalable and durable solution designed for efficient object storage.

* ## Amazon Route 53 for DNS Management
Route 53 is used to establish a private DNS zone, enabling efficient and secure domain name resolution for your application within the AWS environment.

* ## Autoscaling with Autoscaling Groups
We set up Autoscaling groups to automatically adjust the number of EC2 instances based on traffic demand. This ensures that our application can handle varying workloads without manual intervention.

## Setup
* ## Architectural Overview
  - Access the application via a URL configured in GoDaddy DNS, pointing to an endpoint.
  - ACM manages HTTPS encryption for secure communication.
  - The Load Balancer, secured with HTTPS, forwards requests to Tomcat instances.
  - Auto Scaling dynamically manages the capacity of Tomcat instances.
  - Backend servers (MySQL, Memcache, RabbitMQ) are identified using Route 53 private DNS zones.
