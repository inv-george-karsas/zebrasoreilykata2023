# ADR 08: MSAL Based Security

## Status

Accepted

## Context

MSAL (Microsoft Authentication Library) is a library that provides developers with a way to authenticate users and obtain access tokens to secure APIs and web services. MSAL provides several benefits for security:

* Secure authentication: MSAL provides secure authentication using industry-standard protocols such as OpenID Connect and OAuth 2.0.
* Cross-platform support: MSAL supports authentication for a wide range of platforms and programming languages, including .NET, Java, JavaScript, Python, and more.
* Integration with Microsoft identity platform: MSAL integrates with the Microsoft identity platform, which provides a secure and scalable way to manage user identities and access to resources.
* Token caching: MSAL provides token caching, which allows your application to cache access tokens and refresh tokens, reducing the number of times your application needs to authenticate the user.
* Single sign-on: MSAL provides single sign-on (SSO) capabilities, which allows users to sign in once and access multiple applications without having to sign in again.
* Multi-factor authentication: MSAL supports multi-factor authentication (MFA), which provides an additional layer of security by requiring users to provide additional authentication factors, such as a code sent to their phone or an authentication app.

Overall, MSAL provides a secure and flexible way to manage user authentication and access to resources in your application.

## Decision

We will utilise MSAL as part of our General Application Design Standard

## Consequences

We will need to ensure that Engineers are trained in the usage of MSAL in their respective applications.
