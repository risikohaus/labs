---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Attacker Mindset

In order to deliver value with the Social Engineering assessments and Red Teaming activities, we have to give our clients new insights into their security posture. Where are the blind spots? What is the weakest link of a building? How could attackers gain access? To answer these questions, one specific skill comes in handy: _empathy_. What separates a mediocre Social Engineer from a successful one is the ability to put oneself in an attacker's shoes to gain insights into their behaviors and strategies.

A skilled Social Engineer uses empathy to understand the attacker's motives and mindset, what drives them and how much they know. This enables the Social Engineer to anticipate where a potential attacker would strike first, helping to reinforce security measures effectively.

<figure><img src="../.gitbook/assets/skull.webp" alt="" width="563"><figcaption></figcaption></figure>

## The role of Information

You can certainly be a Social Engineer by just sending out phishing emails with a fake landing page. However, does that make you a good social engineer? Most likely, it does not. A key aspect of the art of 'human hacking' is understanding your target. Knowing the interests of your target greatly facilitates rapport building. Having some form of seemingly insider knowledge could increase trust in you. A good pretext is built on a foundation of information gathered through [Open Source Intelligence](https://app.gitbook.com/o/TvfjHvUfn5amUTC0WNAH/s/BLzJQAe7dYvzArn6ZfFx/) and supported by a good understanding of people. So what makes a good Social Engineer is the 'weaponization' of information. The attacker mindset then becomes the act of identifying weaknesses based on collected information and exploiting them.

### Information leads to more information

<figure><img src="../.gitbook/assets/information_iceberg.webp" alt="Information Iceberg with Open Source Intelligence forming the surface level and sensitive insights making up the biggest portion." width="563"><figcaption><p>Information Iceberg in Social Engineering</p></figcaption></figure>

Let's assume the following scenario: you are sitting at a café during your lunch break when suddenly a friendly-looking guy approaches you. "Hey, man, how have you been?" You start asking yourself, do I know this guy? "Doing good. Do I know you?" you reply. "Ah, I'm Max. I used to work at your company. Left shortly after you joined." You're skeptical and rightfully so, you don't remember him. "How is Steven doing? Still managing that big client in Frankfurt?" Now you start thinking: maybe I do know him? He knows my manager, Steven, and he knows that he is doing business in Frankfurt. "Oh yeah, Steven is still on it. Just got back from paternal leave and already back at it ha ha." "Yeah, that's how I remember him. If not for the pay bump at my current employer, I would have stayed with Steven, such a good guy." "Yeah, can't complain. Really a down-to-earth and approachable manager. Where are you working now?" you ask, trying to gauge if there is a threat here or not. "Oh, I left finance to work in consulting, much better hours. I used to manage one account in Shanghai. It was such a pain to fly there. How about you, what clients are you overseeing?" you begin talking...

Three weeks later your manager receives an email from the point of contact at your client: "We were hit with ransomware." While you were cautious not to reveal internal information, you felt rude not reciprocating the conversation request of your random café encounter. After all, he dropped a few bits and pieces that only an insider could have known. You started talking about work, clients, and issues going on. This brief encounter gave the attacker everything he needed. With just a little bit of strategically sprinkled information, the attacker could get you to talk and reveal more information that was not previously known to him. This proved very valuable for crafting sophisticated phishing emails to deliver the malware - the missing link to complete the cyber attack.

As a Social Engineer, you have to apply information strategically to gain deeper insights. Think of it as an iceberg. After your OSINT analysis, you have collected some surface-level information. Eventually, bringing in that information strategically might reveal more information that might not be public at all. Now, all that is left is integrating the information into your story and repeating the process again and again.



### Case Study 1: The Call Center

<figure><img src="../.gitbook/assets/empty call center.webp" alt="" width="563"><figcaption></figcaption></figure>

We were once tasked with conducting a large-scale Vishing assessment at a call center of a telecommunications company with limited prior knowledge. This proved to be harder than one might think! What was our objective? Who were we targeting? And how do we achieve that through a mere phone call?

We started approaching this from an attacker's perspective: how might attackers target the telecommunications company? And how would they use the call center to achieve their objective? Bingo! A very common social engineering attack, if not the most common one, is good old SIM-swapping. An attacker calls a call center, trying to authenticate as a specific person in order to transfer their phone number to a SIM card that they control. Once successful, they hold the key to virtually all accounts of their victim. This telecommunications company tried combating this by implementing a "security pin" that was sent out in a letter. For any support activities, you had to dictate the security pin before any changes could happen.

Knowing this was our objective, we started crafting a multi-phase Vishing scenario. The first scenario was built on the very limited knowledge we had and simply aimed at aggregating more information. Building on that, we would craft a more sophisticated scenario that utilized the gained sensitive insights. Lastly, we would tie it all up with our final scenario that demonstrates the actual attack.

That said, we started talking. In the first few calls, we pretended to conduct an employee satisfaction survey on the call center software. Many were skeptical, but all it takes is one. One nice lady took the time to answer all our questions and gave us enough input. Now we could weaponize the newly gained insights into a more sophisticated scenario. We then called as "tech support," claiming that there was an ad-hoc technical failure that caused client data not to sync with the back end. Again, we had quite a few call center agents who were skeptical, especially since we were calling from their call center hotline. But it takes only one person to believe our story of "this is super spontaneous, and that is the only way I could reach you guys over there." Once we noticed the agent was buying the story, we started asking a few questions and sprinkling insider information here and there to further support our story. We also asked a few questions and tried some "troubleshooting," but this was only a decoy for our main move: "Let's compare the state of the data. The last entry I see is a Mr. Müller." We deliberately dropped wrong information in hopes they would correct it, and they did! "Oh no, I see a Mr. Schneider." That is where we began collecting the most sensitive of all information. After building enough rapport and getting the agent to be invested in the support process, we would then ask for some details about Mr. Schneider. Full name, his birthday to "look him up in the system," and lastly, the security pin with the obligatory "I know we shouldn't be sharing security pins over the phone, but this is quite urgent..."

Once we had all that, nothing stood in our way to make one last call and verify as Mr. Schneider and then do whatever we desired with his account. An attacker could do something similar, but instead of dropping a fake name "Mr. Müller," he could use his actual target and try to get more information on him to e.g., conduct a successful SIM swap.
