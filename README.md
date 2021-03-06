cloudwatch [![circleci](https://circleci.com/gh/GSA/ansible-cloudwatch.svg?style=svg)](https://circleci.com/gh/GSA/ansible-cloudwatch)
=========

This ansible role installs and configures the cloudwatch agent required to communicate with client machines for logging.

Requirements
------------

Required Packages (this role requires access to the following packages/installers via an external repository)
- cloudwatch.rpm - redhat installer package
- cloudwatch.msi - windows installer package

Role Variables
--------------

### Windows

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| windows_cloudwatch_agent_path | "C:\\Program Files\\Amazon\\AmazonCloudWatchAgent" | default windows install directory |
| windows_cloudwatch_agent_url | "" | windows installer msi |
| windows_cloudwatch_product_id | "" | windows product_id |
| windows_agent_log | "C:\Temp\Logs" | default agent windows log directory |

### Redhat

| Variable | Default | Purpose |
| ------ | ------ | ------ |
| redhat_cloudwatch_agent_path | "/opt/aws/amazon-cloudwatch-agent" | default redhat install directory |
| redhat_cloudwatch_agent_url | "" | redhat installer rpm |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - cloudwatch
```

Public domain
-------------

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
