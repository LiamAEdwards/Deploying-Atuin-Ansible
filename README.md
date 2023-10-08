# Deploying Atuin with Ansible

Use Ansible to easily deploy Atuin on all your devices.

## Prerequisites

Ensure you have both Ansible and Atuin installed on your system.

## Configuration

1. **Set Environment Variables**:  
   Edit the `env.yaml` file to include your details:
   - `Username`
   - `Key`
   - `Password`
   - Preferred `SHELL`

2. **Inventory Setup**:  
   Make sure your devices are listed in the `inventory.yaml` file.

## Deployment

To run the playbook, use the following command:

```bash
ansible-playbook playbook.yaml -u YOUR_USERNAME -i inventory.yaml
```

Replace YOUR_USERNAME with your actual username.


## Known Issues

Decryption Problem:

When trying to sync, you may encounter this error.
  ```bash
  atuin sync      
  0/0 up/down to record store
  thread 'main' panicked at 'failed to decrypt history! check your key: could not encrypt
  ```

This issue is being tracked at atuinsh/atuin#1199.
