# Role: sync_uploads

This role synchronizes the `wp-content/uploads` directory between the remote server and the local environment.

## Variables
- `remote_path`: Remote WordPress root directory (default: `/var/www/example`).
- `local_path`: Local WordPress root directory (default: `~/Projects/WordPress/sites/example`).
- `sync_mode`: Direction of synchronization. Options:
  - `"pull"`: Sync from remote to local (default).
  - `"push"`: Sync from local to remote.
- `remote_port`: SSH port for the remote server (default: 2222).

## Usage
Add this role to your playbook:
```yaml
- name: Sync uploads
  roles:
    - sync_uploads