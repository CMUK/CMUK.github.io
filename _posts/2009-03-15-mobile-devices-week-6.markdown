---
date: 2009-03-15 17:10:52+00:00
title: Mobile Devices Week 6
categories:
  - Mobile Devices
---

This week i looked at different types of connection. We were given tasks to have a go at retrieving data from the university website. After getting this working there was a task of reading a text file which contained 2 different URLs to do this i needed to read the text file and store it in a list so the user could chose which file to retrieve. The contents of the text file was split up by a ',' delimiter character. I looked for a read line method but to my amazement couldn't find one in the language so i found the sun forums had a topic about making a readline method. I set up a method to read a line and it worked.
**
The Generic Connection Framework (GCF)**

This is contained in the javax.microedition.io package. The connector class is an interface for connection you pass in a connection string and get back an implementation of connection. The connection string is similar to a URL. HTTP is all about requests and responses you would send a request to a server and it would return a response back. If you want to use a HTTP connection you need to use MIDP 2.0 and pass in a HTTP URL to the connector this will return the implementation of a http connection. To retrieve a file you pass a URL to the open() method, cast it into the connection type you want to use so HttpConnection, Read the data and close the connection.

**Wireless Messaging API (WMA)**

The WMA is built on top of the Generic Connection Framework. Using the Connector.open method with a connection string set out like "sms://phonenumber:port" you receive a MessageConnection. Ports are used for the SMS service between phones. If you send a message without specifying a port it will go to the default inbox on the target device. J2ME application cant be wrote to listen on the default port.\*\* \*\*The basic steps to sending a text sms message are:

- Open a connection using Connector.open
- Create a new empty message using newMessage returning an object of type TextMessage
- Use the method setPayloadText to put the message inside the TextMessage
- Send the message using the send method

There are two main ways to recieve a message using Message Connection.

**Blocking receive()** - This method waits for the message and processes it when it arrives. GetAddress tells you where the message came from. getPayloadText gives you the actual text message in a string.

**Non-Blocking receive()** - This method uses the MessageListener interface. You register a listener using setMessageListener. When the message arrives the method notifyIncomingMessage is called. You receive the message in a separate thread.
