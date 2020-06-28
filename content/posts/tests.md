---
author: "Saintmalik"
date: 2020-06-24
linktitle: How to Install TeamViewer on Ubuntu 20.04
cover: "../images/featured.webp"
type:
- post
- posts
title: How to Install TeamViewer on Ubuntu 20.04
weight: 10
tags: ['value_1', 'value_2']
series: 
- Hugo 101
---

TeamViewer is a cross-platform solution that is used for remote control, web conferencing, desktop sharing, and file transfer between computers.

This article describes how to install TeamViewer on Ubuntu 20.04.

## Prerequisites
You’ll need to be logged in as root or user with sudo access to be able to install packages on your Ubuntu system.

## Installing TeamViewer on Ubuntu 20.04
TeamViewer is proprietary computer software, and it is not included in the Ubuntu repositories. We’ll download and install the TeamViewer package from the official TeamViewer APT repository.

Open your terminal and download the latest TeamViewer .deb package using the following wget command:

wget https://download.teamviewer.com/download/linux/teamviewer_amd64.deb
Once the download is complete, install TeamViewer by running:

sudo apt install ./teamviewer_amd64.deb
When prompted Do you want to continue? [Y/n], type Y to continue the installation.