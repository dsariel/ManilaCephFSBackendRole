# ManilaCephFSBackendRole


Step 1. virtualenv venv
Step 2. source venv/bin/activate
Step 3. pip install ansible >= 2.1.0.0 
Step 4. edit hosts file and provide valid ip for the controller (at this stage there is no need to tester)
Step 5. ansible-playbook -i hosts manila.yml --extra-vars "subscr_user=username@domain.com subscr_password="password" --start-at-task="setup rhscon.repo" --vvvv | sed  's/\\n/\n/g'
