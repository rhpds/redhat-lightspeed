# Module Outline: module-06-recap

### Brief Overview

This module closes the lab by summarizing the four tasks Infinicorp's security team completed and providing a product team commentary on the current state of Red Hat Lightspeed in Satellite. Learners review what they accomplished — CVE evaluation and compliance assessment via the Hybrid Cloud Console, advisor recommendations and vulnerability detection via Red Hat Lightspeed in Satellite — and hear directly from the product team about the containerized Podman architecture, the GA status of each capability, and the update delivery model tied to Satellite ISOs and container image releases.

### Audience and Time

- **Target persona:** Linux system administrators and IT security operators; beginner level
- **Prerequisites for this module:** Completion of modules 01–05
- **Estimated duration:** 5 minutes

### Learning Objectives

- Demonstrate a consolidated understanding of the four Red Hat Lightspeed use cases covered in the lab
- Explore the product team's perspective on the architecture and GA status of Red Hat Lightspeed in Satellite

### Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | Summary of four completed tasks | 3 min |
| 2 | Product team commentary on Red Hat Lightspeed in Satellite | 2 min |

### Detailed Steps

1. Read the summary of the four tasks completed for Infinicorp:
   - Task 1: Evaluated and remediated CVEs on the internet-connected RHEL 9.7 host using Red Hat Lightspeed at the Hybrid Cloud Console.
   - Task 2: Evaluated regulatory compliance against a CIS Level 1 SCAP policy using Red Hat Lightspeed at the Hybrid Cloud Console.
   - Task 3: Managed advisor recommendations on the disconnected RHEL 10.1 host using Red Hat Lightspeed in Satellite.
   - Task 4: Explored vulnerability detection for the disconnected RHEL 10.1 host using Red Hat Lightspeed in Satellite.
2. Read the product team commentary explaining:
   - The containerized architecture of Red Hat Lightspeed in Satellite (Podman containers running on the Satellite server).
   - The generally available status of both the advisor and vulnerability capabilities in Red Hat Lightspeed in Satellite 6.19.
   - How Red Hat Lightspeed in Satellite receives updates: tied to Satellite ISO releases and container image updates.
3. Note any next steps or additional resources linked from the recap page (for example, links to product documentation or Red Hat blog posts).

### Key Takeaways

- Red Hat Lightspeed in Satellite extends the capabilities of the Hybrid Cloud Console to disconnected RHEL environments through a containerized on-premise deployment
- Both the advisor service and the vulnerability service in Red Hat Lightspeed in Satellite are generally available in Satellite 6.19
- Updates to Red Hat Lightspeed in Satellite are delivered through the standard Satellite ISO and container image release cycle, not through a separate update channel
- Red Hat Lightspeed covers the full security management loop: detect CVEs and compliance failures, generate remediation playbooks, and act on advisor recommendations — across both connected and disconnected environments

### Infrastructure Notes

- No learner interaction required in this module — read-only recap
- If the lab includes a feedback survey link, it should be embedded at the end of this module
