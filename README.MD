# Trouble Shooting Cloud Java Application without Debugging

It is critical to have a way of checking root cause in running environment (even production) in which debugging isn't possitble: 
1. We can't reproduce all problems in local environment so debugging in local IDE isn't useful, actually we already had encountered problem that only happen in production in Readiness Check. 
2. Another fact is that trouble shooting by log isn't efficient sometimes, because in many times we have to enhance our codes firstly to create more log, then re-deploy, then start the app ... although that is very important way of trouble shooting, we'd better to have a flexible and lightweight tool as plan B.  

I think it is very easy to understand such tools' important for SAP ABAP developers, in SAP NetWeaver platform, developers have so many powerful tools to trace applications, the famous one is 'SE30'. By the tools developers get a complete view on context of a problem situation. 

After searching tools of this areas in Java world, I find following ones:

**Tool 1: Arthas (recommended by me)**  
[My Research](Arthas.md)

Arthas is an open source tool provided by Alibaba, for me its' functions are much rich than SE30 which is used in ABAP world. That is 'the tool' we are looking for.

**Tool 2: BTrace**  
[To-Be-Created](README.md)