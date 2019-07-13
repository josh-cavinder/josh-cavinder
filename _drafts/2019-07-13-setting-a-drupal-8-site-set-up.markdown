---
layout: post
title:  "Drupal 8: Getting a New Site Started"
featured_image: ""
date: 2019-07-09 17:56:10 +0000
tags:
- jekyll
- draft
---

– In your CLI ( Command Line Interface ), cd to your Sites directory ( or wherever you want the site created )
– Run the below commands to spin up a new site ( reference: https://codepen.io/andy-blum/full/KrgrdQ/ )
– $ composer create-project drupal-composer/SITE_NAME_GOES_HERE project-name --stability dev --no-interaction
– After composer finishes running, run the below command:
– $ ddev config
– Process through the prompts — you should just need to hit enter three times to get through it.
– Run $ ddev start
– Enter your local password if you’re prompted.
– Run $ drush si ( site installer ) to run through the Drupal installation process. This will only need to be done during the initial build. If you’ve cloned the repository and reach this step, you’ll need to run $ drush si config_installer instead so that the UUIDs for the sync files match up. Otherwise, thing will get fucky.
– Type ‘yes’ or hit Enter when prompted.
– After running the installation process, it should provide you with a default username and password. If these don’t work, run the following command:
– $ drush uli
– Log into GitLab and create a new repository for the new site.
– Add your dependencies — at the least you’ll need the config_installer and config_split modules
– Enable the modules you’ve required and push your initial commit.
– Enable the UIKit theme by running the $ composer require drupal/uikit command.
– Go into your /admin/appearance page on your local site and select “Install and set as default”.
– In your IDE, navigate to your ~/web/themes/ directory.
– Create a new directory named “custom”.
– Copy the STARTERKIT directory from the ~/web/themes/contrib/uikit/ directory and paste it into the ~/web/themes/custom/ directory.
– Replace all instances of STARTERKIT with something that’s related to the site, for both the file names and within the files themselves.
– You can replace the file content via Atom with the ‘Search in Folder’ action, and the file names with Finder’s rename function.
– Update the name of the “info.yml.tmp” file to “*info.yml” in the ~/web/themes/custom/SITENAME/ directory.
