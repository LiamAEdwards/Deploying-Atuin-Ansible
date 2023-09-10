# Deploying-Atuin-Ansible
Get atuin on all the devices you use :)

# Set env.yaml variables
Add your Username, Key and Password, along with your preferred SHELL.

# Running the playbook
Replace USERNAME with your username
`ansible-playbook playbook.yaml -u USERNAME -i inventory.yaml`


# Issues
- Currently hitting an issue where it can't decrypt your database.
  ```
  atuin sync      
  0/0 up/down to record store
  thread 'main' panicked at 'failed to decrypt history! check your key: could not encrypt
  ```
  Issue tracked here -> https://github.com/atuinsh/atuin/issues/1199
