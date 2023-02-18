+++
title = "Fast"
date = "2023-02-17T18:48:18-05:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = []
+++

Being fast is the key to build something new. If you have a startup idea, build it within a weekend time. If you have a feature to launch, build it within one day. If you want to learn a new language, learn the most basic 200 words within 2 weeks and start using them. If you want to build a personal website, build it within one hour. If you want to write a blog, finish it within 30 minutes. The longer you **plan** to do something, the more likely you will give up in the middle because of the mental pressure.

You might say "there is no way I can build a product within two days". The key to how to build fast is to limit the scope of the MVP. Before doing anything, keep asking yourself, what is really needed in order for it to work? Relentlessly remove all the unnecessary featurs until there is nothing more to remove. At this moment, if you remove anything, the product becomes unusable and broken.

There are proverbs like "Rome wasn't built in a day" or "慢工出细活" that seem to emphasize on the length of time in building something great. Both show lots of wisdom, but people misunderstand the meaning. As Naval Ravikant eloquently said, ["It’s not 10,000 hours, it’s 10,000 iterations."](https://twitter.com/naval/status/1594923336043069441?lang=en). The effort that perfects a product is not the length of the time, but the iterations: 
- Build the product MVP over the weekend and then have one iteration (e.g. new features) per day
- Write the blog draft in 30 mins and then iterate on it for another 5 times 
- Learn the basic knowledge of a language in 2 weeks, and start using it. Listen to music, watch movies, read articles in that language (iterations on learning the language)

That is why it's important to be "Fast". Being fast meaning you get the 1st interation done as quickly as possible so you can start the rest 9999 iterations.

&nbsp;

### Exercise: build a personal website within 1 hour
Example instructions that build this website are shown below

#### Install Hugo
```
brew install hugo
```

#### Create the site
```
cd /Users/xinyuwu/Workspace
hugo new site mysite
cd mysite
git init
git submodule add https://github.com/janraasch/hugo-bearblog themes/hugo-bearblog
echo "theme = 'hugo-bearblog'" >> config.toml
hugo server
```
Now [http://localhost:1313/](http://localhost:1313) should show your website locally

#### Using Github Page to host your website
First create two repo in your github accounts. One called yourgithubname.github.io to store the website. The other called yourgithubname.github.io.source the source code.
```
git remote add origin https://github.com/yourgithubname/yourgithubname.github.io.source.git
git add .
git commit -m "Initial commit"
git push origin master

hugo // this will generate website data in ./public folder
cd public
git remote add origin https://github.com/yourgithubname/yourgithubname.github.io.git
git add .
git commit -m "Initial commit"
git push origin master
```

#### Github repo setting 
Make sure the Build and Deployment in Github repo setting is like this
![setting](/images/github-build-and-deployment-setting.png)

Checkout [yourgithubname.github.io](yourgithubname.github.io) in browser and you should see your personal website!