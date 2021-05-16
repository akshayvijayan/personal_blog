---
title: "How to map custom domain to Blogger platform"
date: 2020-06-16T12:13:30+05:30
tags: [blogger, domain]
categories: [Technology]
---

Blogger is a easy platform for blogging which doesn't requires any technical skill. Usually a blog started in blogger will have an address which ends with .blogspot.com. We can change this domain to a custom domain which we like to use for the blog(We need to purchase domain from any of the service provider. Google also provides domain service)

After buying a domain, log into blogger.com using profile. Navigate to settings which is seen on the left menu bar. 

Click on the option "Custom Domain"
![Custom Domain](/img/blogger_custom_domain.png)

Now enter your domain & click on save. Most probabily the following error(Error image 1) will come.

![Custom Domain](/img/blogger_domain_mapping.png)
				

Log into the domain service provider's website, and move to DNS settings.
![DNS settings](/img/cname_blogger.png)

Add the following A records as shown below:


| Type	| Name  | Value 		 |
| ------|:-----:| --------------:|
| A     | @ 	|  216.239.32.21 |
| A     | @     |  216.239.34.21 |
| A     | @     |  216.239.36.21 |
| A     | @     |  216.239.38.21 |


Now add CNAME as shown in error image (1):

For example

| Type	| Name  		  | Value 		                            |
| ------|:---------------:| ---------------------------------------:|
| CNAME | www 			  |  ghs.google.com                         |
| CANME | hhgnqw2o63c3    |  gv-jorkv3bpltbxs3.dv2.googlehosted.com |



--Don't add the value displayed here. It will be different for different sites. Add the value displayed in your blogger platform (Refer error image 1)


If the following error is occuring while adding CNAME, then edit already existing CNAME record in the DNS list and update with your value. (There is some limit for the number of CNAME records in DNS)

```
There was an error processing your request. Please try again. If this issue continues, contact support.
```

Now you have successfully connected your blogger platfform with your custom domain. 

Happy Blogging!