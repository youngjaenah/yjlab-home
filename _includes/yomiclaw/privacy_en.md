# YomiClaw Privacy Policy

**Effective date: 2026-06-01**
**Last updated: 2026-06-01**

YomiClaw (the "App") respects your privacy and complies with the Korean Personal Information Protection Act and other applicable laws. This policy describes how the App collects, uses, and stores user information.

---

## 1. Information We Collect

The App **does not require any account registration and does not transmit or store your personal information on any server.** The following information is processed solely on your device and is not sent externally.

| Item | Processing | Purpose |
|---|---|---|
| Microphone input (voice) | Processed in real time, not stored | Voice translation |
| Speech recognition result (text) | Stored locally via SwiftData on your device | Display conversation history |
| Location information | Used only on device, not stored | Recommend translation presets matching your current place |
| Camera image | Processed in real time, not stored | Text recognition on menus, signs, etc. |
| Translation result (text) | Stored locally via SwiftData on your device | Display conversation history |
| User settings (language, voice, etc.) | Stored locally via UserDefaults | Maintain user preferences |

---

## 2. External Communications

The App performs network communication only in the following cases. Your voice, text, and image inputs are **not** transmitted.

- **Language model download** — On first launch or when a model update is required, AI language model files used for translation and response suggestions are downloaded from Hugging Face Hub (`huggingface.co`). Downloaded models are stored on the device and operate offline thereafter.
- **Apple Translation language pack download** — On first use, the App downloads Apple's translation language packs (system feature).
- **Apple Speech Recognition** — The App uses iOS system speech recognition (`SFSpeechRecognizer`). When the device supports on-device recognition for the selected language, the App sets **`requiresOnDeviceRecognition = true`** so that voice data is processed only on the device and is not sent to Apple's servers. In the rare case that the device or OS version does not support on-device recognition for the selected language, recognition may fall back to server-based processing according to Apple's [Speech Recognition and Privacy](https://support.apple.com/HT210657) policy. Even in that case, the App operator has no access to that data.

The App does not use any analytics SDK, advertising SDK, or crash reporting SDK.

---

## 3. Data Retention and Deletion

- All conversation history and settings are **stored only on the user's device**; the operator has no access.
- Users can delete conversation history at any time via the "Trash" feature within the App.
- Uninstalling the App removes all locally stored data (conversation history, settings, downloaded model files).

---

## 4. Third-Party Disclosure and Processing

The App does not share user information with any third party or outsource its processing. However, the system features listed in Section 2 (Apple Speech Recognition, Apple Translation, Hugging Face Hub) are subject to each provider's own policy.

---

## 5. Your Rights

You may exercise the following rights at any time via the App settings or iOS system settings:

- Revoke camera, microphone, speech recognition, or location permissions (iOS Settings → YomiClaw)
- Delete all conversation history (Trash in App)
- Remove all local data by uninstalling the App

---

## 6. Children Under 14

The App does not separately collect personal information from children under 14. All data processing occurs on the device.

---

## 7. Privacy Officer and Contact

For inquiries, complaints, or correction/deletion requests regarding the processing of personal information, please contact:

- **Privacy Officer**: 나영재 (Youngjae Nah)
- **Email**: support@yjlab.io

---

## 8. Changes to This Policy

If the contents of this policy are added, removed, or modified, the changes will be announced via the App or website at least 7 days before the effective date. For material changes (such as the addition of collected items), at least 30 days' notice will be provided.

---

## 9. Remedies for Rights Infringement

For any privacy-related concerns or complaints, please first contact the Operator at **support@yjlab.io**. You may also contact the data protection authority in your jurisdiction to file a report or seek further assistance.
