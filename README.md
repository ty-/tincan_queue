Tin Can Queue 
============

Copyright Michael Dawson (mike@mike-dawson.net) 2014.  Licensed under the
Apache 2.0 License - see LICENSE file for details.

This is a Javascript helper library for Tin Can (the Experience API) to work with 
limited connectivity : queues up Tin Can statements using local storage then sends 
in bulk to LRS.

Base usage:

Make a queue object:
var myQueue= new TinCanQueue();

Queue some statements:

Create Tin Can statements and make sure you use {'storeOriginal' : true} as
the final argument because its needed to correctly stringify and restore.  Add
them to the queue with:

myQueue.queueStatement(myTinCanStmtObject);

Send the queue of statements to the LRS:

Give the sendStatementQueue your tin can object and the queue will get sent

myQueue.sendStatementQueue(tinCanObject);

