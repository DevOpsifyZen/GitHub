# 🧠 GitHub Security Practice Labs Guide

> **Purpose:**  
> This guide provides direct access to official GitHub & Microsoft Learn labs to help you practice core repository security features — **Dependabot**, **Secret Scanning**, and **CodeQL** — hands-on.

---

## ⚙️ Prerequisites
Before starting, ensure you have:
- A **GitHub account**  
- Basic understanding of repositories, branches, and pull requests  
- A test repository or fork permissions  
- A browser and internet connection  

---

## 🛡️ LAB 1 — Dependabot: Automated Dependency Security Updates

### 🔍 Overview
**Dependabot** keeps your dependencies up to date and secure by detecting outdated or vulnerable packages and opening pull requests to fix them automatically.

### 📚 Official Learning Path
- **Microsoft Learn Module:**  
  👉 [Configure Dependabot security updates on GitHub repository](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/7-exercise)
  
- **GitHub Skills Lab:**  
  👉 [Secure repository supply chain](https://github.com/skills-dev/secure-repository-supply-chain)

- **Advisory Database (for CVEs):**  
  👉 [GitHub Security Advisories](https://github.com/advisories)

### 🎯 Learning Goals
- Understand how Dependabot identifies vulnerable dependencies  
- Configure automated dependency updates  
- Review and merge Dependabot pull requests  
- Explore the GitHub Advisory Database  

### 🧭 Practice Tip
> Fork the **skills-dev/secure-repository-supply-chain** repo, enable **Dependabot alerts**, and explore PRs raised by Dependabot.

---

## 🔐 LAB 2 — Secret Scanning: Detect and Prevent Leaked Secrets

### 🔍 Overview
**Secret Scanning** protects your code from accidental secret leaks by scanning for API keys, tokens, and credentials.

### 📚 Official Learning Path
- **Microsoft Learn Module:**  
  👉 [Configure and use secret scanning in a GitHub repository](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/5-exercise)
  
- **GitHub Skills Lab:**  
  👉 [Introduction to Secret Scanning](https://github.com/skills-dev/introduction-to-secret-scanning)

### 🎯 Learning Goals
- Enable and manage secret scanning in repositories  
- Understand push protection and secret alert workflows  
- Learn how GitHub detects exposed secrets  

### 🧭 Practice Tip
> Fork the **skills-dev/introduction-to-secret-scanning** repo and enable secret scanning under **Settings → Code Security and Analysis** to see how alerts are generated.

---

## 🧬 LAB 3 — CodeQL: Static Analysis for Vulnerability Detection

### 🔍 Overview
**CodeQL** performs static code analysis to identify security issues, code quality flaws, and potential vulnerabilities within your project.

### 📚 Official Learning Path
- **Microsoft Learn Module:**  
  👉 [Configure code scanning in a GitHub repository](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/)
  
- **GitHub Skills Lab:**  
  👉 [Introduction to CodeQL](https://github.com/skills-dev/introduction-to-codeql)

### 🎯 Learning Goals
- Understand how CodeQL analyzes source code  
- Set up automated code scanning in GitHub Actions  
- Review and triage security alerts from scans  

### 🧭 Practice Tip
> Use the **skills-dev/introduction-to-codeql** repository to experiment with CodeQL workflows and explore detected vulnerabilities.

---

## 📘 Summary

| 🔧 Feature | 🔗 Official Learning Path | 💡 Key Focus |
|-------------|---------------------------|---------------|
| **Dependabot** | [Dependabot Lab](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/7-exercise) | Secure & update dependencies automatically |
| **Secret Scanning** | [Secret Scanning Lab](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/5-exercise) | Detect and block exposed credentials |
| **CodeQL** | [CodeQL Lab](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/) | Analyze code for vulnerabilities |

---

## 🌐 Additional References
- [GitHub Security Overview](https://docs.github.com/en/code-security)
- [GitHub Actions Security Best Practices](https://docs.github.com/en/actions/security-guides/security-hardening-for-github-actions)
- [Microsoft Learn – GitHub Security Modules](https://learn.microsoft.com/en-us/training/browse/?products=github&expanded=github%2Csecurity)

---

> 🏁 **End of Guide**  
> Practice using the official labs linked above to gain real-world experience securing GitHub repositories with built-in tools.
