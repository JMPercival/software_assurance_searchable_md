class: center, middle
# Software Assurance
---

class: center, middle
![Dilbert](http://assets.amuniversal.com/ea1384e06cbb01301d46001dd8b71c47)
???
Fixing software bugs presents a high-cost when software is already in production. Imagine fixing/replacing a lego block that is embedded deep within your structure!
---
class: center, middle
![Dilbert](http://assets.amuniversal.com/73bbbf606d5c01301d80001dd8b71c47)
???
We have now come to tolerate bugs in software. The "business as usual" culture at its best.
---
class: center, middle
![Dilbert](http://assets.amuniversal.com/26c55a909fd8012f2fe600163e41dd5b)
???
As organizations struggle with the quality/cost of in-house software development, outsourcing does not rid of the responsibilities. In fact, expressing expectations and assessing becomes even more important!
---
class: center, middle
[![sandworm](https://regmedia.co.uk/2014/10/14/sandworm_vuln_logo.jpg)](http://www.theregister.co.uk/2014/10/14/isight_microsoft_announce_windows_and_windows_server_0day/)
???
As we explore this course topic, it helps to know about recent day software failures. Each one of these send organizations scrambling for testing and applying patches in their environments.

2014 Sandworm used a zero day exploit in all version of Microsoft Windows. The vulnerability exists in PACKAGER.DLL, which is a part of Windows Object Linking and Embedding (OLE) property. By using a crafted PowerPoint document, an .INF file in embedded OLE object can be copied from a remote SMB share folder and installed on the system. Attackers can exploit this logic defect to execute another malware, downloaded via the same means. [Source: http://blog.trendmicro.com/trendlabs-security-intelligence/an-analysis-of-windows-zero-day-vulnerability-cve-2014-4114-aka-sandworm/]

CVE: https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2014-4114
CWE: Improper Input Validation (CWE-20)
---
class: center, middle
[![Heartbleed](http://heartbleed.com/heartbleed.png)](http://heartbleed.com)
???
2014 Heartbleed in the OpenSSL library was really a wake-up call for organizations using poor management practices for software acquisition and inventory. Many organizations started paying attention to open source software risk management after this incident. This bug involved a buffer length check issue that allowed an attacker to read all memory contents including SSL\TLS keys used for encryption. At the time, none of the open source or proprietary static or dynamic analysis tools
could discover this vulnerability.
CWE-130: Improper Handling of Length Parameter Inconsistency

---
class: center, middle
[![shellshock](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Shellshock-bug.png/440px-Shellshock-bug.png)](https://en.wikipedia.org/wiki/Shellshock_%28software_bug%29)

???
# Shellshock or Bashdoor
A issue in the bash shell that allowed arbitrary commands to be executed when the commands are concatenated to the end of function definitions stored in the values of environment variables. Within days of the publication of this, intense scrutiny of the underlying design flaws discovered a variety of related vulnerabilities, (CVE-2014-6277, CVE-2014-6278, CVE-2014-7169, CVE-2014-7186, and CVE-2014-7187).
---
class: center, middle
[![ghost](http://www.upstream.be/wp-content/uploads/2015/01/red-gost.jpg)](https://blog.qualys.com/laws-of-vulnerabilities/2015/01/27/the-ghost-vulnerability)
???
The GHOST vulnerability is a serious weakness in the Linux glibc library. It allows attackers to remotely take complete control of the victim system without having any prior knowledge of system credentials. CVE-2015-0235 has been assigned to this issue.
---
class: center, middle
[![badlock](http://img.deusm.com/darkreading/2016/04/1325083/badlock.png)](http://www.darkreading.com/vulnerabilities---threats/badlock-bug-declared-a-bust--but-patch-anyway/d/d-id/1325083)
???
## Badlock
Badlock bug in Windows and Samba revealed that the vulnerability was no blockbuster after all, but rather a widespread--and not critical-- vulnerability that can be abused in man-in-the-middle attacks in file server environments.

An attacker could intercept a user’s credentials and steal or modify files, or wage a denial-of-service attack, but he or she would have to be on the same network as the victim, security experts say.
---
class: center, middle
# [#gotofail](https://www.imperialviolet.org/2014/02/22/applebug.html)
???
# Apple SSL/TLS bug
Two goto fail lines in a row. The first one is correctly bound to the if statement but the second, despite the indentation, isn't conditional at all. The code will always jump to the end from that second goto, err will contain a successful value because the SHA1 update operation was successful and so the signature verification will never fail.

---
class: center, middle
# [Quadrooter](https://www.defcon.org/html/defcon-24/dc-24-speakers.html#Donenfeld)
???
* 2016
4 flaws in android discovered by a checkpoint researchers.
Challenge faced with fixing the Quadrooter flaws:
"Qualcomm has a significant position in the development chain, in that a phone maker isn't taking the Android open-source code directly from Google, they're actually taking it from Qualcomm,"
http://www.zdnet.com/article/quadrooter-security-flaws-affect-over-900-million-android-phones/

https://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2016-2503

---
class: center, middle
## What % is FUD and Marketing?
[![issues](http://techrights.org/wp-content/uploads/2015/04/ven2-1024x774.png)](http://techrights.org/2015/07/01/sonatype-marketing/)

---
## [Security Concerns in 2016](http://www.csoonline.com/article/3013107/security/forecast-2016-security-takes-center-stage.html)
![2016](http://core0.staticworld.net/images/article/2015/11/cw_techforecast2016_03_budget_booms_and_busts-100629394-large.idge.png)
???
# 2016 Predictions

---
class: middle
# [Top Security Concerns in 2017](http://www.csoonline.com/article/3199937/security/top-5-infosec-concerns-for-2017.html)

## Based on Searches on CSOonline
- Network Security
- Networking
- Windows OS (ransomware related)
- OS security
- Active Directory
???
# 2017 Predictions
---

class: left, middle
## .blue[Most discussions of IT security focus on IT infrastructure and process, stopping short of security considerations related to the design and implementation of the application itself...]

.footnote[
Brian Morgan, CTO, Skyline Technologies
]
???
This is an interesting observation. The security community is too busy dealing with fixing things from outside and dealing with the problem after it already is a serious problem. The predictions are almost about the things that the vendors can solve and can currently address. The latter part is the hard problem.

The software engineering community is too busy inventing solutions to build more and more complex pieces of software faster and cheaper.

---
class: center, middle
# Right questions to ask?
[![goal](http://4.bp.blogspot.com/-ZveWaoZMrvg/T74y7Qu2PXI/AAAAAAAACxc/keSwGPQLXkU/s400/soccer_security_blog.png)](http://cacm.acm.org/magazines/2009/6/28488-answering-the-wrong-questions-is-no-answer/fulltext)

???
Story time:  
[Source: http://cacm.acm.org/magazines/2009/6/28488-answering-the-wrong-questions-is-no-answer/fulltext]  
Two buddies leaving a tavern find a distressed and somewhat inebriated man on his hands and knees in the parking  lot, apparently searching for something.
They ask him what he has lost, and he replies that he has dropped his keys. He describes the keys, and says if the two men find them they will receive a
reward. They begin to help search. Other people come by and they too are drawn into the search. Soon, there is a crowd combing the lot, with an air of competition
to see who will be the first to find the keys. Periodically someone informs the crowd of the discovery of a coin or a particularly interesting piece of rock.
After a while, one in the crowd stands up and inquires of the fellow who lost his keys, “Say, are you sure you lost your keys out here in the lot?” To which the
man replies, “No. I lost them in the alley.”  Everyone stops to stare at the man. “Well, why the heck are you searching
for them here in the parking lot!?” someone exclaimed. To which the man replied, “Well, the light is so much better
here. And besides, now I have such good company!”

if we don’t properly define the problem, ask the right questions, and search in the proper places, they may have
good company and funding, but they shouldn’t expect to find what they are really seeking.

So it is in research—especially in cyber security and privacy. We have people seeking answers to the wrong
questions, often because that is where “the light is better” and there seems to be a bigger crowd around them. Until
we start asking questions that better address the problems that really need to be solved, we shouldn’t expect to
see progress. Here are a few examples of misleading questions:

* How do I secure my general purpose software against all threats?

* How do I protect my system with an intrusion-detection system, data
loss and prevention tools, firewalls, and other techniques?

* How do I find coding flaws in the system I am using so I can patch them?

Each of these questions implies it can be answered in a positive, meaningful way.
That is not necessarily the case.
We have generally failed to understand that when we build and deploy
systems they are used in a variety of environments, facing different threats.
There is no perfect security in any real system—hardware fails, people make
mistakes, and attacks outside our expectations may defeat our protection
mechanisms. If an attacker is sufficiently motivated and has enough resources
(including time), every system can be defeated in some manner.
If the attacker doesn’t care if the defeat is noticed, it may reduce the work factor
involved; as an obvious example, an assured denial-of-service attack can
be accomplished with enough nuclear weapons.

The goal in the practice of security is to construct sufficient defenses against the likely threats

---
class: center, middle
[![Tradition](images/tradition.png)](http://security.gloriad.org/blog/2007/10/21/traditional-thinking/)

---
class: center, middle
# What is Software Assurance?
---
# NASA Definition
## The planned and systematic set of activities that ensures that .red[software processes and products] conform to requirements, standards, and procedures.
.red[Processes]: include all of the activities involved in designing, developing, enhancing, and maintaining software    

.red[Products]: include the software, associated data, its documentation, and all supporting and reporting paperwork  
???
* The theme is organizational in nature and emphasizes a well thought-out set of activities to achieve compliance with organizational best practices, requirements standards and procedures.
* Process (a complete cradle to grave  approach for the software lifecycle)
* Products (this amounts to all the software artifacts produced
* NASA stays away from the word security because both security and safety are covered under the umbrella of their software assurance effort and goal is correctness !

---
# Committee on National Security Systems (CNSS)
## The level of confidence that .red[software] is free from .red[_vulnerabilities_], regardless of whether they are .red[intentionally] designed into the software or accidentally inserted later in its life cycle, and that the software functions in the intended manner.
???
- This understanding of software assurance is consistent with the use of the term in connection with information, i.e., information assurance (IA).
- A more technical definition which focuses on software flaws, intention, and time of introduction.  
- __lost the focus on engineering!__

---
![NSA definition](images/nsa-def.png)
.footnote[
.red[NSA Center for Assured Software]
]
???
NSA Center for Assured Software was stood up in 2005
* They focus on **exploitable** vulnerabilities only. Much more refined scope.
* NSA does not develop software, they only test it. So no emphasis on engineering here as well.

* Design analysis, however, is done before any code analysis.
* The "n+1" vulnerability problem. You will never be able to hire enough blackhat hackers, if the foundational design and engineering effort is missing.
---
# DHS
## A planned and systematic set of multidisciplinary activities must be applied to ensure the conformance of both .green[software and processes] to requirements, standards, and procedures
.red[Trustworthiness]: the absence of .green[exploitable vulnerabilities] whether maliciously or unintentionally inserted  

.red[Predictable execution]: provides .red[justifiable confidence] that the software, when executed, will function as intended
???
DHS definition is a medely of all prior definitions with a focus on engineering, vulnerabilities and justifiable confidence for a complex system property
---
# Academics
## Secure software cannot be intentionally .red[subverted or forced to fail]
The software that remains .red[correct] and predictable in spite of intentional efforts to compromise .red[dependability]
???
Leave it to academics to use big words!
---
# Software Engineering Institute

Application of .green[technologies and processes] to achieve a required level of .blue[confidence\*] that software systems and .red[services] function in the intended manner, are free from accidental or intentional vulnerabilities, provide .red[security capabilities appropriate to the threat environment], and .red[recover from intrusions and failures].

.footnote[
\*The use of the word .blue[confidence] implies that there is a .red[basis for the belief] that software systems and services function in the intended manner
]
---
# Dr. Gandhi's Version
## .red[Basis for the belief] that software will operate as expected in its .red[threat environment]
.red[Resist] most attacks  

.red[Tolerate] as many as possible of those attacks it cannot resist  

.red[Contain] the damage and recover to a normal level of operation as soon as possible  
???
Highlights:
* The focus of the definition is on Assurance: Providing the _Basis for the Belief_
* Software behavior is tied to it threat environment (avoid making general statements about secure software)
* Account for known attacks
* Acknowledge unknown attacks and plan for them.
* Recover from failures --> This is "resiliency"
# This is an outcome of Software Security Engineering
---

# Software Weakness

## A type of .red[mistake] in software that, in proper conditions, could contribute to the introduction of vulnerabilities within that software.
Weakness are any mistakes in implementation, design, or other phases of the software development lifecycle.
--

## .red[Basis for belief] increases if engineering evidence is available for _reducing_ weaknesses

---
class: center, middle
# Software Security Engineering*
The .red[Engineering Challenge] is now established.   
Next &mdash; How do we go about it?   

.footnote[
\*it is not the same as Security Software Engineering
]

???
A new term is introduced here to further clarify __Software Assurance__. This terms is better than saying _secure software_. The term security engineering reflects the intent that software has been developed and tested to operate as intended in its operational environment.
---
class: left, middle
## Probably the most serious risk in system software is incomplete design, in the sense that .red[inadvertent loopholes] exist in the protective barriers and have not been .red[foreseen by the designers].
.footnote[
The Ware Report, __1969__
]
???
Are these concerns fresh? think again!
---
class: left, middle
## The technical problem to be solved is that of determining .red[what constitutes an appropriate defense against malicious attack], and then developing hardware and software with the defensive mechanisms .red[built-in].
.footnote[
The Anderson Report, __1972__
]
???
Are these concerns fresh? think again!
---
class: center
# Course Goals
## .red[Internalize]
security engineering during the software development lifecycle
## .green[Assure]
through evidence-based beliefs
## .blue[Experience]
software security engineering by engaging in hand-on activities with Open Source Software
???
## [Internalize](https://www.google.com/#q=define+internalize)
security engineering during the software development lifecycle
## [Assure](https://www.google.com/#q=assure)
through evidence-based security
## [Experience](https://www.google.com/#q=experience)
security engineering by engaging in hand-on activities with  
Open Source Software
---
class: center
# Course Methods
## Process Agnostic
Analysis applicable in any [lifecycle](https://en.wikipedia.org/wiki/Software_development_process) [.blue[strategy]](https://en.wikipedia.org/wiki/Rational_Unified_Process)  
## Lightweight
Share and [institutionalize](https://www.google.com/search?q=intitutaionalize) knowledge  
## Practical
Methods currently used in [software engineering practice](https://www.bsimm.com/framework/)

???
## Process Agnostic
Analysis applicable in any [lifecycle strategy](https://en.wikipedia.org/wiki/Software_development_process)  
_Waterfall, Spiral, UML, Agile, etc._
## Lightweight
Share and [institutionalize](https://www.google.com/search?q=institutionalize) knowledge  
_Relevant and logically analyzable documentation_
## Practical
Methods currently used in software engineering practice  
_e.g., [Microsoft SDL](https://www.microsoft.com/en-us/sdl/), [BSIMM](https://www.bsimm.com/framework/), [SEI Curricula](http://www.cert.org/curricula/software-assurance-curriculum.cfm?)_
---

# Security .red[vs.] Safety, Reliability and Quality

## Common
Software works as expected despite the presence of certain internal and external stimuli, influences, and circumstances
--

## Different for Security
* The nature of external stimuli, influences, and circumstances:   
.red[An Intelligent, persistent adversary]
---
class: center, middle
# A Winning Strategy

---
class: center, middle
![Security Engineering](images/1-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/2-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/3-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/4-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/5-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/6-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/7-engineering-ross.png)
---
class: center, middle
![Security Engineering](images/8-engineering-ross.png)
---
class: center, middle
# Are you ready for it?
.footnote[
[Rugged manifesto](https://www.ruggedsoftware.org/)
]
---
class: center, middle
## “_This whole economic boom in cybersecurity seems largely to be a consequence of .red[poor engineering]._”  
.footnote[
Carl Landwehr, CACM, February **2015**
]
---
class: center, middle
# Discussion?
![that-dont-make-no-sense](https://media.giphy.com/media/DO5JobrylWL7i/giphy.gif)

---
class: center, middle
# Next up...
## Engineering for Assurance
class: center, middle
# Systems Security Engineering*

.footnote[
\*Based on Chapter 2 of [NIST SP 800-160 Systems Security Engineering](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-160.pdf)  
which expands on [ISO/IEC/IEEE 15288:2015
Systems and software engineering](http://www.iso.org/iso/catalogue_detail?csnumber=63711)
]

???
Appendices to NIST SP 800-160 are going to be added soon.
https://beta.csrc.nist.gov/News/2016/NIST-Special-Publication-800-160,-Systems-Secu-%281%29

---

class: center, middle
![Dilbert](http://assets.amuniversal.com/b7797c402f4901348be4005056a9545d)
???
Systems security engineering is hard. Particularly, when you have a well-resourced and capable adversary.

---

# Agenda

1. Need for Security Engineering  

1. Terminology  

1. Security Engineering Perspective  

1. Security Engineering Framework


---

![Tiers](images/dsb-taxonomy.png)
.footnote[
\*[Defense Science Board 2013 Report](http://www.acq.osd.mil/dsb/reports/2010s/ResilientMilitarySystemsCyberThreat.pdf)
]

???

# Report Terminology

## Cyber
broadly used to address the components and systems that provide all digital information, including weapons/battle management systems, IT systems, hardware, processors, and software operating systems and applications, both standalone and embedded.

## Resilience
defined as the ability to provide acceptable operations despite disruption: natural or man-made, inadvertent or deliberate.

## Existential Cyber Attack
defined as an attack that is capable of causing sufficient wide scale
damage for the government potentially to lose control of the country, including loss or damage to significant portions of military and critical infrastructure: power generation, communications, fuel and transportation, emergency services, financial services, etc.

The Task Force developed a threat hierarchy to describe capabilities of potential attackers, organized by level of skills and breadth of available resources
- Tiers I and II attackers primarily exploit known vulnerabilities
- Tiers III and IV attackers are better funded and have a level of expertise and sophistication sufficient to discover new vulnerabilities in systems and to exploit them
- Tiers V and VI attackers can invest large amounts of money (billions) and time (years) to actually create vulnerabilities in systems, including systems that are otherwise strongly protected.

Higher-tier competitors will use all capabilities available to them to attack a system but will usually try lower-tier exploits first before exposing their most advanced capabilities. Tier V and VI level capabilities are today limited to just a few countries such as the *United States, China and Russia*.

---

# Need for Security Engineering
## Vulnerabilities within organizations
- Known vulnerabilities
- .red[Unknown] vulnerabilities
- .red[Adversary-created] vulnerabilities

--

## Visible Vulnerabilities
- Discovery and patching

--

## Invisible Vulnerabilities
- Sound security engineering



???

2013 Defense Science Board Task Force described several tiers of vulnerabilities within organizations including known vulnerabilities, unknown vulnerabilities, and adversary-created vulnerabilities. The important and sobering message conveyed by the Defense Science Board is that the top two tiers of vulnerabilities (i.e., the unknown vulnerabilities and adversary-created vulnerabilities) are, for the most part, totally invisible to most organizations. These vulnerabilities can be effectively addressed by sound systems security engineering techniques, methodologies, processes, and practices—in essence, providing the necessary trustworthiness to withstand and survive well-resourced, sophisticated cyber-attacks on the systems supporting critical missions and business operations.

---
class: center, middle

![iceberg](http://www.titanicuniverse.com/wp-content/uploads/2014/12/iceberg.jpg)

.footnote[
\*.red[above the waterline] and .red[below the waterline] problems
]

???

If we think of an iceberg, the visible vulnerabilities are above the waterline and the invisible ones are the ones below. It is the invisible ones that are difficult to address and can potentially sink the ship!

We will refer to "above the waterline" and "below the waterline" problems

---
class: center, middle
# Systems Engineering View
.top-right[
    ![Abstractions](http://www.espen.com/graphics/math-answer-findx.gif)
]

---

# Terminology

## System
Combination of interacting .red[elements] organized to achieve stated purposes

--

## System Element
Recursively defined as a .red[system]  
Member of a set of elements that constitute a system  

_Examples: hardware; .red[software]; firmware; data; facilities; materials; humans; processes; and procedures_

???
# System and System Element
* The recursive definition of a system element allows us to support the notion of a system of systems.  
* The term **system** may apply to a collection of elements or a single element
* One observer's system may be another observer’s system element.  

---

# Terminology

## System-of-Interest
System that is the focus of the .red[engineering] effort

## Enabling System
System that supports a .red[system‐of‐interest] during its life cycle stages but does not necessarily contribute directly to its function during operation  

_Examples: code compilers, assemblers, prototypes, test harness, unit tests_

???
# System of Interest
* The term system-of-interest is used to define the set of system elements, system element interconnections, and the environment that it operates in.

---

# Terminology

## Other Systems
System that interacts with the .red[system‐of‐interest] in its operational environment

_Examples: a global positioning system space vehicle being an “other system” interacting with a GPS receiver as the “system‐of‐interest.”_

---

class: center, middle
![NIST SP 800-160 Public Draft 2](images/view.png)  
Systems Engineering View

???
# Things to note:
* The system of interest identification scopes the set of system elements, system element interconnections, and the environment that it operates in
* All _other systems_ that interact with the system of interest are included in the operational environment
* Some enabling systems may exist outside the environment of operation, for example, the compiler used at the developer site, open source developer

# Can you think of _other systems_ that introduce risk?
# Can you think of _enabling systems_ that introduce risk?

---

class: center, middle
# Security Engineering Perspective

---
# Security Engineering Perspective

## .red[Security]
Freedom from conditions that can cause _loss of assets_ with _unacceptable consequences_
--

## .red[Engineering challenge]
Engineer _protection capabilities_ for:
1. .red[assets] to which security applies and
1. .red[consequences] against which security is assessed

???

# Conditions
These can be adversity in the form of disruptions, hazards, and threats and are considered synonyms for “bad things that happen” that are of interest to systems security engineering

# Consequence
[ISO/IEC 15026-1]
Effect (change or non-change), usually associated with an event or condition or with the system and usually allowed, facilitated, caused, prevented, changed, or contributed to by the event, condition, or system.

---

# Security Engineering Perspective

## Goal: _have .red[protection capabilities] built-in..._
--

### .red[Active Protections]
* .red[Mechanisms] that exhibit security behavior with functional and performance properties to satisfy security requirements

--

### .red[Passive Protections]
* Provides the environment for the .red[execution] and .red[construction] of all mechanisms (general purpose and security)

???

# Active Protection:
These mechanisms explicitly satisfy security requirements that address the behavior, interaction and utilization of and among technology/machine, environment, human, and physical system elements.

# Passive Protections:
For example, developer training in secure coding provides for the construction of security mechanisms with a higher level of assurance. Similarly, a fully patched and hardened java runtime environment provides a protection capability to the hosted java applications. A visual studio complier with the appropriate compiler flags is also a passive protection.


---

# Protection Examples

## Active Protections

- Access control
- Single sign-on
- Identification
- Authentication
- Encryption at rest and in transit
- Configurations
- Backup
- Two-phase commit
- Filters/Wrappers
- Validators
- ...

---

# Protection Examples

## Passive Protections

- Architecture
- Design
- Coding guidelines
- Code review
- Developer and user training
- Verified and configured compilers
- Acquisition policies
- Red-teaming
- Project management
- Runtime environments
- ...

---

# Adequate Security

## A well-reasoned sum of both active and passive protections
--

### For all .red[system execution modes]
e.g., initialization, operation, maintenance, training, shutdown
--

### For all .red[system states]   
e.g., secure, nonsecure, normal, degraded, recovery
--

### For all .red[transitions]
Between system states and between system execution modes.

???

For Rugged Software, **gradation** is important and hence reflected in our definition of _adequate security_.

---
class: middle, center
# Security Engineering Framework

---
# Framework

### .red[Problem] Context
A sufficiently complete understanding of the problem
--

### .red[Solution] Context
Transforms the security requirements into design requirements for the system
--

### .red[Trustworthiness] Context
Evidence-based demonstration, through reasoning, that the system-of-interest is deemed trustworthy

???
The framework is independent of system type and engineering or acquisition process model and is not to be interpreted as a sequence of flows or process steps but rather as a set of interacting contexts, each with its own checks and balances

---
class: center, middle
![NIST SP 800-160 Public Draft 2](images/framework.png)  
???

???
Figure source: [NIST SP 800-160 Systems Security Engineering &mdash; Public Draft 2](http://csrc.nist.gov/publications/drafts/800-160/sp800_160_second-draft.pdf)

# Systems Security Engineering Framework
Establishing problem, solution, and trustworthiness contexts as key components of a systems security engineering framework ensures that the security of a system is based on achieving a sufficiently complete understanding of the problem as defined by a set of stakeholder security objectives, security concerns, protection needs, and security requirements. This understanding is essential in order to develop effective security solutions &mdash; that is, a system that is sufficiently trustworthy and adequately secure to protect stakeholder’s assets in terms of loss and the associated consequences.

# System security analyses

Employ concepts, principles, means, methods, processes, practices, tools, and techniques from the security perspective to provide relevant data and technical interpretations of issues from the security perspective

Support gradation:  
\* Differentiated to align with the scope and objectives of where they are applied within the systems security engineering framework

\* Performed with a level of fidelity, rigor, and formality to produce data with a level of confidence that matches the assurance required by the stakeholders and engineering team

---

# Problem Context (1/2)
## .red[Security objectives]
What it means to be _adequately_ secure for the assets and the consequences of asset loss against which security will be assessed
--

## .red[Measures of success]
Strength of protection and level of assurance in the engineered protection capability

???

# Security Objectives
This is where you start to think of your mission/business processes. What assets are important and the consequences of asset loss against which security will be assessed.

# Security Objectives and Measures of Success
The security objectives have associated measures of success. The two combine to drive the development of security requirements and the development of assurance claims

---
# Problem Context (2/2)

## .red[Life cycle security concepts]
Distinct contexts for interpretation of security and the associated processes, methods, and procedures

???
# Life cycle security concepts
- Concept
- Development
- Production
- Utilization
- Support
- Retirement

--

## .red[Security requirements]
Specifies the functional, assurance, and strength characteristics for a protection mechanism

???

# Example of Security Requirements:
- Access Control as a functional requirement  
- Secure coding standards as an assurance requirement  
- Rigor in enforcement and granularity of access control is a strength characteristic  
- Rigor in the coding standard and its security relevance is a strength characteristic  

---

# Solution Context

### .red[Define security aspects of the solution]:
- The security architecture views and viewpoints
- The security design
- Security performance verification measures

### .red[Realize security aspects of the solution]:
- Implementation of the system security design

### .red[Evidence for security aspects of the solution]:
- Analysis, demonstration, inspection, and test

---

# Trustworthiness Context

### .red[Developing and maintaining the assurance case]
- Assurance cases are developed for claims based on the security objectives and associated measures of success

### .red[Demonstrating that the assurance case is satisfied]
- An assurance case is a well- defined and structured set of arguments and a body of evidence showing that a system satisfies specific claims with respect to a given quality attribute

???
Assurance cases also provide reasoned, auditable artifacts that support the contention that a claim or set of claims is satisfied, including systematic argumentation and its underlying evidence and explicit assumptions that support the claims [ISO/IEC 15026-2]

---

class: center, middle
![NIST SP 800-160 Public Draft 2](images/framework-course-topics.png)  
???
Figure source: [NIST SP 800-160 Systems Security Engineering &mdash; Public Draft 2](http://csrc.nist.gov/publications/drafts/800-160/sp800_160_second-draft.pdf)

---

class:center, middle
# Next Up
Constructing Assurance Cases using Goal Structuring Notation

TODO: Create a [Lucidchart Account](https://www.lucidchart.com) using your `.edu` email

---

![preview](images/preview.svg)
???
Source: This example is based on the presentation of this paper given at ICSE conference: J. B. Goodenough, C. B. Weinstock and A. Z. Klein, "Eliminative induction: A basis for arguing system confidence," 2013 35th International Conference on Software Engineering (ICSE), San Francisco, CA, 2013, pp. 1161-1164.
---
class: center, middle
# Systems Engineering Lifecycle Processes

---

![lifecycle processes](images/systems-engineering-lifecycle-processes.png)
???
Figure source: [NIST SP 800-160 Systems Security Engineering](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-160.pdf)  
class: center, middle
# Assurance Case*
.footnote[
\* See notes for sources
]
???
This slide deck is based several sources as follows:

1. Goal Structuring Notation
2. [IEEE Standard— Adoption of ISO/IEC 15026-2:2011](https://www.iso.org/standard/52926.html)
Systems and Software Engineering— Systems and Software Assurance— Part 2: Assurance Case
3. Research papers on Eliminative Induction use in Assurance Cases
4. SEI publications on Assurance case use in Safety Cases

---
class: middle

## The first principle is that you must not fool yourself and you are the easiest person to fool... After you've not fooled yourself, it's easy not to fool other scientists.

.footnote[
Richard P. Feynman
]
.top-right[
![RF](http://www.hwscience.com/physics/apphysicsc/Feynman-2.gif)
]
---
class: middle

## .blue[Schneier's Law]  
## Any person can invent a security system so clever that he or she can’t imagine a way of breaking it.

.footnote[
Bruce Schneier
]
.top-right[
![Bruce](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Bruce_Schneier_at_CoPS2013-IMG_9174.jpg/220px-Bruce_Schneier_at_CoPS2013-IMG_9174.jpg)
]
---
class: middle

## False assurance is a danger that is avoidable by only trusting technology that is demonstrably trustworthy.

.footnote[
Roger Schell
]
.top-right[
![Roger](http://www.ieee-security.org/TC/SP2010/photos/.xvpics/0054_IMG-thumb.jpg)
]
---
background-image: url(http://wallpapercraze.com/images/wallpapers/uwp6%20%282%29-110045.jpeg)
???
Scenario: Our goal is to find a black cat in a dark room.
---
background-image: url(images/black.png)

???
We also not sure if there is a cat there to begin with!
## Source:   
The cat example is adapted from the example provided in System Assurance: Beyond Detecting Vulnerabilities (The MK/OMG Press) 1st Edition, by Nikolai Mansourov  and Djenana Campara https://amzn.com/0123814146
---
class:middle
# Task at hand
Find a **black cat** in a **dark room**  
--

Also, we are not sure that the cat is really there!

--

## .blue[
What are the Goals/Claims to be proven?
]

---
class:middle
# Possible claims

## .red[Claim 1:] The room has at least one black cat
--

## .red[Claim 2:] The room has no black cats

--
## .blue[
What is the basis for the belief in these claims?
]
---
class: middle
# .red[Claim 1]
The room has at least one black cat

---
class: middle
# Basis for the Belief

## .blue[Kitty-Kitty-Kitty] Search Process*
1. Search team puts a bowl of milk in the room and says _kitty-kitty-kitty_ three times
1. Four corners and center of room covered
1. Stop when a cat is discovered

.footnote[\* Patent Pending]

---
# Structured Argument
### .red[Claim]
.red[C1:] The room has at least one black cat
--

### .red[Sub-Claims]
.red[C1.1:] Kitty-kitty-kitty search process discovers cats in the room

--

### .red[Evidence]

.red[E1.1.1:] Pictures of cats found

---
class: middle
# .red[Claim 2]
The room has .red[no] black cats

--

### .red[Sub-Claims]
.red[C1.1:] Kitty-kitty-kitty search process discovers no cats

--
### .red[Evidence]

.red[E1.1.1:] Empty findings report


---
class: middle
# Is this argument enough?
Can you ever be 100% sure for a large and complex room?  


---
class: middle
# .red[Assurance]
Basis for the belief in a claim

--

## .green[Belief] increases when .red[doubts] are removed!   

--

A good argument eliminates identified doubts

---

class: middle
# [Eliminative Induction](https://www.google.com/search?q=define+eliminative+induction)
A series of doubts are introduced for some state of affairs,  
and then progressively eliminated by new evidence

---
# Eliminative Induction

## Step 1: Introducing doubts
Challenge the identified claims by introducing doubts
--

## Step 2: Eliminate doubts
For each doubt, identify sub-claims that eliminate the doubt
--

## Step 3: Repeat
Go to Step 1, repeat process for sub-claims
---
class: middle
# Step 1: Introducing doubts

.red[C1.1:] Kitty-kitty-kitty search process discovers no cats
--

* .red[R1.1.1] _Unless_ the cats were not hungry  
* .red[R1.1.2] _Unless_ milk is not put in enough places
* .red[R1.1.3] _Unless_ the people searching are not competent
* .red[R1.1.4] _Unless_ the baby panthers found are indeed cats

---
class: middle
# Step 2: Eliminate doubts

.red[R1.1.1] Unless the cats were not hungry   
* .green[C1.1.1] The room was locked for 5 days  

--

.red[R1.1.2] Unless milk is not put in enough places  
* .green[C1.1.2] The room is simultaneously searched in 10 equal non-overlapping squares  

---
class: middle
# Step 3: Repeat --> Step 1: Identify doubts

.green[C1.1.1] The room was locked for 5 days  
* .red[R1.1.1.1] Unless the room vents allow cats to go in and out  

--

.green[C1.1.2] The room is simultaneously searched in 10 equal non-overlapping squares  
* .red[R1.1.1.2] Unless the cats have an alternate food supply (mice in the room)

---
class: middle
# Step 2: Eliminate doubts

.red[R1.1.1.1] Unless the room vents allow cats to go in and out  
* .green[C1.1.1.1.1] All room vents have nets installed

--

.red[Unless] the cats have an alternate food supply (mice in the room)
* .green[C1.1.1.1.2] There are no mice in the room

---
class: middle
# Stopping condition?

## Evidence
When the argument is convincing enough to the reader, it should end in the presentation of .blue[_facts_] that support the .green[_claims_]

---
class: middle
# Evidence

.red[R1.1.1.1] Unless the room vents allow cats to go in and out  
* .green[C1.1.1.1.1] All room vents have nets installed
* .blue[E1.1.1.1.1 Vent inspection report]

.red[Unless] the cats have an alternate food supply (mice in the room)
* .green[C1.1.1.1.2] There are no mice in the room
* .blue[E1.1.1.1.2 Month old exterminator report for rodents]

---

class: middle
# Basis for the Belief

As more reasons for doubt are eliminated, assurance in the top-level claim increases  

If many doubts remain, assurance is diminished

--

A rigorous argumentation structure assists .red[*trust decisions*] for the presented claims
---

class: middle
# .red[Claim 3]
The room will have .red[no] black cats for the .red[next 12 months]

--

Does it make sense to justify this claim by a single search at a moment in time?

---
class: middle
# Risk: A future adverse event

We can introduce even more doubts!
* .red[R1.1.5] Unless the cats hibernate when search is conducted  
* .red[R1.1.6] Unless cat zapper vents are working intermittently
* .red[R1.1.7] Unless the vents are not being inspected periodically
* .red[R1.1.8] Unless the exterminator skips visits

--

To eliminate these doubts, .green[continuous] efforts are required.

---
# A very catty summary

## Equate Cats to .red[Weaknesses]

### Claim 1 (Point Solution)  
* Produces knowledge about what you found  

.top-right[
![catfunny](http://vignette2.wikia.nocookie.net/animal-jam-clans-1/images/6/6b/Funny-Cat-Meme-Work-16.jpg/revision/latest?cb=20160716231247)
]

--

### Claim 2 (Snapshot)  
* Produces knowledge about the whole system

.top-right[
![catfunny](http://i0.kym-cdn.com/entries/icons/original/000/002/232/bullet_cat.jpg)
]

--

### Claim 3 (Continuous Assurance)  
* Produces knowledge about minimizing  
a future undesirable event

.top-right[
![catfunny](http://i0.kym-cdn.com/photos/images/newsfeed/000/115/642/non-stop-nyan-cat.jpg?1303327212)
]

---
class: center, middle
# Developing Assurance Cases

---
# Assurance Case Logical Structure
![structure](images/structure.png)
.footnote[
[Arguing Security - Creating Security Assurance Cases](https://www.us-cert.gov/bsi/articles/knowledge/assurance-cases/evidence-assurance-laying-foundation-credible-security-case)
]

---
# Assurance Case Contents

## A Top-level Claim
The claim is regarding .red[a critical property] of a system or product
## Argumentation
Arguing through .red[multiple levels of subordinate claims] connects the top-level claim to the evidence and assumptions
## Evidence and Assumptions
.red[Explicit information] that underlies the argumentation
---

class: middle
# Convince a bystander

### _While an assurance case is useful for decision-making by knowledgeable stakeholders (e.g., developers and service providers), often the primary motivation for an assurance case is to support crucial decisions by stakeholders without this background, such as those involved in certification, regulation, acquisition, or audit of the system._

.footnote[
[ISO/IEC 15026-2:2011](http://www.iso.org/iso/catalogue_detail.htm?csnumber=52926)
]
---

# [ISO/IEC 15026-2:2011](http://www.iso.org/iso/catalogue_detail.htm?csnumber=52926)
![iso](images/iso-standard.png)

---
# Claims
### Claims concern critical properties

--

### A claim is always worded as a predicate
- i.e. it can only be true or false

--

### Claim should avoid just details about the supporting method/techniques
- .red[Bad claim:] The system uses AES encryption
- Uninteresting

--

### The claim should be a reasonable goal
- .green[Good claim:] “The system is acceptably secure against communication lines related threats”

---
# Claims

## Claim properties are risk-related
- High confidence is needed in their realization

--

## Good Claim Checklist
- .blue[An entity]
- .orange[A critical property of the entity]
- .green[A value for the property and related uncertainty]

--

## Example
- .blue[The system] .green[is acceptably] .orange[secure]
- .blue[The system] .green[has no] .orange[unacceptable consequences to assets from security threats]

---
class: middle
# [Grammatical Guidance](http://www.sei.cmu.edu/dependability/tools/assurancecase/)

## .blue[&lt;NOUN-PHRASE&gt;]
- .blue[Noun-Phrase] identifies the subject (“entity”) of the claim

## .orange[&lt;VERB-PHRASE&gt;]  
- .orange[Verb-Phrase] defines a predicate using the critical property of the subject along with its expected value and related uncertainty

---
class: middle
# [Grammatical Guidance](http://www.sei.cmu.edu/dependability/tools/assurancecase/)

## Bad Examples
- Just describes an entity: ~~.red[XSS results for Canvas]~~
- Describes an action on entity: ~~.red[Perform XSS on Canvas]~~
- A question: ~~.red[How many XSS weaknesses does Canvas have?]~~
- Fact, no argument needed: .red[~~Canvas uses AES encryption~~]

---
class: middle
# .red[Actual] bad examples

## .red[C5: Security Professionals test code for XSS vulnerabilities]

--

## .red[C18: The System uses a Static Analysis tool]
.footnote[
See notes (hit `p`) for class exercise
]
???
# Class exercise:
# Work with your team to rephrase these appropriately.
When you are done enter your answers in this [Google Doc](https://docs.google.com/a/unomaha.edu/document/d/11Xr8GHBHfWJGLotiLoe-us1EZ4Qjn2msjfxHAKjs64Q/edit?usp=sharing)

---

class: middle
# Good Examples

## .blue[Canvas] .green[has no] .orange[exploitable XSS weaknesses]

--

## .green[All] .blue[Canvas XSS weaknesses] .green[have been sufficiently] .orange[mitigated]

--

## .blue[Canvas] .orange[attack surface] .green[is minimized]

---
class: middle
# Scenario

## OPPD NE has received intelligence.
- Rouge nation states are targeting their software supply chains.
- There is a credible threat. Software bought by OPPD for business functions is being targeted for sabotage with malicious code.

--

## Top Level Claim
- .blue[OPPD NE supply chain processes] .green[minimize ] .orange[the possibility of sabotage by malicious code in software applications]

---
class: middle
# Claim Visual Notation
## Based on Goal Structuring Notation (GSN)

![claim](images/claim.svg)

---
class: middle
# Elaborating the Claim

## .green[Additional information] that is excluded from the claim or evidence
- Context (understanding)
- Justification (rationale)
- Assumptions (validity)

---
class: middle
# Context

## Information necessary for a claim to be understood or amplified
- Includes a statement that defines the .red[scope] of the claim
- Provides means to check .red[satisfaction] of the claim

## Examples
- External references, Definitions, Clarification of myths
- Security considerations for supply chain processes per NIST SP 800-160

---
class: middle
# Assumption

## A statement whose validity has to be relied upon in order to make an argument
- .red[Restricted context]
- .red[Exceptions] or situations the claim does not cover

## Example
- Nuclear energy safety mechanisms do not include software

---
class: middle
# Justification

## Provides .red[rationale] for the use/selection of a claim or strategy

## Example
- Intelligence reports of malicious code in nuclear energy software

---
class: middle
# Context Visual Notation

![context](images/context.svg)

---
class: middle
# Justification Visual Notation

![justification](images/justification.svg)

---
class: middle
# Strategy

## Provides direction for an argument

## Phrased with respect to the argument
- .green[Argument by appeal to] software acquisition practices

## A strategy is elaborated by providing a series of sub-claims
---
class: middle
# Strategy Visual Notation

![strategy](images/strategy.svg)

---
class: middle
# Argument

- Conveys why we believe a claim has been met
- Refine claims into sub claims, until the sub-claim can be directly supported by the actual evidence
- Bridges the gap between claims and evidence

--

## Stopping condition?
- The rigor is acceptable
- Resources are unavailable
- Further expenditure is not justified

---

## Sub-claim

Develop a sub-claim
![argument](images/strategy.svg)

---
## Sub-claim
![sub-claim](images/sub-claim.svg)

---
class: middle
# Evidence

- Every branch must be terminated in evidence
- Something tangible and measureable

## Grammatical Guidance
- Must be a .blue[noun phrase] only (NO verb phrase)
- Should .red[not] be stated as a claim

---
class: middle
# Evidence

## Examples
- .red[E1:] Test results from penetration tools
- .red[E2:] Warnings from static analysis tool
- .red[E3:] Hardware design review results
- .red[E4:] Parameter validation assurance case
- .red[E5:] Reports for assessing compiler settings with security implications

---
class: middle
![Evidence](images/evidence.svg)

---
![arrow](images/arrows.svg)
.topnote[
What do the arrows mean?
]

---
class: center, middle
# Coming up with a good Argument is .large[Hard!]

---

# Eliminative Induction
## Support/assurance increases as reasons for doubt are eliminated

--

## Claim: .blue[The bulb] .green[will] .orange[glow when switched on]
- .red[Unless] switch not connected to light
- .red[Unless] no power
- .red[Unless] dead light bulb  
![light](images/lightexample.png)

???
Image and example provided in slides by John B. Goodenough

---
# Introducing Doubts*

## Making doubts explicit
### Attack claim (rebutting defeater) — why claim could be false
--

### Attack evidence (undermining defeater) — why evidence could be irrelevant
--

### .green[Attack inference] (undercutting defeater) — premise good; conclusion uncertain

.footnote[
\*See notes for sources [hit: `p`]
]

???
The content in next few slides is based on:
1. SEI Report: Toward a Theory of Assurance Case Confidence http://www.sei.cmu.edu/reports/12tr002.pdf
2. Charles B. Weinstock, John B. Goodenough, and Ari Z. Klein. 2013. Measuring assurance case confidence using Baconian probabilities. In Proceedings of the 1st International Workshop on Assurance Cases for Software-Intensive Systems (ASSURE '13). IEEE Press, Piscataway, NJ, USA, 7-11.
3. Explicit permission to use slides provided by John B. Goodenough

---
# Assurance Case Logical Structure
## Notice .green[inference rules]?
![structure](images/structure.png)
.footnote[
[Arguing Security - Creating Security Assurance Cases](https://buildsecurityin.us-cert.gov/daisy/bsi/articles/knowledge/assurance/643-BSI.html)
]

---
class: middle
# Inference Rule

## A generalization that in most circumstances is considered to be true

## Example
- (premise) If X is a bird then (conclusion) X can fly

--
- (Generalization) All birds can fly

--

.red[An argument is an instantiation of one or more inference rules with a specific premises and conclusions]

---

# Example Claim
![claim](images/tweetyclaim.svg)

---
# Inference Rule
![inference](images/inference.svg)

---

# Undercutting defeater
## Premise good; conclusion uncertain
![claim](images/inference.svg)
---

![claim](images/undercut.svg)

---

# Rebutting defeater
## Why claim could be false
![claim](images/inference.svg)
---

# Rebutting defeater
## Why claim could be false
![claim](images/rebutting.svg)

---
# Address Rebutting defeater
![claim](images/rebuttclaim.svg)

---
# Undermining defeater
## Why evidence could be irrelevant
![claim](images/undermine.svg)

---
# Undermining defeater
![claim](images/undermine-done.svg)

---
class: middle
# Measuring Confidence

## Baconinan Probability
- 0|n (no confidence) — no doubts eliminated
- 2|3 (partial confidence) — residual doubt
- n|n (complete confidence) — no doubts remain

--

## Use for relative improvements, not comparison

???
Source: Slides by John B. Goodenough
Source: Charles B. Weinstock, John B. Goodenough, and Ari Z. Klein. 2013. Measuring assurance case confidence using Baconian probabilities. In Proceedings of the 1st International Workshop on Assurance Cases for Software-Intensive Systems (ASSURE '13). IEEE Press, Piscataway, NJ, USA, 7-11.

---
# Few more notations
## Claim to be further developed
![developclaim](images/developclaim.svg)

---
# Few more notations
## No further argumentation
![stop](images/stopargument-1.svg)
![stop](images/stopargument-2.svg)

---
![preview](images/preview.svg)

???
Source: This example is partially based on the presentation of this paper given at ICSE conference: J. B. Goodenough, C. B. Weinstock and A. Z. Klein, "Eliminative induction: A basis for arguing system confidence," 2013 35th International Conference on Software Engineering (ICSE), San Francisco, CA, 2013, pp. 1161-1164.
---

class: middle
# Assurance Cases in Practice

## CC Evaluations and Software Assurance
- Argue how protection profile needs are satisfied by a Security Target
- Assurance cases are recommended for the highest levels of Evaluation Assurance Levels (EAL)

---

class: middle
_In pursuit of Trusted Computer System Evaluation Criteria (TCSEC) or CC evaluations or Federal Information Processing Standard (FIPS) 140-1 or 140-2 certifications for their security-enforcing IT products, vendors are required not only to submit assurance claims for those products to the independent evaluation or certification facility but to .red[provide complete assurance cases] that provide a sufficient basis for the facility to verify those assurance claims.*_

.footnote[
\* [Software Security Assurance State-of-the-Art Report (SOAR)](https://cwe.mitre.org/documents/iatac_swa_soar.pdf), 2007, DoD Information Assurance Technology Analysis Center (IATAC) Data and Analysis Center for Software (DACS)
]
---
class: middle
# Security Controls
[NIST SP 800-53 Rev. 5](https://csrc.nist.gov/csrc/media/publications/sp/800-53/rev-5/draft/documents/sp800-53r5-draft.pdf)

### Makes the security and privacy controls outcome-based
- Focuses on the security and privacy capabilities
- Controls are now .orange[critical properties] of interest.

???
(i.e., what needs to be done to protect the system or information and not which entity carries out the action or where it is carried out);

---
class: middle
# Security Controls
[NIST SP 800-53 Rev. 5](https://csrc.nist.gov/csrc/media/publications/sp/800-53/rev-5/draft/documents/sp800-53r5-draft.pdf)

IA-2 IDENTIFICATION AND AUTHENTICATION
### Current (Rev 4):
- Control: The information system uniquely identifies and authenticates organizational users.

### Proposed (Rev 5):
- Control: Uniquely identify and authenticate organizational users.

---
class: middle
# Software Security Controls
First to develop and apply assurance case based method for control refinement
- Software related controls derived from the NIST SP 800-53 control catalog
- These software assurance controls are enumerated in [NIST SP 800-160 Appendix-J](https://csrc.nist.gov/csrc/media/publications/sp/800-160/archive/2016-05-04/documents/sp800_160_second-draft.pdf)

#### Gandhi, R., Siy, H., Crosby, K., Mandal, S. (Graduate), (2014). Gauging the Impact of FISMA on Software Security, IEEE Computer, vol. 47 (9)
#### Gandhi, R. A., Crosby, K., Siy, H., Mandal, S. (2016) Driving Secure Software Initiatives Using FISMA: Issues and Opportunities. CrossTalk, Journal of Defense Software Engineering, Jan/Feb 2016 Issue.

---
class: middle
# Other Applications

### Forensics
- Jones, C. (2014). __Evaluating the use of assurance cases for digital forensics.__ Dissertations & Theses @ University of Nebraska - Omaha; ProQuest https://search.proquest.com/docview/1528534691?accountid=14692

---
class: middle
# Other Applications

### Research Study Design
- Gandhi R.A. and Lee, S.W., “Assurance Case driven Case Study Design in Requirements Engineering Research,” In: 15th International Working Conference on Requirements Engineering: Foundations for Software Quality, REFSQ 2009.

### Interview Protocol Design
- Gandhi R.A., Germonprez M., Link G., "Open Data Standards for Open Source Software Risk Management Routine: An Examination of SPDX", ACM GROUP 2018 https://github.com/SPDX-CaseStudy/files/blob/master/AssuranceCase.png

---
class: center, middle
# .large[Got Assurance?]
.bottom-left[
![meme](http://s2.quickmeme.com/img/31/315640bead03adc498079b11707081fbfcfc0d4d97b1e1d69ba1d930dfa286d6.jpg)
]
class: center, middle
# Assurance Case Exercise

---
class: middle
# Step 1
## Create an account on [Lucidchart](https://www.lucidchart.com/) using your `.edu` email
- OR Request an upgrade here: https://www.lucidchart.com/pages/usecase/education-request

---
class: middle
# Step 2
## Click on this [template](https://www.lucidchart.com/invitations/accept/e8d3aac4-e62b-4fa0-9fd1-c2cf6a6d318d) to start a new assurance case

---

class: middle
# Step 3
## Build Assurance Cases for your class project

- 5 assurance claims for your OSS project
- Elaborate on each claim with an assurance case

---
# Grading criteria

## Use of proper notations
- Goal Structuring Notation, Eliminative Induction

## Proper wording of assurance case elements
- As prescribed in slides; no typos and grammatical errors

## Argument Quality
- Claims focus on system properties of interest
- Reasonable depth and breadth:     
a) Convince a technical expert  
b) Coherent theme of the argument

---

class: middle
# Step 4
## Submit links to your assurance cases developed in Lucidchart
- Submission of the links on Canvas
- One submission per team
- Due Date: September 27, 2017 11:59 P.M.

---
# Generating shareable links on Lucidchart

![sharing](images/sharing.png)
# Design	Patterns	for	

# Software	Security	Engineering

## Robin	Gandhi



# Architecture

- In	construction,	architecture	often	codifies	the	

## appearance and	 character of	a	structure

- e.g.		Art	Deco,	Victorian,	Industrial,	Contemporary


# Software	Architecture

- Architecture	is	the	 **art of	planning	** the	

## structure and	 functions of	an	artifact

- Software	architecture	takes	the	products	of	the	
    requirements	activity	and	decomposes	the	system	
    at	multiple	levels	of	abstraction into	structured	
    components and	their	interactions
- Decomposition	based	on	 **_patterns_**
- Structures	and	functions	related	to	security	

## can	be	codified	as	patterns


# Design	Patterns

- “Each	pattern	describes	a	problem	which	

## occurs	over	and	over	again	in	our	

## environment,	and	 describes	the	core	of	the	

## solution	to	that	problem ,	in	such	a	way	that	

## you	can	use	this	solution	a	million	times	over,	

## without	ever	doing	it	the	same	way	twice”

- _Chris	Alexander,	1977,	talking	about	patterns	in	_
    _buildings	and	towns_ https://en.wikipedia.org/wiki/Christopher_Alexander


# Design	Patterns	in	

# Software	Engineering

- See	Book	

## (Design	Patterns...Gang	of	Four)

- Few	security	relevant	patterns	follow...


# Recurring	Problem

```
Client Classes
```
**Subsystem Classes**


# Recurring	Solution

```
Client Classes
```
**Subsystem Classes**


# Façade	Pattern

- Intent/Solution:
    - Provide	a	unified	interface	to	a	set	of	interfaces	in	
       a	subsystem
- Applicability
    - Many	dependencies	between	clients	and	
       implementation	classes	of	an	abstraction
    - You	want	to	layer	your	subsystems


# Façade	Pattern

- Structure:


# Façade	Pattern

- Consequences:
    - Promotes	weak	coupling,	reduces	compile	time	
       dependencies
    - Does	not	prevent	clients	from	using	subsystem	
       objects	directly
    - Façade	has	to	perform	the	translation	and	
       redirection	of	client	request	to	appropriate	
       subsystem	object	
- Also	Known	as:
    - Wrappers,	http://microservices.io/patterns/apigateway.htmlAPI	Gateway 11


# Proxy	(Surrogate)	Pattern

- Intent/Solution:
    - Provide	a	surrogate	or	placeholder	for	another	object	
       to	 _control	access	_ to	it
- Applicability
    - A	remote	proxy	provides	a	local	representative	for	a	
       object	in	a	different	address	space
    - Virtual	proxy	creates	expensive	objects	on	demand
    - Protection	proxy	controls	access
    - A	smart	reference	proxy	provides	pointer	
       dereferencing	capabilities


# Proxy	(Surrogate)	Pattern

- Structure:


# Proxy	(Surrogate)	Pattern

- Consequences:
    - Proxymalfunction	cuts	off	attacker	access
    - Smart	proxiescan	act	as	intelligent	wrappers	and	filter	
       requests
    - Remote	proxies	act	as	stubs	in	client	realm	for	critical	
       objects	stored	on	the	server
    - Proxy	enables	inspection	of	encrypted	payload	between	
       the	communication	partners
    - Expose	legacy	applications	using	safer	functions
- Also	Known	as:
    - Interposition 14


# Singleton	Pattern

- Intent/Solution:
    - Ensure	a	class	has	only	one	instance,	and	provide	
       a	global	point	of	access	to	it
- Applicability
    - There	must	be	exactly	one	instance	of	a	class,	and	
       it	must	be	accessible	to	all	clients	from	a	well	
       known	access	point


# Singleton	Pattern

- Structure:


# Singleton	Pattern

- Consequences:
    - _Controlled	access	to	sole	instance.	_ Strict	control	
       over	how	and	when	clients	can	access	the	
       instance
    - _Permits	refinement	of	operations	and	_
       _representation._ The	singleton	class	can	be	sub	
       classed	and	extended	for	use	in	different	
       applications


# Secure	Design	Principles	

# as	Patterns	


# Design	Guidelines	for	Security	(1)

- The	Protection	of	Information	in	Computer	

### Systems	- Saltzer and	Schroeder	[ 1973 ]

```
http://web.mit.edu/Saltzer/www/publications/protection/Basic.html
```
- Security	in	Computing,	Pfleeger and	Pfleeger
- Building	Secure	Software,	Viega and	McGraw
- Secure	Coding,	Graff	and	van	Wyk (Ch 2.)
- Secrets	and	Lies,	Bruce	Schneier
- Build	Security	In	DHS
    https://www.us-cert.gov/bsi/articles/knowledge/principles/design-principles
- ...


# Design	Guidelines	for	Security	(2)

- OWASP	Principles	
    https://www.owasp.org/index.php/Secure_Coding_Principles
- 6	dumbest	ideas	in	CS	
    [http://www.ranum.com/security/computer_security/editorials/dumb/index.html](http://www.ranum.com/security/computer_security/editorials/dumb/index.html)
- McGraw	 10	 steps [http://cybersecurity.ieee.org/center-for-secure-](http://cybersecurity.ieee.org/center-for-secure-)
    design/avoiding-the-top- 10 - security-flaws.html


# Patterns	for	Design	Principles

- Pattern	Name:	
    - How	to	refer	to	it?
- Intent/Solution:	
    - What	is	the	core	of	the	solution	to	the	problem?
- Applicability:	
    - When	to	apply	the	pattern?
- Consequences:	
    - What	are	the	results	/tradeoff	when	applying	the	pattern?
- Connotations:
    - Is	it	referred	to	by	another	name	elsewhere?


# KISS

- Name:	
    - KISS	(Keep	it	Simple,	Stupid!)
- Intent/Solution:
    - _Security-relevant	components	_ should	be	as	small	
       and	simple	as	possible
          - Stingy	with	“features”	and	“transparent”
          - Simple	as	possible,	but	no	simpler
          - Localized
          - Should	minimize	external	dependencies


# KISS

- **Applicability**
    - Designing	trusted	components,	i.e.	those	
       responsible	for	policy	enforcement
    - Designing	components	whose	
       trustworthiness	needs	to	be	verified
    - Heavily	shared	mechanisms
    - Outward	facing	components	
       - Reduce	the	attack	surface


# KISS

- **Consequences**
    - Improves	ability	to	review	and	reason
    - May	increase	the	tendency	to	add	more
       - Success	at	developing	simpler	systems	leads	to	
          aspirations	for	greater	complexity
    - May	require	more	iterations	of	design
       - May	increase	designer	or	user	frustration
    - Succinct	does	not	always	equate	to	simple
       - **int opening_time = (day == WEEKEND)? 9 : 12;**


# KISS

- **Other	connotations	and	extensions**
    - Economy	of	Design
    - Stay	on	the	simple	side
    - Embrace	Simplicity
    - Analyzability
    - Modularize	thoroughly
       - Compartmentalize	
    - Explicit	assumptions


# Secure	Defaults

- **Name:**
    - Secure	Defaults
- **Intent/Solution:	**
    1. Default	state	preserves	security	policies	
       during	initialization,	operation	or	failure
    2. Default	deny	with	whitelist	rules	for	filtering
       - A	second	stage	filtering	can	include	blacklisted	special	
          characters	
    3. Failure	modes	identified	with	error	codes	and	
       actions	to	handle	them	(exception	handling)


# Secure	Defaults

- **Applicability**
    - Transition	of	a	trust	boundary
    - Dependency	on	environment
       - Possibility	of	malformed	input
       - Possibility	of	overload
    - Bootstrapping,	failure/exception	handling	or	
       fresh	installation,	abrupt	failure/shutdown
    - Administrative	or	user	security	settings	dialogs
    - Preserve	privacy	of	user	data	during	operation	and	
       upon	malfunction


# Secure	Defaults

- **Consequences**
    - Trade-offs	for	Availability	vs.	other	security	properties
       - May	cause	denial	of	service
    - Inconvenience	of	defaults	may	motivate	
       unsafe	choices	to	be	made
    - Legacy	systems	might	not	co-operate	
       with	secure	defaults
          - E.g.	Older	wireless	devices	may	not	work	with	WPA2
    - Context	determines	appropriate	
       (e.g.	safe	vssecure)	defaults
          - Water	supply	to	a	nuclear	plant


# Secure	Defaults

- **Other	connotations	and	extensions**
    - Fail-safe	defaults
    - Fail	securely
    - Promote	privacy	(do	not	give	out	more	information	
       than	necessary	upon	exceptions	or	otherwise)
    - Privacy	vs.	usability
    - Degrade	gracefully	(upon	resource	exhaustion)
    - Proper	handling	of	unexpected	errors
       - Design	and	coding	practices
    - Build	in	appropriate	levels	of	fault	tolerance
       - Resistance,	Recognition,	Recovery


# Reference	Check

- **Name:	**
    - Reference	Check
- **Intent/Solution:**
    1. Authenticate	the	source	of	every	request	(at	
       least	for	every	critical	state	change)
    2. Check	authorization	for	every	access	to	a	
       protected	object	
    3. Implement	choke	points	and	limit	their	numbers
    4. Validate	all	inputs	used	to	interact	with	
       protected	objects


# Reference	Check

- **Applicability**
    - Dereference	a	pointer	to	an	
       internal/protected	object
    - Non-atomic	transactions	and	
       TOCTOU	conditions	exist
    - Session	management	in	a	stateless	environment
       e.g.	cookies	and	session	identifiers,	CSRF	attacks


# Reference	Check

- **Consequences**
    - Performance	bottleneck
    - Inconvenience	due	to	frequent	authentication	
       requests	(e.g.	Vista	UAC)
- **Other	connotations	and	extensions**
    - Complete	Mediation
    - Choke	points
    - Be	reluctant	to	trust
    - Test	every	action	against	the	policy


# Reference	Check

- **Other	connotations	and	extensions**
    - Make	sure	some	individual	is	accountable
    - Understand	and	respect	the	chain	of	trust
       - Do	not	invoke	un-trusted	programs	from	within	trusted	ones
          - Escalation	of	privileges
    - Make	sure	it	is	possible	to	reconstruct	events
    - Validate	all	inputs
    - Do	not	trust	input	from	any	un-trusted	source
       - User
       - Config/property/resource	files
       - other	executables 33


# Vetted	Design

- **Name:	**
    - Vetted	design
- **Intent/Solution:**
    - Re-use	known	good	(mature)	designs	and	
       implementations	
          - Do	not	reinvent	the	wheel
    - Security	should	not	depend	on	the
       ignorance	and	obscurity	of	the	
       design/implementation
          - Reverse	engineering	should	be	assumed


# Vetted	Design

- **Applicability**
    - Security	critical	operation
       - Input	validation	
       - Data	and	control	plane	transition
       - Authentication	mechanisms
    - Software	that	will	be	widely	distributed	
       and	available
    - Customers	demand	a	white-box	acquisition	review	
       before	product	acceptance
    - Cryptographic	algorithm	implementations
    - Third	party	developed	software	products 35


# Vetted	Design

- **Consequences**
    - The	user	community	as	well	as	attackers	may	have	
       opportunity	to	closely	examine	the	design
    - Weak	security	will	be	quickly	penalized
       - Vulnerability	reporting	and	handling	
    - Trust	develops	with	time	and	extensive	use
    - Unintended	consequences	of	reuse	(no	diversity)


# Vetted	Design

- **Other	connotations	and	extensions**
    - Vetted	Design	does	not	entail	providing	more	
       information	than	is	necessary
          - Does	not	mean	open	source,	But	assured	mechanisms	
             and	algorithms
          - It	is	OK	to	use	deception,	but	not	extensively
             - The	attacker	does	not	KNOW!
             - Warning	labels,	False	system	information
    - It	is	hard	to	keep	secrets,	especially	in	software
       - Do	not	rely	on	obfuscation,	be	reluctant	to	trust	clients
    - Consult	community	resources


# Divide	and	Conquer

- **Name:**
    - Divide	and	Conquer
- **Intent/Solution** :
    - Split	responsibility	for	a	high	consequence	action
       - Avoid	conflict	of	interest	by	assigning	conflicting	
          responsibilities	to	different	modules	or	roles


# Divide	and	Conquer

- **Applicability**
    - Initiate	actions	with	significant	consequences
    - Components	that	require	higher	privilege	than	other	
       code	segments
    - Enforce	business	process	integrity
    - When	no	single	breach	of	trust	should	cause	violation	
       of	security	policy
          - Limit	the	opportunity	to	misuse	a	
             critical	combination	of	privileges
    - Permit	safe	delegation


# Divide	and	Conquer

- **Consequences:**
    - Implementation	and	management	is	difficult
       - Splitting	introduces	synchronization	overhead
       - Many	roles	are	required
       - May	require	tracking	the	history	of	actions
    - High	granularity	in	privileges	may	cause	
       programmers	avoid	using	it
          - Should	be	used	in	moderation


# Divide	and	Conquer

## • Other	connotations	and	extensions

- Two-man	control
- Predicate	Permission
- Separation	of	duty
- Separation	of	privilege
- Compartmentalize
- Be	reluctant	to	trust!


# Be	Stingy	with	Privileges

- **Name:**
    - Be	Stingy	with	Privileges
- **Intent/Solution:**
    - The	job	function	should	be	carried	out	with	the	
       most	 **restrictive** set	of	 **privileges** necessary,	
       **only	for	time	** necessary	to	do	the	job


# Be	Stingy	with	Privileges

- **Applicability**
    - When	there	are	varying	and	overlapping
       levels	of	authority
          - E.g.	Bank	Manager	and	Teller,	Administrator	and	User
    - Enforce	“Need-to-Know”
    - Installation	vs.	routine	operation
    - Accountability	and	non-repudiation	
       of	an	action	is	important
    - Limit	accidental	misuse
    - Log	management
       - Append	only	log-writer


# Be	Stingy	with	Privileges

- **Consequences**
    - Minimize	damage	from	a	breach	of	trust
    - May	introduce	configuration	burden
       - Installation	is	much	easier	being	root
    - High	granularity	in	privileges	may	cause	
       programmers	to	take	the	all	or	nothing	approach
          - [http://msdn.microsoft.com/en-](http://msdn.microsoft.com/en-)
             us/library/windows/desktop/aa374902(v=vs.85).aspx
          - [http://msdn.microsoft.com/en-](http://msdn.microsoft.com/en-)
             us/library/windows/desktop/aa363858(v=vs.85).aspx


# Be	Stingy	with	Privileges

- **Other	Connotations**
    - Least	Privilege
    - Higher	privileges	should	only	be	
       permitted	for	a	limited	time
    - Assure	that	some	user	is	accountable
    - Prevention	of	privilege	abuse
    - Avoid	the	opportunity	for	privilege	escalation


# Minimal	Touchpoints

- **Name**
    - Minimal	Touchpoints
- **Intent/Solution:**
    - Minimize	the	amount	of	global	state	maintained	and	
       mechanisms	shared	across	different	processes
    - Allocate	and	enforce	limits	on	resource	use	in	a	
       shared/commons	environment
    - Make	resource	usage	opaque	to	other	processes


# Minimal	Touchpoints

- **Applicability**
    - High	risk	of	covert	channels
    - A	shared	service	for	multiple	users	
    - Access	and	resource	control	for
       different	levels	of	data	sensitivity
    - Where	malice	of	one	user	may	affect	many	users


# Minimal	Touchpoints

- **Consequences**
    - Sharing	maybe	difficult
    - May	require	virtualization/duplication	of	
       resources	
    - Need	to	manage	multiple	installations
- **Other	connotations**
    - Least	Common	Mechanism
    - Self-limit	program	consumption	of	resources


# Usable	Security

## • Name:

- Usable	Security

## • Solution:

- Provide	user	interfaces	that	allow	users	to	

### correctly,	routinely	and	automatically	use	

### security	features

- System	policy	enforcements	should	match	

### user	expectations


# Usable	Security

## • Applicability:

- Interactive	and	configurable	systems
- Offload	user	responsibility,	lazy	users
    - Auto-lock	set	to	secure	default	values
- Systems	used	active	environments	(e.g.	

## battlefield,	factory	floor)

- Usable	in	stressful	situations	yet	resist	tampering
- System	security	configuration
- Simple	and	unambiguous


# Usable	Security

- **Consequences**
    - Accessibility	features	may	interfere	with	
       security	requirements
    - Default	settings	may	require	tweaking/learning	for	
       different	environments	and	user	preferences
          - E.g.	Screensaver	lock,	banners
          - Simplicity	can	be	annoying	and	too	restrictive	for	expert	
             customers


# Usable	Security

- **Other	connotations**
    - Psychological	acceptability
    - Security	should	not	get	in	the	
       way	of	the	users	tasks
    - Users	should	fully	understand	the
       consequences	of	an	action
    - Adopt	practical	measures	the	
       users	can	live	with


# Avoid	Spillage

- **Name:**
    - Avoid	Spillage
- **Intent/Solution**
    1. Prevent	spillage	from	the	user-controlled	data	plane	
       over	to	the	control	plane	and	vice	versa.
    2. Set	limits	on	user-provided	data	structures	and	
       provide	throttling	controls	(interaction	rate)
    3. Neutralize	(filter/escape,	en/decode,	
       canonicalize/resolve,	resource	limit)	user-controlled	
       data	before	input	validation	and	output	generation
    4. Limit	information	in	error	notification 53


# Avoid	Spillage

- **Applicability:**
    - When	external	data	is	used	for	the	formation	of	
       parameterized	commands
    - Upon	error	notification	during	operation
    - When	unlimited,	encoded	or	internationalized	
       input	can	be	provided	by	the	user
    - Unpredictable	demand	for	a	limited	resource
    - Output	is	passed	to	another	component


# Avoid	Spillage

- **Consequences:**
    - Additional	processing	for	each	user	request
    - Limitations	on	the	user	input	space	(special	
       characters,	keywords,	length,	etc.)
    - Promotes	maturation	and	re-use	of	input	
       validation	routines
    - General	error	notifications	may	increase	user	
       frustration	and	delay	resolution	of	issues	by	
       technical	support	staff


# Avoid	Spillage

- **Connotations:**
    - Validate	all	input
    - Information	exposure	through	error	message
    - Buffer	Overflow
    - Injection
    - Path	Traversal


# ASK	R	V	DUMB?

- **A** void	Spillage
- **S** ecure	Defaults
- **K** ISS
- **R** eference	Check
- **V** etted	Design
- **D** ivide	and	Conquer
- **U** sable	Security
- **M** inimal	Touchpoints
- **B** e	Stingy	with	Privileges

```
Then remember to ask,
What did I forget?
```

# Example	Scenarios

- The	database	connection	driver	for	the	

## webserver	was	having	trouble	starting	on	port	

## 80	 with	a	limited	user	account,	so	to	make	it	

## work,	gave	it	root	privileges.

- Listing	too	many	options,	options	using	cryptic	

## language,	or	confusing/conflicting	options	to	

## configure	system	security	settings.


# Example	Scenarios

- We	can	base-64	encode	the	user	password	

## and	transmit	it	as	part	of	the	browser	cookie.	

## No	one	will	ever	find	out	what	those	random	

## characters	are.

- The	security	kernel	will	also	include	drivers	for	

## the	biometrics	module.


# Example	Scenarios

- The	flash	installation	requires	
    access	to	video	drivers,	so	we	
    will	perform	the	installation	
    using	administrative	privileges.	
    To	avoid	run-time	issues	it	is	
    better	we	also	continue	to	
    maintain	those	privileges	during	
    normal	operation.	That	will	
    reduce	our	programming	
    burden	and	speed	up	the	
    application	too.	 60
       - **A** void	Spillage
       - **S** ecure	Defaults
       - **K** ISS
       - **R** eference	Check
       - **V** etted	Design
       - **D** ivide	and	Conquer
       - **U** sable	Security
       - **M** inimal	Touchpoints
       - **B** e	Stingy	with	Privileges


# UML	diagram	recap

- **Use	Cases:	** abstract	view	of	functionality
- **Class	diagrams:	** The	static	class	structure	of	a	

### system.	It	includes:	attributes,	operations	of	a	

### class	and	relationships	among	classes.

- At	the	instance	level,	they	are	called	object	diagrams

```
variableNameClassName: type
+ methodName(parm1:type): returnTypevariableName: type Specify State
BehaviorSpecify
+ public# protected
```
- private Parameter syntax roughly follows attribute syntax

Underlined variables
have Class scope. e.g.

```
variablesStatic
comments
```
```
Bob:ClassNamecounter = 1
state
```
```
Object
Syntax
InterfaceName<<interface>>
Constants
Method signatures
```

# Reading	UML	Relationships

**Association** : We start with one endpoint and _always_ start
with a _single instance_ of it.
Read as:
An instance of C opens one or more instances of D
An instance of D is opened by 2 to 4 instances of C
Instances of C are aware of instances of D
However instances of D are unaware of
instances of C that interact with it 62

```
C 2..4 1..* D
```
```
opens
```

# Reading	UML	Relationships

C is the whole and D is the part with a composition association

```
if C is destroyed then typically D is destroyed as well
D is part for a single C only so no multiplicity necessary
```
```
C 1..* D
```
```
uses
```

# Reading	UML	Relationships

C is the whole and D is the part with a aggregation association

```
The life of the part does not depend on the whole
The part can be associated with multiple wholes.
```
```
C 1..* D
1..* uses
```

# Reading	UML	Relationships

```
C D
```
Generalization Relationship between classes or actors

```
C is a sub-class of D
```

# Reading	UML	Relationships

```
C D
```
Realization relationship used in class diagrams

```
C realizes the interface D
```


class: center, middle
# .red[Design] for Software Security Engineering

---
class: center, middle
# Threat and Design\*

![bad threat model](http://imgs.xkcd.com/comics/authorization.png)

.footnote[
\* Recommended by a Prior Student and [Bruce S.](https://www.schneier.com/blog/archives/2013/04/xkcd_on_a_bad_t.html)
]

---
![recap](https://robinagandhi.github.io/swa/slides/lecture-1/images/framework-course-topics.png)
???
# Quick recap
---
class: middle
# Security Analysis during Design

## Start with a Data-flow perspective
- **Most attacks come through .red[data]**
- Control flow is less relevant during the design stage
- A structured, concrete artifact to _discuss_ design:  
Conceptualization, Changes or Re-design

---
class: middle
## Practical Applications
_"Applying a structured approach to threat scenarios during design helps a team more effectively and less expensively identify security vulnerabilities, determine risks from those threats, and establish appropriate mitigations"_   
[Microsoft SDL](https://www.microsoft.com/en-us/SDL/process/design.aspx)

---
class: middle
# Data Flow Diagrams (DFD)

## DFDs are visual representations of .red[**data flows**] through components of a software program
- Components of a software program:  
.green[Data Source] &#8594; .orange[Data Transformations] &#8594; .red[Data Sink]
- All control flows are abstracted into _processes_  
that perform data transformations

---

class: middle
# DFD Elements
1. External Interactors
1. Processes
1. Data Stores
1. Trust Boundaries
1. Data Flows

---

# DFD Elements

.left-column[
## External Interactor/Entity
- .red[_Uncontrollable_] by the codebase of interest but is within the [environment of operation](https://robinagandhi.github.io/swa/slides/lecture-1/systems-security-engineering.html#14)
- Generate data (Source)
- Receive data (Sink)

## Examples    
People, External systems, External APIs
]

--

.right-column[
## Representation
![example](images/externalentity.svg)
## Naming
.red[Noun phrase] that describes the entity
]

???
## NOT the focus of threat modeling
---
# DFD Elements

.left-column[
## Process
- A collection of .red[code]
- Codebase of interest that is being threat modeled
- Transforms input data into output data

## Examples     
- Code, Native code, Executables, Libraries, Process execution scope
]

--

.right-column[
## Representation
![example](images/process.svg)
## Naming
- .red[Verb phrase] that describes the data transformation
- .red[Include process number]
]

---

# DFD Elements

.left-column[
## Data Store
- Place to hold data  
- Storage for a single process or transfer between processes  

## Examples
Files, Registry keys, Databases, Shared memory, Message Queue
]

--

.right-column[
## Representation
![example](images/datastore.svg)
## Naming
- .red[Noun phrase], but plural
]

---

# DFD Elements

.left-column[
## Data Flow
- Flow of data between External Interactors, Processes and Data Stores  
- Contracts between DFD elements

## Examples
Cookie, Form data, Response page, Credentials, etc.
]

--

.right-column[
## Representation
![example](images/dataflow.svg)
## Naming
- .red[Noun phrase] that describes the application data being transferred
]

---

# DFD Elements

.left-column[
## Trust Boundary
- Intersects .red[data flows]
- Component on one side doesn't trust the one on the other side

## Examples  
- Data flows from one privilege level to another  
- External entities and processes with different trust levels
]

--

.right-column[
## Representation
![example](images/boundary.svg)
## Naming
- Describes the boundary placement
]

---
## DFD Example

![example](images/dfd.png)

---
# DFD Levels

## Levels are hierarchically related
### Based on the granularity of the processes
- .red[**Level 0:**] Single process represents the whole system  
Very high-level; entire component / product / system.  
Show how the system interacts with the outside world.
- .red[**Level 1:**] Major processes and data stores identified   
High level; single feature / scenario
- .red[**Level 2:**] Detailed subcomponents of processes  
Low level; detailed features of a single feature / scenario
- ...

---
class: middle

# DFD Construction

## Step 1
### Start with a Level 0 diagram for a use case
- Single process
- Identify all External Interactors
- Draw data flows to connect them
---
class: middle
# DFD Construction
## Step 2
### Transition to a Level 1 diagram
- Breakdown the single Level 0 process into major processes and related data stores
- Check your work
- Can you tell a story without edits?
- Does it match reality?

---
class: middle
# DFD Construction
## Step 3
### Add trust boundaries that intersect data flows
### Trust boundary placement
- Threads are often inside a trust boundary.   
They share the same privileges, rights, identifiers and access    


- Processes talking across a network may create a secure channel, but .red[they’re still distinct entities.]   
Encrypting network traffic is an ‘instinctive’ mitigation, but may not address tampering or spoofing


---
class: middle
# DFD Construction
## Step 4
### Iterate over processes and data stores
- Break them down if more detail needed to explain .red[_security impact of the design_]


- Break them down if an object crosses a trust boundary. For example, a remote procedural call (RPC)


- Break them down if you use words like “sometimes” and “also” in your story

---
class: middle
# DFD Construction
## Step 5: Check the diagram for sanity (1)
### Data stores
- Two data stores should not be connected with data flows directly. They are static entities.
- External interactors should not directly interact with data stores. Their data representation formats are different.
- Data stores should have an input flow
- Try to locate data sinks, whenever possible

### Data Flows
- Attached to at least one process


---
# DFD Construction
## Step 5: Check the diagram for sanity (2)
### External Interactors
- Avoid data flows between External Interactors. They cannot be observed by the system.
- Data always comes from External Interactors.

### Processes
- Avoid direct dataflows between two separate processes. Use intermediate data stores such as message queues or domain sockets.
---
# DFD Construction
## Step 6
### Simplify
- Consolidate data flows that always flow together


- All processes need appropriate _inputs_ to generate _outputs_. No outputs without inputs!


- Avoid partitioning processes based on control logic.  
Partition processes that perform multiple functions.


- DFDs do not typically show time dependencies.   
If processes can communicate directly they are assumed to be synchronous!
---
class: middle
# DFD Modeling Summary
- DFDs depict data flows from sources to sinks with transformations along the way.   
Trust boundaries intersecting these data flows.


- Hierarchical structuring (Levels) allows system analysis at different levels of abstraction

---
class: middle, center
# Threat Identification
DFDs allows potential threats to be .red[automatically generated]!

---

class: middle
# Microsoft STRIDE Threats

.left-column[
## Threat
- .red[S]poofing
- .red[T]ampering
- .red[R]epudiation
- .red[I]nformation Disclosure
- .red[D]enial of Service
- .red[E]levation of Privilege
]

---

class: middle
# Microsoft STRIDE Threats

## Spoofing
* A process or entity is something other than the claimed identity

## Tampering
* Act of altering bits

## Repudiation
* Deny that something happened or an action was taken

---
class: middle
# Microsoft STRIDE Threats

## Information Disclosure
* Information can be read by an unauthorized party

## Denial of Service
* Process or data store not able to process incoming requests

## Elevation of Privilege
* A user can increase capability or privilege by taking advantage of an implementation bug
---

# STRIDE with DFDs (Per Element)

Threats that a DFD element can cause to its connected elements or is subject to itself.

.left-column[
## External Interactor
- SR

## Process
- STRIDE
]

--

.right-column[
## Data Store
- TID, R (logs only)

## Data Flow
- TID
]
---
class: middle
# Practice
![OWASP](https://www.owasp.org/images/0/00/Data_flow1.jpg)
---
class: middle
# Practice (2)
![OWASP](https://www.owasp.org/images/1/16/Data_flow2.jpg)
---
class: middle
# Observations and Reflections

--
## Expensive (Time)
- Too many threats to analyze! (even for small diagrams)

## Redundancy
- Redundant threats when analyzed individually

--

## How can we make this more efficient?
---
class: middle
# STRIDE with DFDs (Per .red[Interaction])
## Focus on Interactions
- Interaction:   
A source and target element connected by a data flow
---
class: middle
# STRIDE with DFDs (Per .red[Interaction])
## Efficiencies and Savings
- For each interactions apply STRIDE
- For each STRIDE threat identify the attacker controlled element and the attacked element
- For data flows inside a .red[single] process space,   
don’t worry about T, I, or D
- Prioritize interactions that cross trust boundaries
???
## Significant reduction in number of threats to be analyzed
---
class: middle
# Trust boundaries
## Trusted/high code reading from untrusted/low
- Look for Tampering threats

## High code writing to low
- Errors may result in Information Disclosure
---
class: middle
# Avoid Distractions
## Applications can't do much here:
- The computer is infected with malware
- Someone removed the hard drive and tampers
- Admin is attacking user
- A user is attacking himself

--

## Applications can’t address any of these   
(unless you’re the OS)

---
class: middle
# Practice

![OWASP](https://www.owasp.org/images/1/16/Data_flow2.jpg)

#### How many interactions? How many are high priority?

---

class: middle
# Practice
![example](images/dfd.png)

#### How many interactions? How many are high priority?
---
class: middle
# Observations and Reflections

--

## Automation
- Much of this analysis can be automated using simple rules based on the diagram structure
- Tool support

## Traceability
- Would be nice to link all analysis along with the diagram
- A bit more than a PPT, Visio or Lucidchart!

---
class: middle
# [Microsoft TMT 2016](https://www.microsoft.com/en-us/download/details.aspx?id=49168)
![toolsupport](images/toolsupport.png)
---
class: middle
# .center[Threat Mitigation]

.footnote[Why bother if you create a great model, identify lots of threats, and .red[stop!]]

---
class: middle
# Threat Mitigations
## Four ways to address each threat
1. Redesign to eliminate
1. Apply standard mitigations  
What have similar software packages done and how has that worked out for them?
1. Invent new mitigations (.red[risky!])
1. Accept vulnerability in design  
Risk acceptable, but must be verified and approved

---
class: middle
# STRIDE Controls

.left-column[
## Threat
- .red[S]poofing
- .red[T]ampering
- .red[R]epudiation
- .red[I]nformation Disclosure
- .red[D]enial of Service
- .red[E]levation of Privilege
]

.right-column[
## Control
- Authentication
- Integrity
- Nonrepudiation
- Confidentiality
- Availability
- Authorization
]
---

class: middle
# Standard Mitigations

## Spoofing
### Require authentication
- Data source
- Code integrity

### Validation of input read from the data source
- Normalization before neutralization
- Avoid recursion bombs

---
class: middle
# Standard Mitigations

## Tampering

### Integrity Checking
- Digital signatures and message authentication codes
- ACLs for data at rest

### Validation of input read from the data source
- Normalization before neutralization
- Avoid recursion bombs

---
class: middle
# Standard Mitigations

## Repudiation
- One-way log and audit generation mechanism
- Strong authentication for logging

## Information Disclosure
- ACLs
- Encryption with good key management and protocols
---
class: middle
# Standard Mitigations

## Denial or service
- ACLs to protect the contents of files from being removed or modified
- Firewall rules to protect against some network based attacks
- Use disk and processor quotas to prevent excess disk or CPU consumption

---
class: middle
# Standard Mitigations

## Elevation of Privilege
- Input validation
- Input validation
- Input validation
- ACLs, Roles, Groups
- Privilege dropping
- Least privilege

---
# How to ignore threats?
## No requirement
- There are no requirements that the &lt;&lt;element&gt;&gt; protect against &lt;&lt;STRIDE&gt;&gt; threat

## Irrelevant
- This threat does not exist, so we don't care about &lt;&lt;STRIDE&gt;&gt; threat to the &lt;&lt;element&gt;&gt;

## Not applicable
- &lt;&lt;STRIDE&gt;&gt; threat does not apply to this &lt;&lt;element&gt;&gt;
---
class: middle
# Validate the Threat Model

1. Do the threats consider misuse cases?
1. Does the diagram match final code?
1. Are threats enumerated? At minimum:
STRIDE per element that touches a trust boundary
1. Has Test / QA reviewed the model?
Testers often finds issues with threat model or details
1. Is each threat mitigated?
1. Are mitigations done right?  (Assurance case?)
---
class: middle
# Playsound API

"_The PlaySound API takes as input a string which represents either a WAV filename or an alias.  If the input is an alias, the PlaySound API retrieves data from the registry under HKCU to convert the alias into a filename.  Once the filename is determined, the PlaySound API opens the WAV file specified and reads the two relevant pieces from the file: the WAVEFORMATEX that defines the type of data in the file and the actual audio data.  It then hands that data to the audio rendering APIs._"

## Build a Threat Model based on this description

???

![solution](images/playsoundthreatmodel.png)  
http://blogs.msdn.com/b/larryosterman/archive/2007/09/13/threat-modeling-again-analyzing-the-threats-to-playsound.aspx

---
# Making this Fun

## Elevation of Privilege Card Game
- Ease developers into doing threat modeling
- [Card Game Introduction](https://www.microsoft.com/en-us/sdl/adopt/eop.aspx)
- [How to play](http://social.technet.microsoft.com/wiki/contents/articles/285.elevation-of-privilege-the-game.aspx)
- [Card Images](https://robinagandhi.github.io/swa/slides/lecture-4/images/eopcardcameimages.pdf)

![EOP](https://c.s-microsoft.com/en-us/CMSImages/EoP_game_screen_shot.jpg?version=4a082487-9fb4-7dd9-ed9f-e79c888c2df4)

---
class: middle
# More about threat modeling

## Blogs
- Microsoft Tutorial on [TMT 2014](http://blogs.microsoft.com/cybertrust/2014/04/15/introducing-microsoft-threat-modeling-tool-2014/  )
- Bruce Schneier on [threat modeling](http://www.schneier.com/blog/archives/2007/10/threat_modeling.html)

## Practice Diagrams
- Microsoft [Readings](https://msdn.microsoft.com/en-us/library/aa562036.aspx)

---
# Sources

- This presentation is borrows a lot from Microsoft training materials on threat modeling
- Many sources for Data flow diagrams
---

class: center, middle
# Threat Modeling Exercise

---
class: middle

# Step 1
- Download and install [TMT 2016](https://www.microsoft.com/en-us/download/details.aspx?id=49168)
- You may also directly access it on your machine at view.unomaha.edu

---

class: middle
# Step 2
## Recall the misuse case assignment
- You identified several use cases to include misuse cases.

---
class: middle
# Step 3
## Elaborate the Misuse cases using Threat models
- Develop Level 1 DFDs that supports each of your use cases.
- Perform analysis on your code base to align the diagram with reality
- Draw the DFDs in TMT 2016
- Identify appropriate trust boundaries on the diagram
- Validate the diagram for any obvious structural deficiencies

---
class: middle
# Step 4
## Analyze the Level 1 diagram to identify the applicable STRIDE threats
- Examine each threat automatically identified
- Document mitigation strategies for the identified threats
- Pay special attention for elements that interact across threat boundaries
- Generate a full HTML report using TMT 2016
- Host the reports on your project github repo.
- Review OSS project actual software design for security related issues based on your threat models. Summarize your observations.

---
# Grading criteria

### Use of proper notations
- DFD notation

### Threat Model Quality
- Threat model focuses on critical components of interest
- Proper wording of the model elements
- Clean, coherent and valid DFD diagram

### Threat Mitigation Quality
- Quality of analysis to mitigate threats

---
class: middle
# Due Date
Wednesday November 8th, 2017
# Structural	Patterns	for	

# Security	Engineering


# Distrustful	Decomposition


# Distrustful	Decomposition

- **Name**
    - Distrustful	Decomposition
- **Intent/Solution**
    - Move	 **_separate	functions	needing	different	privilege	_**
       **_levels	_** into	 **_mutually	untrusting	components_**
    - Reduce	functionality	and	data	exposed	to	an	
       attacker	if	one	of	the	mutually	untrusting	components	
       is	compromised	
- **Also	Known	As	**
    - Privilege	reduction	


# Distrustful	Decomposition

- **Applicability**
    - A	process	performs	more	than	one	
       high-level	function	
       But,	various	functions	of	the	system	require	
       different	privilege	levels.	
       So,	the	process	is	forced	to	run	at	the	highest	
       privilege	level	required	among	all	the	function!


# Distrustful	Decomposition

- **Structure**
    - Decompose	the	system	up	into	two	or	more	
       programs	that	run	as	separate	processes	that:
          - Potentially	have	different	privileges	
          - Perform	a	small,	well-defined	sub-function
          - Uses	inter-process	communication to	talk	to	other	
             processes.	E.g.	RPC,	sockets,	SOAP	or	shared	files
          - Are	 **mutually	untrusting**


# Distrustful	Decomposition

- **Structure**

```
The trust boundaries enforce mutually untrusting behavior between the
Frontend Process and the Authorization Process
```

# Distrustful	Decomposition

- **Consequences**
    - Compartmentalization	of	faults
       - prevents	an	attacker	from	compromising	an	entire	
          system	in	the	event	that	a	single	component	program	is	
          successfully	exploited	because	no	other	program	trusts	
          the	results	from	the	compromised	one
    - Easier	system	maintenance
    - Communication	overhead/slowdown
    - Protect	inter-process	communication	channels	
       from	tampering/disclosure/dos


# Distrustful	Decomposition

- **Implementation**
    - Each	program	runs	in	its	own	process	space	with	
       potentially	separate	user	privileges
    - Communication	between	separate	programs	is	
       either	one-way	or	two-way
          - One-way:	fork()/exec()(UNIX),	CreateProcess()
             (Windows)	is	used	to	transfer	control	
          - Two-way:	RPC,	sockets,	SOAP,	shared	files
    - No	component	places	any	inherent	trust in	the	
       contents	of	the	inter-process	communication


# Sendmail

**This is a single process
that runs as root!** 75


# Q-mail	(secure)


# q-mail

- qmail	ensures	that	local	mail	delivery	is	secure	by	

### breaking	it	into	two	processes:

- qmail-lspawn	and	qmail-local
- qmail-lspawn	runs	as	the	super-user
- Short	(less	than	500	lines)	and	simple
    - Looks	up	the	target	user	to	find	the	uid,	then	it	runs	qmail-
       local	after	becoming	that	user.	It	does	not	write	any	files,	nor	
       does	it	read	any	files	once	it	decides	on	its	new	uid.	


# Distrustful	Decomposition

- Known	Use
    - Qmail design
- Must	read	Papers

```
http://www.nrg4u.com/qmail/the-big-qmail-picture- 103 - a4.pdf 78
```
```
http://hillside.net/plop/
4/papers/mhafiz1/PLoP
04_mhafiz1_0.pdf
https://cr.yp.to/qmail/qmails
ec-20071101.pdf
```

# Privilege	Separation


# Privilege	Separation

- Intent/Solution
    - Reduce	the	“ **_amount	of	exposed	code_** ”	that	runs	
       with	special/high	privilege	without	affecting	or	
       limiting	the	functionality	of	the	program
    - Run	exposed	system	interfaces	as	limited	privilege	
       clients	(slave)	to	high	privilege	system	services	
       (monitor)	with	defined	information	requests	only	


# Privilege	Separation

- Applicability:
    - Useful	for	system	services	that	must	authenticate	
       users	and	then	allow	the	users	to	run	interactive	
       programs	with	normal,	user-level	privileges
    - Also	be	useful	in	general	for	authenticating	
       services


# !!	Vulnerable	Design	!!


# Privilege	Separation

- Implementation
    - Create	a	privileged	server.	Initial	user	requests	will	be	
       directed	to	this	server.	
    - When	a	user	request	arrives	at	the	server
       - The	server	will	spawn	off	an	untrusted,	unprivileged	child	to	
          handle	the	user	interaction	required	during	authentication
       - The	root	directory	of	the	child	process	is	set	to	an	
          unimportant,	empty	directory	or	a	jail	
    - After	the	user	has	been	authenticated,	the	server	will	
       spawn	off	another	child	process	with	the	appropriate	
       UID	to	actually	handle	the	user’s	request.	


# Privilege	Separation

[http://www.citi.umich.edu/u/provos/ssh/privsep.html](http://www.citi.umich.edu/u/provos/ssh/privsep.html)^84


# Privilege	Separation

[http://www.citi.umich.edu/u/provos/papers/privsep.pdf](http://www.citi.umich.edu/u/provos/papers/privsep.pdf)^85


# Privilege	Separation

- Consequences
    - An	adversary	who	gains	control	over	the	child	
       - is	confined	in	its	protection	domain	and	
          does	not	gain	control	over	the	parent	
       - does	not	gain	control	of	a	process	possessing	elevated	privileges,	
          thereby	limiting	the	damage	that	the	adversary	can	inflict	
    - Additional	verification,	such	as	code	reviews,	additional	
       testing,	and	formal	verification	techniques,	can	be	focused	
       on	code	that	is	executed	with	special	privilege,	which	can	
       further	reduce	the	incidence	of	privilege	escalation.	
    - System	administration	overhead	(unprivileged	user	IDs)


# Privsep.c Threat	Model

- **Structure**


# Summary	for	Interaction	Level	

# Structural	Patterns


# Modular	with	Mutual	Suspicion

- Components	should	not	trust	other	

## components	

- Trust	but	verify
- Each	component	in	an	interacting	pair	should	

## always	be	prepared	to	protect	itself	against	an	

## attack	from	the	other

- Perform	a	small,	well-defined	function
    - Separation	of	 _function_ and	 _privilege	levels_


# Least	privilege

- Separate	functions	that	require	different	

## privilege	levels

- Minimize	privilege	levels	in	components	

## exposed	to	users	or	network	connections

- Communicate	using	defined	messages	

## between	slave	client	and	privileged	server


# Compartmentalization

- Can	be	achieved	using:
    - Different	processes	spaces	with	different	user	
       accounts	and	privilege	sets
    - Empty	root	directories	of	child	process
    - Containers	or	Virtual	machines
    - Structured	Encapsulation	(Ring	architecture)
    - Sandboxing
    - Access	control


# Implementation	Level	

# Patterns


# Input	Validator

- Three	categories	of	input	 _handling_
    - Integrity	checks:	ensure	data	has	not	been	tampered	
       with	(requires	digital	signatures	and	hashing)
    - Validation:	a	set	of	rules	for
       - Data	is	of	a	certain	type
       - Has	correct	syntax,	canonicalized
       - Within	specified	length	boundaries
       - Contains	only	permitted	characters
    - Business	rules:
       - Checks	that	enforce	business	logic
          - Disallowing	due-dates	already	passed	when	paying	bills


# Structure


# Consequences

- Prevents	attacks	in	message	content
- Whitelisting	wards	off	unknown	attacks
- Accounting	of	attacks	by	capturing	rule	

## violations

- Centralized	mechanism	
- Reusable	solution,	but	do	not	reuse	

## implementation


# Secure	Logger

- Problem
    - Logs	can	leak	sensitive	system	information
    - Allow	attackers	to	hide	their	action	if	the	logs	can	
       be	edited
- Solution
    - Use	a	secure	logging	system	that	handles	and	
       stores	log	data


# Secure	Logger

- Structure
    - **Application:** generates	logging	data
    - **Secure	Logger:	** responsible	for	storing	
       the	logging	information	in	a	manner	
       that	makes	it	difficult	or	impossible	for	
       an	unauthorized	user	to	access	the	
       logging	data.Runs	in	a	separate	
       process
    - **Log	Reader:** a	reading	mechanism	
       specific	to	the	secure	logging	system
    - **Log	Viewer:	** An	authorized	user	may	
       read	the	log	data	using	some	sort	of	
       log-viewing	application.	


# Secure	Logger

- Consequences
    - Logs	provide	accountability	and	forensics	
       capabilities
    - Need	to	protect	log	files	(Compartmentalize)
    - Need	to	maintain	separate	logging	privileges
       - Prevents	covert	channels	and	improves	confidence	
          in	accountability
- Also	known	as:
    - Accountability	and	Traceability	


# Path	Name	Canonicalization

- Intent/Solution:
    - All	files	read	or	written	by	a	program	are	referred	
       to	by	a	valid	path	that	does	not	contain	any	
       symbolic	links	or	shortcuts,	i.e.	a	canonical	path	
    - Call	OS	specific	canonicalization	routines	before	
       performing	analysis	on	the	path	name
    - https://www.securecoding.cert.org/confluence/display/cplusplus/FIO02-
       CPP.+Canonicalize+path+names+originating+from+untrusted+sources


# Secure	Directory

- Intent/Solution:
    - File	operations	should	be	performed	in	a	 _secure	_
       _directory_ .	
          - Secure	Directory:	A	directory	in	which	no	one	other	
             than	the	user,	or	possibly	the	administrator,	has	the	
             ability	to	create,	rename,	delete,	or	otherwise	
             manipulate	files
    - https://www.securecoding.cert.org/confluence/display/c/FIO15-
       C.+Ensure+that+file+operations+are+performed+in+a+secure+directory


# Secure	Assertion

- Intent/Solution:
    - Disseminate	security	assumption	checks	
       throughout	the	application	to	continually	monitor	
       the	program	for	correct	behavior	and	detect	
       evidence	of	attack/misuse
    - Self-checks,	Self-analysis
       - e.g.		
          Begin: Critical Function
             {
                assert authorizationFlag == True
                dosomething....
             }
             [http://docs.oracle.com/javase/7/docs/technotes/guides/language/assert.html](http://docs.oracle.com/javase/7/docs/technotes/guides/language/assert.html) 101


# Deter/Slowdown

- Intent/Solution
    - Slow	password	hashing	functions	(PBKDF2,	bcrypt)
    - Account	lockout
       - Protects	accounts	from	automated	password-guessing	
          (known	username)	or	username	guessing	(known	password)	
          attacks,	by	implementing	a	limit	on	incorrect	attempts	
          before	further	attempts	are	disallowed
       - Time	limited	lockout	prevents	DoSattack


# Clear	Sensitive	Information

- Intent/Solution:
    - Sensitive	information	stored	in	a	reusable	
       resource	may	be	accessed	by	an	unauthorized	
       user	if	the	sensitive	information	is	not	cleared	
       before	freeing	the	reusable	resource
- Applicability:
    - Application	stores	sensitive	information	in	a	
       reusable	resource	


# Clear	Sensitive	Information

- Structure


# Deception

- Intent/Solution
    - Make	it	difficult	for	an	attacker	to	discern	the	
       internal	workings	of	an	application
          - Hide	all	error	messages	to	generic	one
          - Use	appropriate	compiler	flags
          - Remove	debugging	capabilities,	and	comments	in	
             generated	code
    - Trick,	detect,	and	block	attackers	during	a	
       break-in	attempt
    - Aggressively	introduce	variations	that	aid	
       in	detection	of	an	attacker 105


# Questions?



# Patterns	Sources

- Dougherty,	Chad	et	al.	 _Secure	Design	Patterns._ CMU/SEI- 2009 - TR-010.	
    Software	Engineering	Institute,	Carnegie	Mellon	University.	2009.	
    [http://resources.sei.cmu.edu/library/asset-view.cfm?AssetID=9115](http://resources.sei.cmu.edu/library/asset-view.cfm?AssetID=9115)
- High-Assurance	Design:	Architecting	Secure	and	Reliable	Enterprise	
    Applications	by	Clifford	J.	Berg **.ISBN-13:	** 978 - 0321793270.
    [http://amzn.com/0321793277](http://amzn.com/0321793277)



class: center, middle
# .red[Coding] for Software Security Engineering

---
# Good Code
.right-column[
![xkcd-good-code](http://imgs.xkcd.com/comics/good_code.png)
]
---
class: middle
# What to .red[avoid]?
## Enumerations and Dictionaries
- Common Weakness Enumeration
- Common Attack Pattern Enumeration and Classification
- Common Vulnerabilities and Exposures
- Coding Guidelines

???
An enumeration is a complete, ordered listing of all the items in a collection. The term is commonly used in mathematics and computer science to refer to a listing of all of the elements of a set. [Source Wikipedia]

---

class: middle
# Building Abstractions

## .orange[Weaknesses]\* span a range of languages, products and environments
- Enumeration is appropriate

## .red[Vulnerabilities]\* in code are language, product or environment specific
- Dictionary is appropriate

.footnote[
\* Relationships between a [vulnerability](https://cwe.mitre.org/documents/glossary/#Vulnerability) and [weakness](https://cwe.mitre.org/documents/glossary/#Weakness)
]

---
class: middle

## Building Abstractions for .orange[Weaknesses]
Examine commonalities and differences in mistakes

--

### Leads to useful analysis
- Which class of mistakes to address first?
- What are the related mistakes in an attack vector?
- What are the known/reusable mitigations?

---

class: middle
# Learning from .red[mistakes]

## Landwehr Software Flaw Taxonomy (1993)
- Genesis, Location, Time of introduction

--

## More recent efforts...
- Seven Pernicious Kingdoms, PLOVER, 19 Deadly Sins, OWASP top ten, WASP, etc,.

--

## Common Weaknesses Enumeration [(CWE)](http://cwe.mitre.org)
- Assimilates and advances categorization efforts

---

![CWE](http://cwe.mitre.org/about/images/lg_consensus.jpg)

---

class: middle
# CWE purpose
## Measurement
- Unified, .red[measurable] set of software weaknesses

## Communication
- Effective .red[sharing], description, selection, and use of software security tools and services

## Prioritization
- .red[Ranking] of software weaknesses related to design and code

---

class: middle
# CWE organization
![cwe](images/cwe-organization.png)

---
# CWE Types
### Weakness Class: e.g. [CWE-20](https://cwe.mitre.org/data/definitions/20.html)
- Abstract, independent of any specific language or technology

### Weakness Base: e.g. [CWE-79](https://cwe.mitre.org/data/definitions/79.html)
- Abstract, sufficient details to infer specific methods for detection and prevention

### Weakness Variant: e.g. [CWE-85](https://cwe.mitre.org/data/definitions/85.html)
- Detailed, limited to a specific language or technology.

### Weakness Category: e.g. [CWE-990](https://cwe.mitre.org/data/definitions/990.html)
- A set of other entries that share a common characteristic

---

# Finding the best CWE

## [Mapping Guidance](https://cwe.mitre.org/documents/cwe_usage/mapping_navigation.html)
- Map to a Weakness only
- .red[DO NOT] map to Categories or Views
- Map at the lowest abstraction level possible

## Search resources
- [Full text search](https://cwe.mitre.org/find/index.html)
- [Full listing](https://cwe.mitre.org/data/definitions/2000.html)
- Navigating views: [CWE-1000](https://cwe.mitre.org/data/definitions/1000.html), [CWE-699](https://cwe.mitre.org/data/definitions/699.html), [CWE-888](https://cwe.mitre.org/data/definitions/888.html)  
Turn on .blue[_Show Details_] option
- For a CWE page, turn on .blue[_Mapping-Friendly_] option.  
Then navigate to parent, child, peer relationships

---

class: middle

# Exercise
## Map [CVE-2004-0492](https://nvd.nist.gov/vuln/detail/CVE-2004-0492) to CWEs
- Description:   
Heap-based buffer overflow in proxy_util.c for mod_proxy in Apache 1.3.25 to 1.3.31 allows remote attackers to cause a denial of service (process crash) and possibly execute arbitrary code via a negative Content-Length HTTP header field, which causes a large amount of data to be copied.  
- Build a list of most relevant CWE IDs. Example: .red[79 35 34]

--

## Submit Response
- [Poll](http://PollEv.com/robingandhi)

???
# http://PollEv.com/robingandhi

---
<iframe src="https://embed.polleverywhere.com/free_text_polls/pKUP1ssJBP39qFC?controls=none&short_poll=true" width="100%" height="100%" frameBorder="0"></iframe>

---
class: middle
# Some CWEs to Remember
- [CWE-120](https://cwe.mitre.org/data/definitions/120.html): Classic buffer overflow
- [CWE-798](https://cwe.mitre.org/data/definitions/798.html): Use of hardcoded credentials
- [CWE-311](https://cwe.mitre.org/data/definitions/311.html): Missing encryption
- [CWE-434](https://cwe.mitre.org/data/definitions/434.html): Unrestricted upload of file with dangerous type
- [CWE-250](https://cwe.mitre.org/data/definitions/250.html): Execution with unnecessary privileges
- [CWE-494](https://cwe.mitre.org/data/definitions/494.html): Download of code without integrity check
- [CWE-22](https://cwe.mitre.org/data/definitions/22.html):  Path traversal
- [CWE-759](https://cwe.mitre.org/data/definitions/759.html): Use of one-way hash without a salt

## CWE Compatibility
- [CWE Compatibility and Effectiveness Program](http://cwe.mitre.org/compatible/index.html)

---

class: middle
# CWE Prioritization
## [Technical Impacts](https://cwe.mitre.org/cwss/cwss_v1.0.1.html#2.3.1) of [Weaknesses](https://cwe.mitre.org/cwraf/ti_scorecard.html)
1. Read data  
1. Modify data  
1. Denial-of-Service: unreliable execution  
1. Denial-of-Service: resource consumption  
1. Execute unauthorized code or commands  
1. Gain privileges / assume identity  
1. Bypass protection mechanism  
1. Hide activities  

## Top CWE lists
- [CWE/SANS Top 25](https://cwe.mitre.org/top25/index.html)
- Scoring mechanisms: [CWSS](https://cwe.mitre.org/cwss/index.html), [CWRAF](https://cwe.mitre.org/cwraf/index.html)

???
The technical impacts help focus on the set of weaknesses that contribute to the negative technical impact of relevance in a given context. This helps to filter and prioritize a set of weaknesses.

---

class: middle

# Attack Patterns

---

class: middle
# Common Attack Pattern Enumeration and Classification

## Enumerates .red[attack patterns] used in exploits
- Total of 550+ attack patterns
- Abstractions:   
Meta, Standard, Detailed Patterns and Categories

## CAPEC:  
- Patterns:  
[CAPEC-242](https://capec.mitre.org/data/definitions/242.html), [CAPEC-63](https://capec.mitre.org/data/definitions/63.html), [CAPEC-86](https://capec.mitre.org/data/definitions/86.html), [CAPEC-245](https://capec.mitre.org/data/definitions/245.html)    
- Views:    
[CAPEC 1000](https://capec.mitre.org/data/definitions/1000.html), [CAPEC-3000](https://capec.mitre.org/data/definitions/3000.html)

---
class: middle

# Vulnerabilities

---

class: middle
# Common Vulnerabilities and Exposures (CVE)

## One name for a vulnerability
- Akin to a .red[\#hashtag] to track all discussions and reports related to a [vulnerability in different databases](http://cve.mitre.org/about/)

![cve](http://cve.mitre.org/about/images/cve_example.gif)

---
class: middle

# [National Vulnerability Database](http://nvd.nist.gov)
- Maintains a dictionary of CVEs
- CVEs use Common Platform Enumeration (CPE) to identify affected products and packages. [Search Engine](https://nvd.nist.gov/vuln/search)
- Total CVEs: 80000+, ~15-20 added every day

---

# Visual Recap
![relationships](images/CVE-CWE-CAPEC.png)

---
class: middle
# Secure Coding Guidelines

---
class: middle
# CERT Secure Coding Guidelines
- Normative requirements (aka. coding standards) for programming languages
- [C, C++, Java, Perl, and the Android platform](https://www.securecoding.cert.org)
- Software development and software security communities
- Violation does not mean vulnerability but a weakness


## Rules
- [DCL30-C](https://www.securecoding.cert.org/confluence/display/c/DCL30-C.+Declare+objects+with+appropriate+storage+durations), [MEM30-C](https://www.securecoding.cert.org/confluence/display/c/MEM30-C.+Do+not+access+freed+memory)

## Other resources
- [Secure Programs HowTo](http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO.html#LANGUAGE-SPECIFIC)

---
# Rejoicing Project Managers!
### Johnny, avoid these weaknesses!
- CWE

### Johnny...these are the ways of the bad guys
- CAPEC

### Johnny...learn from your mistakes
- CVE

### Johnny...follow secure coding guidelines
- Secure coding guidelines
.top-right[
![dr.evil](https://upload.wikimedia.org/wikipedia/en/1/16/Drevil_million_dollars.jpg)
]
---
class: middle
# Why Johnny Can't Write Secure Code?
---
class: middle
## Poor Johnny!
![poorjohnny](images/poorjohnny.png)

---
class: middle
## Training Surgeons
![GA](https://pbs.twimg.com/media/CtPPfC3XEAA_sdq.jpg)

---
class: middle
## Paradox we Face!
![paradox](images/paradox.png)

---
class: middle
# Reducing the Cognitive Overload

## When the Devil is in the Details...
- The details to consider for avoiding weaknesses are enormous during the coding phases

## ...simple, intuitive guides are need
---
class: middle
# Key Questions for a Weakness
### What are the .blue[Software flaws] (omission, commission, operational) that lead to the weakness?
### What are the defining characteristics of the .orange[Weakness]?
### What are the .green[Resources/Location] where the weakness is typically manifest?
### What are the .red[Consequences] that the weakness precedes?

---
# Do CWEs answer them?
### CWE-119: Failure to Constrain Operations within the Bounds of a Memory Buffer
- The software performs operations on a memory buffer, but it can read from or write to a memory location that is outside of the intended boundary of the buffer.
- Certain languages allow direct addressing of memory locations and do not automatically ensure that these locations are valid for the memory buffer that is being referenced. This can cause read or write operations to be performed on memory locations that may be associated with other variables, data structures, or internal program data. As a result, an attacker may be able to execute arbitrary code, alter the intended control flow, read sensitive information, or cause the system to crash.

---
# Do CWEs answer them?
### CWE-119: .orange[Failure to Constrain Operations within the Bounds of a] .green[Memory Buffer]
- .orange[The software performs operations on a] .green[memory buffer].orange[, but it can read from or write to a memory location that is outside of the intended boundary of the] .green[buffer].
- Certain languages allow direct addressing of memory locations and .blue[do not automatically ensure that these locations are valid for the memory buffer that is being referenced.] .orange[This can cause read or write operations to be performed on memory locations that may be associated with other variables, data structures, or internal program data.] .red[As a result, an attacker may be able to execute arbitrary code, alter the intended control flow, read sensitive information, or cause the system to crash.]

---
# Untangling

![untangle](images/untangle.png)

---
# Full Extraction

![extraction](images/extraction.png)

---
# Buffer Overflow Template
![bo](images/botemplate.png)

---
class: middle
# Putting the pieces together
![crash](https://qph.ec.quoracdn.net/main-qimg-08cc5472e55ff2becf09468b9ae6c650-c?convert_to_webp=true)

---
class: middle
# CVE-2004-0492
- NVD Description:   
.green[Heap-based] .orange[buffer overflow] in proxy_util.c for mod_proxy in Apache 1.3.25 to 1.3.31 .red[allows remote attackers to cause a denial of service (process crash) and possibly execute arbitrary code] via a .blue[negative Content-Length HTTP header field], which .red[causes a large amount of data to be copied.]  

---

![source](images/sourcechanges.png)

---
#### **Buffer Overflow Semantic Template CVE-2004-0492**

![filledbo1](images/filledbo.png)

---
![filledbo2](images/filledbo2.png)

---
# Buffer Overflow Secure Coding Assessment

![checklist](images/checklist.png)
---

#### Injection template

![injection](images/injectiontemplate.png)

---
![filledinjection1](images/filledinjection1.png)

---

# Some take aways...
## Ask Johnny (or your software vendor):
### What CWEs do the vulnerabilities in your project typically map to? Have you taken any hands-on training for them?

--
### Have you looked at the [semantic templates](http://faculty.ist.unomaha.edu/rgandhi/st) by being developed at UNO?
### Here are some [example vulnerabilities](http://faculty.ist.unomaha.edu/rgandhi/st/CVEsamples.zip), why don’t you fill-up the semantic templates to study them?

---

class: middle
# Use/mentions of Semantic Templates

## NIST Bug Framework (BF)
https://samate.nist.gov/BF/
https://samate.nist.gov/BF/Enlightenment/ST.html

## CWE Acknowledgement
http://cwe.mitre.org/about/process.html#follow_on_opportunities

---
class: middle
# Acknowledgements
## This research is partially funded by
### DoD/AFOSR, NSF FA9550-07-1-0499, .blue[High Assurance Software] and
### NIST 70NANB12H013, .blue[Developing Precise and Accurate Descriptions of Common Software Weaknesses]
