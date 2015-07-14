---
title: Major security threat! LinkedIn, Facebook, Github, etc and secondary email addresses
layout: post
categories:
  - security
  - problem
tags:
  - linkedin
  - facebook
  - github
  - email
  - primary
  - reset
  - password
---

## TL;DR

**If you have secondary email addresses associated to your online accounts, remove them NOW!**

**Chances of getting your account hacked increases not n-fold, but exponentially with each secondary email that you add due to poor security.**

## In short

**I got hacked today**

or so I thought initially.

I received an email saying ~ "Your LinkedIn password got reset. Click here to reset it again". My reaction timeline:

1. Nice try! I call [phishing](https://en.wikipedia.org/wiki/Phishing)
2. Why didn't Gmail catch this one?
3. I should open the LinkedIn app and check.
4. Oh fuck! It logged me out, and now my password doesn't work.
5. Oh fuck! Did my Gmail get hacked then? -- No, there isn't any suspicious login.
6. WTF?!

In practice, already at reaction #4 I was resetting my password.

I then assumed (although [assumption is the mother of all fuckups](https://www.youtube.com/watch?v=wg4trPZFUwc)) that it's somehow related to my secondary email addresses that I have connected to the LinkedIn account. I proceeded to deleting them immediately, and reassess the situation later. As you now by now, the assumption was correct.

## There are also nice people in the world

Soon after I got home, and started thinking about password managers, changing passwords, etc. I receive an email from andrei.neculau@yahoo.com (me from another parallel universe, another personality ?!?!) saying that he wanted to create a LinkedIn account with his @yahoo.com email, LinkedIn failed with ~ "There is already an account with the email address", and he proceeded to ask for a password reset, got an email, reset the password and got access to **my account**.

Everything looked legit. Gmail says andrei.neculau@yahoo.com [has an account on Google+](https://plus.google.com/103719053882244206786/posts), then there is [a sale add](http://www.anuntul.org/anunt-vand-pickhammer-picamer-bosch-sgh-27-0f0-131277.html), etc.

I've always knew this day (bumping online into someone with the same name) would come, just didn't know when and how.

## Let's deal with LinkedIn! (their version)

From their [Changing, Adding, or Removing Your Email Address](https://help.linkedin.com/app/answers/detail/a_id/60/) support page:

> **We recommend** that you have at least **one personal address** and **one work address** registered to your LinkedIn account. **To access or make changes** to your account you'll need to use **any email address** assigned to your account and know the password.

So far so good. It makes sense, right? That's one of the reason why until 2 hours ago, I had about 5 email addresses associated to my LinkedIn account. I've been locked out of email accounts before (inactivity, stupid security measures, etc). Plus, there is usually an added bonus (coming below).

From their ["Why You Should Add a Secondary Email Address"](https://help.linkedin.com/app/answers/detail/a_id/59) support page:

> Add a second email address to ~~help~~ make sure you never get accidentally locked out of your account. Most people add a work and a personal email. **This provides an important backup in case you lose access to your primary email address (for example, if you change jobs and lose access to work email)**.

Whoever is the copyrighter/product-owner/whatever-your-position-is for the bolded text should quit. Not be fired, but they should quit. And since it's probably a design-by-committee outcome, please quit in mass.

Not because of the "help" typo, but because of that second sentence, which I'm sure got phrased and rephrased one too many times until nobody understood anything but everyone was happy to finally go home to their families at 9pm, which fails basic logic. (Hedging: if it is by a small chance logical, then they fail to explain properly that they want the primary email address to be the work email address)

LinkedIn could do some statistics on the domain names of their users, but my assumption is that most people use their personal email as the primary one. Not only this is the logical way, but this is also the habitual way. Despite LinkedIn being a social network for the *business* side of our personality, it is still painting a picture for a **person** called Andrei, not for a **\<input company name\> employee** called Andrei.

\#cuzfucklogic:

* if my primary email address is my personal one
* and if I change jobs and I lose access to my work email
* then I lose access to my primary email address

That's **exactly** what that paragraph says! I'm not making it up.

**I think we can agree now that it fails logic!**

**And not only that, but the problem was just starring at them!!!**

If we want people to have one personal and one work email address, and they change jobs, and lose access to their work email, then doesn't that mean automatically that the account is susceptible to access by a 3rd party?!

> If you only have one email address listed on your LinkedIn account and you lose access to it, we won't be able to send you a reset link if you forget your password. That means you **won't be able to sign in to your LinkedIn account**.

And now they are lying. Not by omission, by just contradicting themselves.

On their [No Access to Email Address](https://help.linkedin.com/app/answers/detail/a_id/1501) support page, they clearly state that in this very specific case, "we can help by verifying your identity. To do this, we use a technology that scans your government-issued ID so that we can help get you back into your account as quickly and securely as possible."

> **You'll see a warning message** at the top of your Settings page if you don't have 2 confirmed email addresses in your LinkedIn account.

**Basically that's LinkedIn pushing everyone to the edge of the cliff, where everyone can get hacked tomorrow.**


## Not one, but two logical solutions!!!

> It's important to add all email addresses that someone might use to connect with you on LinkedIn. **If someone sends an invitation to an email address you haven't listed, you could get an error message or accidentally create a second account when you try to accept.**

Now we get to the added bonus I mentioned earlier.

People might know me from university, from my previous work place, etc, and search for me on LinkedIn via the email address @university.edu or @previous.company.co.uk. That's actually incorrect, because most people will search for me by name. I don't need any stats to know that. But LinkedIn **will**, not **might**, use that email for discovering new connections by importing your email contacts.

Above all, the bonus is that you create an online identity saying "hey, I'm the same individual behind @gmail.com and @university.edu and @company.co.uk". I find it less important IMO for social networks like LinkedIn and Facebook, than on services like Github.

So above-all-*infinity* is that you **should** be able to lock your pool of email addresses to this identity that you created on LinkedIn. Since I once had access to andrei@university.edu (you verified it after all), then lock that email address to **ME**, the **individual** Andrei, who **should** be recognized by the *primary* email address, and secondly by that government-issued ID.

When I finish university, and that email address gets into someone else's hands **without me being notified** (either the password is changed, or the address it gets into a catch-all filter that sysadmins can then check up-front, or it's now an alias for my old boss/team, or the address gets recycled and given to another student, etc),

if they try to create or associate or reset the password on a LinkedIn account with the same email address that I still have as secondary, then there are two logical options:

1. verify that they have access to the email address, by sending an email
2. in that email, give **2 links** (not 1) so that they can either
3. A. reset the password of my account after e.g. some extra security questions, or after verifying a 3rd email address that I also have as secondary, etc
4. B. or create a new account and/or move that secondary address to their account, thus removing it from my account

or another solution:

1. tell them that andrei@university.edu is already associated with a LinkedIn account
2. they can start a process of getting it associated to them by notifying the current account holder
3. verify that they do have access to the email address, by sending an email, they click a link, and then I get an email
4. I receive an email saying "Someone called Foo says they now own andrei@university.edu and are asking you to de-associate this secondary email address. Failing to accept/decline within a week's time will be treated as accepting the request."
5. If it is so i.e. that I can/cannot log in anymore into the POP3/IMAP server, then I accept/decline and that's that.
6. PS: Make sure that you don't spam me, so if I declined today, then don't notify me of more requests in the upcoming month, 3 months, whatever.


## What happens in reality is totally wrong!

So if you get access to a secondary email address (i.e. via hacking, or sysadmins recycling emails) then all your accounts are someone else's.

You saw what happened with LinkedIn.

With Facebook, it gets worse! When you try to reset the password to an account, it automatically shows **all** primary and secondary email address. They are partially masked, but it can be very easy to guess. Then all you need is **not hack**, but try to see if you can create an account that was inactive and deleted.

**With Github, is utterly unacceptable!** I expected so much more from them.

There, the email addresses totally create an identity across different organizations (in the real sense, not Github organizations) that you contribute to. Due to processes or just narrow-mindedness, we end up committing code at work as andrei@work.com, and in private as andrei@gmail.com and at some hacking club as andrei@hack.org , etc etc. When that code surfaces to a central place like Github, it's maybe not necessary, but still important to link all those commits to you. Not because of showing off, but because after you lost access to @work.com, **you** (not someone else named like you) can still be reached elsewhere by reading/inferring other contact means from your Github profile. It can be enough with an avatar that you share on github and on twitter that people can suddenly reach you.

All in all, Github profiles acts like a Github-wise [.mailmap](https://github.com/git/git/blob/master/.mailmap). And that's wonderful!

But at Github the same thing happens.

**Any sysadmin that has access to one of your previous work email addresses (which your do not control anymore, for obvious reasons) can just take over your Github account. NOW! Then make that one primary, delete all the secondary email addresses that you have, and then you're all locked out!**


## And there's more shit

LinkedIn thinks it's ok to notify all of my accounts that the password has been reset. That is not a security issue, but a privacy issue, especially since the notification email has details about the author of the reset-password request.

Facebook does something similar. When I remove a secondary email address, it thinks it's ok to notify **all** the other email addresses - primary and secondary alike.

\#cuzfucklogic

Moreover, multi-factor authentication (at least for LinkedIn) makes no difference for password resets, so:

* "oh wow, you are logging in from an unknown device/browser? fuck off! not secure enough, give me your second code!"
* "oh wow, poor you, you've lost your password and now you want to reset it by using your n-th secondary email address that you probably don't own anymore? sure, just click this link, it's that easy!"

**Don't you think, the gravity of the two situations should be somewhat reversed, or at least on par?**


## PS: There is still a dilemma to investigate

Because I removed my secondary email addresses in haste, on a small screen device, I cannot be sure of this, but most probably I had andrei.neculau@ymail.com (I only know of neculau_andrei@yahoo.com and andrei.neculau@ymail.com as email addresses that I have ever had on Yahoo) and **not andrei.neculau@yahoo.com** . I wanted to see if LinkedIn is trying to be smart (which in the world of software development means *utterly dumb and insecure*) and actually assume that user@ymail.com is an alias for user@yahoo.com, **when in fact it's not.** Unfortunately Yahoo seems to have turned off the ability to create [@ymail.com and @rocketmail.com accounts](http://www.cnet.com/news/yahoo-mail-hopes-to-lure-users-with-ymail-com/).
