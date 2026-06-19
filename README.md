# EBS Snapshot Automation

This project is designed for AAP workflow execution triggered by ServiceNow.

## Playbooks
- `precheck.yml` - Validate EC2 and collect volumes
- `create_snapshot.yml` - Create EBS snapshots
- `snow_success.yml` - Update ServiceNow on success
- `snow_failure.yml` - Update ServiceNow on failure

## Extra vars expected from ServiceNow / AAP Survey
- `cr_number`
- `servicenow_sys_id`
- `instance_id`
- `region`
- `environment`

## Notes
- AWS credentials should be provided through AAP credentials or IAM role
- ServiceNow credentials should be managed securely in AAP for production
