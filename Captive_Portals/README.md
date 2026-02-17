# FortiGate Captive Portal Pages (Custom HTML)

This folder contains **custom captive portal pages** you can use on a **FortiGate** (often paired with **FortiAP**) to build a clean, branded guest Wi-Fi experience.

These templates are designed to be **copy/paste ready** into FortiGate **Replacement Messages** so you can quickly deploy:

- Disclaimer-only portals  
- Guest user authentication portals  
- Email collection portals  
- Matching “failed/declined/invalid” pages

---

## What’s Included

Depending on what you pulled from this repo, you’ll typically see pages like:

- **Disclaimer Page** (Terms + Accept/Decline)  
- **Disclaimer Declined Page** (simple “access denied” + return button)  
- **Guest Authentication Page** (username/password login)  
- **Authentication Failed Page** (error + retry login)  
- **Email Collection Page** (collect email before granting access)  
- **Email Invalid Page** (invalid email error + retry)  

---

## How to Install on FortiGate (GUI)

1. In the FortiGate GUI, go to:  
   **System → Replacement Messages Groups**
   Note: You must enable this in feature visibility

3. Locate the **Captive Portal** section (or the relevant page type you’re editing).

4. Open the page you want to replace and set:  
   **Message Format:** `text/html`

5. Copy the HTML from this repo and **paste** it into the editor.

6. Click **Save**.

7. Test by connecting a client to the guest SSID and triggering the captive portal.

> Tip: If the portal doesn’t pop automatically, open a browser and visit an HTTP site like `neverssl.com` to trigger the redirect.

## Branding / Logo Image (Important)

These templates reference an uploaded image named **demo** using FortiGate’s image token. Example:

    background: url(%%IMAGE:demo%%) no-repeat center center;

### Uploading images on FortiGate

Upload your logo/background image here:

**System → Replacement Messages → Manage Images**

### Image requirements (FortiGate)

- Supported types: **JPEG, PNG, GIF, TIFF**
- Maximum image size: **32 KiB**

### Using your own image

You have two options:

**Option A (recommended):**
- Upload your image and name it **demo** to match the templates.

**Option B:**
- Upload your image with a different name (example: **company_logo**)
- Update the HTML anywhere you see:

    %%IMAGE:demo%%

Replace it with your image name:

    %%IMAGE:company_logo%%


---

## Notes / Best Practices

- Keep images **small** (32 KiB max). Resize/compress if needed before uploading.
- Adjust disclaimer wording to match your organization’s policy/legal requirements.
- Test with multiple client types:
  - **Phone** (usually best captive portal detection)
  - **Laptop** (may require opening a browser manually)
- If the portal doesn’t pop automatically, open a browser and visit an HTTP site like `neverssl.com` to trigger the redirect.

---

## Disclaimer

These templates are provided **as-is**. Review and customize the text for your organization’s security and legal requirements.






