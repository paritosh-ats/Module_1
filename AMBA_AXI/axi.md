# AMBA AXI - Advanced Extensible Interface
## Creative Take - [Collected]
<details>
<summary>  </summary>
</details>

<details>
<summary> 𝗔𝗫𝗜𝟯 𝗦𝗽𝗲𝗰 𝗗𝗲𝗲𝗽 𝗗𝗶𝘃𝗲 (𝟵c/𝟭𝟮): 𝗢𝗿𝗱𝗲𝗿𝗶𝗻𝗴 𝗠𝗼𝗱𝗲𝗹 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀
𝗖𝗹𝗮𝗿𝗶𝗳𝗶𝗰𝗮𝘁𝗶𝗼𝗻: 𝗛𝗼𝘄 𝗱𝗶𝗱 𝘁𝗵𝗲 𝗣𝗢 "𝗸𝗻𝗼𝘄" 𝗶𝘁 𝘄𝗮𝘀 𝘂𝗿𝗴𝗲𝗻𝘁? </summary>


  - You are right to be confused. The Post Office (Interconnect) did not know that transaction #202 was "urgent." The ID itself has no priority.
  - The "urgency" came from the destination of the request.
  
  - In our example:
    - ID #101 was going to the "Main Warehouse" (a slow peripheral, like main memory, which might be busy).
    - ID #202 was going to the "Local Mailbox" (a fast peripheral, like an internal control register, which can respond in 1 cycle).
  
  𝗧𝗵𝗲 𝗥𝗲𝗮𝗹 𝗟𝗼𝗴𝗶𝗰 (𝗪𝗵𝘆 𝗶𝘁 𝗥𝗲𝗼𝗿𝗱𝗲𝗿𝗲𝗱)
  The Post Office (Interconnect) is a smart traffic controller. It saw two requests:
  A request for the slow warehouse (ID #101).
  A request for the fast mailbox (ID #202).
  Because the IDs were different, the traffic controller knew it was allowed to reorder them.
  
  It saw that the request to the slow warehouse (#101) was going to take a long time to get a response. It also saw that the request to the fast mailbox (#202) could be completed immediately.
  To maximize efficiency, it processed the fast transaction (#202) first, while the slow transaction (#101) was still waiting.
  
  𝗧𝗵𝗲 𝗞𝗲𝘆 𝗧𝗮𝗸𝗲𝗮𝘄𝗮𝘆
  
  The ID itself (#202 vs. #101) does not mean "urgent."
  The different IDs simply gave the Interconnect permission to reorder.
  The Interconnect's own intelligence (knowing one destination was fast and one was slow) is what motivated it to reorder for maximum performance.
  
  Does that distinction make sense?
  
</details>

