---
title: Why Did I Do It
date: "2021-09-25"
description: "Basic Overview of DIDs and Their Use Cases"
tags:
  - decentralized
  - identifiers
  - blog
---

What's up, all? This blog and this post have been hacked together, so I would have an excuse to write 
a bit about DIDs, aka [decentralized identifiers](https://www.w3.org/TR/did-core/). This modern 
technology is igniting my imagination for a future full of trust. After the past few years of 
divisiveness and power plays, it would be nice for the benefits of identity and privacy to be 
placed back into the hands of individuals. It is possible that DIDs could accomplish this goal.

<br>

Because my understanding of this concept is evolving, and the technology itself is evolving, I ask 
that you please take any knowledge written about here with a grain of salt. I will explain here 
the concepts to the best of my knowledge, but like most humans, I will make mistakes. I would like 
to add code snippets and project ideas here when I have time to do so. I'm sure others will do 
the same once DIDs and Verifiable Credential systems become more widespread, but right now, we are 
riding the sexy, cutting edge. 

<br>

## Paraphrasing the Spec

A DID is a like a web URL, a Uniform Resource Locator. Instead of pointing to a website, it points 
instead to a DID Document. The DID Document is a file which exposes "cryptographic material". One 
can think of this material as a lock. Should one have the proper key, one may access the DID Subject 
described by the DID Document. The DID Subject is a noun - it may be a person or some data. In the 
case of a person, cryptographically authenticating with the DID Document will show that you are 
that person, the DID Subject. In the case of some data, cryptographically authenticating with the 
DID Document will show that you have the proper rights to access that data. The entity that holds key 
that fits into the lock exposed by the DID Document is known as the DID Controller. The DID Controller 
can be a human or a computer, but the key here is the DID Controller can prove control over the 
DID Subject without requiring the help of a third party. 

<br>

Another interesting tidbit about DIDs is this. A DID Controller can provide others with incremental 
access to the DID Subject. Imagine that you have some medical records as the DID Subject, and you 
are the DID Controller. To view your medical records, you insert your key into the DID Document to 
unlock them. You can be confident that you are the only entity able to view the records, and they 
have not been tampered with because there is a digital papertrail of edits to the records. Imagine 
you visit a specialist doctor - let's say a psychiatrist. Does this doctor need to see your entire 
medical history, including dental records, social security number, and past surgeries? I don't know, 
but let's imagine they do not need all of this. They only need access to your medications, mental 
health history, and allergies in order to prescribe the proper medicine. As the DID Controller, you 
may provide the psychiatrist with access to only the information they need and lock all other 
information cryptographically so that it is inaccessible. When the psychiatrist prescribes medicine 
and updates your medication list, they will digitally sign the update, so you know it is legitimate, 
and the paper trail is kept up to date. Only you and the psychiatrist may view the information which 
was shared - no third parties but rather peer to peer.

<br>

That's it for now. For next steps, I plan on adding more detail about the fundamentals of DIDs as I 
continue reading through the spec, adding the basics of Public Key Infrastructure and how the key / lock 
relationship works, and adding more about the different use cases of DIDs in the future. If you are 
interested in current implementations of this technology, you can check out 
[Microsoft's ION](https://techcommunity.microsoft.com/t5/identity-standards-blog/ion-we-have-liftoff/ba-p/1441555).
