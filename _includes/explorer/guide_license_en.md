# Explorer Pro License Guide

Explorer Pro is a **one-time purchase ($19 USD) with a perpetual license**. There's no subscription and no account to create. When you buy, you get a small **license file** (`.explorerlicense`); import it into the app once and Pro is unlocked.

You don't have to buy Pro to keep using Explorer: the free version keeps every feature it has today. To see what Pro adds, read [Explorer Pro features](/explorer/guide/pro/?lang=en).

## 1. Buying Pro

1. Click the buy button on the [Explorer Pro page](/explorer/#pro). From inside the app, you can also choose **Help ▸ Upgrade to Explorer Pro…** or **Explorer ▸ Settings… ▸ Explorer Pro ▸ Upgrade to Pro**.
2. The checkout opens in your browser. Payment is handled by **Lemon Squeezy**, our Merchant of Record. Nothing is ever paid inside the app.
3. When the payment is complete, your **license key** is sent in your purchase confirmation email. <!-- TODO 확인: Lemon Squeezy 구매 확인 이메일에 라이선스 키가 포함되는지 실제 주문으로 확인 -->

A license key looks like `XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX`. You'll need it if you ever download your license file again, so keep that email.

If you're on the free version and use a Pro feature, Explorer shows a single message: "**… is an Explorer Pro feature.**" Click **Upgrade to Pro…** to open the purchase page, or **Import License…** to import a license you already have. **Cancel** does nothing.

## 2. Getting your license file

This step turns your license key into a license file.

1. Open the [license activation page](/explorer/activate.html).
2. Paste the key from your purchase email into **License key** and click **Get license file**.
3. `Explorer-Pro.explorerlicense` is downloaded (usually to your Downloads folder).

You can download it again **any time, as many times as you need**, with the same key. Downloading again doesn't use anything up.

If the activation page shows an error:

- **That key wasn't recognized.** — The key may have been mistyped. Copy it from your purchase email again.
- **This key has been deactivated** — The key was turned off, for example after a refund.
- **Too many attempts.** — Too many requests in a short time. Wait about a minute and try again.
- **The license service is temporarily unavailable.** — Try again shortly.

## 3. Activating Pro in the app

Use whichever method is easiest. They all do the same thing.

**Option A — Double-click the file (easiest)**

1. Double-click the downloaded `Explorer-Pro.explorerlicense` file.
2. Explorer opens and shows **Explorer Pro Unlocked**, licensed to your name and email.

**Option B — Import from Settings**

1. Choose **Explorer ▸ Settings…** (⌘,).
2. In the **Explorer Pro** section at the bottom, click **Import License…**.
3. Select your license file.

You can also drag the license file onto the **Explorer Pro** section. To paste instead of using the file, paste its contents into **Or paste your license here** and press Return. The license file is plain text, so you can paste it straight from an email, for example.

Once activated, the section's **Status** changes from **Free** to **Licensed to (name) (email)**. You don't need to restart the app.

**If you see "Not a Valid License"**

The file is damaged, only part of it was pasted, or it isn't an Explorer Pro license. Download your license file again from the [activation page](/explorer/activate.html) and import it. If you already had a license activated, it is left unchanged.

## 4. Using Pro on more than one Mac

A Pro license is granted to **one person, the purchaser**, who can use it on **any number of Macs** they own or use, for both personal and work use. See section 4 of the [Terms of Service](/explorer/terms/?lang=en) for details.

To use Pro on another Mac, import the same license file there, as described in section 3. The license isn't tied to a particular device.

Sharing your license file or key with other people isn't allowed. If several people use Pro, each person needs their own license.

## 5. Moving to a new Mac or reinstalling

- **Updating or reinstalling the app**: the license is stored on your Mac separately from the app, so you usually don't need to import it again. <!-- TODO 확인: 앱 삭제 후 재설치 시 ~/Library/Application Support/io.yjlab.Explorer/license 유지되어 Pro 상태가 복원되는지 실제 확인 -->
- **Moving to a new Mac**: install Explorer on the new Mac, then double-click your license file or import it with **Import License…**.
- **Can't find the license file?** Download it again from the [activation page](/explorer/activate.html) with the same license key.

Keeping a copy of the license file in cloud storage or your password manager makes this even easier next time.

## 6. If you lose your license key

1. Search the inbox you bought with for the purchase confirmation email from **Lemon Squeezy**.
2. You can also find the key on your Lemon Squeezy order page. <!-- TODO 확인: Lemon Squeezy 구매자용 주문 페이지(My Orders)에서 라이선스 키가 표시되는지와 그 URL -->
3. Still can't find it? Email support@yjlab.io with your **order number or the email address you purchased with**. Once we confirm the purchase, we'll send you your license file.

## 7. Removing the license

1. Choose **Explorer ▸ Settings…**.
2. In the **Explorer Pro** section, click **Remove License**.

The license is removed right away, without a confirmation, and Pro features turn off immediately. All free features keep working. To turn Pro back on later, just import your license file again.

## 8. Refunds

**Within 14 days of purchase**, we give a full refund, no questions asked. See the [Refund Policy](/explorer/refund/?lang=en) for how to request one and what qualifies.

Once a refund is complete, the license key is deactivated, the license file can no longer be downloaded, and the right to use the license ends. Please remove the license as described in section 7.

## 9. Offline use and privacy

- **The app never contacts a server to check your license.** The license file carries an Ed25519 digital signature, which the app verifies on your Mac against a public key built into the app. Pro keeps working without an internet connection.
- **It never expires.** The license check doesn't use the system clock, so changing the date or staying offline for a long time won't lock you out.
- **No server dependency.** Even if distribution of the app ever stops, Pro features you've activated keep working in that version of the app.
- **What's in the license file**: only the name, email address, and order number from your purchase, and it is stored only on your Mac.
- You need the internet only to pay and to download your license file from the [activation page](/explorer/activate.html), and both happen in your browser, not in the app. The license server checks your key and doesn't store any personal information.

For details, see the [Privacy Policy](/explorer/privacy/?lang=en).

## 10. Learn more

- [Getting started](/explorer/guide/getting-started/?lang=en) · [Explorer Pro features](/explorer/guide/pro/?lang=en) · [Keyboard shortcuts](/explorer/guide/shortcuts/?lang=en) · [FAQ](/explorer/guide/faq/?lang=en)
- [Terms of Service](/explorer/terms/?lang=en) · [Refund Policy](/explorer/refund/?lang=en) · [Privacy Policy](/explorer/privacy/?lang=en)
- Contact: support@yjlab.io
