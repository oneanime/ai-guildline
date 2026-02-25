---
apply: always
---

## Prohibited system-level package management commands
- **Ubuntu/Debian:** - `sudo apt install`, `sudo apt remove`, `sudo apt purge`, `sudo apt update`, `sudo apt upgrade`
    - `sudo apt-get install`, `sudo apt-get remove`, `sudo apt-get update`, `sudo apt-get upgrade`
    - `sudo dpkg -i`, `sudo dpkg -r`
- **macOS:** - `brew install`, `brew uninstall`, `brew update`, `brew upgrade`
    - `sudo installer -pkg`

## Naming Conventions (Java)

- **Principle: No Abbreviations**
  - All variable names, method names, class names, and file names must use **full words**.
  - Common abbreviations (e.g., `msg`, `err`, `idx`, `cnt`, `ctx`) are strictly prohibited. You must use the full form (e.g., `message`, `error`, `index`, `count`, `context`).
- **Exception: Names Exceeding 5 Words**
  - Abbreviations are permitted **only** if the name consists of a combination of **more than 5 words**, to prevent the name from becoming excessively long.
- **Mandatory Requirement: Chinese Comments**
  - If an abbreviation is used under the exception above, you **must** add a **comment in Chinese** on the same line (or immediately above) explaining the full meaning of the abbreviation.
- **Examples**
  - (Incorrect - Under 5 words, strict no abbreviation policy)
  - `String getUserInfo();`
  - (Correct - Full words used)
  - `String getUserInformation();`
  - (Correct - Over 5 words, abbreviation allowed with mandatory Chinese comment)
  - `// 缩写全称：calculateAverageMonthlyRecurringRevenueGrowth (计算平均月经常性收入增长)`
  - `double calcAvgMrrGrowth();`

## pom.xml (Maven)
- If `pom.xml` is modified, run `mvn dependency:resolve`.
