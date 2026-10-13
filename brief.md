Version: NAFATH-V1

Track: AI

## Overview
This research explores six key areas for building a fully secure random login service. It examines the use of a single account to access government services via a mobile app and website. The service must upload personal information, securely verify users, and be trustworthy. Standards help explain automated logins to potential vulnerabilities, while artificial intelligence can support detection of suspicious logins.Mobile licensing, bell networks, phishing-resistant verification, and regulations on data protection are equally important. These regions are essential since any weakness in one could jeopardize system security. This research reviews officially accepted guidelines to understand the key requirements before launching a specialized service.


## Software
OpenID Connect and OAuth 2.0 are distinct protocols used for different purposes. OAuth 2.0 is a protocol for authorization that enables an application to have limited access to certain resources under authorized access. OpenID Connect utilizes OAuth 2.0 and provides authentication capabilities that enable applications to authenticate the identity of a user by making use of an ID Token. In conclusion, OpenID Connect can be said to be for logins while OAuth 2.0 is for delegated access.

Resource: OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html

## AI
The NIST framework should be applied by the government body before the deployment of the AI-based tool to detect any suspicious login. The framework requires the assessment of the reliability and accuracy of the algorithm, the possibility of biasing the model that can result in the unjust detection of certain users, the protection of the citizens’ private information, and identification of the potential security risk of the model.

Resource: AI Risks and Trustworthiness - https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/

## Mobile
For Android, there is a permission-at-runtime concept that allows apps to ask users for permission before doing something that can cause harm or affect user privacy. If the user attempts to use the app and tries to access certain features, then the user should be asked for permission to use that particular feature. For example, if a user wants to use the app to take photos or use the location feature, then permission must be granted to access that feature.

Resource: Request runtime permissions -https://developer.android.com/training/permissions/requesting 

## Networking

In DoH, DNS requests are sent using the encrypted HTTPS channel rather than the traditional DNS channel that was not encrypted. The technique will make it difficult for someone to monitor and even alter the DNS requests made. But the process does not hide the IP address of the user nor encrypts all data sent using the internet connection. DoH can be used together with HTTPS and other network security techniques by a government authority.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484.html

## Cybersecurity

Phishing-resistant authentication ensures that the user is safe from fraudulent login sites that attempt to steal their password or verification code. Authentication based on passkeys or security keys, which use FIDO2/WebAuthn technology, is phishing-resistant since it is connected to the legitimate website. On the other hand, passwords, SMS codes, and manual one-time passwords are susceptible to being stolen via phishing. It is essential for a government sign-on system to use phishing-resistant methods.

Resource: NIST SP 800-63B - Digital Identity Guidelines: Authentication and Authenticator Management - https://pages.nist.gov/800-63-4/sp800-63b.html

## Data

The Personal Data Protection Law of Oman is used to control the manner of collecting and processing of personal data. It is the responsibility of the government body to inform citizens of the reason for the collection of information and to seek their consent wherever necessary and also safeguard their data from any unauthorized access. There are certain citizen rights in respect to their personal data that include correction of their personal data.

Resource: NIST SP 800-63B - Digital Identity Guidelines: Authentication and Authenticator Management - https://pages.nist.gov/800-63-4/sp800-63b.html 

## Misconception in My Track

AI Risk Management Framework:

One of the fallacies is that a highly accurate AI model is guaranteed to be safe and can be deployed. However, a highly accurate model cannot be considered to be necessarily fair, private, secure, or resistant to attacks. For instance, a login detection algorithm will make mistakes and wrongly mark a user or fail to detect a malicious user. The regulator needs to ensure that the model is tested using various scenarios, that there is no bias, personal data protection measures are taken, the key decision-making processes can be explained, and post-deployment monitoring is conducted. Human oversight is also necessary in case decisions might affect citizens' access to governmental services.

Resource evidence: NIST AI Risk Management Framework 1.0 - “Map, Measure, Manage” - https://www.nist.gov/itl/ai-risk-management-framework


## Open Question

How can a government authority ensure that an AI model detecting suspicious logins remains accurate, fair, and secure as attackers change their techniques, while protecting citizens’ privacy and avoiding the blocking of legitimate users?
