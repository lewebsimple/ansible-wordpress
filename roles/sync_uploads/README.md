# Role: sync_uploads

This role synchronizes the `wp-content/uploads` directory from the remote server to the local environment.

## Variables
- `remote_path`: Remote WordPress root directory (default: `/var/www/example`).
- `local_path`: Local WordPress root directory (default: `~/Projects/WordPress/sites/example`).
- `remote_port`: SSH port for the remote server (default: 2222).

## Usage
Add this role to your playbook:
```yaml
- name: Synchronize uploads
  roles:
    - sync_uploads