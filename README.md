# Awesome-Static-Code-Analysis-SAST

# Top Static Code Analysis (SAST) Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Semantic Taint Analysis, Quality Gates & CI/CD Security Integration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Static Application Security Testing (SAST)**. These tools analyze source code, bytecode, and binaries without executing them — identifying injection flaws, insecure patterns, hardcoded secrets, and compliance violations before code reaches production.

**Examples** include Veracode, Checkmarx, SonarQube, Snyk Code, Fortify, Mend.io, Rapid7 InsightAppSec, Coverity, GitHub Advanced Security, and Codacy (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom rule authoring, and transparent taint tracking — ideal for security engineers prioritizing code privacy, developers building DevSecOps pipelines, and organizations that need SAST depth without per-application enterprise licensing.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Veracode](https://www.veracode.com/)**  
  **The reference enterprise SAST platform for regulated industries.** Mature **interprocedural taint engine** considered one of the most robust on the market, with the vendor claiming low false-positive rates . Supports static testing across **100+ languages and frameworks**, plus DAST and SCA in a unified cloud platform . **Risk Manager** aggregates and deduplicates findings from scanners you already run. **Veracode Fix** proposes AI-assisted remediations covering over 70% of detected flaws in 10 languages . **Compliance reporting** covers PCI DSS, HIPAA, OWASP, NIST SP 800-53, ISO 27001, SOC 2 Type II, GDPR, and DORA; SaaS platform holds **FedRAMP Moderate ATO** . **Limitations**: **No on-premise or air-gapped option** — excludes sectors with data residency requirements . No free tier; pricing negotiated per application through sales . Traditional model favors scheduled, upload-based scans, pushing findings to end of sprint rather than the moment code is written .

- **[Checkmarx One](https://checkmarx.com/)**  
  **The closest like-for-like competitor to Veracode on breadth and enterprise depth.** Cloud-native platform bundling **SAST, DAST, SCA, API security, IaC scanning, container security, and Codebashing** developer training . **Deep language and framework coverage**, particularly in Java and complex enterprise stacks . Named a Leader in the **2026 Gartner Magic Quadrant for Software Supply Chain Security** . **On-premise deployment available** for organizations with code residency requirements . **Compliance reporting** mapped to PCI DSS, HIPAA, OWASP, and GDPR with enterprise SIEM, ticketing, and GRC integrations . **Limitations**: **No free tier** — pricing only via sales . SAST engine historically **chatty on false positives** if left at default settings; budget time for triage tuning . Configuration and tuning take real effort .

- **[SonarQube](https://www.sonarsource.com/)**  
  **The most widely adopted code quality and security platform.** The **Community Build is free and open source**, covering **21 languages and frameworks** including Java, JavaScript, TypeScript, Python, C#, Go, Ruby, Terraform, Docker, Kubernetes, and more . Detects **bugs, basic vulnerabilities, security hotspots, and hardcoded secrets** with **quality gates** that fail builds when new code falls below standard . Tracks **technical debt** with effort estimates for prioritization . **CI/CD integration** with GitHub, GitLab, Bitbucket, and Azure DevOps; extensible with **50+ community plugins** . **Commercial editions** (Developer, Enterprise, Data Center) add **advanced SAST with taint analysis**, C/C++ support, branch/PR analysis, SCA, IaC analysis, and enterprise reporting . **Limitations**: **Security depth lower than Checkmarx** on Java and enterprise stacks . **No native DAST** — pair with a dedicated tool . **Community Build has limited security checks** — advanced SAST and secrets detection require Developer Edition . Self-hosting means running the database and scanners yourself.

- **[Snyk Code](https://snyk.io/product/snyk-code/)**  
  **Developer-first SAST with fast IDE and pull-request feedback.** Built for **shift-left workflows** — findings appear in the editor and CI pipeline rather than a separate portal . Strong **open source and dependency risk** focus alongside code scanning. **Limitations**: **Less depth on enterprise SAST** than Checkmarx or Veracode . **Cost at scale and alert volume** are recurring critiques .

- **[Fortify (OpenText)](https://www.opentext.com/)**  
  **Long-standing enterprise SAST** with broad language coverage and centralized policy management. Often shortlisted alongside Veracode and Checkmarx for **large compliance-driven AppSec programs** .

- **[Mend.io](https://www.mend.io/)**  
  **Unified governance for code and AI you build.** Pioneered enterprise **Software Composition Analysis**, now expanded to SAST, secrets detection, and reachability analysis . **AI-focused capabilities** include continuous AI behavioral testing and runtime in-application protection . Independent from model providers.

- **[Rapid7 InsightAppSec](https://www.rapid7.com/)**  
  **DAST-first platform with SAST capabilities** within the Rapid7 vulnerability management ecosystem. Best for teams already using Rapid7 for infrastructure scanning.

- **[Coverity (Synopsys)](https://www.synopsys.com/)**  
  **Pioneering SAST engine** known for deep static analysis of C/C++ and complex embedded systems. Strong in **safety-critical and regulated environments** where code cannot leave the perimeter.

- **[GitHub Advanced Security](https://github.com/features/security/code)**  
  **Native SAST within GitHub** powered by **CodeQL** — deep semantic analysis with the QL query language. **Free on public repositories**; **paid add-on for private repos** . Results post to the Security tab as severity-rated dataflow findings including taint, deserialization, SSRF, and command injection . Built by GitHub Security Lab for vulnerability research .

- **[Codacy](https://www.codacy.com/)**  
  **Automated code review platform** with static analysis, coverage tracking, and quality metrics. Simpler and cheaper than enterprise SAST for smaller teams.

## Open-Source GitHub Projects

- **[Semgrep](https://github.com/semgrep/semgrep)**  
  **The leading open-source lightweight SAST** — 9,700+ GitHub stars . **Custom YAML rules** enable writing organization-specific security patterns without complex DSLs. **Supports 30+ languages** including C#, Go, Java, JavaScript, Python, Ruby, Rust, Scala, Terraform, TypeScript, and more . **Fast CI/CD integration** with SARIF output for PR annotations . The **Opengrep fork** (LGPL-2.1) provides a community-driven alternative with 30+ language support and Semgrep-compatible rules . **Best for teams wanting customizable, fast SAST without commercial licensing** .

- **[CodeQL](https://github.com/github/codeql)**  
  **Deep semantic analysis engine powering GitHub Advanced Security** — the standard CodeQL libraries and queries are **MIT licensed** . Uses **QL query language** for expressing complex dataflow and taint-tracking queries. **Supports ~17 languages** including C/C++, C#, Go, Java, JavaScript, Python, Ruby, Swift . **Built for vulnerability research** — GitHub Security Lab uses it to find CVEs in open source projects . **CodeQL CLI** is in a separate repository and licensed separately . **Best for security researchers and teams wanting deep semantic analysis with custom queries** .

- **[SonarQube Community Build](https://github.com/SonarSource/sonarqube)**  
  **The free, open-source edition of SonarQube** — **21 languages and frameworks** with static analysis for bugs, basic vulnerabilities, and security hotspots . **Quality gates** enforce standards on new code. **Technical debt tracking** with effort estimates. **CI/CD integration** with GitHub, GitLab, Bitbucket, Azure DevOps. **Extensible with 50+ community plugins** . **Limitations**: **No advanced SAST taint analysis** — that requires Developer Edition . **Single-threaded** and limited for large projects . **Best for small teams and individual developers** starting with code quality and basic security.

- **[Bandit](https://github.com/PyCQA/bandit)**  
  **Security linter for Python** — analyzes Python AST for common vulnerabilities and hardcoded secrets . Fast, focused, and widely adopted in Python CI pipelines. **Best for Python-specific security scanning** .

- **[Brakeman](https://github.com/presidentbeef/brakeman)**  
  **Deep Rails framework-aware analysis with low false positives** — understands Rails conventions and data flow . **Best for Ruby on Rails security** where generic SAST tools produce excessive noise .

- **[gosec](https://github.com/securego/gosec)**  
  **Security inspector for Go source code** — scans AST for vulnerabilities including injection, crypto misuse, and file permissions . **Best for Go security scanning** .

- **[SpotBugs](https://github.com/spotbugs/spotbugs)**  
  **Successor to FindBugs** — detects bug patterns in Java bytecode . Mature and widely integrated into Java build pipelines . **Best for Java bytecode analysis** .

- **[PMD](https://github.com/pmd/pmd)**  
  **Extensible multi-language analyzer** for Java, JavaScript, Swift, and more . Detects common flaws like unused variables and empty catch blocks . **Best for multi-language code quality** .

- **[NodeJsScan](https://github.com/ajinabraham/nodejsscan)**  
  **Static security code scanner for Node.js applications** — 2,300+ GitHub stars . Detects injection, insecure dependencies, and common Node.js vulnerabilities . **Best for Node.js security scanning** .

- **[Flawfinder](https://github.com/david-a-wheeler/flawfinder)**  
  **Built-in database of dangerous functions** (strcpy, gets, printf) for C/C++ . Simple and fast. **Best for quick C/C++ dangerous function detection** .

- **[cppcheck](https://github.com/danmar/cppcheck)**  
  **Focuses on errors compilers miss, aims for zero false positives** — static analysis for C/C++ . **Best for C/C++ where false positives are costly** .

- **[Bearer](https://github.com/Bearer/bearer)**  
  **Security and privacy-focused SAST** with data-flow analysis for **PII/PHI detection** — 1,800+ GitHub stars . Supports Go, Java, JS, PHP, Python, Ruby, TS . **Best for privacy compliance and data flow security** .

- **[Horusec](https://github.com/ZupIT/horusec)**  
  **Orchestrates 20+ SAST tools in one command** — 1,100+ GitHub stars . Great for **DevSecOps pipelines** wanting unified output across multiple scanners . Supports C#, Go, Java, JS, Kotlin, Python, Ruby, and more . **Best for orchestrating multiple SAST tools** .

- **[Terrascan](https://github.com/tenable/terrascan)**  
  **Compliance and security violation detection for Terraform, Kubernetes, and Docker** — 4,400+ GitHub stars . **Best for Infrastructure as Code security** .

- **[Checkov](https://github.com/bridgecrewio/checkov)**  
  **Static analysis for Terraform, CloudFormation, Kubernetes, and ARM** — IaC security scanning with 1,000+ policies . **Best for multi-cloud IaC security** .

- **[KICS](https://github.com/Checkmarx/kics)**  
  **2,000+ queries for infrastructure code** from Checkmarx — comprehensive IaC security scanning . **Best for deep IaC security coverage** .

- **[gitleaks](https://github.com/gitleaks/gitleaks)**  
  **Hardcoded secrets detection** for API keys, passwords, and tokens — 25,000+ GitHub stars . **Best for preventing secret leaks in Git history** .

- **[TruffleHog](https://github.com/trufflesecurity/trufflehog)**  
  **Deep credential scanning across Git repositories** — 25,000+ GitHub stars . **Best for comprehensive credential discovery** .

- **[codegrep](https://github.com/deepusingh2530/codegrep)**  
  **Fast, fully-offline SAST scanner in Rust** — curated MIT-original rule corpus across **27 languages** . **No network, no telemetry** . Features **diff-aware CI gating** (`--baseline main --diff-only`), **SARIF/JSON/JUnit output**, and **tree-sitter parsing** for Python, JavaScript, TypeScript, Go, Java, Ruby, PHP, C#, C, C++ . **Best for privacy-sensitive environments** where code cannot leave the perimeter .

### Additional Strong Open-Source Options

- **Globstar** — Fast, feature-rich open-source static analysis toolkit based on tree-sitter. MIT licensed .
- **analysis-tools-dev/static-analysis** — Curated directory of static analysis tools with 12,800+ GitHub stars .
- **ShiftLeftSecurity/sast-scan** — Free and open-source DevSecOps tool for SAST scanning, CI and Git friendly. 879 GitHub stars .
- **betterscan** — Code Scanning/SAST/Static Analysis using many tools/scanners with one report. 764 GitHub stars .
- **NodeSecure/js-x-ray** — JavaScript & Node.js open-source SAST scanner for detecting malicious patterns. 203 GitHub stars .

**Frameworks for building custom systems**: Combine **Semgrep** for fast, customizable SAST with YAML rules, **CodeQL** for deep semantic taint analysis and vulnerability research, **SonarQube Community Build** for code quality plus basic security with quality gates, **gitleaks** and **TruffleHog** for secrets detection, and **Checkov** or **KICS** for Infrastructure as Code security — to build a complete self-hosted SAST pipeline covering code, dependencies, secrets, and infrastructure.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- SAST tools differ significantly in analysis depth, false-positive rates, and deployment constraints. **Veracode has no on-premise option** — excludes defense, central banking, and critical infrastructure with code residency requirements . **SonarQube Community Build has limited security checks** — advanced SAST with taint analysis requires Developer Edition . **Checkmarx and Veracode SAST engines are chatty on false positives at default settings** — budget triage tuning time . **Migrating SAST tools mid-project is risky** — run old and new tools in parallel for 2-3 weeks without blocking merges before switching . **Alert fatigue is the main reason SAST fails in practice** — use baselining so only new findings break builds, limit PR scans to changed files, and prioritize IDE feedback over portal results .
- Self-hosted open-source solutions require proper rule maintenance, database management for SonarQube, and integration with existing CI/CD pipelines.

---

**Made for security engineers, DevSecOps teams, application security architects, and developers building SAST into their workflows.**  
Let's make static code analysis more open, accurate, and developer-friendly.
