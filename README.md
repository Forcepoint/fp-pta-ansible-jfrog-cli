# jfrog-cli

Install the JFrog CLI client. 

https://jfrog.com/getcli/

https://www.jfrog.com/confluence/display/CLI/CLI+for+JFrog+Artifactory

For information about PTA and how to use it with this Ansible role please visit https://github.com/Forcepoint/fp-pta-overview/blob/master/README.md

## Requirements

None

## Role Variables

### OPTIONAL

* jfrog_cli_version: The version of the client to install.
* jfrog_cli_version_type: Versions up to 1.52.0 use 'v1' while newer ones use 'v2'.
* jfrog_cli_base_url: The URL to install from. Useful for downloading from Artifactory. 
  This variable is not used/honored for runs on Windows because chocolatey is used 
  and doing offline chocolatey installs is not trivial. Not worth automating ATM.

## Dependencies

None

## Example Playbook

    - name: jfrog cli
      hosts: all
      vars:
        jfrog_cli_version: "1.44.0"
        jfrog_cli_version_type: "v1"
        jfrog_cli_base_url: "https://artifactory.COMPANY.com/artifactory/releases.jfrog.io-artifactory-jfrog-cli"
      roles:
        - role: jfrog-cli

## License

BSD-3-Clause

## Author Information

Jeremy Cornett <jeremy.cornett@forcepoint.com>
