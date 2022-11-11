+++
categories = [
  "cloud",
  "tech"
]
date = 2022-11-11T00:39:15Z
draft = false
tags = [
  "github",
  "GitOps",
  "CI/CD",
  "docker",
  "unbiasedgeek"
]
title = "Gitops With Github Actions"
+++

# Getting Started with a simple GitHub actions workflow.  
The work flow will build an container image and publish it to dockerhub.  I will need to setup a different flow to watch
for updates to the container registry to redeploy in the cluster. 

Note: It did not initially work because the "path" was for the `public` folder.  The path should have been recursive 
i.e., `public/**`
