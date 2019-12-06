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
[My Research](BTrace.md)  

BTrace injects tracing-purpose-codes to target class (no matter provided by jdk or your own application), the codes will be ran to let you print helpful information. It works like AOP. As developer you need to write tracing codes,define when the codes will be ran, then ask BTrace to inject them to the target Java process.  

If we compare Arthas and BTrace, I think Arthas is a well warped toolsets, which includes many tools; BTrace is a small but highly flexible (because developer can code to read data of many aspects in trace codes) tool. Both of them working base on JVM 'Attach API' so I guess they have similar impact on system performance. 

Of course BTrace isn't suitable for unexperienced developer, because low quality trace codes may destroy your production application easily.