This is a module designed to integrate version 4 of the PhpGedView genealogy program 
(http://www.phpgedview.net/) with the Drupal framework. It requires Drupal 4.7+ 


OVERVIEW

This program will allow you to integrate PGV into a Drupal site. You will have an option
in the settings to embed PGV in a Drupal page as an iframe, or to link to a full-page
version of PGV. Either way, the programs will work together to allow users to log in 
once and have access to both programs. 

THEMES

The INSTALL.txt file contains information on how to adapt both PhpGedView and Drupal
themes so that the embedded program looks as seamless as possible. 


USERS

The program is designed to rely on Drupal login and access control and the assumption is that
login access from PhpGedView will be disabled and/or redirected to Drupal. You should map Drupal users
to PhpGedView users, since user records in both systems will be retained. That's because there are many 
options that need to be identified to the PhpGedView program to ensure that privacy settings 
work correctly. User info is not duplicated information in Drupal, but links are provided on the
user account page to update it in PhpGedView.

The module allows you to map users in both applications to each other. It will automatically create 
a new user in PGV for any logged in Drupal user who tries to access the program, if they don't 
already have an account in PGV. Users will use their Drupal login and password to log into either
program. The PGV program will still contain password information, but it is not used for 
authentication, so it is important to be sure that your users change their passwords in their
Drupal account, not in their PGV account.

No attempt has been made to truly synchronize users between the two systems, i.e. if a user is
deleted in Drupal they are not deleted in PGV, and vice versa. This is because it is not yet certain
whether users might be shared between multiple Drupal installations, and because it starts to get
very complicated. For now, deletions must be done manually.

IFRAMES

The embedded version of the program works by displaying PhpGedView in an iframe. There may still 
be some browsers that don't recognize iframes, but any reasonably modern browser should be OK. There 
may also be accessibility issues, but the stand-alone PhpGedView program is really not designed for
accessibility anyway, so even if the iframe was not a barrier, the program would probably still
not work well, so I'm going to leave that as an unresolvable issue. I tried many different ways
of displaying a view without using iframes, but nothing would work. Even if you get it working,
following links will pop you out of the embedded view and into the stand-alone view. Every other
integration of PhpGedView I researched displays the program in an iframe, and it seems that that 
is really the only way it can be done.

SEARCH ENGINES

Search engines will not be able to navigate the links in the iframe, so if it is important to
give search engines access to your site, choose the option to integrate PGV externally. This
will provide a link to the stand-alone application that is search-engine-friendly.

MULTISITE INSTALLATIONS

It appears that the module as designed will allow you to share a single PhpGedView installation
with multiple Drupal installations, so long as they share a domain name (so cookies set by
Drupal can be accessed by PhpGedView). This not been thoroughly tested yet, but preliminarily
seems to work. The need to share cookies seems to be the only limitation on this setup.

CREDITS
----------------------------
Adapted and maintained for Drupal by Karen Stevenson

