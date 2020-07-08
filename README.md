# blog-provisioning-rds-access-ansible

<https://blog.atathome.me/provisioning-rds-access-via-ansible/>

Mock repository for provisioning RDS access via Ansible.  

## How to use

To use you need to ammend serveral files to suit your setup.

- Update `group_vars/myapplication` with the correct host/subnet to match your application, update the MySQL Password hashes and the RDS identifier.
- Update `roles/aws/rds/vars/main.yml` with the correct user, privileges and state.

```bash
ansible-playbook --limit myapplication-db-master -i hosts.aws_rds aws_rds.yml -DC
```

Feel free to email if you have any issues/questions
<andrew@exclusivewebsystems.com>
