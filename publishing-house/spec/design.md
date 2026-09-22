# Hands on with Red Hat Lightspeed in Satellite

## Overview

This lab demonstrates how Red Hat Lightspeed integrates with both the Red Hat Hybrid Cloud Console and Red Hat Satellite 6.19 to provide AI-powered security and compliance management for Red Hat Enterprise Linux environments. Organizations managing a mix of internet-connected and air-gapped RHEL hosts can use Red Hat Lightspeed to identify CVEs, evaluate regulatory compliance, and act on advisor recommendations — all without leaving their existing management toolchain. Participants will use the Hybrid Cloud Console to analyze CVE exposure and run a SCAP compliance scan on an internet-connected RHEL 9.7 host, then switch to Red Hat Satellite to manage advisor recommendations and view vulnerability data on a Satellite-connected RHEL 10.1 host.

## Target Audience

- **Role:** Linux system administrators and IT security operators responsible for managing Red Hat Enterprise Linux environments
- **Experience level:** Beginner
- **What they already know:** Basic web browser navigation, Linux terminal use, general familiarity with CVE terminology and compliance concepts (CIS, DISA STIG), and foundational RHEL system administration
- **What they don't know:** How to use Red Hat Lightspeed at the Hybrid Cloud Console or Red Hat Lightspeed in Satellite to surface and remediate security findings; how to generate Ansible remediation playbooks from vulnerability and compliance data; the distinction between connected and disconnected Red Hat Lightspeed deployment modes

## Prerequisites

- Basic web browser and Linux terminal use
- General familiarity with CVE terminology and IT security concepts such as vulnerability severity and compliance frameworks; no scripting knowledge required
- Cannot be validated automatically — the lab environment is pre-configured, but prior knowledge of CVEs and compliance frameworks cannot be verified programmatically

## Learning Objectives

1. Analyze CVE exposure on internet-connected Red Hat Enterprise Linux hosts using the Red Hat Lightspeed vulnerability service at the Hybrid Cloud Console and generate Ansible remediation playbooks.
2. Evaluate Red Hat Enterprise Linux regulatory compliance against a CIS Level 1 SCAP policy using Red Hat Lightspeed at the Hybrid Cloud Console and identify actionable remediation steps.
3. Manage advisor recommendations on Satellite-connected Red Hat Enterprise Linux hosts by downloading and triggering remediation playbooks through Red Hat Lightspeed in Satellite.
4. Explore the vulnerability service in Red Hat Satellite 6.19 to identify and investigate CVEs detected on disconnected Red Hat Enterprise Linux hosts.
5. Demonstrate the difference between the cloud-connected Red Hat Lightspeed offering at the Hybrid Cloud Console and the on-premise Red Hat Lightspeed in Satellite deployment model running via Podman containers on the Satellite server.

## Content Type

Lab (hands-on)

## Products & Technologies

- Red Hat Lightspeed (via the Hybrid Cloud Console and Red Hat Satellite)
- Red Hat Hybrid Cloud Console (console.redhat.com)
- Red Hat Satellite 6.19
- Red Hat Enterprise Linux 9.7
- Red Hat Enterprise Linux 10.1
- insights-client
- OpenSCAP
- SCAP Security Guide (SSG)
- CIS Benchmarks
- Red Hat Ansible Automation Platform (referenced for playbook execution; not directly exercised in the lab)
- Podman (hosts Red Hat Lightspeed in Satellite containers on the Satellite server)

## Module Map

| Module | Title | Duration |
|--------|-------|----------|
| 1 | Welcome to Infinicorp - we have tasks for you! | 10 min |
| 2 | Red Hat Lightspeed via the Hybrid Cloud Console - Evaluate and remediate CVEs | 35 min |
| 3 | Red Hat Lightspeed via the Hybrid Cloud Console - Evaluate regulatory compliance | 30 min |
| 4 | Red Hat Lightspeed Advisor in Satellite | 25 min |
| 5 | Red Hat Lightspeed Vulnerability in Red Hat Satellite | 10 min |
| 6 | Recap | 5 min |
| — | **Total hands-on (modules 2–5)** | **100 min** |
| — | Overview + Recap (modules 1, 6) | ~15 min |
| — | **Total lab** | **~115 min (~2 hours)** |

## Difficulty Level

Beginner

## Environment

**Learner view:** When the lab starts, three virtual machines are pre-provisioned and pre-configured. A RHEL 9.7 host (rhel-{guid}-1) is registered directly to the Hybrid Cloud Console and has existing CVE and compliance data already visible in Red Hat Lightspeed. A RHEL 10.1 host (rhel-{guid}-2) is registered to the Satellite server and has advisor recommendations and vulnerability data populated. A Red Hat Satellite 6.19 server (satellite-{guid}) is fully deployed with Red Hat Lightspeed in Satellite containers running via Podman. Learners interact primarily through two browser-based UIs — the Hybrid Cloud Console at console.redhat.com and the Satellite Web UI — and run two short terminal commands during the lab. A shared Hybrid Cloud Console organization account (rhpd-lightspeed-lb1187) is used across concurrent lab users.

**Automation needed:** Yes. Pre-provisioning installs and registers both RHEL hosts (one to the Hybrid Cloud Console, one to Satellite), deploys and configures Red Hat Satellite 6.19, starts the Red Hat Lightspeed in Satellite containers via Podman, and syncs initial insights data so that CVE findings, advisor recommendations, and compliance scan results are populated when the lab begins.

## Infrastructure Requirements

- **Cloud provider:** CNV
- **Platform:** RHEL VMs
- **Topology:** Per-student
- **VMs per student (3):**
  - 1 × RHEL 9.7 host — registered to the Hybrid Cloud Console; packages installed: insights-client, rhc, rhc-worker-script, scap-security-guide-0.1.80-1.el9_7
  - 1 × RHEL 10.1 host — registered to Red Hat Satellite 6.19; packages served from Satellite content views
  - 1 × Red Hat Satellite 6.19 server on RHEL 9 (latest) — runs Red Hat Lightspeed in Satellite containers via Podman
  - Sizing: RHEL 9.7 host (2 vCPU, 4GB RAM, 20GB disk), RHEL 10.1 host (2 vCPU, 4GB RAM, 20GB disk), Satellite 6.19 server (4 vCPU, 20GB RAM, 300GB disk)
- **Automation approach:** Ansible
- **AI/MaaS:** None
- **External services:**
  - *Student session:* console.redhat.com, access.redhat.com
  - *Provisioning:* cdn.redhat.com (RHEL packages and Satellite content sync), subscription.rhsm.redhat.com (host registration)
- **AAP version:** N/A
- **Non-GA products:** None (all products are GA)

## Assessment Strategy

Trust-based — learners follow guided steps and observe results directly in the Hybrid Cloud Console and Satellite Web UI. Completion of each module is verified visually (CVE lists populated, compliance reports generated, recommendations displayed and remediated). No automated verification scripts are required.
