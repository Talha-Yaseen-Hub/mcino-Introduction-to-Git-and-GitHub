<a name="top"></a>
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:043927,50:10b981,100:043927&height=220&section=header&text=Interest%20Calculators&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=32&desc=Simple%20%26%20Compound%20Interest%20Tools%20%E2%80%94%20Bash%20%2B%20Python&descAlignY=54&descSize=15" width="100%"/> 
  <br/> 
  <img src="https://readme-typing-svg.demolab.com/?font=Poppins&weight=600&size=20&duration=2800&pause=900&color=D4AF37&center=true&vCenter=true&width=680&lines=Simple+Interest%3A+(P+%C3%97+T+%C3%97+R)+%2F+100;Compound+Interest%3A+P+%C3%97+(1+%2B+R%2F100)%5ET;Two+Calculators.+One+Git%2FGitHub+Practicum." alt="Typing SVG" /> 
  <br/><br/>
  <img src="https://skillicons.dev/icons?i=bash,py,linux,git,github&theme=dark" /> 
  <br/><br/>
  <img src="https://img.shields.io/badge/License-Apache%202.0-043927?style=for-the-badge&labelColor=D4AF37&logoColor=black" /> 
  <img src="https://img.shields.io/badge/Course-IBM%20Git%20%26%20GitHub-043927?style=for-the-badge&labelColor=10b981" /> 
  <img src="https://img.shields.io/badge/Contributor%20Covenant-043927?style=for-the-badge&labelColor=D4AF37&logoColor=black" /> 
  <br/><br/>
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:10b981,50:d4af37,100:10b981&height=4&section=header" width="60%"/> 
</div> 

<br/>

A pair of lightweight, open-source interest calculators — one in Bash, one in Python — built as part of the IBM "Introduction to Git and GitHub" practicum. The repository follows the same open-source governance standard as a production project: a clear license, a code of conduct, and structured contribution guidelines, so it doubles as hands-on practice for both financial math and real GitHub workflows.

<br/> 

<div align="center">
  <table>
    <tr>
      <td align="center"><b>➗ Simple Interest</b><br/>Linear growth, via Bash</td>
      <td align="center"><b>📈 Compound Interest</b><br/>Exponential growth, via Python</td>
      <td align="center"><b>🌐 Cross-Platform</b><br/>Linux, macOS, WSL</td>
      <td align="center"><b>📜 Governed</b><br/>Apache 2.0 + Contributor Covenant</td>
    </tr>
  </table>
</div> 

<br/>

## 📖 Table of Contents

<details open> 
<summary><b>▼ Click to expand / collapse</b></summary> 
<br/> 
<table> 
<tr> 
<td valign="top"> 

