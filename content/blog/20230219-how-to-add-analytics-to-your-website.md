+++
title = "How to Add Analytics to Your Website"
date = "2023-02-19T16:17:42-05:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = []
+++

After you have your personal website ready, you might wonder how many people have visited your website and where they are. Here are the steps you need to add analytics to your website.

### Step 1: Setup Google Analytics

1. Create an account at [google analytics](https://analytics.google.com)
2. Go to Admin -> Property -> Property Settings to create a property
3. Go to Admin -> Property -> Data Streams to create a stream

You will get a Google Tracking Code that looks like "G-XXXXXXXXXX"


### Step 2: Add Google Tracking Code to Your Website

If you are using Hugo, it's simple. 

1. Open config.toml, add the follow code
```
[params.analytics]
  measurement_id = "G-649QMBQG52"
```

2. Copy your Hugo Theme's layouts/partials/header.html to your project's layouts/partials/header.html and add the following code
```
{{ with .Site.Params.analytics.measurement_id }}
  <script async src="https://www.googletagmanager.com/gtag/js?id={{ . }}"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag() {dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', '{{ . }}');
  </script>
{{ end }}
```

3. Generate new website using command `hugo` and commit your change to remote repo

### Step 3: Test

Now if you visit your website, you should be able to see it in your google analytic's home page:
![setting](/images/20230219-how-to-add-analytics-to-your-website/google.png)

Now we see the visit in the dashboard! Good job!

One caveat: if you are using any kind of adblocker, it may prevent google tracking code from working properly. Try disable the adblocker and test again.

Enjoy the analytics for your website!


