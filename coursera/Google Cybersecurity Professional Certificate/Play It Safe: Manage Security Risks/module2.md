# Module 2: Security Frameworks and Controls

> *Created: 12 November 2025 | Last Updated: 12 November*

## Navigation

- [Frameworks](#frameworks)
- [Controls](#controls)
- [Threats, Risks, and Vulnerabilities](#threats-risks-and-vulnerabilities)
- [The Relationship Between Frameworks and Controls](#the-relationship-between-frameworks-and-controls)
- [Use the CIA Triad to Protect Organizations](#use-the-cia-triad-to-protect-organizations)
- [NIST Frameworks](#nist-frameworks)
- [Explore the Six Functions of the NIST Cybersecurity Framework](#explore-the-six-functions-of-the-nist-cybersecurity-framework)
- [OWASP Security Principles](#owasp-security-principles)
- [More About OWASP Security Principles](#more-about-owasp-security-principles)
- [Understanding Security Audits](#understanding-security-audits)
- [More About Security Audits](#more-about-security-audits)
- [Terms and Definitions](#terms-and-definitions-from-course-2-module-2)

---

## Frameworks

[Frameworks](https://www.coursera.org/learn/manage-security-risks/lecture/172X9/frameworks?trk_ref=coach_copy) Nov 12, 2025

**Understanding Security Frameworks**

-   Security frameworks provide a starting point for organizations to develop their security policies and processes.
-   These frameworks offer guidelines for building plans to mitigate risks and threats to data and privacy, including social engineering attacks and ransomware.

**Scope of Security**

-   Security encompasses both virtual and physical spaces, requiring plans to maintain safety in the work environment, such as using key cards for building access.
-   Frameworks also guide how to prevent, detect, and respond to security breaches, especially those targeting employees through social engineering attacks like phishing.

**Employee Awareness and Training**

-   Employees are a significant factor in security, so frameworks help create plans to increase their awareness and educate them on protecting the organization and themselves.
-   Providing training on recognizing potential threats and having reporting procedures are crucial for minimizing breaches.

[Back to Navigation](#navigation)

---

## Controls

**Understanding Security Controls**

-   Security controls are safeguards designed to reduce specific security risks, preventing significant financial and reputational damage.
-   They are crucial in protecting against various risks, such as unauthorized access or fraudulent activities.

**Types of Security Controls**

-   **Encryption:** This process converts readable data into an encoded format (ciphertext) to ensure confidentiality, making it unreadable until decrypted.
-   **Authentication:** This verifies the identity of a user or system, often through methods like usernames and passwords, or more advanced multi-factor authentication (MFA) using biometrics.
-   **Authorization:** This grants specific permissions to access resources within a system, ensuring that only authorized individuals can view or interact with particular data.

**Connection to the CIA Triad**

-   These security controls are integral components of the core security model known as the CIA triad, which focuses on confidentiality, integrity, and availability.

[Back to Navigation](#navigation)

---

## Threats, Risks, and Vulnerabilities

### Understanding Key Concepts

**Threat:** Any circumstance or event that can negatively impact assets
- *Examples:* Insider threats, Advanced Persistent Threats (APTs)

**Risk:** Anything that can impact the confidentiality, integrity, or availability of an asset
- *Formula:* Risk = Likelihood of a threat

**Vulnerability:** A weakness that can be exploited by a threat


### Risk Management Strategies

- **Acceptance:** Accepting risk to maintain business continuity
- **Avoidance:** Creating plans to avoid risks
- **Transference:** Transferring risk to third parties
- **Mitigation:** Lessening impact of known risks


### Common Risk Factors

- **External risk:** Threats outside the organization
- **Internal risk:** Current/former employees, vendors, partners
- **Legacy systems:** Outdated but still operational systems
- **Multiparty risk:** Third-party vendor access
- **Software compliance:** Unupdated or non-compliant software


### Notable Vulnerabilities

- **ProxyLogon:** Microsoft Exchange server vulnerability
- **ZeroLogon:** Netlogon authentication protocol weakness
- **Log4Shell:** Remote code execution in Java applications
- **PetitPotam:** Windows NTLM authentication manipulation
- **Security logging failures:** Insufficient monitoring capabilities

[Back to Navigation](#navigation)

---

## The Relationship Between Frameworks and Controls

Previously, you learned how organizations use security frameworks and controls to protect against threats, risks, and vulnerabilities. This included discussions about the National Institute of Standards and Technology's (NIST's) Risk Management Framework (RMF) and Cybersecurity Framework (CSF), as well as the confidentiality, integrity, and availability (CIA) triad. In this reading, you will further explore security frameworks and controls and how they are used together to help mitigate organizational risk.

## Frameworks and Controls

**Security frameworks** are guidelines used for building plans to help mitigate risk and threats to data and privacy. Frameworks support organizations' ability to adhere to compliance laws and regulations. For example, the healthcare industry uses frameworks to comply with the United States' Health Insurance Portability and Accountability Act (HIPAA), which requires that medical professionals keep patient information safe.

**Security controls** are safeguards designed to reduce _specific_ security risks. Security controls are the measures organizations use to lower risk and threats to data and privacy. For example, a control that can be used alongside frameworks to ensure a hospital remains compliant with HIPAA is requiring that patients use multi-factor authentication (MFA) to access their medical records. Using a measure like MFA to validate someone's identity is one way to help mitigate potential risks and threats to private data.

## Specific Frameworks and Controls

There are many different frameworks and controls that organizations can use to remain compliant with regulations and achieve their security goals. Frameworks covered in this reading are the Cyber Threat Framework (CTF) and the International Organization for Standardization/International Electrotechnical Commission (ISO/IEC) 27001. Several common security controls, used alongside these types of frameworks, are also explained.

### **Cyber Threat Framework (CTF)**

According to the Office of the Director of National Intelligence, the CTF was developed by the U.S. government to provide "a common language for describing and communicating information about cyber threat activity." By providing a common language to communicate information about threat activity, the CTF helps cybersecurity professionals analyze and share information more efficiently. This allows organizations to improve their response to the constantly evolving cybersecurity landscape and threat actors' many tactics and techniques.

### **International Organization for Standardization/International Electrotechnical Commission (ISO/IEC) 27001**

An internationally recognized and used framework is ISO/IEC 27001. The ISO 27000 family of standards enables organizations of all sectors and sizes to manage the security of assets, such as financial information, intellectual property, employee data, and information entrusted to third parties. This framework outlines requirements for an information security management system, best practices, and controls that support an organization's ability to manage risks. Although the ISO/IEC 27001 framework does not require the use of specific controls, it does provide a collection of controls that organizations can use to improve their security posture.

### **Controls**

Controls are used alongside frameworks to reduce the possibility and impact of a security threat, risk, or vulnerability. Controls can be physical, technical, and administrative and are typically used to prevent, detect, or correct security issues.

Examples of physical controls:
-   Gates, fences, and locks
-   Security guards
-   Closed-circuit television (CCTV), surveillance cameras, and motion detectors
-   Access cards or badges to enter office spaces

Examples of technical controls:
-   Firewalls
-   MFA
-   Antivirus software

Examples of administrative controls:
-   Separation of duties
-   Authorization
-   Asset classification

To learn more about controls, particularly those used to protect health-related assets from a variety of threat types, review the U.S. Department of Health and Human Services' [Physical Access Control presentation](https://www.hhs.gov/sites/default/files/physical-access-control.pdf).

## Key Takeaways

Cybersecurity frameworks and controls are used together to establish an organization's security posture. They also support an organization's ability to meet security goals and comply with laws and regulations. Although these frameworks and controls are typically voluntary, organizations are strongly encouraged to implement and use them to help ensure the safety of critical assets.

[Back to Navigation](#navigation)

---

## Use the CIA Triad to Protect Organizations

Previously, you were introduced to the confidentiality, integrity, and availability (CIA) triad and how it helps organizations consider and mitigate risk. In this reading, you will learn how cybersecurity analysts use the CIA triad in the workplace.

## The CIA Triad for Analysts

The **CIA triad** is a model that helps inform how organizations consider risk when setting up systems and security policies. It is made up of three elements that cybersecurity analysts and organizations work toward upholding: confidentiality, integrity, and availability. Maintaining an acceptable level of risk and ensuring systems and policies are designed with these elements in mind helps establish a successful **security posture**, which refers to an organization's ability to manage its defense of critical assets and data and react to change.

### **Confidentiality**

**Confidentiality** is the idea that only authorized users can access specific assets or data. In an organization, confidentiality can be enhanced through the implementation of design principles, such as the principle of least privilege. The principle of least privilege limits users' access to only the information they need to complete work-related tasks. Limiting access is one way of maintaining the confidentiality and security of private data.

### **Integrity**

**Integrity** is the idea that the data is verifiably correct, authentic, and reliable. Having protocols in place to verify the authenticity of data is essential. One way to verify data integrity is through [cryptography](https://www.nist.gov/cryptography#:~:text=Cryptography%20uses%20mathematical%20techniques%20to,that%20drives%20research%20and%20innovation.), which is used to transform data so unauthorized parties cannot read or tamper with it (NIST, 2022). Another example of how an organization might implement integrity is by enabling encryption, which is the process of converting data from a readable format to an encoded format. Encryption can be used to prevent access and ensure data, such as messages on an organization's internal chat platform, cannot be tampered with.

### **Availability**

**Availability** is the idea that data is accessible to those who are authorized to use it. When a system adheres to both availability and confidentiality principles, data can be used when needed. In the workplace, this could mean that the organization allows remote employees to access its internal network to perform their jobs. It's worth noting that access to data on the internal network is still limited, depending on what type of access employees need to do their jobs. If, for example, an employee works in the organization's accounting department, they might need access to corporate accounts but not data related to ongoing development projects.

## Key Takeaways

The CIA triad is essential for establishing an organization's security posture. Knowing what it is and how it's applied can help you better understand how security teams work to protect organizations and the people they serve.

[Back to Navigation](#navigation)

---

## NIST Frameworks

**Purpose of Frameworks**

-   Frameworks provide a starting point for developing plans to mitigate risks, threats, and vulnerabilities to sensitive data and assets.
-   Organizations worldwide create these frameworks to guide security professionals in developing effective security plans.

**NIST Cybersecurity Framework (CSF)**

-   The NIST CSF is a voluntary framework offering standards, guidelines, and best practices for managing cybersecurity risk.
-   It consists of five core functions: Identify, Protect, Detect, Respond, and Recover, which help organizations handle security incidents.

**NIST Special Publication (SP) 800-53**

-   NIST SP 800-53 provides a unified framework for protecting information systems within the U.S. federal government.
-   Its security controls are used to maintain the Confidentiality, Integrity, and Availability (CIA) triad for government systems.

[Back to Navigation](#navigation)

---

## Explore the Six Functions of the NIST Cybersecurity Framework

**NIST CSF Core Functions**

-   **Identify:** This function relates to managing cybersecurity risk and its impact on an organization's people and assets. For example, a security analyst might monitor systems to identify potential security issues.
-   **Protect:** This involves implementing policies, procedures, training, and tools to mitigate cybersecurity threats. This could include studying historical data to improve existing policies.
-   **Detect:** This function focuses on identifying potential security incidents and improving monitoring capabilities for faster and more efficient detection. An analyst might review a new security tool to ensure it flags risks appropriately.
-   **Respond:** This ensures proper procedures are used to contain, neutralize, and analyze security incidents, and to implement improvements. An analyst might collect data to document an incident and suggest process improvements.
-   **Recover:** This is the process of returning affected systems to normal operation after an incident. An entry-level security analyst might work with a team to restore systems, data, and assets.

[Back to Navigation](#navigation)

---

## OWASP Security Principles

**Minimizing Attack Surface and Least Privilege**

-   **Minimize Attack Surface Area:** Reduce potential vulnerabilities by disabling unnecessary software features, restricting asset access, and enforcing stronger password policies.
-   **Principle of Least Privilege:** Grant users only the minimum access necessary for their tasks to limit damage if credentials are compromised.

**Defense in Depth and Separation of Duties**

-   **Defense in Depth:** Implement multiple security controls like multi-factor authentication, firewalls, and intrusion detection systems to create layered protection.
-   **Separation of Duties:** Prevent fraud by ensuring no single individual has excessive privileges that could allow misuse of the system.

**Keeping Security Simple and Fixing Issues Correctly**

-   **Keep Security Simple:** Avoid overly complex security solutions that can become unmanageable and hinder collaboration.
-   **Fix Security Issues Correctly:** Identify the root cause of security incidents, correct vulnerabilities, and test repairs to ensure effectiveness.

[Back to Navigation](#navigation)

---

## More About OWASP Security Principles

Previously, you learned that cybersecurity analysts help keep data safe and reduce risk for an organization by using a variety of security frameworks, controls, and security principles. In this reading, you will learn about more Open Web Application Security Project, recently renamed Open Worldwide Application Security Project® (OWASP), security principles and how entry-level analysts use them.

## Security Principles

In the workplace, security principles are embedded in your daily tasks. Whether you are analyzing logs, monitoring a security information and event management (SIEM) dashboard, or using a [vulnerability scanner](https://csrc.nist.gov/glossary/term/vulnerability_scanner), you will use these principles in some way.

Previously, you were introduced to several OWASP security principles. These included:

-   **Minimize attack surface area**: Attack surface refers to all the potential vulnerabilities a threat actor could exploit.
-   **Principle of least privilege**: Users have the least amount of access required to perform their everyday tasks.
-   **Defense in depth**: Organizations should have varying security controls that mitigate risks and threats.
-   **Separation of duties**: Critical actions should rely on multiple people, each of whom follow the principle of least privilege.
-   **Keep security simple**: Avoid unnecessarily complicated solutions. Complexity makes security difficult.
-   **Fix security issues correctly**: When security incidents occur, identify the root cause, contain the impact, identify vulnerabilities, and conduct tests to ensure that remediation is successful.

## Additional OWASP Security Principles

Next, you'll learn about four additional OWASP security principles that cybersecurity analysts and their teams use to keep organizational operations and people safe.

### **Establish Secure Defaults**

This principle means that the optimal security state of an application is also its default state for users; it should take extra work to make the application insecure.

### **Fail Securely**

Fail securely means that when a control fails or stops, it should do so by defaulting to its most secure option. For example, when a firewall fails it should simply close all connections and block all new ones, rather than start accepting everything.

### **Don't Trust Services**

Many organizations work with third-party partners. These outside partners often have different security policies than the organization does. And the organization shouldn't explicitly trust that their partners' systems are secure. For example, if a third-party vendor tracks reward points for airline customers, the airline should ensure that the balance is accurate before sharing that information with their customers.

### **Avoid Security by Obscurity**

The security of key systems should not rely on keeping details hidden. Consider the following example from OWASP (2016): [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/2016-risks/)

The security of an application should not rely on keeping the source code secret. Its security should rely upon many other factors, including reasonable password policies, defense in depth, business transaction limits, solid network architecture, and fraud and audit controls.

## Key Takeaways

Cybersecurity professionals are constantly applying security principles to safeguard organizations and the people they serve. As an entry-level security analyst, you can use these security principles to promote safe development practices that reduce risks to companies and users alike.

[Back to Navigation](#navigation)

---

## Understanding Security Audits

-   A security audit systematically reviews an organization's security controls, policies, and procedures against established expectations.
-   Internal security audits, often conducted by an organization's compliance officer and security team, aim to improve security posture and ensure compliance, helping to avoid fines.

### Elements of Internal Security Audits

-   **Establishing Scope and Goals:** The scope defines the specific criteria of the audit, including people, assets, policies, and technologies, while goals outline the desired security objectives.
-   **Conducting a Risk Assessment:** This involves identifying potential threats, risks, and vulnerabilities to determine necessary security measures for asset protection.

## Entry-Level Analyst Contributions

-   While senior staff typically establish audit scope and goals, entry-level analysts may review and understand them to complete other audit tasks.
-   Entry-level analysts might also analyze risk assessment details to help determine appropriate controls and compliance regulations.

### Review and Assessment

-   Before proceeding, it's crucial to review the audit's scope, goals, and risk assessment to ensure alignment and address key questions about assets, risks, and control sufficiency.
-   A controls assessment involves a detailed review of an organization's assets and potential risks to evaluate the effectiveness of existing internal controls and processes.

### Control Classifications and Compliance

-   Controls are categorized into administrative (human-related policies like password policies), technical (hardware/software solutions like intrusion detection systems), and physical (measures preventing physical access like surveillance cameras).
-   Assessing compliance ensures the organization adheres to necessary regulations, such as GDPR and PCI DSS for businesses operating in the European Union and accepting credit card payments.

### Communication and Improvement

-   The final step is communicating audit results and recommendations to stakeholders, summarizing the scope, goals, existing risks, and compliance adherence.
-   Internal audits are valuable for identifying security gaps and areas for improvement, ultimately strengthening an organization's security posture.

[Back to Navigation](#navigation)

---

## More About Security Audits

Previously, you were introduced to how to plan and complete an internal security audit. In this reading, you will learn more about security audits, including the goals and objectives of audits.

## Security Audits

A **security audit** is a review of an organization's security controls, policies, and procedures against a set of expectations. Audits are independent reviews that evaluate whether an organization is meeting internal and external criteria. Internal criteria include outlined policies, procedures, and best practices. External criteria include regulatory compliance, laws, and federal regulations.

Additionally, a security audit can be used to assess an organization's established security controls. As a reminder, **security controls** are safeguards designed to reduce specific security risks.

Audits help ensure that security checks are made (i.e., daily monitoring of security information and event management dashboards), to identify threats, risks, and vulnerabilities. This helps maintain an organization's security posture. And, if there are security issues, a remediation process must be in place.

## Goals and Objectives of an Audit

The goal of an audit is to ensure an organization's information technology (IT) practices are meeting industry and organizational standards. The objective is to identify and address areas of remediation and growth. Audits provide direction and clarity by identifying what the current failures are and developing a plan to correct them.

Security audits must be performed to safeguard data and avoid penalties and fines from governmental agencies. The frequency of audits is dependent on local laws and federal compliance regulations.

## Factors That Affect Audits

Factors that determine the types of audits an organization implements include:
-   Industry type
-   Organization size
-   Ties to the applicable government regulations
-   A business's geographical location
-   A business decision to adhere to a specific regulatory compliance

## The Role of Frameworks and Controls in Audits

Along with compliance, it's important to mention the role of frameworks and controls in security audits. Frameworks such as the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF) and the international standard for information security (ISO 27000) series are designed to help organizations prepare for regulatory compliance security audits. By adhering to these and other relevant frameworks, organizations can save time when conducting external and internal audits. Additionally, frameworks, when used alongside controls, can support organizations' ability to align with regulatory compliance requirements and standards.

There are three main categories of controls to review during an audit, which are administrative and/or managerial, technical, and physical controls. To learn more about specific controls related to each category, click the following link and select "Use Template."

Link to template: [Control categories](https://docs.google.com/document/d/1Ut_H5A9FHwuQEy6_qG6Lfy3zwF6GSJnj3DZTMaNRWEE/template/preview?resourcekey=0-i4dR5qZFqQyfzr8uk3OOmA)

OR

If you don't have a Google account, you can download the template directly from the following attachment

## Audit Checklist

It's necessary to create an audit checklist before conducting an audit. A checklist is generally made up of the following areas of focus:

**Identify the scope of the audit**
-   The audit should:
    -   List assets that will be assessed (e.g., firewalls are configured correctly, PII is secure, physical assets are locked, etc.)
    -   Note how the audit will help the organization achieve its desired goals
    -   Indicate how often an audit should be performed
    -   Include an evaluation of organizational policies, protocols, and procedures to make sure they are working as intended and being implemented by employees

**Complete a risk assessment**
-   A risk assessment is used to evaluate identified organizational risks related to budget, controls, internal processes, and external standards (i.e., regulations).

**Conduct the audit**
-   When conducting an internal audit, you will assess the security of the identified assets listed in the audit scope.

**Create a mitigation plan**
-   A mitigation plan is a strategy established to lower the level of risk and potential costs, penalties, or other issues that can negatively affect the organization's security posture.

**Communicate results to stakeholders**
-   The end result of this process is providing a detailed report of findings, suggested improvements needed to lower the organization's level of risk, and compliance regulations and standards the organization needs to adhere to.

## Key Takeaways

In this reading you learned more about security audits, including what they are; why they're conducted; and the role of frameworks, controls, and compliance in audits.

Although there is much more to learn about security audits, this introduction is meant to support your ability to complete an audit of your own for a self-reflection portfolio activity later in this course.

## Resources for More Information

Resources that you can explore to further develop your understanding of audits in the cybersecurity space are:
-   [Assessment and Auditing Resources](https://www.nist.gov/cyberframework/assessment-auditing-resources)
-   [IT Disaster Recovery Plan](https://www.ready.gov/it-disaster-recovery-plan)

[Back to Navigation](#navigation)

---

## Terms and Definitions from Course 2, Module 2

**Asset:** An item perceived as having value to an organization

**Attack vectors:** The pathways attackers use to penetrate security defenses

**Authentication:** The process of verifying who someone is

**Authorization:** The concept of granting access to specific resources in a system

**Availability:** The idea that data is accessible to those who are authorized to access it

**Biometrics:** The unique physical characteristics that can be used to verify a person's identity

**Confidentiality:** The idea that only authorized users can access specific assets or data

**Confidentiality, integrity, availability (CIA) triad:** A model that helps inform how organizations consider risk when setting up systems and security policies

**Detect:** A NIST core function related to identifying potential security incidents and improving monitoring capabilities to increase the speed and efficiency of detections

**Encryption:** The process of converting data from a readable format to an encoded format

**Govern**: A NIST core function related to ensuring an organization establishes, oversees, and improves its cybersecurity strategy, policies, roles, and risk management processes to align with business goals and regulations

**Identify**: A NIST core function related to management of cybersecurity risk and its effect on an organization's people and assets

**Integrity:** The idea that the data is correct, authentic, and reliable

**National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF):** A voluntary framework that consists of standards, guidelines, and best practices to manage cybersecurity risk

**National Institute of Standards and Technology (NIST) Special Publication (S.P.) 800-53:** A unified framework for protecting the security of information systems within the U.S. federal government

**Open Web Application Security Project/Open Worldwide Application Security Project (OWASP):** A non-profit organization focused on improving software security

**Protect:** A NIST core function used to protect an organization through the implementation of policies, procedures, training, and tools that help mitigate cybersecurity threats

**Recover:** A NIST core function related to returning affected systems back to normal operation

**Respond:** A NIST core function related to making sure that the proper procedures are used to contain, neutralize, and analyze security incidents, and implement improvements to the security process

**Risk:** Anything that can impact the confidentiality, integrity, or availability of an asset

**Security audit:** A review of an organization's security controls, policies, and procedures against a set of expectations

**Security controls:** Safeguards designed to reduce specific security risks

**Security frameworks:** Guidelines used for building plans to help mitigate risk and threats to data and privacy

**Security posture:** An organization's ability to manage its defense of critical assets and data and react to change

**Threat:** Any circumstance or event that can negatively impact assets

[Back to Navigation](#navigation)
