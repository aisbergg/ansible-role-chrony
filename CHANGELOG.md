# Changelog

All notable changes to this project will be documented in this file.

- [2.0.1 (2021-10-11)](#201-2021-10-11)
- [2.0.0 (2021-10-11)](#200-2021-10-11)
- [1.2.2 (2020-09-11)](#122-2020-09-11)
- [1.2.1 (2020-05-28)](#121-2020-05-28)
- [1.2.0 (2020-05-18)](#120-2020-05-18)
- [1.1.0 (2020-03-22)](#110-2020-03-22)
- [1.0.0 (2020-02-13)](#100-2020-02-13)

---

<a name="2.0.1"></a>
## [2.0.1](https://github.com/aisbergg/ansible-role-chrony/compare/v2.0.0...v2.0.1) (2021-10-11)

### Documentation

- **README.md:** update readme


<a name="2.0.0"></a>
## [2.0.0](https://github.com/aisbergg/ansible-role-chrony/compare/v1.2.2...v2.0.0) (2021-10-11)

### CI Configuration

- add Github action for automatic releases

### Chores

- update changelog
- update development configs
- **.pre-commit-config.yaml:** bump pre-commit hook versions
- **CHANGELOG.tpl.md:** update changelog template

### Code Refactoring

- drop support for Ansible < 2.10


<a name="1.2.2"></a>
## [1.2.2](https://github.com/aisbergg/ansible-role-chrony/compare/v1.2.1...v1.2.2) (2020-09-11)

### Bug Fixes

- forcefully flush handlers

### Chores

- update changelog


<a name="1.2.1"></a>
## [1.2.1](https://github.com/aisbergg/ansible-role-chrony/compare/v1.2.0...v1.2.1) (2020-05-28)

### Code Refactoring

- clean up repo


<a name="1.2.0"></a>
## [1.2.0](https://github.com/aisbergg/ansible-role-chrony/compare/v1.1.0...v1.2.0) (2020-05-18)

### Code Refactoring

- clean up


<a name="1.1.0"></a>
## [1.1.0](https://github.com/aisbergg/ansible-role-chrony/compare/v1.0.0...v1.1.0) (2020-03-22)

### Bug Fixes

- restart only when service is enabled
- timesyncd service name
- correct Ansible version requirement

### Chores

- update changelog
- add bumpversion config

### Features

- make use of service_facts module and add tags


<a name="1.0.0"></a>
## [1.0.0]() (2020-02-13)

- Initial Release
