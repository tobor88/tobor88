# 👋 Hi, I'm Robert H. Osborne

### Cloud Solutions & Automation Engineer | Security | Infrastructure | Architecture

I'm a **Cloud Solutions & Automation Engineer at Vinebrook Technology** and the founder of **OsbornePro LLC**.

I work across the boundaries of infrastructure, cloud, security, networking, identity, development, and automation. 
My career has taken me across the technology stack. 
From administering and troubleshooting systems to engineering automation and designing solutions that span infrastructure, cloud, networking, identity, security, and software.

That breadth has shaped how I approach engineering today: **understand the whole system, automate what should be automated, secure it by design, and build solutions that someone can actually operate and maintain.**

A lot of what you'll find here is the result of that philosophy-tools, scripts, security projects, experiments, and solutions built while figuring out how things *really* work.

[![Website](https://img.shields.io/badge/OsbornePro.com-Technical%20Case%20Studies-red)](https://osbornepro.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Robert%20H.%20Osborne-0A66C2)](https://www.linkedin.com/in/roberthosborne)
[![GitHub followers](https://img.shields.io/github/followers/tobor88?label=Follow\&style=social)](https://github.com/tobor88)

---

## 🧠 What I Do

My work tends to live where **systems, security, automation, and architecture intersect**.

🔹 **Cloud & Hybrid Infrastructure** - Designing, integrating, automating, and troubleshooting infrastructure across cloud and on-premises environments.

🔹 **Automation Engineering** - Turning repetitive or error-prone operations into reliable tooling, scripts, workflows, and reusable processes.

🔹 **Security Engineering** - Working with identity, authentication, PKI, encryption, secure protocols, hardening, and security-conscious design.

🔹 **Systems & Networking** - Troubleshooting across operating systems, applications, networks, identity, and infrastructure rather than stopping at the boundary of a single technology.

🔹 **Architecture & Technical Strategy** - Evaluating technologies, understanding constraints and tradeoffs, and turning technical and operational requirements into practical solutions.

🔹 **Development & Tooling** - Building software and utilities when an off-the-shelf solution doesn't solve the problem—or when there's a better way to automate it.

> **I like solving the problems that don't fit neatly into one technology stack.**

---
## 🏗️ Selected Architecture & Engineering Case Studies

Code can show **what** someone built. I'm equally interested in documenting
**why** it was built that way.

At **[OsbornePro.com](https://osbornepro.com)**, I publish technical articles
and case studies covering the engineering behind real-world solutions.

I focus on the parts that often get left out of technical tutorials:
architecture decisions, constraints, security implications, tradeoffs,
automation, failure modes, and long-term maintainability.

### 🔹 Operations & Assurance Platform

**Problem:** Rapid MSP growth created a need to systematically translate client SOW obligations into recurring, verifiable operational work. The platform needed to ensure contractual responsibilities were understood and performed, provide evidence of completion, manage recurring service and access-verification tasks, incorporate new clients into established operational workflows, account for staffing conflicts during maintenance windows, and identify work that fell outside contracted scope.

**Approach:** Architected a centralized operations and assurance platform that converts client obligations and operational requirements into structured, trackable workflows for the engineering team. A Power Apps interface provides administrators with a centralized work queue, while Power Automate and SharePoint coordinate recurring tasks, onboarding workflows, maintenance activities, access verification, patching obligations, evidence collection, and management escalation.

The platform also incorporates AI-assisted review of out-of-band client project requests submitted through Microsoft Forms, helping determine whether requested work aligns with the client's SOW or requires separate billing and review.

The supporting Azure architecture uses Functions and Storage Queues for backend processing, Key Vault for third-party API secrets, Managed Identities where supported to reduce credential exposure, and Azure Monitor and Log Analytics for application monitoring, alerting, and troubleshooting.

**Key areas:** `Solution Architecture` · `Operational Governance` · `Automation` · `Power Platform` · `Azure` · `Security` · `Identity` · `Observability`

[Read the Operations & Assurance Platform Case Study →](https://osbornepro.com/blogs/operations-assurance-platform)

### 🔹 Patch Governance Platform

**Problem:** Patch governance across an MSP required administrators to repeatedly perform the same research for each client-reviewing known issues, identifying applicable KBs by operating system, correlating security advisories, and gathering vendor-specific vulnerability information. This duplicated effort across the organization and made consistent patching decisions more difficult.

**Approach:** Designed a centralized, tool-agnostic patch governance platform using SharePoint and automation to aggregate patching and security intelligence into a single operational resource. The platform collects information from Microsoft Graph, MSRC, Red Hat, Ubuntu, Action1, BleepingComputer, Palo Alto Networks, and other vendor and security feeds. A scheduled automation correlates the latest known issues, security advisories, and patch information and generates an interactive HTML report every Patch Tuesday, which is published to SharePoint for the engineering team.

Administrators can then work from a common intelligence source and filter the information according to each client's environment and requirements, instead of independently repeating the same research for every customer.

**Key areas:** `Solution Architecture` · `Patch Governance` · `Security` · `Automation` · `Microsoft Graph` · `SharePoint` · `API Integration`

[Read the Patch Governance Platform Case Study →](https://osbornepro.com/blogs/tool-agnostic-patch-governance)

### 🔹 DMARC Analytics Platform

**Problem:** Gain visibility into SPF and DKIM authentication failures and provide the insight needed to safely progress toward a `p=reject` DMARC policy, while minimizing deployment time, operational complexity, and cost. The solution also needed to be repeatable, allowing an MSP to efficiently deploy the platform across multiple client environments.

**Approach:** Designed an Azure-based DMARC analytics platform and automated its deployment using Bicep and Power Automate. The solution combines report ingestion, storage, SQL-based processing, and Grafana visualization to turn DMARC aggregate reports into actionable authentication data.

**Key areas:** `Solution Architecture` · `Azure` · `Infrastructure as Code` · `Automation` · `DMARC` · `DKIM` · `SPF`

[Read the DMARC Analytics Platform Case Study →](https://osbornepro.com/blogs/dmarc-analytics-platform)

### ➜ [Explore all technical work and case studies at OsbornePro.com](https://osbornepro.com)

---

## 🛠️ Projects, Tools & Open Source

I build and maintain tooling around infrastructure, automation, administration, and security.

Many of my projects start with a simple question:

**"Why am I doing this manually?"**

...and occasionally:

**"Why doesn't a tool for this already exist?"** 😄

### 🔑 NovaKey

A secure secret-delivery system designed to move sensitive values from a mobile device to a desktop without turning the desktop into another long-term secret store.

NovaKey addresses a problem that sits between traditional password managers and everyday workflows: **how do you securely deliver a secret to the system where it's needed while minimizing unnecessary handling and exposure?**

Rather than functioning as another password manager, NovaKey focuses on the **secure delivery and controlled use of secrets between devices**. It provides a purpose-built workflow for getting credentials and other sensitive values from a trusted mobile device into desktop workflows when they're needed.

The project explores the kind of security problem I find particularly interesting: **designing around trust boundaries, minimizing secret exposure, and making secure behavior practical enough to use every day.**

[![GitHub](https://img.shields.io/badge/GitHub-NovaKey-181717?style=for-the-badge\&logo=github)](https://github.com/OsbornePro/NovaKey-Daemon)

### 🌐 RDAP-CLI

A modern command-line replacement for the traditional `whois` utility.

As RDAP replaced WHOIS as the standardized protocol for domain and IP registration data, there wasn't a natural command-line successor to the familiar `whois` workflow. I built RDAP-CLI to fill that gap—providing a practical CLI for querying modern RDAP services while preserving the simplicity administrators and engineers expect from a command-line utility.

This is the kind of project I enjoy building: **identify a gap, understand the underlying standards and protocols, and create tooling that makes the technology practical to use.**

[![GitHub](https://img.shields.io/badge/GitHub-RDAP--CLI-181717?style=for-the-badge\&logo=github)](https://github.com/OsbornePro/rdap-cli)

### 🔐 EncrypIT

One of my original security-focused projects, built to make strong file encryption accessible and practical. EncrypIT is still available through SourceForge.

[![Download EncrypIT](https://img.shields.io/badge/Download-EncrypIT-0066CC?style=for-the-badge)](https://sourceforge.net/projects/encrypit/files/latest/download)

### 🛡️ BTPS-SecPack

An endpoint security and administration toolkit I developed before modern EDR platforms became commonplace. BTPS-SecPack brought together security tooling and administrative capabilities to help protect and manage Windows environments.

[![BTPS SecPack](https://img.shields.io/badge/BTPS-SecPack-222222?style=for-the-badge)](https://btpssecpack.osbornepro.com)

### ⚡ PowerShell

PowerShell has been one of my primary tools for turning systems administration into engineering. I build and publish reusable modules and tooling designed to automate operations, standardize processes, and solve real-world infrastructure problems.

[![PowerShell Gallery](https://img.shields.io/badge/PowerShell%20Gallery-tobor-5391FE?style=for-the-badge\&logo=powershell)](https://www.powershellgallery.com/profiles/tobor)


### 💻 More Code

[![GitHub](https://img.shields.io/badge/GitHub-tobor88-181717?style=for-the-badge\&logo=github)](https://github.com/tobor88)
[![OsbornePro GitHub](https://img.shields.io/badge/GitHub-OsbornePro-181717?style=for-the-badge\&logo=github)](https://github.com/OsbornePro)
[![GitLab](https://img.shields.io/badge/GitLab-tobor88-FC6D26?style=for-the-badge\&logo=gitlab\&logoColor=white)](https://gitlab.com/tobor88)

---

## ⚙️ Tools & Languages

These are some of the technologies I regularly use to build, automate, troubleshoot, and secure systems.

<table>
  <tbody>
    <tr valign="top">
      <td width="20%" align="center">
        <strong>C#</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/c-sharp.svg">
      </td>
      <td width="20%" align="center">
        <strong>PowerShell</strong><br><br>
        <img height="55px" src="https://raw.githubusercontent.com/theJasonHelmick/PowerShellImages/master/Icons/ps_black_128.svg">
      </td>
      <td width="20%" align="center">
        <strong>Bash</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/bash.svg">
      </td>
      <td width="20%" align="center">
        <strong>.NET</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/dotnet.svg">
      </td>
      <td width="20%" align="center">
        <strong>Ansible</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/ansible.svg">
      </td>
    </tr>
    <tr valign="top">
      <td width="20%" align="center">
        <strong>JavaScript</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/javascript.svg">
      </td>
      <td width="20%" align="center">
        <strong>Git</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/git-icon.svg">
      </td>
      <td width="20%" align="center">
        <strong>YAML</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/yaml.svg">
      </td>
      <td width="20%" align="center">
        <strong>VS Code</strong><br><br>
        <img height="55px" src="https://cdn.svgporn.com/logos/visual-studio-code.svg">
      </td>
      <td width="20%" align="center">
        <strong>Automation</strong><br><br>
        ⚙️
      </td>
    </tr>
  </tbody>
</table>

---

## 🎥 OsbornePro TV

I also run the **OsbornePro YouTube channel**, where I break down technologies, security concepts, infrastructure, automation, and secure protocols.

The channel originally started as a way for me to demonstrate hands-on technical knowledge and share what I'd learned as an administrator and engineer. Today, it's another part of the larger OsbornePro technical library.

My goal has always been to go beyond surface-level *"click here, run this command"* tutorials.

I want someone watching to understand **how the technology works, why we're configuring it this way, what can go wrong, and how to build it securely and maintainably.**

If detailed walkthroughs and getting into the weeds sounds like your kind of thing, come join the community.

[![YouTube](https://img.shields.io/badge/YouTube-OsbornePro%20TV-FF0000?style=for-the-badge\&logo=youtube\&logoColor=white)](https://www.youtube.com/c/OsborneProLLC?sub_confirmation=1)

---

## 🔒 Security Research & Labs

Security has always been an important part of how I approach infrastructure and engineering.

I also spend time breaking things on purpose. 😉

My security work and labs have included offensive and defensive security concepts, Hack The Box challenges, security tooling, protocol analysis, and documenting the techniques I've learned along the way.

[![HTB Writeups](https://img.shields.io/badge/HTB-Writeups-9FEF00?style=for-the-badge\&logo=hackthebox\&logoColor=black)](https://writeups.osbornepro.com)
[![Hack The Box](https://img.shields.io/badge/Hack%20The%20Box-tobor-9FEF00?style=for-the-badge\&logo=hackthebox\&logoColor=black)](https://app.hackthebox.com/public/users/52286)

---

## 🎓 Certifications & Credentials

Technology changes constantly. Continuing to learn isn't optional in this field.

My certifications and professional credentials are available through Credly:

[![Credly](https://img.shields.io/badge/Credly-View%20Credentials-FF6B00?style=for-the-badge)](https://www.credly.com/users/roberthosborne/badges)

---

# 🏆 GitHub Trophies

Because serious engineering and shiny internet trophies don't have to be mutually exclusive. 😎

![trophy](https://github-profile-trophy.vercel.app/?username=tobor88)

---

# 📈 GitHub Activity

<table>
  <tr>
    <td>
      <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=tobor88&theme=monokai"
           width="100%"
           height="auto"
           alt="GitHub Profile Details">
    </td>
  </tr>
</table>

---

## 😄 Joke of the Day

![Jokes Card](https://readme-jokes.vercel.app/api?theme=dark)

---

## 🌐 Find Me Around the Internet

[![OsbornePro](https://img.shields.io/badge/Official-OsbornePro-red?style=flat-square)](https://osbornepro.com)  
[![NovaKey App](https://img.shields.io/badge/NovaKey-Documentation-purple?style=flat-square)](https://novakey.app)  
[![RDAP-CLI](https://img.shields.io/badge/RDAP--CLI-Documentation-white?style=flat-square)](https://rdap-cli.osbornepro.com)  
[![EncrypIT Docs](https://img.shields.io/badge/Official-OsbornePro-green?style=flat-square)](https://encrypit.osbornepro.com)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-roberthosborne-lightblue?style=flat-square)](https://www.linkedin.com/in/roberthosborne)  
[![YouTube](https://img.shields.io/badge/YouTube-OsbornePro%20TV-red?style=flat-square)](https://www.youtube.com/c/OsborneProLLC)  
[![GitHub](https://img.shields.io/badge/GitHub-tobor88-lightgray?style=flat-square)](https://github.com/tobor88)  
[![GitHub](https://img.shields.io/badge/GitHub-OsbornePro-lightgray?style=flat-square)](https://github.com/OsbornePro)  
[![GitLab](https://img.shields.io/badge/GitLab-tobor88-orange?style=flat-square)](https://gitlab.com/tobor88)  
[![PowerShell Gallery](https://img.shields.io/badge/PSGallery-tobor-darkblue?style=flat-square)](https://www.powershellgallery.com/profiles/tobor)  
[![HTB Writeups](https://img.shields.io/badge/HTB-Writeups-yellow?style=flat-square)](https://writeups.osbornepro.com)  
[![BTPS SecPack](https://img.shields.io/badge/BTPS-SecPack-black?style=flat-square)](https://btpssecpack.osbornepro.com)  
[![Hack The Box](https://img.shields.io/badge/HackTheBox-tobor-green?style=flat-square)](https://app.hackthebox.com/public/users/52286)  
[![Credly](https://img.shields.io/badge/Credly-roberthosborne-blue?style=flat-square)](https://www.credly.com/users/roberthosborne/badges)  

### 📬 Contact

**[rosborne@osbornepro.com](mailto:rosborne@osbornepro.com)**

---

*"Automate the boring stuff. Understand the complicated stuff. Secure all of it."*
