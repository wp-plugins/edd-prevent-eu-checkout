=== EDD - Prevent EU Checkout ===
Contributors: Ipstenu
Donate link: https://store.halfelf.org/donate/
Tags: easy digital downloads, edd, purchase, prevent, checkout, e-commerce, eu, VAT
Requires at least: 3.3
Tested up to: 4.1
Stable tag: 1.0.4
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Prevents customer from being able to checkout if they're from the EU.

== Description ==

This plugin requires [Easy Digital Downloads](http://wordpress.org/extend/plugins/easy-digital-downloads/ "Easy Digital Downloads").

In an attempt to comply with the 2015 changes to VAT and the EU, this plugin prevents a customer from being able to checkout if they're from the EU. It does this by checking that the IP is not in an EU country based on data from one of two places:

1. GeoIP, if it's installed for PHP: http://php.net/manual/en/book.geoip.php
2. Otherwise, it uses HostIP.Info: http://www.hostip.info

In addition, it adds a *required* checkbox that has the customer confirm they're not from the EU.

Code is developed on [Github](https://github.com/Ipstenu/edd-prevent-eu-checkout/) - Issues and pull requests welcome.

* Credit to [Michelle](http://thegiddyknitter.com/2014/11/19/wip-wednesday-solutions-digital-businesses-eu-vat) for the idea
* Forked from [EDD Prevent Checkout](http://sumobi.com/shop/edd-prevent-checkout/) by Sumobi

== Installation ==

After installation, visit the EDD Extensions page and edit the values for "Prevent EU Checkout" as needed.

== Screenshots ==

1. The Setting Page

== Frequently Asked Questions ==

= Why do I care if someone's from the EU? =

On the 1st of January 2015, the VAT place of supply rules will change and make it a legal requirement that you charge VAT on a product sold to someone, based on the country where the buyer is. This means you will have to be registered for VAT in that country. There are 28 countries in the EU with 75 rates of VAT, however under a special provision for non-EU businesses, a *non-EU* firm need register in only one EU country.

It's currently unknown if this applies to US based business or not. One argument is that it shouldn't, since we're not in the bloody EU. The other is that it does because the US agreed to a 1998 OECD agreement, we're in trouble too.

Please read the following links and contact legal professionals with any and all questions of if you need to use this or not.

* [EU-VAT by Rachel Andrew](http://rachelandrew.github.io/eu-vat/)
* [The Definitive Guide to the New EU VAT Rules](http://blog.sitesell.com/2014/12/definitive-guide-new-eu-vat-rules.html)

= Why does this plugin just block the EU? =

The easiest solution for most small business is to simply stop offering their products to the EU from their own stores. So here you go. If you intend to go for VAT registration, this isn't the plugin for you.

= How do I know if I absolutely must use this? =

You hire a lawyer and let them sort it out. I'm not a lawyer. I'm not even sure if I need this.

= Isn't this illegal in the UK? =

I don't know. Again, not a lawyer. Ask one.

= How does it know if someone is in the EU? =

It checks their IP address against GeoIP (if installed with your PHP) and then against http://www.hostip.info

= What if that's wrong? =

IPs aren't perfect, I know. That's why there's a checkbox added to checkout to have the user confirm they're *not* in the EU.

= What if they lie? =

Then they broke the law, not you.

= What countries are included? =

Everyone in the EU (Austria, Belgium, Bulgaria, Croatia, Republic of Cyprus, Czech Republic, Denmark, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Italy, Latvia, Lithuania, Luxembourg, Malta, Netherlands, Poland, Portugal, Romania, Slovakia, Slovenia, Spain, Sweden and the UK).

= I thought South Africa was doing this too! =

They were. And then they had a burst of common sense and said "If you make under R50,000/annum from digital sales, carry on!"

= Why isn't this working? =

The code won't run until Jan 1, 2015, based on your blog's internal chronometer. Until then, sell away!

== Changelog ==

= 1.0.4 =
* Removing South Africa ([Per KPMG](http://www.kpmg.com/global/en/issuesandinsights/articlespublications/vat-gst-essentials/pages/south-africa.aspx) the threshold is R50,000)
* Filtering purchase buttons (nice catch @StephenCronin)

= 1.0.3 =
* Small date check improvement on checkout.

= 1.0.2 =
* Dates were wrong. You're supposed to CHECK if it's before or after Jan 1, 2015... TARDIS.

= 1.0.1 =
* '/" mixup (thanks @macmanx)
* Better handling of failures.

= 1.0 =
* Initial release