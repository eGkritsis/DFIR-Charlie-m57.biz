# DFIR Case Study: M57.biz Incident Investigation

## Case Metadata
- **Case ID:** 00111122009  
- **Date Reported:** 10/12/2009  
- **Investigation Team:** DigiFor  
- **Subject:** Charlie (Patent Researcher at M57.biz)  
- **Keywords:** Data exfiltration, Steganography, Corporate espionage  

## Executive Summary
Digital forensic investigation into suspected data breach and intellectual property theft by employee Charlie at M57.biz, a patent research firm. Evidence indicates unauthorized disclosure of confidential client data to competitors using steganographic techniques and attempted extortion.

## 1. Case Background
### Incident Overview
- **Reporting Party:** Pat McGoo (CEO, M57.biz)
- **Trigger Event:** MAILER-DAEMON notification of failed email from Charlie's account
- **Suspected Timeframe:** November-December 2009 (post-hire period)
- **Allegations:** 
  - Unauthorized disclosure of confidential client data
  - Potential sale of trade secrets to competitors
  - Suspected use of data hiding techniques

## 2. Evidence Collection
### Seized Items (11/12/2009)
| Item | Serial Number | Status When Seized |
|------|---------------|--------------------|
| DELL Laptop | DEJ485BIDFGJF | Powered on |
| USB Flash Drive | 2007110203195377 | Disconnected |
| Power Adapter | Q4W0406021262 | Connected |
| Wired Mouse | 1939HS01D6W8 | Connected |

**Chain of Custody:** See Appendix E

### Witnesses Present
| Name | Role | Relation to Case |
|------|------|------------------|
| Charlie | Patent Researcher | Suspect |
| Terry | IT Administrator | Witness |
| Jack | Security Officer | Witness |

## 3. Forensic Methodology
### Investigation Phases
1. **Preparation** (10/12/2009 19:30-22:30)
   - Team briefing and role assignment (Appendix A)
   - Legal documentation (Appendix Z)
   - Equipment preparation (Table 1)

2. **Identification** (11/12/2009 08:32-09:10)
   - Workspace documentation
   - Witness interviews (Appendix B)

3. **Preservation** (11/12/2009 08:57-09:39)
   - Volatile data collection (RAM, Cache, Registry)
   - Disk imaging (FTK Imager, FEX Imager)
   - Tools: MDD MoonSols DumpIt, Win32dd

4. **Analysis** (Lab Examination)
   - Memory analysis: Volatility Framework 2.4
   - Disk analysis: Autopsy
   - Full findings: Appendices Γ and Δ

## 4. Key Findings
### File System Analysis
| Metric | Laptop HDD | USB Drive |
|--------|------------|-----------|
| OS | Windows XP (5.1) | N/A |
| Capacity | 10.24GB | 1.06GB |
| MD5 Hash | 0377b3d41bbbc295a1c9f00aa07ee174 | 9c0de6c8532d7a66ddcf01861dfb6535 |
| User Accounts | 12 | N/A |
| Installed Programs | 19 | N/A |

### Critical Evidence
#### Files of Interest
| File | Location | MD5 Hash | Significance |
|------|----------|----------|--------------|
| astronaut1.jpg | Disk: Files | 45eade24b3a89b21fed303310ccbdc54 | Steganographic file |
| 01.zip | Disk: Emails | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | Patent documents |
| microscope1.jpg | Disk: Emails | 4be2c4abb48c4389ca798e6c21736ea1 | Password carrier |

#### Suspicious Software
| Program | Install Date | Path |
|---------|--------------|------|
| Cygnus Hex Editor | 2009-11-24 | C:\Program Files\Cygnus FREE EDITION\ |
| Invisible Secrets 2.1 | 2009-11-19 | C:\Program Files\Invisible Secrets 2.1\ |

### Incriminating Communications
#### Email Evidence
1. **Data Sale to Competitor** (Charlie → jaime@project2400.com)
   - Offered Nitroba's confidential data for $50,000
   - Transferred steganographic file (astronaut1.jpg)
   - Provided password "nitro" after partial payment

2. **Extortion Attempt** (Charlie → andy@swexpert.com)
   - Demanded $100,000 for "immortality patent" information
   - Used password-protected ZIP and steganographic JPG

#### Web Search History
| Date | Search Query | Engine |
|------|--------------|--------|
| 2009-11-19 | "steganography" | Google |
| 2009-11-19 | "steganography tool free" | Google |
| 2009-11-24 | "open source hex editor" | Google |

## 5. Conclusions
Charlie is implicated in:
1. Breach of confidentiality agreements
2. Unauthorized sale of trade secrets
3. Attempted extortion
4. Data concealment using steganography
5. Violation of corporate security policies

**Recommendation:** Legal prosecution supported by digital evidence maintaining ACPO standards. Full timeline available in Appendix Η.

## Appendices
- Α: RACI Matrix
- Β: Witness Statements
- Γ: Disk Analysis
- Δ: Memory Analysis
- Ε: Chain of Custody
- Η: Activity Timeline
- Θ: Steganalysis Report
- Z: Legal Agreements
