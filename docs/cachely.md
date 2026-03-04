## Cachely – Privacy Policy

**App Name:** Cachely - Cache Cleaner  
**Package Name (Application ID):** com.cachely.app  
**Developer/Company Name:** Aneesh  
**Effective Date:** March 4, 2026

---

### Introduction

This Privacy Policy explains how Cachely ("**the App**", "**we**", "**us**" or "**our**") handles information when you install and use the App on your Android device.  
Cachely is a minimal, one‑tap cache cleaner focused on performing a single, clear task: helping you clear app cache on your device. The App has **no ads** and **no tracking SDKs**.

Cachely operates locally on your device. Based on the current implementation, the App does **not** collect, transmit, sell, or share your personal data with third parties. Any technical information processed by the App is used solely to provide the core cache‑cleaning functionality and remains on your device.

By using the App, you agree to the handling of information as described in this Privacy Policy. If you do not agree, you should not use the App.

---

### Data Controller

For the purposes of applicable data protection laws (including the EU General Data Protection Regulation), the **data controller** responsible for the processing of personal data in connection with the App is:

- **Name:** Aneesh  
- **Country:** India  
- **Contact email:** thealectronai@gmail.com

---

### Information We Collect

Cachely is designed to avoid collecting personal data. However, certain device and app‑level information must be processed locally in order to provide the cache‑cleaning feature.

#### 1. Installed App and Cache Information (On‑Device Only)

To show you which apps can have their cache cleaned and to estimate freed space, the App reads the following information from the Android system:

- **Installed applications metadata**, including:
  - App display name
  - Package name (e.g., `com.example.app`)
  - Whether the app is a system app
  - Whether the app is launchable
  - Whether the app is currently enabled or disabled
- **Approximate cache size per app**, obtained via Android’s `StorageStatsManager` when you have granted **Usage Access** permission (`android.permission.PACKAGE_USAGE_STATS`) in system settings.

This information is:

- Obtained from the Android operating system.
- Processed in memory to:
  - Build and display the app list.
  - Sort apps (for example, by approximate cache size).
  - Determine whether an app is eligible for cache cleaning.
- Used to compute session results such as:
  - Total bytes freed.
  - Number of apps cleaned and skipped.
- **Not transmitted** to any server or third‑party service according to the current code.

Because the App does **not** declare the Android `INTERNET` permission, it technically cannot transmit data over the network.

#### 2. Accessibility Information (On‑Device Only, Optional)

If you choose to enable the optional Accessibility Service in system settings, the App can assist with tapping the **"Clear cache"** button on system Settings screens (App Info / Storage) for the apps you have selected to clean.

In this mode, the App:

- Listens for window changes on Android system Settings screens related to App Info / Storage.
- Searches the visible text to find elements such as:
  - "Storage" / "Storage & cache"
  - "Clear cache"
- Optionally reads the **numeric cache size** text near the "Cache" label in order to estimate how many bytes of cache are cleared when you run a cleaning session.

Important safeguards in the current implementation:

- The Accessibility automation only runs when you **explicitly start a cleaning session** in the App, and a cleaning session is marked as active.
- When there is **no active cleaning session**, the service ignores Accessibility events and does not attempt to take actions.
- The service is focused on **Settings screens only** and is used to:
  - Navigate to the Storage screen.
  - Tap the "Clear cache" button.
  - Report the estimated number of bytes cleared back to the App for that session.
- The App does **not**:
  - Save the full contents of any screen.
  - Transmit Accessibility content off the device.
  - Use Accessibility for background monitoring or unrelated purposes.

The Accessibility Service is used exclusively to automate the cache‑clearing interaction inside Android system settings and is not used for data collection or monitoring general user activity.

Accessibility permissions can be disabled at any time via your device’s system settings. If disabled, assisted cleaning is turned off and Cachely will fall back to a manual flow where you are guided to clear cache yourself.

#### 3. Usage Access Information (On‑Device Only, Optional)

If you grant the Usage Access permission in system settings:

- The App uses `StorageStatsManager` and related Android APIs to obtain **approximate cache sizes** for other apps.
- This is used exclusively to:
  - Show estimated cache size per app.
  - Improve the transparency of cleaning actions and potential storage savings.

If you do **not** grant Usage Access:

