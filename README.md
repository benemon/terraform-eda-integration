# Terraform Cloud Integration with Event Driven Ansible

## Overview

This repository contains Ansible artifacts designed to facilitate the integration of Terraform Cloud with Event-Driven Ansible. It includes a collection of Ansible playbooks, roles, and rulebooks to setup the integration, and carry out mock tasks on a host created using Terraform Cloud.

## Prerequisites

Before using this repository, ensure you have the following installed and configured:

- Ansible Automation Platform (2.4 or later)
- Terraform Cloud
- A Terraform Cloud User Token,set up as a Custom Credential in Ansible Automation Platform Controller.

Input configuration:
```yaml
fields:
  - id: tfc_user_token
    type: string
    label: TFC User Token
    secret: true
required:
  - tfc_user_token
```

Injector configuration:
```yaml
extra_vars:
  tfc_user_token: '{{ tfc_user_token }}'

```

## Demonstration

![a demonstration of the integration](tfc-eda-integration.gif)
