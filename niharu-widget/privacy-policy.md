# Privacy Policy — NiHaru Widget for Android

*An app by Niharu* · Last updated: October 3, 2026

🇦🇷 [Leer esta política en español](politica-de-privacidad.md)

## 1. Scope of this policy

This policy applies **only to the NiHaru widget for Android** (package `app.niharu.widget`), a companion app with no launcher icon that shows a Japanese word or kanji on your home screen.

The widget **does not use your NiHaru account** or any login. If you use the website [niharuapp.com](https://niharuapp.com), that experience is governed by its own privacy policy on the site.

## 2. Who is responsible

- **Data controller:** Santiago Agustín Playa, developer and owner of NiHaru.
- **Legal address:** Autonomous City of Buenos Aires, Argentina. The full address is available upon request of the supervisory authority.
- **Contact:** hola@niharuapp.com

## 3. Data we collect

| Data | Purpose | Where it lives |
|------|---------|----------------|
| **Device hash**: a SHA-256 fingerprint of your `ANDROID_ID`, computed on your phone. The raw `ANDROID_ID` never leaves your device | Prevent abuse and block installations that harm the service | Server and device |
| **Hash of your IP address** (HMAC-SHA256 with a server-side secret key). The raw IP is not stored | Apply usage limits and abuse blocks | Server |
| **Installation key (`widgetKey`)**: a random identifier (UUID) issued by the server the first time you use the widget | Identify your installation anonymously on each content request | Server and device |
| **Last activity**: the date and time of your most recent content request (a single value that is overwritten, with no history) | Detect inactive or abusive installations | Server |
| **Filters you choose** (JLPT level, word type, frequency, category) | Return matching content. They are sent with each request but **not stored** on the server | Your device only |
| **Visual settings and last content shown** (mode, visible fields, color, opacity, refresh interval) | Make the widget look and behave as you configured it | Your device only |

In addition, while processing each request the server temporarily sees your IP address, like any web server. It uses it for in-memory usage limits and does not record it in its application logs.

## 4. Data we do NOT collect

- Location, contacts, device accounts, advertising ID, or the app or operating system version.
- Name, email, password, or any NiHaru account data.
- Analytics or telemetry: the widget has no analytics or crash-reporting SDK, and your taps, refresh counts, and errors are not logged.
- Study history: the server does not store which words or kanji it showed you.

The widget only declares the Android permissions `INTERNET` and `ACCESS_NETWORK_STATE`.

## 5. How we use the data

Only to (a) deliver the widget's content and (b) protect the service against abuse (usage limits and blocks). **We do not sell or share your data, run advertising, or build profiles.**

## 6. Where data is stored and who processes it

Server data is stored in a PostgreSQL database hosted on **Railway**. Database backups are stored encrypted on **Cloudflare R2** and retained for 14 days. These providers act as infrastructure processors and may process data outside Argentina.

The widget communicates with the server over HTTPS only (`api.niharuapp.com`).

## 7. How long we keep data

Your installation data is kept while the widget remains in use. Uninstalling the widget stops all further requests to the server. Data that lives only on your device is deleted when you uninstall the app.

## 8. Android backups

The app allows Android's automatic backup. This means the installation key and device hash may be included in your Google account backup, which is governed by Google's policies, not this one.

## 9. Your rights

As a data subject under Argentina's Personal Data Protection Law No. 25,326, you have the right to **access, correct, and delete** your data. Because the widget is anonymous, we need your installation key to locate your installation; if you don't have it, write to us anyway and we'll work out how to help.

You can exercise these rights by writing to **hola@niharuapp.com**.

Argentina's **Agency for Access to Public Information (AAIP)**, as the supervisory authority of Law No. 25,326, is empowered to handle complaints from anyone whose rights are affected by non-compliance with the personal data protection rules in force.

## 10. Children

The widget is not directed at children under 13 and does not ask for or collect age or personally identifying information.

## 11. Changes to this policy

If we change this policy, we will publish the new version at this same location and update the date above. The full change history is available in this repository's history.

## 12. Contact

Questions about this policy? Write to **hola@niharuapp.com**.
