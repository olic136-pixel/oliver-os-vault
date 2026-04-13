---
source: plaud
type: inbox
file_id: 0ce3b0c8e47589b6c6e0c2534fcde800
title: "11-04 Meeting: Law Firm Platform, Client Onboarding & Business Model"
date: 2025-11-04
duration: 34 min
projects:
  - Qanun-Platform
  - Dubai-Law-Firm
people:
  - Oliver-Cook-KC
  - Tai
  - Gabe
jurisdictions:
  - UAE
  - Kuwait
tags:
  - business-model
  - client-onboarding
  - B2B-SaaS
  - regulatory-compliance
  - multi-firm-deployment
  - payment-model
status: active
last_reviewed: 2026-04-09
---

# 11-04 Meeting: Law Firm Platform, Client Onboarding & Business Model

## Summary
### 🔑 Keywords:
`Law Firm Platform` `Client Onboarding` `Business Model`

### ⏰ Meeting Information
> Date: 2025-11-04 13:02:22
> Location: [Insert Location]
> Participants: [Speaker 1] [Speaker 2] [Speaker 3] [Speaker 4]

### 📝 Meeting Notes
#### **Initial Discussion: Subscription vs. Case-Based Models**
- The current approach fits individual cases but not subscriptions. A central conflict is whether clients subscribe to the platform or directly to a law firm.
- The group agreed to center on the standard client flow: a client opens a ticket (a "case") and pays for a service.
- Proposed rule: a client cannot open a new case unless they hold an active subscription with a law firm on the platform.

#### **Platform Architecture: Supporting Multiple Law Firms**
- The initial build targets a specific law firm, KBH.
- Concern: an overly firm-specific model may hinder scalability and adaptability for future firms without a major rebuild.
- Goal: design an upgradable system that can onboard new law firms later, even with varied pricing models or logic.

#### **Payment and Service Model**
- A key topic was the flow of funds and related regulatory implications.
- **Initial Idea:** The client pays the platform (e.g., via wallet tokens), and the platform pays the law firm.
  - **Problem:** This makes the platform the instructing party to the lawyer and the handler of client funds, introducing heavy regulatory burdens.
- **Final Agreed Model:** Operate the platform within the law firm's regulatory perimeter.
  - The platform charges the law firm a monthly subscription, potentially tied to user count.
  - The law firm manages all financial arrangements with the client (e.g., retainers, per-case fees).
  - The platform does not process payments between clients and law firms, avoiding regulatory exposure.

#### **Revised Client Onboarding and Access Flow**
- A clear onboarding and access process was defined:
  - **Step 1:** A new client signs up and receives access to a **limited dashboard** to complete initial KYC/AML.
  - **Step 2:** The law firm’s admin reviews and approves the client.
  - **Step 3:** The law firm sends a formal agreement (e.g., client care letter) to the client.
  - **Step 4:** Upon signing, the client gains access to the **full dashboard** and can open cases.
  - The law firm’s admin may pause a client’s access (reverting to the limited dashboard) if the client fails to renew their contract or make payments.

#### **Strategy for Multi-Firm Deployment**
- The agreed model scales across multiple law firms.
- Each firm receives its own separate, branded instance (e.g., "KBH Powered by Kai," "Criminal Lawyers Powered by Kai").
- A client working with two firms will have two distinct logins/accounts; data will not be shared between firm-specific portals.
- The backend codebase remains the same but is redeployed and customized per firm (branding, templates, specific requirements).

### 📅 Next Arrangements
- [x] Capture a photo of the whiteboard diagram illustrating the final agreed model to guide development.

### 💡 AI Suggestions
> **AI Suggestions**
> AI has identified the following unresolved or insufficiently defined items; please review:
> 1. The exact parameters and options a law firm can configure for fee structures (e.g., per case, hourly, retainer) within the platform were mentioned but not fully specified.
> 2. The detailed feature set for the "limited dashboard" (unapproved clients) versus the "full dashboard" (approved clients) needs definition for development.

