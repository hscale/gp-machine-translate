# GP Machine Translate
A machine translate plugin for [GlotPress as a WordPress plugin](https://github.com/GlotPress/GlotPress-WP).

Three machine translation providers are supported (though only one at a time):

* Google Translate (pay per character)
* Microsoft Translator (free tier available)
* translte.org (free)
* Yandex.Translate (free but requires Yandex account)

Note: This plugin assumes the source language is English as support for automated translation from other source languages is limited.

## Configuration

Once you have installed GP Machine Translate, go to your WordPress admin screen and select "Settings > GP Machine Translate".

You will have three Fields to configure:

	1. Translation Provider
	2. Global API Key
	3. Client ID
	
You can select from four providers with some requiring the additional fields to be filled in.

## Google

Google Translate requires an API key to function, to do this you must register with Google and provide a payment method.

* Login/signup your [Google developers console](http://console.developer.google.com)
* Select "APIs & auth"->Credentials.
* Create a new "Public API access" key.

The public access key is what you will use to configure GP Machine Translate with, either for all users or a specific user.

## Microsoft Translator

Microsoft Translator requires an API key to function, to do this you must register with Microsoft.  Microsoft does have a free tier for translation, limited to 2 million characters a month so you do not need to provide payment details for this tier.

Microsoft has a walkthrough on how to subscribe to the Translator service here:

	https://www.microsoft.com/en-us/translator/getstarted.aspx
	
You will need both the client secret and client id for it to function with GP Machine Translate. 

## transltr.org

transltr.org is a completely free service and does not require any API key or other configuration.  Simply select it as the desired translation service in the GP Machine Translate settings page and you're off to the races.

This service operates via unsecured HTTP, while that's probably not a concern, it should be noted for your reference.

## Yandex.Translate

Yandex.Translate is a free service, however you must sign up to their service and adhere to their terms of service.  This includes providing a link back to the service for translated text.

One other thing to note with Yandex.Translate is that when you sign up, you get a Yandex e-mail address and other services they provide and there is no option to opt out of them.

To get an API key, follow the instructions here:

	https://tech.yandex.com/translate/

[Powered by Yandex.Translate](http://translate.yandex.com/).

## Setting the API key

To set the API key for all users, go to the WordPress Dashboard, then Settings, then "GP Machine Translate" and set the API key (and Client ID if required).

To set if for a specific user, go to the users profile and scroll down to the "GP Machine Translate" section and set the API key (and Client ID if required).

Note, if both a global and user API key are set, the user API key will override the global API key.