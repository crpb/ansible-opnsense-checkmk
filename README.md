[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
[![lint](https://github.com/Rosa-Luxemburgstiftung-Berlin/ansible-opnsense-checkmk/actions/workflows/lint.yml/badge.svg)](https://github.com/Rosa-Luxemburgstiftung-Berlin/ansible-opnsense-checkmk/actions?query=workflow%3Aansible-lint)
[![pylint](https://github.com/Rosa-Luxemburgstiftung-Berlin/ansible-opnsense-checkmk/actions/workflows/pylint.yml/badge.svg)](https://github.com/Rosa-Luxemburgstiftung-Berlin/ansible-opnsense-checkmk/actions?query=workflow%3Apylint)

# ansible-opnsense-checkmk

Ansible role for opnsense installing check_mk agent.

It includes some local checks:

  * gateway status monitoring
  * crash detection

## Role Variables

[defaults/main.yml](defaults/main.yml)

## Setup

### Check_MK Agent

Download the **Check_MK Agent for FreeBSD** from your check_mk instance (https://yourCheckMK/check_mk/wato.py?folder=&mode=download_agents) to `files/check_mk_agent.freebsd`.

### opnsense-facts

The role requires to be run after https://github.com/Rosa-Luxemburgstiftung-Berlin/ansible-opnsense-facts .

### Notes

The role must be run as root or w/ `become: true`.
