# PROJECT 6: WEB SOLUTION WITH WORDPRESS


### 1. First of all create 3 EBS volume on AWS and then Create a single partition on each of the 3 disks with ```gdisk```

![1](https://user-images.githubusercontent.com/55023518/166164673-d04d1d42-eb3a-498a-9a5d-ef521b64af22.jpg)

### 2. Use ```lsblk``` utility to view the newly configured partition on each of the 3 disks

![2](https://user-images.githubusercontent.com/55023518/166164849-0002606c-7bda-4095-81ff-8ce5c7f525e3.jpg)

### 3. Use ```pvcreate``` utility to mark each of 3 disks as physical volumes (PVs) to be used by LVM

![3](https://user-images.githubusercontent.com/55023518/166165021-595d80ef-9967-4acb-b6ba-ce2e9aeea373.jpg)

### 4. Use ```vgcreate``` utility to add all 3 PVs to a volume group (VG). Name the VG webdata-vg

![4](https://user-images.githubusercontent.com/55023518/166165109-e8492e0b-9850-40c2-a236-dee0f57062a3.jpg)

### 5. Use ```lvcreate``` utility to create 2 logical volumes

![5](https://user-images.githubusercontent.com/55023518/166165160-864e74c9-272f-4f10-8cd3-ef8b87547d7c.jpg)

### 6. Use ```mkfs.ext4``` to format the logical volumes with ext4 filesystem

### 7. Create ```/var/www/html``` and ```/home/recovery/logs``` directory

### 8. Mount ```/var/www/html``` on apps-lv logical volume

### 9. rsync utility to backup all the files in the log directory /var/log into /home/recovery/logs

### 10. Mount /var/log on logs-lv logical volume

### 11. Restore log files back into /var/log directory

### 12. UPDATE THE `/ETC/FSTAB` FILE

![6](https://user-images.githubusercontent.com/55023518/166165669-c7ce1ed2-e8e9-4ff6-ace2-b5751b2c1c9f.jpg)

### 13. Verify your setup by running df -h

![7](https://user-images.githubusercontent.com/55023518/166165708-eb719088-954a-4ac7-8ab0-39c9685ed6c7.jpg)

### 14. Launch a second RedHat EC2 instance that will have a role – ‘DB Server’
Repeat the same steps as for the Web Server, but instead of apps-lv create db-lv and mount it to /db directory instead of /var/www/html/

![8](https://user-images.githubusercontent.com/55023518/166166535-36783e7e-f3e7-45d3-8e05-f0163c3b4a7d.jpg)

### 15. Install WordPress on your Web Server EC2, connect to database server and verify

![9](https://user-images.githubusercontent.com/55023518/166167001-3366a366-60e3-46f9-b7cb-212e7afc4ce3.jpg)
<img width="959" alt="image" src="https://user-images.githubusercontent.com/55023518/166170764-0b9ec54d-6791-4869-aee8-618a017ffd3c.png">

















