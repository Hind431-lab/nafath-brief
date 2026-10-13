Version: NAFATH-V1

Track: Software

## Overview

This research explores six key areas for building a fully secure random login service. It examines the use of a single account to access government services via a mobile app and website. The service must upload personal information, securely verify users, and be trustworthy. Standards help explain automated logins to potential vulnerabilities, while artificial intelligence can support detection of suspicious logins.Mobile licensing, bell networks, phishing-resistant verification, and regulations on data protection are equally important. These regions are essential since any weakness in one could jeopardize system security. The following document also analyzes the way how OAuth 2.0 and OpenID Connect work together to support secure access to government services.

## Software

OAuth 2.0 and OpenID Connect have different uses. OAuth 2.0 is an authorization protocol whereby an app has access to limited resources after being authorized. On the other hand, OpenID Connect uses OAuth 2.0 and adds authentication such that an app has the ability to authenticate a person's identification via an ID token. OpenID Connect can thus be used for signing in, whereas OAuth 2.0 is useful for delegated access.

Resource: OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html

## AI

Prior to deploying the AI-based model for detecting suspicious login events, the authority should adhere to the NIST AI Risk Management Framework guidelines. In particular, it should test the effectiveness and reliability of the model, ensure its lack of biases which might cause unfair flagging of certain individuals, secure the private data of the citizens, and examine potential threats to security.

thiness - https://airc.nist.gov/airmf-resources/airmf/3-sec-characteristics/
Mobile

## Mobile

For Android, there is a permission-at-runtime concept that allows apps to ask users for permission before doing something that can cause harm or affect user privacy. If the user attempts to use the app and tries to access certain features, then the user should be asked for permission to use that particular feature. For example, if a user wants to use the app to take photos or use the location feature, then permission must be granted to access that feature.Requesting permissions in a timely manner helps users understand their purpose and make informed decisions. 

Resource: Request runtime permissions -https://developer.android.com/training/permissions/requesting 

## Networking

DoH transmits DNS requests via a secure HTTPS connection rather than an unsecured DNS connection. The main advantage of using DoH is that it allows citizens to conceal their DNS queries from any party monitoring or tampering with those requests on the same local network. DoH does not encrypt users' IP addresses or the rest of internet traffic, nor does it offer privacy protection against DNS resolution servers. An authority of the government must use DoH in conjunction with other measures.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484.html

## Cybersecurity

Phishing-resistant authentication prevents the attacks of using fake web login pages where the attackers try to steal user passwords and verification codes. Passkeys and security keys that use FIDO2/WebAuthn standards are phishing resistant since authentication is tied to an authentic website. On the other hand, passwords, SMS codes, and manually typed one-time password are subject to phishing attacks. A government sign-on system should rely on phishing-resistant techniques and ensure account recovery.

Resource: NIST SP 800-63B - Digital Identity Guidelines: Authentication and Authenticator Management - https://pages.nist.gov/800-63-4/sp800-63b.html

## Data

The Personal Data Protection Law of Oman is used to control the manner of collecting and processing of personal data. It is the responsibility of the government body to inform citizens of the reason for the collection of information and to seek their consent wherever necessary and also safeguard their data from any unauthorized access. There are certain citizen rights in respect to their personal data that include correction of their personal data.The entity must implement appropriate security measures, comply with legal requirements relating to data transfer, and report any breach of personal data in accordance with applicable regulations.

Resource: Royal Decree 6/2022 - Promulgating the Personal Data Protection Law - https://www.mtc.gov.om/itaportal/Data/English/DocLibrary/2024115132533256/PROMULGATING%20THE%20PERSONAL%20DATA%20PROTECTION%20LAW.pdf

## Misconception in My Track

OAuth 2.0 Is Not a Login Protocol :

The myth surrounding OAuth 2.0 is that it is used as a login protocol that identifies the user's credentials. However, OAuth 2.0 is built for delegated authentication where the application gets access to the resources based on the permissions provided. OpenID Connect brings an identity layer on top of OAuth 2.0 and supplies details of the authenticated user. In the case of the government single sign-on service, knowing the correct roles of protocols can be helpful in developing the security mechanisms. This difference is explained in the OpenID Connect Core spec.

Resource: OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html 


## Open Question

How can a government authority design a single sign-on system that securely authenticates citizens across multiple services while protecting their personal data and maintaining reliable access through both mobile applications and websites?
