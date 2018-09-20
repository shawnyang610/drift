# drift
when sending messages are no longer easy, even a single word takes luck and effort to deliver. Will your next word be different? 

## concept & design
 - clients can send text messages to each other.
 - message passing itself does not depend on central server(s).
 - central server(s) maintains a fresh ledger of all the clients that are online (username / ip).
 - NO DIRECT MESSAGE PASSING FROM SENDER AND RECIEVER. Message hops through a specific number of other clients before reaching to its receiver. 
 - a succesfull delivery of the message can take anywhere from seconds to years based on senders selection, a message takes at least 15 seconds to deliver by default.
 - sender has the option of guaranteeing a delivery of a message if the specified time is very long(eg. 2 hours ~ 50 years).
 - when a long-time message is finally delivered, the sender might have died long ago, when the message finally being perceived, as if the feelings at the time lived through time. 
 - a piece of message contains the message itself as well as a list of all the ip addresses it needs to go through.
 - when a piece of message passes through a client, the message will be briefly displayed on the client's screen.
 - the passing-by message will be displayed annonymously. 
 - while the message is being displayed (before leaving for next stop), should that intermediate client shut down, the message will fail to deliver.
 - the transmission stats of the message is shown to the sender. Should the delivery fail, the sender may choose to send one more time.
 - the transmission stats is not shown to receiver. A slow message could be due to delivery failure or long itenerary.
 - upon a successful delivery, "trip history" is made available to the receiver.

 ## interface / UI
  - retrofit style - command line.

 ## implementation
  - retrofit client: C++
  - webapp client: js 
  - server: rest-api by python


 * idea & author: Shawn Yang (shawnyang610@gmail.com)
 * all rights reserved