- Approximate cache sizes are treated as zero by the App.
- The UI may instead show generic states (for example, "Ready to clean") without specific size estimates.

The App does not use Usage Access data for analytics, profiling, or tracking.

#### 4. Local Settings and UI State

The App manages certain local settings such as appearance (dark/light mode) and user interface state. Based on the current implementation:

- These settings are used to control the App’s look and behavior on your device.
- They are not linked to personal identifiers such as your name, email, or address.
- They are not transmitted to remote servers.
- Any local storage used is limited to non‑sensitive preferences and remains fully on‑device.

#### 5. Contacting Support

From the "Support & Legal" section in the App, you can choose to contact support via email. When you tap this option:

- The App opens your chosen email client with a pre‑filled **support email address** (`thealectronai@gmail.com`).
- You may include information such as:
  - Your email address.
  - Device model and Android version (if you choose to share this).
  - Screenshots or a description of the issue.

The App itself:

- Does **not** read, intercept, or transmit the content of your support email.
- Does **not** access your email inbox.

Any information you choose to send to support is handled by:

- Your email provider; and
- The developer’s support processes. Support emails may be retained for up to 12 months for troubleshooting, record‑keeping, and legal compliance, and only the developer has access to these emails.

#### 6. External Links and Store Interactions

The App can open external links on your device, including:

- A **Privacy Policy** URL currently hosted at `https://github.com/Aneesh-Madupalli/public_docs/blob/main/docs/cachely.md`.
- The App’s listing on the **Google Play Store**.
- A share sheet link where you can share the Play Store URL with others.

When you tap these options:

- The App instructs your device to open a web browser, the Play Store app, or a share/intents chooser.
- Any data collected during your use of these external services is governed by the privacy policies and terms of those services (for example, Google Play, your web browser, your messaging apps), **not by this App**.

The page hosting this Privacy Policy does not use analytics, cookies, or other tracking technologies.

---

### How We Use Information

Cachely uses the information described above solely to provide and improve the core cache‑cleaning experience, including:

- Displaying a list of installed apps that can have their cache cleaned.
- Estimating and showing approximate cache sizes (when Usage Access is granted).
- Orchestrating assisted cleaning:
  - Opening App Info / Storage screens.
  - Tapping the "Clear cache" button using the Accessibility Service (if enabled).
  - Calculating estimated bytes freed per cleaning session.
- Presenting progress and results to you (for example, how many apps were cleaned, how many were skipped, and total cache cleared).

Cachely does **not** use your information to:

- Create a personal profile or behavioral record.
- Serve targeted or interest‑based advertising.
- Share data with third parties for marketing or analytics.

---

### Third‑Party Services

According to the current project configuration:

- The App does **not** integrate analytics SDKs such as Firebase Analytics, Google Analytics, or similar services.
- The App does **not** integrate advertising SDKs such as AdMob or Facebook Audience Network.
- The App does **not** integrate crash‑reporting SDKs such as Firebase Crashlytics.
- The App does **not** declare the `INTERNET` permission, which prevents network access from the App itself and technically stops the App from sending data over the network.

The only third‑party interactions are:

- Your **email provider**, when you choose to send a support email.
- Your **web browser** or **Google Play Store app**, when you open links for the Privacy Policy, rating the App, or sharing the App.

These third parties operate under their own terms and privacy policies.

If additional third‑party SDKs or backend services are added in future versions that would send device or usage data off the device, this Privacy Policy and the Google Play Data Safety section will be updated to describe them accurately.

---

### Advertising and Monetization

For the current version of Cachely:

- The App shows **no in‑app advertisements**.
- The App does **not** use advertising SDKs, ad networks, mediation platforms, or user profiling for ads.
- The App does **not** sell or share data with third parties for advertising or marketing purposes.

If a future version of Cachely introduces ads or other monetization features that rely on data processing, this Privacy Policy and the Google Play Data Safety section will be updated in advance to:

- Clearly describe what data is used for advertising or monetization; and
- Provide appropriate choices or controls where required by applicable law.

---

### Data Sharing and Disclosure

Based on the current implementation, Cachely:

- **Does not sell** your data.
- **Does not share** your data with third parties for advertising, analytics, or user profiling.
- **Does not transfer** the app and cache metadata it processes to any remote server.

Information may be disclosed only in the following limited circumstances:

