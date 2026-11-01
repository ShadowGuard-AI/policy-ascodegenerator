# policy-AsCodeGenerator
Generates security policy code (e.g., Terraform, Ansible) from a high-level, human-readable policy description using a template engine like Jinja2. Supports multiple policy formats and target platforms. - Focused on Defines and enforces security policies related to network connectivity and access control lists. Each rule is checked before rendering: the source and destination must parse as an IP address or network with the standard library ipaddress module, and ports must be a list of integers in 1 to 65535. A policy with no rules exits with an error and generates nothing. The output file must not be the policy file or the template file; such a run is refused with an error.

## Install
`git clone https://github.com/ShadowStrikeHQ/policy-ascodegenerator`

## Usage
`./policy-ascodegenerator [params]`

## Parameters
- `-h`: Show help message and exit
- `--policy_file`: No description provided
- `--template_dir`: Path to the directory containing Jinja2 templates.
- `--template_name`: Name of the Jinja2 template to use (e.g., 
- `--output_file`: Path to the output file where the generated code will be written.
- `--log_level`: No description provided

## License
Copyright (c) ShadowStrikeHQ
