---
layout: post
title:  "Infrastructure as Code Generator: Project Breakdown"
date:   2023-03-06 12:00:00 -0700
author: Kevin Schrock
categories: projects iac
---

This post discusses the Infrastructure as Code generator that we will be building. Our goal is to test out the capabilities of OpenAI's Codex Model's to generate Ansible Playbooks from configurations pulled from devices.

### Sections
- Why build a Infrasturcutre as Code Generator
- Key Technologies in Use
- End Goal of this Project

### Why build a Infrasturcutre as Code Generator?
#### Background
When I was a Network Administrator, I spent a lot of my time dedicated to projects focused around building Infrastructure as Code (IaC). This code consisted of Ansible Playbooks and DNA Center Plug and Play (DNAC PnP). This code focused on initial provisioning, auditing, and making changes to our network devices. 
The work, at its simplist consisted of taking current configurations of our devices, and translating that to Ansible or DNAC PnP scripts; easy enough right? However, a majority of my time was spent translating Cisco configurations to code. Exploring OpenAI and their Codex model series, this seems like a perfect pairing to use AI to help translate from a configuraiton to code.
#### The Problem
Generating Infrastructure as Code from current Infrastructure configurations is a tedious, time consuming act that is mainly the act of translation.
#### The Solution
Build a application that can ingress current configurations for devices and output translated Infrastructure as Code. 

### Key Technologies in Use
The key technologies that will be used to explore this solution will be: 
- [OpenAI's Codex Model][codex]
- [Ansible][ansible]
- [PfSense][pfsense]

#### Codex Model
The Codex model is a descendnt of GPT-3 from OpenAI which can translate natural language to code. Learn more about Codex from OpenAI [here][codex].
#### Why Codex?
OpenAI and their API's have proven to be the industry leader in this technology. A notible company using GPT-3 is WARP (warp.dev insert link.). They are building a terminal that can take natural language and turn it into teminal commands.
#### Ansible
Ansible is a powerful platform where you build Ansible Playbooks written in YAML to automate your infrastructure changes. Learn more about Ansible and its uses [here][ansible].
#### Why Ansible?
Ansible is a populare technology in Infrastructure automation and is simple to use. The end user can develop and deploy playbooks from their personal computer with no additional infrasturcture needed to be built out.
#### PfSense
PfSense is a free network firewall distribution based on FreeBSD. It is one of the leading open source firewall solutions that you can install and is easy to use and configure with their Web Portal GUI. Learn more about PfSense [here][pfsense].
#### Why PfSense?
I use PfSense personally to secure my home network and love their product. Additionally, PfSense is widely available for no cost to many users making it a perfect platform to test out this concept.  

### End Goal of this Project.
The end goal of this project is to test out OpenAI's Codex Model in building Infrastructure as Code. We hope to discover the drawbacks and benefits of using AI as a translator to Ansible Playbooks. 
A succesfull end will be a simple applicaiton where a user can input their PfSense configuration with some basic instructions on what they want out, then they will get a ready to use Ansible Playbook that they can deploy. 

[codex]: https://platform.openai.com/docs/guides/code
[ansible]: https://www.ansible.com/
[pfsense]: https://www.pfsense.org/