- **At your direction**:
  - When you choose to send an email to support, you voluntarily share the contents of that email with the developer and your email provider.
  - When you share the App’s Play Store link using your device’s share sheet, you voluntarily choose the recipient and channel.
- **Legal and safety reasons**:
  - We may disclose information if we reasonably believe it is necessary to:
    - Comply with applicable law, regulation, legal process, or governmental request.
    - Enforce applicable terms of use.
    - Detect, prevent, or address fraud, security, or technical issues.
    - Protect the rights, property, or safety of the developer, users, or the public as required or permitted by law.

---

### Data Retention

For the App itself:

- Installed app information, cache sizes, and cleaning session statistics are processed **in memory** to provide functionality and display results.
- This information is not written to a remote server.
- The App, as written, does not maintain long‑term, user‑identifiable logs of cache sizes or which apps you cleaned.

For support communications:

- If you contact us via email, the content of your message and any associated metadata (such as your email address and the date of your message) may be stored by us for as long as reasonably necessary to:
  - Respond to your request.
  - Maintain records of support interactions.
  - Comply with legal obligations or resolve disputes.
- As a general rule, support emails may be retained for up to 12 months, and only the developer has access to these emails.

---

### Security

We take reasonable technical and organizational measures designed to protect information processed by the App, including:

- Designing the App to work **without network access**, minimizing exposure of information.
- Restricting Accessibility and Usage Access processing to what is necessary for the cleaning feature.
- Avoiding the collection of user account information or direct identifiers.

However, no method of electronic storage or transmission is completely secure. While we strive to protect your information, we cannot guarantee absolute security.

If you believe you have discovered a security or privacy issue in the App, you are encouraged to contact us using the information in the **Contact Information** section below.

---

### Children’s Privacy

Cachely is not directed to children under the age of 13, and we do not knowingly collect personal data from children under 13.

Given the App’s design:

- The App does not create user accounts.
- The App does not request names, contact details, or other direct identifiers.
- The App does not transmit personal data to servers.

If you are a parent or guardian and you believe that a child under 13 has provided personal information to us (for example, via a support email), please contact us so that we can delete that information.

---

### Your Rights and Choices

Even though the App is designed to minimize data collection and to keep processing on‑device, you may have rights under data protection laws such as the EU General Data Protection Regulation (GDPR) and the California Consumer Privacy Act (CCPA), including:

- **Right of access (GDPR)** / **Right to know (CCPA)**:  
  To request information about whether we hold any personal data about you and, if so, what that data is.

- **Right to correction/rectification**:  
  To request correction of inaccurate personal data about you.

- **Right to deletion/erasure**:  
  To request deletion of personal data about you, subject to legal obligations.

- **Right to restriction and objection**:  
  To object to or request restriction of certain processing, where applicable.

- **Right to data portability (GDPR)**:  
  To receive a copy of certain personal data in a structured, commonly used, and machine‑readable format.

Because Cachely is intentionally built so that it does not collect or store personal data via the App itself, these rights may be most relevant in relation to information you have voluntarily provided, such as support emails. If you contact us to exercise your rights, we may need to verify your identity to protect your privacy and security.

To exercise any applicable rights, please contact us using the information in the **Contact Information** section below.

Residents of California may also have the right to:

- Request information about categories of personal information (if any) collected, disclosed, or sold in the preceding 12 months.
- Request deletion of certain personal information.
- Not be discriminated against for exercising their privacy rights.

At this time, based on the current implementation, Cachely does **not** sell personal information.

This Privacy Policy is consistent with the information disclosed in the Google Play "Data Safety" section for Cachely.

---

### Changes to This Privacy Policy

We may update this Privacy Policy from time to time. When we do, we will:

- Update the **Effective Date** at the top of this document; and
- Where required by applicable law, provide additional notice or obtain consent.

Your continued use of the App after any changes to this Privacy Policy becomes effective means that you accept the revised Policy. If you do not agree with the updated Policy, you should stop using the App and may uninstall it from your device.

---

### Contact Information

If you have any questions, concerns, or requests regarding this Privacy Policy or the App’s privacy practices, you can contact us at:

- **Email:** thealectronai@gmail.com

Please include sufficient information for us to understand your request. If you are making a privacy‑rights request, please indicate the country or state in which you reside so we can assess which laws may apply.

