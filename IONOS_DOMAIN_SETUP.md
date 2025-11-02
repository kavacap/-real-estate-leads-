# Connect Your IONOS Domain to Netlify - Step by Step

## Overview

You have your domain (www.webuyrealestateanycondition.com) registered with IONOS. This guide shows you how to connect it to your Netlify-hosted landing page in about 15 minutes.

---

## Step 1: Deploy Your Site to Netlify First

If you haven't done this yet, follow the QUICK_START.md guide to:
1. Create a GitHub account
2. Upload your landing page files
3. Deploy to Netlify

**You'll need your Netlify site name for the next steps.**

---

## Step 2: Get Your Netlify DNS Records

### In Netlify:

1. Log in to your Netlify account at https://app.netlify.com
2. Click on your site (real-estate-leads)
3. Go to **Site settings** (top menu)
4. Click **Domain management** (left sidebar)
5. Click **Add custom domain**
6. Type your domain: `webuyrealestateanycondition.com`
7. Click **Verify**
8. Click **Yes, add domain**

**Important:** Netlify will show you a message saying you need to update your DNS. It will display your **nameservers** (they look like `dns1.p01.nsone.net`, `dns2.p01.nsone.net`, etc.)

**Copy these nameservers - you'll need them in the next step.**

---

## Step 3: Update DNS Settings in IONOS

### In IONOS:

1. Go to https://www.ionos.com and log in to your account
2. Click **Domains** (in the left sidebar)
3. Find your domain: `webuyrealestateanycondition.com`
4. Click on it to open the domain settings
5. Look for **DNS** or **Nameservers** section
6. Click **Edit nameservers** or **Change DNS**

### Replace the Nameservers:

You'll see existing nameservers. **Delete them all** and replace with Netlify's nameservers:

**Netlify Nameservers (copy from your Netlify dashboard):**
- `dns1.p01.nsone.net`
- `dns2.p01.nsone.net`
- `dns3.p01.nsone.net`
- `dns4.p01.nsone.net`

(Your actual nameservers from Netlify might be slightly different - use the ones Netlify showed you)

### Steps in IONOS:

1. Delete all existing nameservers
2. Add the 4 Netlify nameservers one by one
3. Click **Save** or **Confirm**
4. You'll see a message saying changes are pending

---

## Step 4: Wait for DNS to Propagate

**This is the hardest part - you have to wait!**

DNS changes take **24-48 hours** to fully propagate. Here's what happens:

- **First 1-2 hours:** Changes start spreading across the internet
- **6-12 hours:** Most people can access your site
- **24-48 hours:** Fully propagated everywhere

### Check if it's working:

After a few hours, go to: https://www.webuyrealestateanycondition.com

If it doesn't work yet, wait a few more hours and try again.

### Speed up the process:

1. Clear your browser cache (Ctrl+Shift+Delete on Windows, Cmd+Shift+Delete on Mac)
2. Try in an incognito/private window
3. Try on your phone
4. Use a DNS checker: https://mxtoolbox.com/dnscheck

---

## Step 5: Verify It's Working

Once DNS propagates, you should see:

1. ✅ Your landing page loads at `www.webuyrealestateanycondition.com`
2. ✅ The URL shows your domain (not the Netlify temporary URL)
3. ✅ The form works and you can test it
4. ✅ HTTPS (green lock icon) appears in your browser

---

## Step 6: Set Up HTTPS (SSL Certificate)

Netlify automatically creates an HTTPS certificate for your domain. This happens automatically once DNS is set up.

**You don't need to do anything** - just wait for the green lock icon to appear.

---

## Troubleshooting

### "Domain not connecting after 48 hours"

1. **Check your nameservers in IONOS:**
   - Go back to IONOS domain settings
   - Verify you entered the Netlify nameservers correctly
   - Make sure there are no typos

2. **Check Netlify status:**
   - Log in to Netlify
   - Go to Domain management
   - Look for any error messages
   - Click "Check DNS configuration"

3. **Flush DNS cache:**
   - Windows: Open Command Prompt and type: `ipconfig /flushdns`
   - Mac: Open Terminal and type: `sudo dscacheutil -flushcache`

### "I see the old website, not my landing page"

1. Clear your browser cache completely
2. Try in an incognito/private window
3. Wait another 12-24 hours for full propagation
4. Try on a different device (phone, tablet)

### "HTTPS not working (no green lock)"

1. Wait up to 24 hours - Netlify needs time to issue the certificate
2. Hard refresh your browser (Ctrl+F5 or Cmd+Shift+R)
3. Check Netlify's domain settings for any error messages

---

## What Happens Next

Once your domain is connected:

1. **Your landing page is live** at www.webuyrealestateanycondition.com
2. **Form submissions work** - you'll get emails with leads
3. **You can start marketing** - share your domain on social media, directories, etc.
4. **Leads start coming in** - people can find you and submit their property info

---

## Quick Reference

| Step | What to Do | Where |
|------|-----------|-------|
| 1 | Deploy to Netlify | https://app.netlify.com |
| 2 | Add custom domain in Netlify | Site settings → Domain management |
| 3 | Copy Netlify nameservers | Netlify domain settings |
| 4 | Update nameservers in IONOS | https://www.ionos.com → Domains |
| 5 | Wait 24-48 hours | Patience! |
| 6 | Test your domain | Visit www.webuyrealestateanycondition.com |

---

## Need Help?

If something goes wrong:

1. **Check the DEPLOYMENT_GUIDE.md** for more detailed instructions
2. **Contact Netlify support:** https://support.netlify.com
3. **Contact IONOS support:** https://www.ionos.com/help
4. **Use DNS checker:** https://mxtoolbox.com/dnscheck to diagnose issues

---

## You're Almost There!

Once your domain is connected, you'll have a professional, free-hosted landing page collecting real estate leads. The hardest part is done - now it's just waiting for DNS to propagate and then marketing your site to get leads!
