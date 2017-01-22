# Ansible Role: SonarQube Runner

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-sonar-runner.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-sonar-runner)

An Ansible Role that installs Sonar Runner on RedHat/CentOS and Debian/Ubuntu Linux servers.

The role is currently configured to support SonarQube installations using MySQL as a database backend.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    workspace: /root

Directory where downloaded files will be temporarily stored.

    sonar_runner_download_url: http://repo1.maven.org/maven2/org/codehaus/sonar/runner/sonar-runner-dist/2.3/sonar-runner-dist-2.3.zip
    sonar_runner_download_file: sonar-runner-dist-2.3.zip
    sonar_runner_expanded_file: sonar-runner-2.3

URL and filenames for sonar distribution/version.

    sonar_protocol: http
    sonar_host: localhost
    sonar_port: 9000

The SonarQube installation to which sonar-runner will connect.

    sonar_login: ""
    sonar_password: ""

The SonarQube installation login (if configured).

    sonar_mysql_host: localhost
    sonar_mysql_port: 3306
    sonar_mysql_database: sonar
    sonar_mysql_user: sonar
    sonar_mysql_password: sonar

SonarQube MySQL database connection details.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: geerlingguy.sonar-runner }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
