+++
title = "How to Add Custom Domain For Your Github Page"
date = "2023-02-19T15:06:57-05:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = []
+++

### Step 1: Buy a custom domain you like. 

You could use services like Godaddy.

![setting](/images/20230219-how-to-add-custom-domain/godaddy.png)


### Step 2: Add DNS record for your custom domain

Add these 4 type A DNS record to point to github pages

![setting](/images/20230219-how-to-add-custom-domain/type-a-dns-record.png)

Then add this type CNAME DNS record to point to your github pages

![setting](/images/20230219-how-to-add-custom-domain/type-cname-dns-record.png)

Then wait for the DNS to propagate. It could take from minutes up to 24 hours to propagate.


### Step 3: Add custom domain in your Github Page repo

Go to settings and select Pages. Then type in your custom domain name and select Enforce HTTPS

![setting](/images/20230219-how-to-add-custom-domain/custom-domain.png)


### Summary

To add a custom domain to your github page is simple. You just need to
1. Buy a custom domain
2. Add DNS records for your custom domain
3. Add the custom domain in your github page settings.

Enjoy your new website domain!