# 🌩️ Cloudflare Rules – Protect Your Site from DDoS Attacks

![Cloudflare Banner](https://imgs.search.brave.com/vMssRmSQL8CxVIYYu6fluUEdgYemos7Kx5djNyAncas/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9ib290/ZmxhcmUuY29tL3dw/LWNvbnRlbnQvdXBs/b2Fkcy8yMDIzLzAz/L0Nsb3VkZmxhcmUt/TG9nby5wbmc)

This guide shows you how to set up **Cloudflare Firewall Rules** to protect your website from **DDoS attacks**, bad bots, and other malicious traffic.  
All examples work with the **Free Plan** of Cloudflare.

---

## 📌 What You’ll Learn

- How to create Cloudflare **Firewall Rules**
- How to block traffic based on **country**, **IP**, or **URI**
- **Rate limiting** and bot protection
- Best practices for **security and performance**

---

## 🛠️ Setup Guide

### Step 1: Open Your Domain Settings

1. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Choose your domain
3. Follow all the Steps below

![Cloudflare Firewall UI](https://imgur.com/a/dn3qDxs)

1. Head over to Security
2. Click on "Security rules"
3. Click on "Create Custom Rule"
4. Make this your FIRST CloudFlare expression: (ip.src.continent in {"AF" "AN" "AS" "NA" "OC" "T1" "SA"}) use Action BLOCK
5. Make this the Second Cloudflare expression: (http.request.method in {"PUT" "HEAD" "OPTIONS" "DELETE" "PATCH" "PURGE"}) use Action BLOCK
6. Make this the third Cloudflare expression: (http.request.version in {"HTTP/1.0" "HTTP/1.1" "HTTP/1.2" "HTTP/2"}) use Action JS OR BLOCK ( i use BLOCK as i dont allow Unsafe HTTP Protocols. )

At the Last step, Click on "Launch Zero-Trust"

## Your Site should now be fully Protected against DDoS Attacks. If you need further help, dont hesitate to DM me on Discord: 36lw / ID: 186672191218253825
Thanks for reading this and i hope i could help you <3
