# Contact Form Setup Guide

## Current Issue
Your contact form currently uses a `mailto:` link which:
- Requires visitors to have an email client installed
- Messages may not send if they close the window
- You won't receive messages reliably

## Simple Solution: Use Formspree (Free & Easy!)

### Step 1: Sign up for Formspree
1. Go to https://formspree.io/
2. Sign up for a free account
3. Click "New Form"
4. Enter your email: **li848509@gmail.com**
5. You'll get a Form ID like: `xyzabc123`

### Step 2: Update Your HTML
Open `index.html` and find this line (around line 1092):
```html
<form class="contact-form" id="contact-form">
```

Replace it with:
```html
<form class="contact-form" id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
(Replace `YOUR_FORM_ID` with the ID you got from Formspree)

### Step 3: Test!
1. Refresh your portfolio
2. Fill out the contact form
3. Click "Send Message"
4. Check your email - you should receive the message!

## Alternative: Use EmailJS (More features, still free)

If you want more control, use EmailJS:
1. Go to https://www.emailjs.com/
2. Sign up for free
3. Create an email service
4. Create an email template
5. Get your Service ID, Template ID, and Public Key

Then I can help you integrate it with JavaScript!

## Quick mailto: Fix (Temporary)

Your current form opens the user's email client. While not ideal, it works if you just want to make sure the email is correct.

The current implementation is in `script.js` lines 150-169.

---

**Recommendation**: Use Formspree - it's the easiest and most reliable solution!

Let me know which option you'd like to implement and I'll help you set it up! 🚀