## Highlights
- • Decision: The product will pivot to a B2B model, operating from within each law firm's regulatory structure and charging the firm directly, not the end-client.
• Key Insight: The lengthy meeting successfully unblocked a key developer by providing critical clarity on the business logic, validating the session's value despite its duration.
• Risk Identified: The existing data model is now considered incompatible with the new architecture and requires significant rework to support clients subscribing to multiple law firms.
• Action Item: Capture and distribute the diagram created during the meeting that visually explains the new system logic to ensure team alignment.

## Transcript
Speaker 1: This whole thing works with the case thing, but not with the subscription thing.
Speaker 2: But I think it doesn't make any difference whether it's the subscription or the case. So look at it like this, let's do all the flow here. We've got a client, a client, forget everything other than the general flow. So forget KYC, forget compliance, forget all of that. No, KYC and . So the client.
Speaker 1: The sign up.
Speaker 2: The client. the client wants something okay whether it's a document drafting or whether it's to sue coca-cola yeah he wants something okay hey what is query yeah raise his ticket yeah it goes so they pay.
Speaker 1: away raise the ticket you know yesterday we we planned uh client cannot make duty or open a new case until he he have a subscription with certain agency platform.
Speaker 2: yeah so at the moment so so this is it every iteration of our model is going to be specific to a law firm okay so we're not building a, a model where we select which law firm goes to so this is uh this is you know law firm and if in future we want uh different law firm with us they have a different model so we're going to you know.
Speaker 1: work with them the client uh current platform logics will not be uh to adopt the new law firm.
Speaker 2: i mean i don't i mean why does it matter whether it's law firm x or law firm y.
Speaker 1: it's to start with do you know what if we will create uh you know we will define the constants for our platform and in future we will want to integrate the new flow form uh if it current private platform logic didn't support the new law form we need you know we need a software that can talk in future or totally upgradable. from the start if we will not do that from the start yeah if you know it could be mess yeah.
Speaker 1: and we have to recreate from scratch again uh to do but i mean but so i don't understand.
Speaker 2: help me oh i think what we've got right now works doesn't it yeah you agree i i think so yeah but i mean this is so this client here has a subscription which you can't get onto the system without a subscription because the client has to be on board who are subscribed to with what.
Speaker 3: so yeah or to the law firm to the law firm if yeah but they pay the subscription to us.
Speaker 2: No, I would have that no because we don't want we don't we want to be inside the law firm So that so the regulatory bubble is the law firms not us But if we got no job, so we will be law firm time We'd be like law firm powered by Chi or we'd be you know Smith and Smith powered by color Yeah, so we get like I get in the law like Harvey like our videos or like every single other piece of yeah There's more they don't know they don't but it's the but it's the same. It's the same sort of thing.
Speaker 2: In terms of so, you know, we're here and the law firms here. So we we're affected We're in power with power in the law firm, but we're not you know, we're not separate from yeah.
Speaker 1: How about the future if we once? Ended the law firm, but we are in the law firm. We are you know have the constraints of The law firm we cannot move, You, We wouldn't have an ability to move.
Speaker 2: But if we've got a model and then that model is going to learn from law firms.
Speaker 1: That's a totally separate thing.
Speaker 3: And then the logic in those onboarding firms is the same.
Speaker 2: It's the same for every law firm. Because of the regulations. Because of the rules. The rules for onboarding clients are the same for every law firm. So the logic will be the same.
Speaker 1: But the conflict is if the client signs up and he wants a subscription. He wants a subscription to a law firm. Or he's subscribing to us. What kind of charging method do we have? We need to have a concrete plan.
Speaker 3: That's the only thing I want to know.
Speaker 1: subscription model on the client side are we charging based on the lot from or or who we have any logic for for how how are you going to pay and at what rate of.
Speaker 2: work so the law firm pages but the user paid a subscription to to the law firm.
Speaker 1: the law firm pays off wait a second yes user client paid subscription how by.
Speaker 3: I thought by our token so methodology always I mean however the money they pay the law firm money okay via us so does the law firm give the client access to the system.
Speaker 2: Yes, it's got to be the law firm admin, because they can't, like we went through the whole process yesterday.
Speaker 3: I think your question is how does the client get in contact with the law firm.
Speaker 1: No, it's just like, let me explain. As Oliver explained, like users, we did marketing, and a user got our URL, he said click it, or he left it on our page. He just signed up, provided his AML and KYC thing and other stuff, and we checked the user, verified, okay. Now, yesterday we discussed, like user can open the case, like here, I can, you know, talk with the AI, and he will explain, okay.
Speaker 1: Provide me these details, okay. So opening the case, when we provide, it's opening the case for us. Okay. But we want to restrict the user if the user didn't. subscribe to any law firm we will not open a case yeah if we have like three or four law firms with us and now there is how is it going to you know subscribe to.
Speaker 3: whom there's no different yeah are you saying when a client has different law.
Speaker 1: firms yeah for example one law firm is specializing the startups yeah one law firm is specializing criminal thing so how are we going to yeah and all these.
Speaker 3: opportunities are the opposite crowds is that what and we have different you know.
Speaker 1: charging rates yeah different you know logics of working yeah.
Speaker 3: Oli, so that'll happen in reality, isn't it, where it works in different ways.
Speaker 2: Yeah, so at the moment, we're going to, so the law firm that we're going to partner with is called KBH. They do commercial employment, intellectual property law in Dubai, Abu Dhabi, and Kuwait. So the brand will be KBH Powered by Kind. They are going to go to the law firm, and they're going to go to that law firm because that law firm can provide them particular services. Yeah. In future, we partner with a different law firm, you know.
Speaker 3: Yeah, this is where the complexes are going to be.
Speaker 2: Okay, tell me the complexity. Criminal Lawyers Powered by Kind. Then they go to the criminal lawyers.
Speaker 3: So that'll be a, so they've already got an account of KBH, i.e. a client after KBH. Then there'll be a second dashboard.
Speaker 1: with the criminal lawyer exactly that second super admin yeah uh for for their law firm, yeah yeah so each law firm will have a separate admin here yeah exactly and now client comes to our platform he wants uh charge against x y and z uh how we uh the payment.
Speaker 2: the point is because we're inside the law firm they're not coming to us they're coming to the law firm oh i'm saying and so so if if i want to come say on me and say forget about kai for a minute say i've got a commercial problem i'll go to kbh to have my commercial problem i have a retainer with kbh i'm paying them 10 000 pounds a year to look after my company yeah okay, That's good, fine, they're paying 10,000 pounds a year. I then run someone over in the street, okay?
Speaker 2: I then go to a different law firm. The 10,000 pounds that I pay to KBA, it doesn't get transferred to this law firm. Yeah. I have to pay them separately.
Speaker 1: Yeah, exactly. I mean, like, if I want subscription, we have two different firms, A and B, and I want subscription with A, how I'm going to subscribe to A.
Speaker 3: Well, the lawyers, I'm going to give them an ask for a login.
Speaker 1: Yeah.
Speaker 3: Yeah.
Speaker 1: I think that's the best way to explain.
Speaker 2: But because, so, are you asking whether, say you subscribe to this firm.
Speaker 1: what happens if you also want to subscribe to this book no no we can manage multiple subscriptions no problem that's not a problem but the thing is when user wants to open a case it should come under a different subscription method we we have a uh you know what uh like we planted a model. uh it was like client we have so what you're asking we just want a second uh and uh we have a.
Speaker 1: case okay before uh as the oliver's name we have this kind of model but problem with this model, if if we have a multiple yeah law forms yeah this is a lot yeah this is well yeah so it's.
Speaker 3: about how we want to do it we could have the client have two separate logins or we could have, one client login and then one of the client they have different i think i think uh which.
Speaker 1: can and this model also breaks this thing like each client have a subscription model you need to remove this one under the subscription not separate now the model become like this one. under subscription if I subscribe to, now we.
Speaker 1: with the new updates we need to modify this one now we can add law form one or. law form two, Okay, if we subscribe to law form one, okay, it has a total different. Subscription and the case is.
Speaker 3: Okay, we should ignore the subscription.
Speaker 1: Without the subscription we as we planned it without subscription, Listen, we got a client from the marketing and he just signed up He just randomly spamming opening cases without subscription. It would be heading for the law forms And if he subscribed like he paid something in his account. Yeah, he because uh before uh making any case he we we showed like we have this law form this law form you can stagnate subscribe they they charge like uh one credit per day and whether you opening a.
Speaker 1: case or not uh the case would require a different uh or more payment yeah okay but uh if you need some work you need to pay like it will be like one one credit per day or whatever we want and, same here with the different law form too here they have their own subscription metal their own cases uh portal you know now we have to remove yeah now we have a model like this yeah right yeah.
Speaker 3: Yeah, and then the client has its, for example, its own wallet in which you can sort of spread between that and that.
Speaker 1: Yeah, the main wallet is here. We can make it like, we can transfer certain credit for lock period. When he subscribes, we will consume X amount of tokens for each work. Yeah, like for example, we use a client did like 30 day subscription. Yeah, we consume 30 days in advance. Yeah, now user can open the case. Yeah, yeah. And each case will have a different payment consumption system.
Speaker 1: Yeah. They will decide by the law firm, they will provide it to the client. Once client will approve, it will detect it from the client created.
Speaker 3: Yeah.
Speaker 1: while you know approving or confirming the terms and condition each and every like in the real world happens like if I comes to him I want something I said okay I'll charge you 10,000 pounds for 40 services do you get these are the terms and condition I said okay okay he said okay pay me in a month okay I hold your payment you know we can start work this is how things are work in this.
Speaker 3: model so our time not just me yeah just me so we just needs it so standard I the.
Speaker 1: toes right so so it's correct so we don't know how I just remove this subscription and yeah you know as a developer we need to understand how them.
Speaker 3: you know you always want to work so you have a client not planning how I said tell them all that I'll tell them all that then on the decline account you may, KBH like I want, then you're a criminal by law.
Speaker 2: You can't do it like that, because if you're effectively taking the money from the client, and you're paying the lawyer, then you're the one that's instructing the lawyer, not the client. So it would be better to completely remove the subscription and let the law firm deal with... There'll be no internal payments with our system. But what you're saying is the client's a wallet, presumably the wallet then resides on our system. Because if you're going to spread the funds between our system and the.
Speaker 2: different law firms, then you're the one that's taking custody of the client's funds or tokens, and then you're issuing the tokens to the lawyers. So then that's caused by the same regulation. well if we if what we're doing is operating inside the law firm yeah right but that's not operating inside the law firm because then you can you are instructing two different law firms so if you know, maybe then what we do is have engineer engineer the model to be to work within the within a law.
Speaker 2: firm okay all the onboarding all of that stuff all the structure and everything will be the same for the law firm um, Allow the law firm to determine.
Speaker 1: Let's just pause this one revision cases say again based on work. How are they going to charge the reason of kisses.
Speaker 2: Baseball, okay, guess based based on work. Okay. Yeah. Okay. So let them say this law firm is going to charge you a Thousand pounds a month. Okay, this law firm is going to charge you a thousand pounds a case Or whatever, but let's leave that then within the discretion of the of the law for me.
Speaker 3: I mean that it's in the law to describe the that's that how many, Options. Yeah. Okay. Yeah.
Speaker 2: So then when we're doing when we're setting this out when we're doing the client letter of engagement the terms and conditions, the company and the law firm can set the parameters they can say in the in the letter that goes out to the client set drop-down box 10 10 cases 10 pieces of.
Speaker 1: work 10 hours 10 whatever it is and then the client agrees to it okay okay now we remove the subscription thing from the order now we have client a client can open a case it goes to the admin their super admin yeah so bad me approves or assign the lawyer with the client yeah and the lawyer created a legal document.
Speaker 1: agreement document yeah and pass to the right like agreed to the document now, they they are on the same page and they are working yeah but the. this can work with you know based on case okay there's a single law firm working not multiple we this model cannot go with the multiple law firms.
Speaker 2: it can go with multiple law firms if we have a different if we're inside the law.
Speaker 1: firm in each several law firm yeah so now the problem is like if if you, created a case and they agreed on for the 12 months okay but we are using the terminology case this can it can be closed after a certain period of time this is and it doesn't make sense we will pass all of this headache into.
Speaker 2: law firm we will charge the law firm we know a thing.
Speaker 1: pass all of this headache on to them for example okay come here so you can come, in okay we have a client and it can open the previously there was a vertical law forms yeah there's no money provide outcomes now we have a case thing okay.
Speaker 1: case to now if if we have multiple cases like one or two and Edwin sign a, lawyer with each case but but this is not the case it's a subscription model for 12 months okay.
Speaker 1: flying once, six, you know, or a great month's work hours. Like a retainer.
Speaker 2: Yeah, retainer. What? Retainer. So the client, so now, the client, so we're inside the law firm. Yeah. Okay. So we are going to take money from the law firm. We're not taking money from the client. Okay. Because that's all sorts of regulatory issues there are. Yeah. Okay. So we're going to take money from the law firm. We'll charge the law firm a monthly subscription. Okay. Based on the number of users. Yeah. And then we'll also take money off the cases in terms of our case prediction model. Okay. What we talked about. Yeah.
Speaker 2: Okay. And the agreement as to whether it's done on a retainer or not done on a retainer. Okay. Is for the law firm to work out. Where are they going to pay us whether they get money from the client or not.
Speaker 1: There's a case where the model is breaking. Like, he's offering a case but this is not the case this is the subscription thing user asking from the law firm like he wants 12 months agreement with the law firm to help them out to sorting the documents restring this and once they, agree the the lawyer completed this thing but this is closed now this is.
Speaker 1: Marcus here yeah and if we keep open this case thing this has single board not a multiple order but then so I don't understand why this is the subscription.
Speaker 2: model in the air so you'd have once again the client here everything comes under the client.
Speaker 1: for example this uh this is the cases yeah and let's say this is the uh subscription thing.
Speaker 2: but what no so that's why i don't understand this well i don't understand why this subscription thing is like you you told me that yeah but we've decided that we've moved away from that we're.
Speaker 1: not doing subscriptions anymore then how um if i have a new startup i need uh somebody to you know give me assistance uh i i mean i may need in the future then yeah um he needs subscription model.
Speaker 3: like but that's what they have that's the agreement between them and the law firm privately and those and then it's on the law the lawyer's side to approve each option in here so they won't be able to do an option without approval from the lawyer case yeah that makes sense. it goes over yeah all right ah yes so we have 10th iteration of the day.
Speaker 1: and then the other thing is like my english is so bad.
Speaker 2: your accent is so complex for me yeah yeah so kbh power bike car okay oh it's a panties. don't buy some it's probably just for a cheap panties and that's okay so yeah it's much better.
Speaker 4: okay okay so.
Speaker 2: So this is what the law firm does, and this is what we're worried about, so onboarding, KYC, conflict, AML, that's the first thing that we do, onboarding, KYC, AML, then client approval, so we do this, we send the action to the law firm.
Speaker 2: That's the closest client, so this is the client approval, so this is onboarding, so then this is the client approval. At that point the client exists in the system, so when this is ticked, the client exists. okay okay agreement on fees law firm action separate yeah yeah so we don't do that the law firm does that open the case of action okay okay this is a.
Speaker 2: client interaction with us case action approval on the law firm side okay yeah so each case or action is a separate folder yeah in client portal.
Speaker 1: So far it is almost compatible with the current model, we just need to add one more thing, to let the user see the dashboard without getting approval from the admin, so here we will have limited KYC as well, after the client approval from the law firm, client approval client exists, full dashboard, so now the client can open the KYC, there is only difference.
Speaker 2: between limited and full dashboard, limited dashboard, client approval, agreement on fees and this will be the client care letter. Yeah, that thing that we saw. So, they create it, it's sent to the client, funds through it.
Speaker 3: This isn't within CAI at all, is it.
Speaker 2: No, this is the law firm, yeah. Okay. So, the agreement on fees is law firm, yeah.
Speaker 3: Well, that case action approval happens within CAI.
Speaker 1: Before accessing the full dashboard, client will see agreement document. The client receives the agreement document and he has to sign the document to see the full dashboard.
Speaker 2: Yeah, there you go.
Speaker 1: The client exists, agreement on fees. We are nowhere and we don't have to care about... the timeline and this kind of thing that will be that will be in here if the client exceeds for example they agreed for the 12 months period and they usually exceed uh let's say in on the 13 months um they the admin can you know decline the case they can pause user if they didn't pay the.
Speaker 1: yeah or renew their argument with them they the admin can pause their.
Speaker 2: cases and ongoing thing or if they don't pay fees or they don't pay whatever's agreed they can pause it.
Speaker 1: now now the client have a limited dashboard again yeah he has to renew the contract yeah and then he can onboard again yeah okay okay I agree now and now we have a better view picture just get rid of that token idea without yeah yeah and also there's a possibility like if we work with multiple in future this model can work with them as well yeah yeah it's the.
Speaker 3: same is that process every time mm-hmm but we treat it separate for the board.
Speaker 1: that yeah yeah so that would be KVH or you know doesn't matter ABCD power back I yeah.
Speaker 2: Yeah, and then all this will be the same, and then the back end, the... So each client will have a different login.
Speaker 3: So they have a separate login for KBH Power by Kai, separate login for LeapFighter Power.
Speaker 2: Just like if you're going to two different law firms to do two different cases, they'd have one file here and one file there and they don't talk to each other.
Speaker 3: So they won't have one login for Kai and under that you'll see different clients, separate.
Speaker 1: Because where you are would be different.
Speaker 3: Well that makes it a lot easier.
Speaker 2: The branding would be different.
Speaker 3: Everything's separate rather than trying to merge everything into one because that makes sense.
Speaker 2: So the branding would be different. So the UX and the UI on this portal would be KBH and the UI on the criminal law portal would be the criminal law firm.
Speaker 1: Yeah, okay.
Speaker 2: I mean the main elements would be the same, the branding would just be different.
Speaker 1: Yeah, it's the colours. You know what I was thinking. A single universal system. A system that can adopt every kind of law firm. No, no, no. better picture like we need to deploy our backend. The process will be the same. Absolutely. We have the same source code we need to make some things that we have to redeploy for the A form, B form, C form, D form. And then the.
Speaker 2: letters and things like this will be based on the firm's letters. So when we onboard a client, we'll take their client care letters, we'll take their all of these things, we'll put them into our system and then we will be able to produce letters and documents and things like that, that are based on their templates. It means that we can take our backend, the, data analytics and stuff, and we can take it to different. So say we get you know.
Speaker 1: if we want to deploy our services for the, from B, we can see how they work, a very general idea, then we can tweak something based on their requirement, then we can redeploy according to exactly what they want. Exactly.
Speaker 2: And it means that if we deploy institutional, so say we go and work with Dubai Police Department, and they want to use our data analytics, then we can take this part out and they can use it at our back end, or we can deploy different parts of it depending on whatever the user or whatever the client is. And the important thing is that we stay inside the regulatory bubble for the law firm, so that we're safe, there's no regulation. Okay, I understand that.
Speaker 2: Are we all happy that we spent three hours going around the big circle and that's where we started.
Speaker 1: No, it's much better because everything is clear. I was stuck here, like what to do next, because I'm not a lawyer. Now I have a better perspective, how to move, what kind of logic I have to implement. I need one picture of this world.
Speaker 4: Yeah, okay, we'll take a picture of that.

