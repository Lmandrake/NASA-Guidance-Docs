# FIPS PUB 199 — Standards for Security Categorization of Federal Information and Information Systems

> **External, not NASA governance.** Useful for comparison and vocabulary. It never establishes
> what NASA requires, and must not be cited as NASA coverage.

| | |
|---|---|
| **Publisher / owner** | National Institute of Standards and Technology (NIST), Information Technology Laboratory, Computer Security Division; U.S. Department of Commerce |
| **Kind** | Federal Information Processing Standard (a mandatory federal standard for in-scope systems) |
| **Status** | Dated February 2004 (cover, PDF p.1). "These standards are effective upon approval by the Secretary of Commerce" (§2, PDF p.5). Whether it has been revised or withdrawn since was not checked against any register here |
| **Where to get it** | Public: `https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.199.pdf` (confirmed anonymously off-network, 2026-10-26) |
| **Binds whom** | "all federal information systems other than those information systems designated as national security systems" and federal information other than classified information (§2, PDF p.5) |

**What it is good for, relative to NASA's documents.** The common federal vocabulary for how bad a security loss would be: three security objectives and three impact levels. Useful for reading any NASA or contractor document that "categorizes" a system as Low, Moderate or High. It is a security-impact scheme, not a safety-hazard or mission-risk classification (our reading).

**Key content.**
- Purpose: standards "to categorize all information and information systems [...] based on the objectives of providing appropriate levels of information security according to a range of risk levels" (§1, PDF p.5).
- Three security objectives: confidentiality, integrity, availability (§3, PDF p.6).
- Three impact levels. LOW is "a limited adverse effect"; MODERATE is "a serious adverse effect"; HIGH is "a severe or catastrophic adverse effect" (§3, PDF pp.6-7).
- Information types are categorized per objective, then a system takes the "highest values (i.e., high water mark)" across the types it holds (§3, PDF p.8).
- Security categories are "to be used in conjunction with vulnerability and threat information in assessing the risk" (§3, PDF p.5).
- It says nothing specific about AI or machine learning (our reading; the text predates that vocabulary).

**Nearest NASA counterpart.** `../documents/NPR_2810.1F.md` (Security of Information and Information Systems), which lists categorizing systems by criticality and sensitivity among information system owner duties (§1.2.3.10, p.13-14). That is our reading of the closest counterpart; we have not found, on that page, a statement that NPR 2810.1F invokes FIPS 199.
