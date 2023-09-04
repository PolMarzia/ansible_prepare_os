## Ansible prepare_os role

It's a test task.
### How to use:
1) clone this repo
2) make inventory.ini file in the root directory of the project with following text:

    [servers]  
server1 ansible_connection=ssh ansible_host=your_host ansible_user=your_user ansible_ssh_private_key_file=/path/to/your/key disk_to_encrypt=/path/to/disk

Change items in inventory to your items.

3) Run playbook by the command:

    ansible-playbook - playbooks/prepare_os_playbook.yml -l server1 

You can use following tags for partial role usage:

 - prepare_os.encrypt_disk
 - prepare_os.encrypt_part
 - prepare_os.cpu
 - prepare_os.network
 - prepare_os.show_info
 
Add tag name with flag --tags im the command for running playbook
