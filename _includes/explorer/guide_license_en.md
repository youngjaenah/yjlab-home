# Explorer Pro License Guide

Explorer Pro is a **one-time purchase ($19 USD; ₩25,000 in Korea, VAT included) with a perpetual license**. There's no subscription and no account to create. When you buy, you get a small **license file** (`.explorerlicense`); import it into the app once and Pro is unlocked.

You don't have to buy Pro to keep using Explorer: the free version keeps every feature it has today. To see what Pro adds, read [Explorer Pro features](/explorer/guide/pro/?lang=en).

## 1. Buying Pro

1. Click the buy button on the [Explorer Pro page](/explorer/#pro). From inside the app, you can also choose **Help ▸ Upgrade to Explorer Pro…** or **Explorer ▸ Settings… ▸ Explorer Pro ▸ Upgrade to Pro**.
2. The checkout opens in your browser. Payment is handled by **Paddle**, our Merchant of Record. You can pay by card, and in Korea also with Naver Pay or Kakao Pay. Nothing is ever paid inside the app.
3. When the payment is complete, your **license file** (`Explorer-Pro.explorerlicense`) **downloads right away**, usually to your Downloads folder.
4. A copy is also emailed to you from **license@yjlab.io** with the subject "Your Explorer Pro license". Keep that email; it's the easiest backup.

If you're on the free version and use a Pro feature, Explorer shows a single message: "**… is an Explorer Pro feature.**" Click **Upgrade to Pro…** to open the purchase page, or **Import License…** to import a license you already have. **Cancel** does nothing.

**Bought before November 24, 2026?** Those purchases were made through Lemon Squeezy, and your purchase email has a **license key** (`XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX`) instead of a file. It keeps working; section 2 explains how to turn it into a license file.

## 2. Getting your license file again

You can get your license file again **any time, as many times as you need**, from the [license page](/explorer/activate.html). Getting it again doesn't use anything up.

**By email (any purchase)**

1. Open the [license page](/explorer/activate.html).
2. Under **Email me my license**, enter the email address you purchased with and click **Email my license**.
3. Within a few minutes, the license file arrives at that address. Check your spam folder too.

For your security, the file is only ever sent to the address on the purchase, and the page shows the same message whether or not it found a purchase. If nothing arrives, try the other email addresses you might have used, or contact us (section 6).

**With a license key (Lemon Squeezy purchases)**

1. Open the [license page](/explorer/activate.html).
2. Under **Have a license key?**, paste the key from your purchase email and click **Get license file**.
3. `Explorer-Pro.explorerlicense` is downloaded right away.

If the license page shows an error:

- **That key wasn't recognized.** — The key may have been mistyped. Copy it from your purchase email again.
- **This key has been deactivated** — The key was turned off, for example after a refund.
- **Too many attempts.** / **Too many requests.** — Too many requests in a short time. Wait a while and try again.
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

The file is damaged, only part of it was pasted, or it isn't an Explorer Pro license. Get your license file again from the [license page](/explorer/activate.html) (section 2) and import it. If you already had a license activated, it is left unchanged.

## 4. Using Pro on more than one Mac

A Pro license is granted to **one person, the purchaser**, who can use it on **any number of Macs** they own or use, for both personal and work use. See section 4 of the [Terms of Service](/explorer/terms/?lang=en) for details.

To use Pro on another Mac, import the same license file there, as described in section 3. The license isn't tied to a particular device.

Sharing your license file or key with other people isn't allowed. If several people use Pro, each person needs their own license.

## 5. Moving to a new Mac or reinstalling

- **Updating or reinstalling the app**: the license is stored on your Mac separately from the app, so you don't need to import it again.
- **Moving to a new Mac**: install Explorer on the new Mac, then double-click your license file or import it with **Import License…**.
- **Can't find the license file?** Look for the license email, or get the file again from the [license page](/explorer/activate.html) (section 2).

Keeping a copy of the license file in cloud storage or your password manager makes this even easier next time.

## 6. If you can't find your license

1. Search your inbox for the email from **license@yjlab.io** ("Your Explorer Pro license"). For Lemon Squeezy purchases, look for the purchase confirmation from **Lemon Squeezy**, which has your license key.
2. Or use **Email me my license** on the [license page](/explorer/activate.html) with the email address you purchased with (section 2). This works for both Paddle and Lemon Squeezy purchases.
3. Still stuck, for example because you no longer use that email address? Email support@yjlab.io with your **order number or the email address you purchased with**. Once we confirm the purchase, we'll send you your license file.

## 7. Removing the license

1. Choose **Explorer ▸ Settings…**.
2. In the **Explorer Pro** section, click **Remove License**.

The license is removed right away, without a confirmation, and Pro features turn off immediately. All free features keep working. To turn Pro back on later, just import your license file again.

## 8. Refunds

**Within 14 days of purchase**, we give a full refund, no questions asked. See the [Refund Policy](/explorer/refund/?lang=en) for how to request one and what qualifies.

Once a refund is complete, the license can no longer be downloaded or re-sent (for Lemon Squeezy purchases, the license key is deactivated), and the right to use the license ends. Please remove the license as described in section 7.

## 9. Offline use and privacy

- **The app never contacts a server to check your license.** The license file carries an Ed25519 digital signature, which the app verifies on your Mac against a public key built into the app. Pro keeps working without an internet connection.
- **It never expires.** The license check doesn't use the system clock, so changing the date or staying offline for a long time won't lock you out.
- **No server dependency.** Even if distribution of the app ever stops, Pro features you've activated keep working in that version of the app.
- **What's in the license file**: only the name, email address, and order number from your purchase, and it is stored only on your Mac.
- You need the internet only to pay and to get your license file (the download, the email, or the [license page](/explorer/activate.html)), and all of that happens in your browser or inbox, not in the app.
- The license server checks your purchase with the payment provider and doesn't keep your personal information. To email the license file, your email address is passed to our email delivery provider, and for re-send requests the address is kept for up to one hour to prevent abuse.

For details, see the [Privacy Policy](/explorer/privacy/?lang=en).

## 10. Learn more

- [Getting started](/explorer/guide/getting-started/?lang=en) · [Explorer Pro features](/explorer/guide/pro/?lang=en) · [Keyboard shortcuts](/explorer/guide/shortcuts/?lang=en) · [FAQ](/explorer/guide/faq/?lang=en)
- [Terms of Service](/explorer/terms/?lang=en) · [Refund Policy](/explorer/refund/?lang=en) · [Privacy Policy](/explorer/privacy/?lang=en)
- Contact: support@yjlab.io
