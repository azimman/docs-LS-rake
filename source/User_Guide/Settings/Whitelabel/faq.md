---
layout: page
weight: 0
title: FAQ
seo:
  title: Whitelabel FAQ
  description: Frequently asked questions about SendGrid Whitelabel
  keywords: whitelabel faq, domain whitelabel faq, email link faq
navigation:
  show: true
---


{% anchor h2 %}
What is whitelabeling?
{% endanchor %}

The whitelabeling process involves the creation of several new DNS records including establishing a new subdomain (like em.example.com) in your domain registrar pointing to SendGrid. These DNS records ensure compliance with popular email standards, as well as give SendGrid express permission to deliver your mail by authenticating your outbound mail with your domain.

{% anchor h2 %}
Does whitelabeling require a certain type of account?
{% endanchor %}

[Domain]({{root_url}}/User_Guide/Settings/Whitelabel/domains.html) and [email link]({{root_url}}/User_Guide/Settings/Whitelabel/links.html) whitelabeling are available for all SendGrid users, no matter the account type. However, the IP whitelabeling process revolves around one central element: the dedicated IP address. Customers at SendGrid with a Pro account or higher are automatically assigned one dedicated IP address, which they whitelabel for their outbound mail. During this process, one of the DNS records that must be hosted is an A record, which specifies that all mail going out along this dedicated IP address is authorized to send mail on behalf of your domain.

{% anchor h2 %}
What is domain whitelabeling?
{% endanchor %}

[Domain whitelabeling]({{root_url}}/User_Guide/Settings/Whitelabel/domains.html) adds an SPF (Sender Policy Framework) record to your domain and DKIM (DomainKeys Identified Mail) entries, which effectively authorizes and authenticates SendGrid sending on behalf of your domain. Choosing SendGrid's new automated domain whitelabeling feature allows SendGrid the ability to securely manage your account’s DKIM and SPF records. Domain whitelabeling is the best way to get rid of the "sent on behalf of" or "via" message that some email providers display.

{% anchor h2 %}
What is email link whitelabeling?
{% endanchor %}

[Email Link whitelabeling]({{root_url}}/User_Guide/Settings/Whitelabel/links.html) adds a CNAME record for a subdomain that you choose, which masks click and open tracking links to your domain rather than a SendGrid domain. This increases deliverability, builds trust, and strengthens your brand in your emails.

{% anchor h2 %}
What is IP whitelabeling?
{% endanchor %}

[IP whitelabeling]({{root_url}}/User_Guide/Settings/Whitelabel/ips.html) adds an A record on a subdomain that points directly to your unique sending IP address. This further increases trust and improves deliverability of your email.

{% anchor h2 %}
How do I whitelabel?
{% endanchor %}

Each whitelabel type is a two-step process:

1. SendGrid will generate DNS records that you must add to your domain host (GoDaddy, Network Solutions, Hover, etc.).
2. Click the gear icon in line with your domain name on the main whitelabel page, then select “validate” in the dropdown list to initiate a check that ensures the records on your DNS host match the records SendGrid generated.

{% anchor h2 %}
Can I whitelabel multiple domains?
{% endanchor %}

Yes, it's possible to whitelabel multiple domains using the improved whitelabel management process. When multiple whitelabel domains exist on your account, SendGrid will use the from address for each email you send through SendGrid and match it to a domain and link whitelabel. If the from address does not match an existing whitelabel, SendGrid will fall back to the whitelabel you have chosen as the default.

{% anchor h2 %}
Why is my whitelabel marked with a caution sign?
{% endanchor %}

This means that you have a valid whitelabel, but it is using our old whitelabel instructions. You can improve your whitelabel for better deliverability and security by creating a new whitelabel. This new whitelabel will give you access to all of the new whitelabel features that come from our improved whitelabel setup.

{% anchor h2 %}
Will my old whitelabel still work?
{% endanchor %}

Yes. It will automatically show up in the whitelabel settings and will be set as the default. You will not lose your whitelabel. We do suggest that you update your whitelabel by making a new one and updating your DNS to reap the benefit of our new features.

[When you upgrade]({{root_url}}/Classroom/Troubleshooting/Authentication/upgrading_your_whitelabel.html), you will need to create new subdomains for IP, link, or domain whitelabels because we have split the whitelabeling functionality from "whitelabel everything" to individually whitelabel each separate piece.

{% anchor h2 %}
Why whitelabel?
{% endanchor %}

Have you ever noticed that email you send through your SendGrid account displays “sent on behalf of” or “via sendgrid.me” and wondered how to get rid of it? Have you noticed that click tracking links point to a SendGrid domain rather than your domain? Whitelabeling effectively masks SendGrid's delivery and click/open tracking to your domain, giving your emails a consistent and professional appearance where all links and sources point back to your domain.

{% anchor h2 %}
What do I do if I have more than 10 IPs?
{% endanchor %}

There is a character limit in SPF records that means that if you have more than 10 IP addresses, they will not fit in the record. When this is true, we will provide you with the generic SendGrid SPF record which includes all IPs at SendGrid, not just yours. If you would like to secure your SPF record to only include your IPs, you can chain multiple SPF records together manually. For more information see [Open SPF's website](http://www.openspf.org/Introduction).

{% anchor h2 %}
What's with the second email link domain?  Will that be used to track my links?
{% endanchor %}

The second link domain is generated by SendGrid and is strictly used to validate that the user who is setting up the email link whitelabel is actually in ownership of that domain.  If the user is not able to setup the second link CNAME, they will not be able to validate their link whitelabels. That secondary CNAME will never be used to for click tracking.


{% anchor h2 %}
Related Articles
{% endanchor %}

* [All You Need To Know About Whitelabeling]({{root_url}}/Classroom/Deliver/Delivery_Introduction/all_you_need_to_know_about_whitelabeling.html)
* [How to upgrade your old whitelabel]({{root_url}}/Classroom/Troubleshooting/Authentication/upgrading_your_whitelabel.html)
* [I have created DNS records, but SendGrid is not validating them.]({{root_url}}/Classroom/Troubleshooting/Authentication/i_have_created_dns_records_but_the_whitelabel_wizard_is_not_validating_them.html)
* [Open SPF](http://www.openspf.org/Introduction)
* [Whitelabel - Do I need to make DNS changes?]({{root_url}}/Classroom/Deliver/Delivery_Introduction/whitelabel_do_i_need_to_make_dns_changes_pro_and_higher.html)
