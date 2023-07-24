---
author: cmuk
comments: true
date: 2009-03-01 19:21:49+00:00
layout: post
link: https://mckellar.wordpress.com/2009/03/01/mobile-devices-week-5/
slug: mobile-devices-week-5
title: Mobile Devices Week 5
wordpress_id: 355
categories:
  - Mobile Devices
---

This week we looked at the** MIDP Record Store**. This allows you to store persistent data such as High score tables. The role of the record store is to store multiple records even after the midlet has been destroyed. It even keeps the data when the device has been restarted or the battery has been replaced. Midlets cant see the location of the record stores. The record stores are identified uniquely by their names. The record store is an array of bytes. record stores can be accessed by multiple threads at the same time so need to careful to change the data.

The RecordStore class helps to modify the record store and work with the records. OpenRecordStore() method is used to open the store for editing. To work through the stores you need to use enumerateRecords this returns an enumerator to allow you to search record by record using nextRecord method.
