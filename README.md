# BuildScript1
Bash Build Script 1 [Friday Update Logs]

CODE EXPLAINATION:

#!/bin/bash

#This script will be used to update the server and creates a new file with the number of upgradable packages every Friday at 11pm

1. echo "Hello, here are Fridays updates.."
This is to let the user know what the script will do 

2. touch update_logs.txt
This part of the script will create the file where the update information will go 

3. sudo apt update && sudo apt upgrade -y
This part of the script will update the server

4. apt list --upgradable > update_logs.txt
This part of the script will send over the list of upgradeable packages to the file we created earlier (update_logs.txt)

5. date >> update_logs.txt
This part of the script will append the date at the bottom of the file (update_logs.txt) after the upgradeable package information

6. cat update_logs.txt
This portion of the script will allow the user to view everything that was just entered into the file (update_logs.txt)



Resources:
For Cron: 
1. https://www.baeldung.com/linux/schedule-script-execution
2. https://dev.to/shuaib/setting-up-cron-jobs-to-run-bash-scripts-n5n#:~:text=To%20setup%20a%20cronjob%2C%20you,job%20that%20will%20be%20executed.

How to see upgradable stuff:
1. https://itsfoss.com/apt-list-upgradable/
