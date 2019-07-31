---
layout: post
title:  "Printing the Date Range that Your Site Launched"
featured_image: ""
date: 2019-07-30 20:20:13 +0000
tags:
- jekyll
- draft
---

```
<?php
  $currentYear = date("Y");
  $launchYear = 2019; // or whatever year the site will launch

  if ($currentYear > $launchYear) {
   $copyright = $launchYear . ' - ' . $currentYear . '.';
  }
  else {
  	$copyright = $launchYear . '.';
  }
  echo $copyright;
?>
```
