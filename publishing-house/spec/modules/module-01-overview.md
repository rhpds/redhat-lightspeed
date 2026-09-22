# Module Outline: module-01-overview

### Brief Overview

This module introduces the fictional company Infinicorp and establishes the scenario that drives the rest of the lab. Learners meet the Red Hat Lightspeed product through a realistic business context: Infinicorp operates a mix of internet-connected and disconnected Red Hat Enterprise Linux hosts, and the security team has been asked to close gaps in CVE remediation and compliance posture. The module explains the two deployment modes of Red Hat Lightspeed — via the Hybrid Cloud Console and on-premise through Red Hat Lightspeed in Satellite — and sets expectations for what learners will accomplish across the four hands-on tasks ahead.

### Audience and Time

- **Target persona:** Linux system administrators and IT security operators; beginner level
- **Prerequisites for this module:** None — this is the starting point of the lab
- **Estimated duration:** 10 minutes

### Learning Objectives

- Explore the distinction between Red Hat Lightspeed at the Hybrid Cloud Console and the on-premise Red Hat Lightspeed in Satellite deployment model
- Demonstrate awareness of the connectivity modes (connected and disconnected) and which Red Hat Lightspeed capabilities apply to each

### Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | Infinicorp scenario and lab goals | 3 min |
| 2 | Red Hat Lightspeed in Satellite — what it is and how it works | 4 min |
| 3 | Connectivity options and data collection overview | 3 min |

### Detailed Steps

1. Read the Infinicorp scenario introduction describing the company's hybrid RHEL environment.
2. Review the list of four tasks the security team needs to complete.
3. Read the explanation of Red Hat Lightspeed at the Hybrid Cloud Console (console.redhat.com) — the cloud-connected service.
4. Read the explanation of Red Hat Lightspeed in Satellite — the on-premise container-based service running via Podman on the Satellite 6.18 server.
5. Review the connectivity diagram showing the two host types: rhel-{guid}-1 (connected to the Hybrid Cloud Console) and rhel-{guid}-2 (connected to the Satellite server).
6. Read the data collection and security information section covering what insights-client data is shared with Red Hat Lightspeed.
7. Note the shared lab organization account (rhpd-lightspeed-lb1187) — learners will see data from the shared account during Hybrid Cloud Console modules.

### Key Takeaways

- Red Hat Lightspeed is an AI-powered RHEL management product available both via the Hybrid Cloud Console and as an on-premise capability embedded in Red Hat Satellite
- The Hybrid Cloud Console service requires outbound internet connectivity from the RHEL host; Red Hat Lightspeed in Satellite supports disconnected hosts via the Satellite server
- The same insights-client agent is used on both connected and disconnected hosts; the routing destination differs
- Learners will complete four tasks: CVE evaluation, compliance evaluation (Hybrid Cloud Console), advisor recommendations, and vulnerability detection (Red Hat Lightspeed in Satellite)

### Infrastructure Notes

- No learner interaction required in this module — read-only overview
- The shared Hybrid Cloud Console organization (rhpd-lightspeed-lb1187) means concurrent learners may see each other's host data during modules 2 and 3; instructors should note this during delivery
