---
author: "Saintmalik"
date: 2020-12-18
slug: "how-i-found-my-first-bug"
title: Stored XSS on Private Bounty Program (My First Bug)
cover: "../images/bypassauth.png"
tags: ['websec', 'infosec']
type:
- post
- posts
title: Stored XSS on Private Bounty Program (My First Bug)
description: "How i go my first bug and i was paid $$$ bounty"
weight: 10
series: 
- Web AppSec
---

So I started to participate in bug bounty programs not so long before, and soon later I found at least 2 places are vulnerable for stored XSS on quite a big educational platform which i was using for learnig web development last year.

They have many users and also have some big banks and firms being as their partner, the website helps users to learn how to code.

The website’s dashboard enables users to submit their details and luckily it doesn't sanitize users input, XSS payloads can be added into the Boxes to triggered XSS on the profile page of the user in a browser.

So any users visiting another user's profile is vulnerable to the execution of the payload.

## How I Discovered The Stored XSS

On this very day, I logged into the platform, because the platform is a learning ground, so I wasn't in the mood to start looking at video tutorial nor to ready to read anything cause the course in my list out table seems bulky.

So instead of learning, I said let me even test some of my bug bounty skills on this platform, first I looked for any reflected XSS entry points like searching function on the website and improper error messages displayed.

And I had no luck 😦 , But sometimes misfortune is a blessing in disguise.

After digging well, Soon I found that I can leave something on the profile dashboard.

Because the user profile has an option to edit, add your bio, add some texts, so I wrote somethings, and I started with >< and I was like this is my fish, I have to catch and roast it.

So I didn't even stress myself, I got the common payload which is "<script>alert(1)</script>", I inserted this payload into the bio box and I saved it and the bio box went blank.

Not that the payload isn't there but the website functionality made it looks like a white text, so immediately I refreshed the page and boom!!!.

The stored XSS triggered, Damm I was so happy, you know that feeling when you get your first Stored XSS.

But the anxiety in me made me report without thinking of some ways to make the bug more complex and dangerous, so I got a some $ and at least am happy because I got my first bug.
