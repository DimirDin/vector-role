# Vector Role

Ansible role for installing and configuring Vector log collector.

## Requirements

- Ansible 2.9+
- RHEL/CentOS 7/8

## Role Variables

### Defaults (can be overridden)

| Variable | Default | Description |
|----------|---------|-------------|
| `vector_version` | `0.34.0` | Vector version to install |
| `vector_config_dir` | `/etc/vector` | Configuration directory |
| `vector_data_dir` | `/var/lib/vector` | Data directory |
| `vector_user` | `vector` | System user |
| `vector_group` | `vector` | System group |

### Variables (should not be overridden)

| Variable | Description |
|----------|-------------|
| `vector_package_name` | Package name |
| `vector_service_name` | Service name |
| `vector_config_file` | Path to config file |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: vector
  roles:
    - role: vector-role
      vars:
        vector_version: "0.34.0"
        clickhouse_host: "clickhouse.example.com"
License

MIT
