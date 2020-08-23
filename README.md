# Visual Studio Code for macOS role for Ansible

[![GitHub workflow status](https://img.shields.io/github/workflow/status/ayltai/ansible-vscode-mac/CI?style=flat)](https://github.com/ayltai/ansible-vscode-mac/actions)
[![Ansible quality score](https://img.shields.io/badge/quality-5-success)](https://galaxy.ansible.com/ayltai/vscode_mac)
[![Ansible role](https://img.shields.io/badge/role-ayltai.vscode_mac-blue)](https://galaxy.ansible.com/ayltai/vscode_mac)
![Maintenance](https://img.shields.io/maintenance/yes/2020?style=flat)
[![Release](https://img.shields.io/github/release/ayltai/ansible-vscode-mac.svg?style=flat)](https://github.com/ayltai/ansible-vscode-mac/releases)
[![License](https://img.shields.io/github/license/ayltai/ansible-vscode-mac.svg?style=flat)](https://github.com/ayltai/ansible-vscode-mac/blob/master/LICENSE)

Install and configure [Visual Studio Code](https://code.visualstudio.com) and extensions on macOS.

[![Buy me a coffee](https://img.shields.io/static/v1?label=Buy%20me%20a&message=coffee&color=important&style=flat&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoff.ee/ayltai)

## Quick start

### Installation
```sh
ansible-galaxy install ayltai.vscode_mac
```

### Usage
```yaml
---
- hosts: all
  roles:
    - ayltai.vscode_mac
  vars_prompt:
    - name: sudo_password
      prompt: root password
  vars:
    vscode_extentions:
      - VisualStudioExptTeam.vscodeintellicode
```

## Variables
| Name | Type | Default | Description |
|------|------|---------|-------------|
| `vscode_package` | `string` | `visual-studio-code` | The package name on Homebrew Cask |
| `vscode_extentions` | `list` | `[]` | A list of extensions to be installed with Visual Studio Code. Supports `[publisher name].[extension name]` format. |
| `sudo_password` | `string` | | The root password to be passed to Homebrew Cask during installation. |

## License
[MIT](https://github.com/ayltai/ansible-vscode-mac/blob/master/LICENSE)

## References
* [Visual Studio Code](https://code.visualstudio.com)
* [Homebrew](https://brew.sh)
* [Ansible](https://www.ansible.com)
* [Ansible Galaxy](https://galaxy.ansible.com)
