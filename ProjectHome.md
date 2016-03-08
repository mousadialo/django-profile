## Introduction ##
This is a [Django pluggable](http://djangopluggables.com) user profile zone which can be used and customized easily in your social application web platform developed in django.

It's developed with [Django](http://www.djangoproject.com) for the backend framework and uses [Jquery](http://jquery.com) as the javascript library for the client UI. It avoids big amounts of development time process in such a generic thing as the User Profile and account utilities.

## News ##

**2008-09-24** Version 0.6 published. These are the most important changes:

Version 0.6.0
  * Compatible with Django 1.0.
  * Lot of simplifications. Removed the public/private user selection. It was confusing.
  * Model abstraction with django model inheritance. Now the Profile class has been renamed BaseProfile. Thanks to Rob Yates and Alvaro Mouriño.
  * Better management of avatars. New templatetag to generate thumbs on the fly. Thanks to Alvaro Mouriño.
  * Password managament modified to use the new django password management utilities.
  * Added internacionalization of the urls. Credits to Alvaro Stevens.


---

**2008-07-21** The actual version on the SVN trunk is only compatible with the SVN version of Django. That's because newforms-admin has been merged into Django, newforms is the official forms library now, and this has a lot of implications that has been solved to make django-profile compatible with the new version of Django.

**2008-07-21** Django-profile 0.5 was the last version compatible with django 0.96. The next version will only be compatible with Django 1.0.

**2008-07-05** Version 0.5 published.

This is the first mature version of django-profile. Lot of time has been spent on developing an pulishing the initial idea. Now there's no gratuit javascript code, the application usability has been increased, lot of improvements, etc. You're invited to try the demo and test it for yourself: http://profile.coredump.es

CHANGELOG:

  * CSS and HTML formatted with Blueprint CSS (http://code.google.com/p/blueprintcss/).
  * Lot of code optimization of Django, HTML, CSS and Javascript.
  * Great effort on application usability and template design.
  * Removed every javascript effectism not really needed.
  * Lot of this work made as team with jonas.esp (http://code.google.com/u/jonas.esp/).

**2008-06-22** Version 0.4.1 published.
  * Solved some bugs on the optional configuration parameters APIKEY and WEBSEARCH. Now they are totally optional. Thanks to Kless.
  * Solved a bug on the image crop&resize. If you didn't select a portion of the image, an error was raised. Thanks to David Castello for the report.
  * Some cleanup of the javascript files.

**2008-06-16** Version 0.4.0.1 published.

  * Solved a problem with license issues. Thanks to Kless.
  * Solved a typo on the registration form. Thanks to stephan.d.walter.
  * Renamed ROOT\_PATH to PROJECT\_PATH and solved a bug about directory

**2008-06-11** Version 0.4 launched. Try the demo to see what's new.

**2008-06-10** The upcoming new version 0.4 is going to have dramatic changes. I have uploaded a demo of a development version to show what you will find on it. Try it here:
> http://profile.coredump.es

**2008-05-26** I have started a new branch of django-profile, titled django-profile-gae. This branch makes compatible the django-profile code on [Google AppEngine](http://code.google.com/appengine). It works at 80% of its capabilities, mainly because the PIL (Python Imaging Library) limitations of the Google AppEngine Framework. You can try a demo here:

> [http://django-profile.appspot.com](http://django-profile.appspot.com)


The source code is available on the "branches" directory of the repository.

**2008-02-01** Check the **[Sites](SitesUsing.md)** using django-profile.

## Changelog ##

### Version 0.4.0 ###

  * Changed the license type. Now this project has a Simplified BSD license.
  * Backward incompatible with older versions.
  * Simpler, easier to integrate.
  * New interface, more usable and structured.
  * Removed the "account" module. Everything is integrated in the module "userprofile".
  * Added fixtures for the inital load of Countries and Continents. Thanks to Rob Yates.
  * Solved some bugs on the "account" module. Thanks to Rob Yates again.
  * Removed the "libmagic" dependency.
  * Updated jquery version.
  * New avatar crop&resize plugin.
  * New avatar management. You can insert an image from an URL, or make a search to Picasaweb.
  * Removed the Avatar model. It was innecesary and everything is better managed from the Profile model.

### 0.3.1 version ###
  * Solved some bug issues. Thanks to evo for the report.
  * Modified the Profile model with the new syntax for the OneToOne fields after the [QuerySet Refactor on Django](http://code.djangoproject.com/wiki/QuerysetRefactorBranch#Backwardsincompatiblechanges). Thanks to Arin.
  * Added Italian translation. Thanks to the author of [django-press](http://code.google.com/p/django-press).

### 0.3 version ###
  * We can activate an e-mail validation on the registration process.
  * Lot of re-work and optimizations.
  * Solved some mess with the importing of settings variables. Thanks to Mario Cesar.
  * "profile" module renamed to "userprofile".

### 0.2.1 version ###
  * Lot of bugfixes.
  * Better registration form. Check valid usernames.
  * Allow registration of usernames with uppercase.
  * Added Portuguese Brazilian (pt-br) localization. Thanks to Pedro Valente.
  * Added Spanish (es) localization.
  * Localization framework.

### 0.2 version ###
  * Better Google maps integration (now supports delayed load of the google maps framework)
  * New avatar crop&resize. Everything is simpler with a new jquery plugin.
  * HTML code/CSS. Much cleaner.

## Features ##
It has now the following features:

  * [Registration Framework](RegistrationFramework.md). A utility for the user to register in our site.
  * [Login form](LoginForm.md). Templated login form for our users to access to the authenticated content of our site.
  * [Password lost form](PasswordLostForm.md). Password recovery tool for the users who have lost their password.
  * [Password change form](PasswordChangeForm.md). Password change utility.
  * [E-Mail change form](EmailChangeForm.md). E-mail change utility.
  * [Avatar selection](AvatarSelection.md). Gmail like crop&resize image as avatar asssociated with our profile.
  * [Google maps integration for geopositioning the user location](GoogleMapsIntegration.md).
  * [Possibility of clear all the user profile information when the user wants](ClearUserProfile.md).

## 3rd party software needed to run ##
It relays on this software to run properly:

  * [Django platform](http://djangoproject.com)
  * [Jquery javascript library](http://jquery.com)
  * [Python Imaging](http://www.pythonware.com/products/pil/)
  * [Jquery Json library](http://jollytoad.googlepages.com/json.js)
  * [Jquery User Interface](http://ui.jquery.com)
  * [Jquery Dimensions Plugin](http://brandonaaron.net/docs/dimensions/)
  * [Google Maps API](http://www.google.com/apis/maps/)
  * A modified version of the [Jquery Maps Library](http://code.google.com/p/jmaps/)
  * A slightly modified version of the great [Jquery Calendar](http://marcgrabanski.com/code/jquery-calendar/)

## The Live Demo ##

You could try the demo application included in the Subversion repository which shows the registration process and the user profile management to take a look of what can be done with this software. Once you register in the demo and insert some info in your profile, a usercard will appear in the frontpage of the demo.

[Try the demo](http://profile.coredump.es)

## Some demo screenshots ##

![![](http://django-profile.googlecode.com/files/demo1_thumb.png)](http://django-profile.googlecode.com/files/demo1.png)
![![](http://django-profile.googlecode.com/files/demo2_thumb.png)](http://django-profile.googlecode.com/files/demo2.png)
![![](http://django-profile.googlecode.com/files/demo3_thumb.png)](http://django-profile.googlecode.com/files/demo3.png)
![![](http://django-profile.googlecode.com/files/demo4_thumb.png)](http://django-profile.googlecode.com/files/demo4.png)

## Download ##

The last version is django-profile-0.2. You can download it from the featured downloads box right on this page.

Also, you could use the SVN version to get the most actual code:

$ svn checkout http://django-profile.googlecode.com/svn/trunk/ django-profile

## Want to help? ##

A lot of work can be done. If you want to help you could:

  * Write your suggestions, ideas or questions to the [mailing list](http://groups.google.com/group/django-profile)
  * Report bugs or features.
  * Help with the documentation.
  * Help with the design of the CSS/XTHML.
  * Help with the Jquery javascript.
  * Help with the django code.