+++
categories = [
  "tech"
]
date = 2022-11-11T02:00:39Z
draft = false
tags = [
  "GitOps",
  "unbiasedgeek.com",
  "docker",
]
title = "Site Now With Less Baggage"
+++

# A More Elegant Process
Changed the build process for the published container image only has the generated files.  Pushing to main now triggers a build step 
which checkouts out the source, builds the site, builds a new container with nginx and copies only the generated files over.  All in 
all it leads to smalling container sizes and a cleaner more streamlined process.