- [✨ Features](#-features)
- [🧮 The Two Formulas](#-the-two-formulas)
- [🔄 Program Logic](#-program-logic)
- [🚀 Quick Start](#-quick-start)
- [💡 Usage Guide](#-usage-guide)

</td> 
<td valign="top"> 

- [📁 Repository Structure](#-repository-structure)
- [👥 Open Source Governance](#-open-source-governance)
- [🔀 Contribution Workflow](#-contribution-workflow)
- [👤 Author](#-author)
- [📜 License](#-license)

</td> 
</tr> 
</table> 
</details> 

<br/>

---

## ✨ Features

| Feature | Script |
|---|---|
| ⚡ **Floating-point precision via `bc`** | `simple-interest.sh` |
| 🎨 **ANSI-colored terminal banners** | `simple-interest.sh` |
| 🛡️ **Numeric input validation** | `simple-interest.sh` |
| 📈 **Exponential growth calculation** | `compound_interest.py` |
| 🐍 **Native Python floating-point math** | `compound_interest.py` |
| 🌐 **Runs on Linux, macOS, WSL, Git Bash** | Both |
| 📜 **Apache 2.0 licensed, open governance** | Repository-wide |

<br/>

---

## 🧮 The Two Formulas

<div align="center"> 

### Simple Interest — grows in a straight line; interest only ever applies to the original principal.

$$\text{Simple Interest} = \frac{P \times T \times R}{100}$$

<br/>

### Compound Interest — grows exponentially; each period's interest gets added back into the principal before the next period is calculated.

$$\text{Compound Amount} = P \times \left(1 + \frac{R}{100}\right)^{T}$$

</div>

| Symbol | Meaning |
|---|---|
| **P** | Principal Amount ($) |
| **T** | Time Period (Years) |
| **R** | Annual Rate of Interest (%) |

<br/>

### Side by Side Comparison:

| Aspect | Simple Interest | Compound Interest |
|---|---|---|
| **Growth pattern** | Linear | Exponential |
| **Interest earned on** | Principal only | Principal + accumulated interest |
| **Typical real-world use** | Short-term loans | Savings & long-term investments |

<br/>

---

## 🔄 Program Logic

### `simple-interest.sh` Execution Flow:

```mermaid
flowchart TD 
    S([▶️ Run ./simple-interest.sh]) --> P1[💵 Prompt: Principal Amount] 
    P1 --> P2[📅 Prompt: Time in Years] 
    P2 --> P3[📈 Prompt: Annual Rate %] 
    P3 --> V{Valid Numeric Input?} 
    V -- No --> ERR[⚠️ Show Error & Re-prompt] 
    ERR --> P1 
    V -- Yes --> CALC[🧮 Compute via bc: P × T × R / 100] 
    CALC --> OUT[📊 Display Formatted Result] 
    OUT --> END([✅ Done]) 
    
    style S fill:#043927,color:#fff 
    style OUT fill:#10b981,color:#fff 
    style ERR fill:#E74C3C,color:#fff
```

<br/>

---

## 🚀 Quick Start

### Prerequisites

| For | Requires | Install |
|---|---|---|
| 🐚 `simple-interest.sh` | Bash + GNU `bc` | `# Debian / Ubuntu / Mint`<br/>`sudo apt-get update && sudo apt-get install -y bc bash`<br/><br/>`# macOS (Homebrew)`<br/>`brew install bc` |
| 🐍 `compound_interest.py` | Python 3 | `python3 --version` |

<br/>

### Installation

```bash
git clone https://github.com/Talha-Yaseen-Hub/mcino-Introduction-to-Git-and-GitHub.git
cd mcino-Introduction-to-Git-and-GitHub
chmod +x simple-interest.sh
```

<br/>

---

## 💡 Usage Guide

### ➗ Simple Interest (Bash)

```bash
./simple-interest.sh
```

```text
======================================================== 
          📊 SIMPLE INTEREST CALCULATOR 
======================================================== 
Enter the principal amount ($): 1000 
Enter time period in years: 3 
Enter rate of interest per year (%): 5 

======================================================== 
Calculated Simple Interest: $150.00 
======================================================== 
Thank you for using the Simple Interest Calculator!
```

---

## 📁 Repository Structure

```text
mcino-Introduction-to-Git-and-GitHub/ 
├── 📂 .github/             # Repository workflow configuration 
├── 🚫 .gitignore 
├── 🤝 CODE_OF_CONDUCT.md   # Community behavior standards 
├── ✍️ CONTRIBUTING.md      # Contribution guidelines 
├── 📜 LICENSE              # Apache License 2.0 
├── 📄 README.md            # Project documentation (this file) 
└── ➗ simple-interest.sh   # Bash simple interest calculator
```

<br/>

---

## 👥 Open Source Governance

| Document | Purpose |
|---|---|
| 📜 **[License](LICENSE)** | Released under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) |
| 🤝 **[Code of Conduct](CODE_OF_CONDUCT.md)** | Community behavior and interaction standards |
| ✍️ **[Contributing Guide](CONTRIBUTING.md)** | Steps for reporting bugs, submitting features, and opening Pull Requests |

<br/>

---

## 🔀 Contribution Workflow

```mermaid
flowchart LR 
    F[🍴 Fork Repository] --> B[🌿 Create Feature Branch] 
    B --> C[💻 Make Changes] 
    C --> T[✅ Test Locally] 
    T --> P[📬 Open Pull Request] 
    P --> R[👀 Maintainer Review] 
    R --> M[🔀 Merge] 
    
    style F fill:#043927,color:#fff 
    style M fill:#10b981,color:#fff
```

<br/>

---

## 👤 Author

<div align="center"> 

### **Talha Yaseen**
*Software Engineer | Tech Enthusiast*

<br/>

<a href="https://github.com/Talha-Yaseen-Hub"> 
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" /> 
</a> 
<a href="https://talha-yaseen.vercel.app/"> 
  <img src="https://img.shields.io/badge/Portfolio-043927?style=for-the-badge&logoColor=white" /> 
</a> 
<a href="mailto:talhavectorarts@gmail.com"> 
  <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /> 
</a> 

</div>

<br/>

---

## 📜 License

<div align="center"> 

<img src="https://img.shields.io/badge/License-Apache%202.0-043927?style=for-the-badge&labelColor=D4AF37&logoColor=black" /> 

<br/><br/>

Released under the Apache License 2.0 — see the [LICENSE](LICENSE) file for full details.

</div> 

<br/>

<div align="center"> 

*Built while learning Git & GitHub — one commit at a time.*

<br/><br/>

[⬆ Back to Top](#top)

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:10b981,50:043927,100:10b981&height=100&section=footer" width="100%"/> 

</div>
