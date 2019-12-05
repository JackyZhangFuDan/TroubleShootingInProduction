# Trouble Shooting without Debugging

It is critical to have a way of checking root cause in running environment (even production) without debugging: 
1. We can't reproduce all problems in local environment so debugging in local IDE isn't useful, actually we already had encountered problem that only happen in production in Readiness Check. 
2. Another fact is that trouble shooting by log isn't efficient sometimes, because in many times we have to enhance our codes firstly to create more log, then re-deploy, then start the app ... although that is very important way of trouble shooting, we'd better to have a flexible and lightweight tool as plan B.  

After searching tools in this areas, I find following ones:

**Tool 1: Arthas**
[My Research](Arthas.md)

**Tool 2: BTrace**
[To-Be-Created](README.md)