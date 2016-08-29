# ManilaCephFSBackend


Step 1. virtualenv venv

Step 2. source venv/bin/activate

Step 3. pip install ansible >= 2.1.0.0 

Step 4. login to the node intended to become a ceph node and install ceph (this step assumes that the node is running rhel 7.2)

'''
ansible-playbook -i hosts ceph_install.yml --extra-vars "subscr_user=username@domain.com subscr_password="password" --start-at-task="setup rhscon.repo" --vvvv | sed  's/\\n/\n/g
'''



Step 4. logout from the ceph node
Step 5 edit hosts file and provide valid ip for the controller and tester
Step 5. Setup the controller node 

'''
ansible-playbook -i hosts manila_controller.yml  --vvvv | sed  's/\\n/\n/g'
'''


Step 5. Setup the tester node 

'''
ansible-playbook -i hosts manila_tester.yml  --vvvv | sed  's/\\n/\n/g'
'''

