<div align="center">

# 🚀 Introduction to Git and GitHub

### *IBM Skills Network - Collaborative Git & GitHub Workflow Demonstration*

[![Forked From](https://img.shields.io/badge/Forked_From-ibm--developer--skills--network-blue.svg)](https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-green.svg)](LICENSE)
[![GitHub Branches](https://img.shields.io/badge/Branches-main%20%7C%20bug--fix--typo%20%7C%20bug--fix--revert-orange.svg)]()
[![Maintainer](https://img.shields.io/badge/Maintainer-Talha--Yaseen--Hub-purple.svg)](https://github.com/Talha-Yaseen-Hub)

---

[Overview](#-overview) • [Formula & Specification](#-formula--specification) • [Git CLI Workflow](#-git-cli-workflow) • [License](#-license)

</div>

---

## 📌 Overview

This repository demonstrates collaborative version control practices using the **Git CLI** and **GitHub**. Originally forked from [ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub](https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub), it showcases practical workflows including:

- Repository forking & local cloning
- Feature branch creation & isolated development (`bug-fix-typo`)
- Branch merging into `main`
- Reverting commits using `git revert` (`bug-fix-revert`)
- Pull Request (PR) management to upstream repositories

---

## 🧮 Formula & Specification

The project provides specifications for computing simple interest given the principal amount, annual rate of interest, and time period in years.

### Input Parameters
```text
Input:
   p = principal amount ($)
   t = time period in years
   r = annual rate of interest (%)
```

### Mathematical Formula
$$\text{Simple Interest} = \frac{p \times t \times r}{100}$$

### Output
```text
Output:
   simple interest = (p * t * r) / 100
```

---

## 🛠️ Git CLI Workflow Demonstration

### 1. Branching & Merging (`bug-fix-typo`)
```bash
# Create and switch to bug-fix-typo branch
git checkout -b bug-fix-typo

# Apply fix and commit
git commit -am "Fix typo in copyright year in README.md"

# Merge back into main
git checkout main
git merge bug-fix-typo
```

### 2. Commit Revert (`bug-fix-revert`)
```bash
# Create revert branch
git checkout -b bug-fix-revert

# Revert commit safely without altering history
git revert HEAD --no-edit

# Verify branch tracking status
git branch -vv
```

---

## 📄 License

This project is licensed under the terms of the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.

---

<div align="center">

_© 2023 XYZ, Inc._

**Maintained by [Talha Yaseen (@Talha-Yaseen-Hub)](https://github.com/Talha-Yaseen-Hub)**

</div>
