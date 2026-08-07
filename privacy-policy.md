
# Privacy Policy

**Last updated:** August 4, 2026

This policy explains what data NutriCore collects and why, how that data is handled, and your rights regarding it. We never sell your data.

This policy is split into sections:

- What we collect and why
- When we access or disclose your information
- Your rights with respect to your information
- How we secure your data
- What happens when you delete content or your account
- Data retention
- Location of infrastructure and data
- Changes and questions

This policy applies to NutriCore, a fitness and nutrition tracking app built and maintained by the NutriCore team ("we," "us," "our"). It applies to our handling of information about app users ("you") across the NutriCore mobile app and any associated web or backend services.

---

## What we collect and why

Our guiding principle is to collect only what we need to make NutriCore work.

### Identity and access

When you register for NutriCore, we collect your email address and password (stored as a salted BCrypt hash, never in plaintext). We use a verification step before your account is created — an unverified signup is held temporarily and only becomes a real account once you confirm your email. We use your email to authenticate you (via JWT-based sessions), send account-related notices, and, where you opt in, product updates.

### Health, fitness, and nutrition data

This is the core data NutriCore works with, and we treat it as sensitive:

- **Body metrics and weight logs** you enter, used to show your progress over time and to power calorie/macro calculations.
- **Nutrition data**: foods you log, portion sizes, and nutrient breakdowns (sourced against our USDA-derived food database).
- **Workout data**: exercises performed, sets/reps/weight, and your weekly workout schedule, used to estimate calories burned (including post-exercise afterburn) and to show training history. Exercise names, instructions, and illustrative images shown in the app come from the [free-exercise-db](https://github.com/yuhonas/free-exercise-db) dataset, which is released under the Unlicense (public domain) — this is third-party reference content displayed in the app, not data collected from you.
- **Step and activity data**: if you grant permission, we read step counts via Android Health Connect (or a device pedometer as a fallback) to estimate daily activity.
- **Chat messages** you send to the in-app AI nutrition/fitness assistant, and the assistant's responses, so you can see your conversation history.

We use this data to run the core functionality of the app: tracking, recommendations, and your AI chat history. We do not use your health data for advertising targeting.

### AI processing of your data

To power the AI assistant and food recognition, parts of your data are sent to third-party AI infrastructure we use as processors:

- Chat messages and relevant context (e.g., your recent logs) are sent to Groq, our AI inference provider, to generate responses.
- Your nutrition queries may be matched against a knowledge base of food data using vector search (retrieval-augmented generation) to ground the assistant's answers in accurate nutrition facts.

These providers process this data on our behalf to deliver the feature; they do not use it to train their own models except as disclosed in their own terms, and we choose providers that commit to not using submitted data for model training where possible.

### Advertising

If you use the free tier, NutriCore may show ads via Google AdMob, including rewarded ads (which unlock in-app perks) and interstitial ads. To verify rewarded ads, ad-completion signals are validated server-side (server-side verification), which involves your device and Google's ad servers exchanging a signed callback with us — this is used only to confirm ad completion and prevent reward fraud, not to build an advertising profile of you beyond what AdMob itself does. AdMob may set identifiers and collect device information under Google's own privacy policy; where required, we request your consent before showing personalized ads.

### Device and log data

We log IP address and basic device/request metadata for security, fraud prevention, and diagnosing crashes. We keep this for as long as your account is active.

### Voluntary correspondence

If you email us for support, we keep that correspondence, including your email address, so we have a history to reference if you reach out again.

### App permissions

NutriCore may request permission for Health Connect (steps/activity) and notifications. Each is optional — the app remains usable without it, though related features (like automatic step tracking) won't work without the relevant permission.

---

## When we access or disclose your information

**To provide the service.** We use third-party subprocessors to run the app, including:

- Cloud hosting and database infrastructure for storing your account and log data.
- **Railway** for hosting and our MySQL database.
- **Groq** for AI inference powering the chat assistant.
- **ChromaDB** for vector search / nutrition knowledge retrieval (RAG).
- **Google AdMob** for advertising.

**No human reviews your content** except in limited cases — for example, investigating a bug that broke your data, or a support request you've raised — and only to the extent needed to resolve it.

**To investigate abuse.** If we discover the app is being used for a purpose that violates our terms (e.g., abuse of the rewarded-ad system, credential stuffing), we may access relevant account data as a last resort to investigate and take action.

**Aggregated and de-identified data.** We may aggregate or de-identify usage data (e.g., "average calories logged per user") for product analytics or improvement. This is never sold.

**When required by law.** We do not respond to law enforcement requests for user data unless legally compelled (e.g., valid warrant, subpoena, or court order). Where legally permitted, we will notify you before disclosing your data.

**If NutriCore is acquired or changes ownership,** we will notify you before your personal data is transferred or becomes subject to a different privacy policy.

---

## Your rights with respect to your information

Regardless of where you're located, you generally have the right to:

- **Know** what personal information we collect and why (this policy).
- **Access** the personal information we hold about you.
- **Correct** inaccurate personal information.
- **Delete** your personal information, subject to certain limits (e.g., data we must retain for legal/billing reasons). Deleting certain data may mean parts of the app stop working, and full deletion may require closing your account.
- **Restrict or object** to certain processing of your data.
- **Export** your data (your logged foods, workouts, weight history, and chat history) in a portable format.
- **Not be discriminated against** for exercising these rights — we won't charge you more or degrade your service because you did.

To exercise these rights, contact us at **nutricoreapp1@gmail.com**. We may need to verify your identity (at minimum, your account email) before acting on a request.

---

## How we secure your data

- Data in transit is encrypted via TLS between your device and our servers.
- Passwords are stored as salted hashes, never in plaintext.
- Access to production data and infrastructure is restricted to what's needed to operate and support the app.
- Database backups are stored securely.

No system is perfectly secure, and we continue to invest in hardening our infrastructure as NutriCore grows (e.g., moving from ad hoc schema management to versioned database migrations, tightening service-to-service access).

---

## What happens when you delete content or your account

If you delete a specific log entry (a food, workout, or weight entry), it is permanently deleted from our database immediately upon request.

If you delete your account, your account and all associated personal data (profile, logs, chat history) are permanently deleted from our database immediately upon request.

---

## Data retention

We keep your information for as long as your account is active and as needed to provide the service. After account deletion, we retain only what's legally required (e.g., billing records for tax purposes) for the minimum period the law requires, then delete it.

---

## Location of infrastructure and data

NutriCore's backend infrastructure is hosted with third-party cloud providers. If you are located outside the country where our infrastructure is hosted, your information will be transferred to and processed in that location. By using the app, you consent to this transfer.

---

## Changes and questions

We may update this policy as the app evolves and to comply with applicable law. If we make significant changes, we'll update the date at the top of this page and, where required, notify you in-app or by email.

Questions, comments, or concerns about this policy or your data? Contact us at **nutricoreapp1@gmail.com**.

---

**Notes for Omer (remove before publishing):**
- "Immediate" deletion above assumes you're not running scheduled DB backups/snapshots on Railway. If you turn those on later, add a line noting backups are purged on Railway's rotation schedule (check Railway's retention period and update this doc).
- No registered company/LLC yet, so this doc refers to "the NutriCore team" instead of a legal entity name — deliberate, since claiming an unregistered name as a company could misrepresent your legal structure. If/when you incorporate, swap this for the real entity name. Until then, your Google Play/Apple developer account name is the actual legally responsible party — worth checking that matches what you'd want visible if this ever gets scrutinized.
- Draft only, not legal advice — worth a lawyer's pass before shipping, especially if you pick up EU/California users (GDPR/CCPA add specific disclosure requirements around AI processing of health data).
- 
