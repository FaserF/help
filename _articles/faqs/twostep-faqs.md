---
layout: article
title: Two-step Login FAQs
categories: [two-step-login]
featured: true
popular: false
hidden: false
tags: []
order: "10"
description: "This article contains FAQs about two-step login - an important piece of good security practice when using Bitwarden."
---

This article contains Frequently Asked Questions (FAQs) regarding **Two-step Login**.

### Q: Can I use SMS 2FA?

**A:** Bitwarden does not support SMS 2FA due to vulnerabilities, including SIM hijacking. We do not recommend SMS 2FA for other accounts unless it is the only available method. Any second factor is recommended over having none, but most alternatives are safer than SMS 2FA.

### Q: Can I require my Organization's users to use Two-step Login?

**A:** You can require your Organization's users to use Two-step Login by enabling the [Two-step Login Policy]({{site.baseurl}}/article/policies/#two-step-login). Additionally, you can setup [Organization-wide Duo 2FA]({{site.baseurl}}/article/setup-two-step-login-duo/) to ensure that all of your users have a secure Two-step Login method at their disposal.

### Q: Is FIDO U2F or FIDO2 WebAuthn supported on my iOS or Android App?

**A:** Yes! Please see [Two-step Login via FIDO2 WebAuthn]({{site.baseurl}}/article/setup-two-step-login-fido/).

### Q: Why is Bitwarden not asking for my enabled Two-step Login method?

**A:** In most cases, one of two things is happening:

1. You may be already logged in to Bitwarden and only unlocking your Vault. Two-step Login is required to **Log In** but not to **Unlock** your Vault. For more information on the difference between Logging In and Unlocking, see [Vault Timeout Action]({{site.baseurl}}/article/vault-timeout/#vault-timeout-action).

2. You may have previously checked the **Remember me** checkbox on a device when accessing your Vault using Two-step Login.

   {% image two-step/twostep-remember.png Remember me option %}

   If you used the **Remember me** option, you will need to **Deauthorize Sessions** from your Web Vault (**Settings** &rarr; **My Account**) for that device to continue asking for your Two-step Login method.
