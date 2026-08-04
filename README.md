# EBS
# Ex 1A – Amazon Elastic Block Store (EBS)
### NAME: VIJAYAKUMAR S
### REG NO: 212224040359

## Aim

To create and manage Amazon Elastic Block Store (EBS) volumes, attach them to an EC2 instance, create snapshots, and restore data from snapshots. 

---

## Objectives

* Create an Amazon EBS volume.
* Attach and mount the EBS volume to an EC2 instance.
* Create a file system and store data on the volume.
* Create a snapshot of the EBS volume.
* Restore a new volume from the snapshot and verify the stored data. 



# Procedure

## Task 1: Create a New EBS Volume

1. Log in to the AWS Management Console.
2. Open the EC2 service and navigate to **Volumes**.
3. Create a new **General Purpose SSD (gp2)** volume of **1 GiB**.
4. Select the same Availability Zone as the EC2 instance.
5. Assign the tag **Name: My Volume**.
6. Create the volume and wait until its status changes to **Available**. 



## **Task 2: Attach the EBS Volume to an EC2 Instance**

1. Select the newly created volume.
2. Choose **Attach Volume**.
3. Select the existing **Lab** EC2 instance.
4. Assign the device name **/dev/sdb**.
5. Attach the volume and verify that its status changes to **In-use**. 



## **Task 3: Create and Configure the File System**

1. Connect to the EC2 instance using Session Manager.
2. Create an **ext3** file system on the attached volume.
3. Create the mount directory **/mnt/data-store**.
4. Mount the volume and update the **/etc/fstab** file.
5. Verify the mounted volume using the `df -h` command.
6. Create a text file on the mounted volume and verify its contents. 


## **Task 4: Create an Amazon EBS Snapshot**

1. Select **My Volume** in the EC2 console.
2. Choose **Create Snapshot**.
3. Assign the tag **Name: My Snapshot**.
4. Create the snapshot and wait until its status changes to **Completed**.
5. Delete the previously created file from the mounted volume. 



## **Task 5: Restore the Snapshot**

1. Create a new volume from **My Snapshot**.
2. Assign the tag **Name: Restored Volume**.
3. Attach the restored volume to the EC2 instance using **/dev/sdc**.
4. Mount the restored volume to **/mnt/data-store2**.
5. Verify that the previously stored file is restored successfully. 



# **Outputs**

### **Output 1: EBS Volume Creation**

<img width="1919" height="1076" alt="Screenshot 2026-08-04 090053" src="https://github.com/user-attachments/assets/39f54125-3a90-4eaa-a6e6-7041dcbd207f" />


### **Output 2: Volume Attachment**

<img width="1919" height="1069" alt="Screenshot 2026-08-04 090310" src="https://github.com/user-attachments/assets/eb6c9516-cc69-4adf-8799-ff3c29379a0f" />


### **Output 3: File System Configuration**

<img width="1919" height="1069" alt="Screenshot 2026-08-04 090812" src="https://github.com/user-attachments/assets/279e2d17-0e04-4665-922c-f0ae26c518c1" />

<img width="1919" height="1064" alt="Screenshot 2026-08-04 091115" src="https://github.com/user-attachments/assets/2028849c-525e-4498-b405-64dcc8cd9e24" />


### **Output 4: Snapshot Creation**

<img width="1919" height="1068" alt="Screenshot 2026-08-04 091512" src="https://github.com/user-attachments/assets/e78f027d-b631-4e5b-a76b-6352b9e35c19" />


### **Output 5: Snapshot Restoration**

<img width="1919" height="1068" alt="Screenshot 2026-08-04 091512" src="https://github.com/user-attachments/assets/e626627a-7280-44b9-aa33-3353fae69970" />



# **Result**

An Amazon EBS volume was successfully created, attached, formatted, and mounted to an EC2 instance. A snapshot of the volume was created, restored as a new volume, and the stored data was successfully recovered, demonstrating EBS storage management and backup using snapshots. 