## Oliver OS Classification

**Summary:** Pivotal meeting that resolved the Qanun platform's business model: shifting from a client-facing payment/token model to a B2B SaaS model operating inside each law firm's regulatory bubble. The platform will charge law firms a monthly subscription (not clients), with each firm branded separately (e.g., "KBH Powered by Kai"). Initial deployment targets KBH, a Dubai/Abu Dhabi/Kuwait commercial law firm.

**Key Decisions:**
- Platform pivots to B2B model: charges law firms directly, not end-clients, to avoid regulatory exposure
- Remove token/wallet subscription from client side; law firms manage all fee arrangements with clients
- Each partner law firm gets a separate branded instance with the same backend codebase
- Clients have separate logins per law firm; no cross-firm data sharing
- Limited dashboard before law firm approval; full dashboard after signing client care letter

**Key Open Items:**
- Define feature set for limited vs full dashboard
- Specify configurable fee structure options within the platform for law firms
- Rework existing data model to support new B2B architecture
- Capture whiteboard diagram of final agreed model for development reference

**Projects:** [[01-Projects/Qanun-Platform]], [[01-Projects/Dubai-Law-Firm]]
**People:** [[02-Entities/Oliver-Cook-KC]], [[03-People/Tai]], [[03-People/Gabe]]
