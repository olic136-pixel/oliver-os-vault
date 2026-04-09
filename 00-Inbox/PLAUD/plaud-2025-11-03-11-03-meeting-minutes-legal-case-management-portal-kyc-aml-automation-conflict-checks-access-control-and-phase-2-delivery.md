---
source: plaud
type: inbox
file_id: a4eedb0555f9c734a0cf87d4a8e49d07
title: "11-03 Meeting Minutes: Legal Case Management Portal – KYC/AML Automation, Conflict Checks, Access Control, and Phase 2 Delivery"
date: 2025-11-03
duration: 43 min
projects:
  - Qanun-Platform
  - Dubai-Law-Firm
people:
  - oliver-cook
  - tai
  - gabe
jurisdictions:
  - England & Wales
  - UAE
tags:
  - KYC-AML
  - conflict-checks
  - access-control
  - client-onboarding
  - phased-delivery
  - SaaS
status: active
last_reviewed: 2026-04-09
---

# 11-03 Meeting Minutes: Legal Case Management Portal – KYC/AML Automation, Conflict Checks, Access Control, and Phase 2 Delivery

## Summary
> Date & Time:  2025-11-03 13:46:30
> Location: [Insert Location]
> Attendees: [Speaker 2] [Speaker 1] [Speaker 3] [Speaker 6] [Speaker 4] [Speaker 5]
## Overview
This consolidated record, created on 2025-11-03 13:46:30, summarizes multi-speaker discussions on a legal case management portal’s functionality, phased development, and a lawyer-led onboarding model with KYC/AML and conflict checks. It merges overlapping sections on current functionality, development phases, onboarding flows, KYC/AML automation, conflict checks, access control, platform integrations, service tiers, scope strategy (single firm first), and spam/marketing considerations. Key themes include automating compliance, enforcing controlled access until checks and acceptance are complete, running dual conflict checks (onboarding and per case), enabling client–agent chat only post-acceptance, and stabilizing priority workflows. Open issues span vendor/tool selection for KYC/AML, routing and data segregation for multiple firms, pricing tiers, and clear sequencing of compliance and communication triggers.
## Key Topics
- Current functionality and recent changes
  - The system allows agents to approve cases, set priority, and chat with clients after accepting a case. If an agent is not available, basic handling is in place but may need refinement.
  - A recent crash occurred because priority-setting was removed from the client side; only agents can now set priority.
  - A new case (“personal inquiry”) flow was demonstrated; the agent can approve and set priority, and client–agent chat is enabled post-acceptance.
- Development phases and progress
  - The project is divided into three phases: Phase 1 is complete; Phase 2 is targeted to be completed within this week and is described as extremely important; Phase 3 will involve LLM and AI-related features.
  - Frontend and services are communicating; some issues are known and will be addressed.
- Client onboarding flow for partner law firms
  - The platform will act as a “secretary” for a law firm, not as a lawyer; all acceptance decisions remain with the law firm.
  - Initial contact comes via marketing or a link associated with the partner law firm; clients are directed to a landing page to begin onboarding.
  - The proposal is to provide a restricted portal where users sign up, complete KYC/AML, and submit a concise case description; chatting is disabled until onboarding is complete.
  - Onboarding requires AML and KYC checks, plus an initial conflict check before any platform access.
  - After passing checks, the law firm must explicitly accept the client, issue client care letters and terms of service, and only upon acceptance/click-to-accept are clients granted platform access with an immutable record of acceptance.
  - The onboarding is organized per case: each case requires acceptance by both the law firm and the user, along with agreement to terms and conditions. Once accepted, the case becomes approved and open.
  - Users should only approach the law firm when they have a case; a short case description produces a data package including KYC, AML, conflict information, and the case description for the firm’s review.
- KYC/AML requirements and automation
  - Required items include proof of identity, proof of business, proof of address, and proof of funds; identity and residential address documents are standard.
  - The team intends to automate KYC/AML using AI to avoid bots and streamline verification; this can be performed together (KYC and AML).
  - It was suggested to integrate automated KYC and AML within the chat or portal, reducing manual questioning by agents.
  - If documents are missing or problematic, the system should not grant access; issues are flagged for the law firm to resolve.
  - The client can complete KYC only once within the client portal, implying reuse across cases.
  - There is interest in understanding what system Astra uses for KYC/AML, though no one knew during the meeting.
- Conflict checks: scope, timing, and handling
  - Two separate conflict checks are required:
    - At client onboarding: determines whether the law firm can take the person/company as a client at all.
    - Per case: every time a client opens a new case, run a case-level conflict check.
  - The system checks client name and company against the law firm’s database and flags potential conflicts (green flag if none; red flag if potential conflict).
  - AI performs matching and flags; lawyers make final determinations. Red flags trigger manual review by the law firm.
  - Applies equally to individuals and companies; personal names are checked against the database to detect conflicts.
  - Conflicts can emerge mid-case; lawyers must remain vigilant. The system’s role is to continually flag potential conflicts.
- Access control and user sign-up philosophy
  - Clients should not gain dashboard access until AML/KYC and initial conflict checks are passed and the law firm accepts them.
  - Open public sign-up risks spam and misuse; the preferred model is controlled onboarding via law firm invitation or guided intake.
  - Law firm reception/agents may create client profiles and portals, share credentials, and manage the onboarding sequence.
  - Even with multiple partner firms (e.g., corporate and employment law), each firm performs its own KYC and conflict check against its own database.
- Platform responsibilities and integrations
  - The platform is a SaaS layer integrated with the law firm, tailored via a bespoke LLM model that learns the firm’s processes.
  - Conflict checks run only against the partner law firm’s database to respect firm-specific matters and confidentiality.
  - The system will record immutable acceptance of client care letters and terms of service (e.g., click-to-accept captured and stored).
- Service tiers and offerings for startups
  - The target market is startups and businesses; the service may include assistance with structure, IP, corporate documents, and NDAs.
  - Clients can choose service tiers, with pricing tied to tier selection.
  - Marketing (email, social) directs startups to a landing page to initiate contact and onboarding with the partner law firm.
- Scope: single firm first, multi-firm later
  - Initial rollout will start with one firm, focusing on corporate law.
  - Future expansion envisions multiple firms across markets and specialties (corporate, employment, criminal), with clients creating a case to engage the appropriate firm(s).
- Spam and marketing considerations
  - Potential spamming issues require planned measures to tackle them.
  - Marketing may bring clients who sign up but cannot be helped; the short case description helps determine suitability early.
## Open Issues & Risks
- Unresolved
  - Specific methods for name/entity matching in conflict checks are not finalized, especially for common names and entity disambiguation.
  - Details of how multiple law firms will coexist on the platform (routing logic, data segregation) need definition.
  - It is unclear which tool or vendor will be used for KYC/AML verification and how automation will be implemented.
  - Responsibility and timeline for Phase 2 completion within this week are not clearly assigned.
  - Unclear sequencing of compliance steps: whether AML is required per case or only once at sign-up.
- Unclear
  - Exact pricing and definition of service tiers are unspecified.
  - The precise landing page experience after a marketing link click is not fully defined (what is displayed, what data is collected before checks).
  - Communication rules: Specific triggers and permissions for enabling chat and other communications post-approval need definition.
- Risks
  - Allowing open sign-ups could lead to spam and misuse; the team prefers controlled onboarding to mitigate this.
  - False positives/negatives in automated conflict checks could cause delays or ethical issues; robust manual review procedures are essential.
  - Mid-case emergence of conflicts requires ongoing monitoring; failure to flag could create professional responsibility risks.
  - The system experienced a crash related to priority-setting changes; stability and error handling around priority workflows may need further attention.
## Action Items
- [ ] Look into what system Astra uses for KYC/AML.
- [ ] Explore implementing automated KYC and AML within the chat/portal flow.
- [ ] Automate KYC/AML verification, including proof of identity, business, address, and funds, with bot-avoidance measures.
- [ ] Implement conflict-check logic that flags potential conflicts (green/red) at onboarding and per case, with manual review by lawyers.
- [ ] Build access control so clients only see the dashboard after law firm acceptance and click-to-accept of client care letters and terms of service, with immutable recording.
- [ ] Configure law firm admin tools for reception/agents to create client accounts/portals and manage invitations.
- [ ] Set up firm-specific databases and ensure conflict checks are scoped to each partner law firm’s data.
- [ ] Create marketing-to-landing-page intake flow that routes inquiries to the appropriate partner law firm.
- [ ] Plan measures to handle spamming and unwanted communications during onboarding.

> **AI Suggestion**
> AI has identified the following issues that were not concluded in the meeting or lack clear action items; please pay attention:
> 1. Lawyer-led onboarding sequence and access control are undefined: There is no agreed, end-to-end onboarding flow that specifies when and how KYC, AML, and conflict checks are triggered; what the acceptance criteria are; how an immutable acceptance record is created; and how access control withholds the dashboard/chat until checks are passed and the firm formally accepts. Ownership, steps, and deadlines are missing, creating a blocker for safe client activation.
> 2. KYC/AML scope, vendor selection, and automation details are unresolved: The team has not selected a verification vendor/tool, defined document requirements, or clarified whether AML is run once at sign-up or per case and how KYC can be reused across multiple matters. The execution plan for automation inside the chat/portal (including bot-avoidance) is not defined. No responsible person or timeline is set, and there is no evaluation of Astra’s KYC/AML system or integration path.
> 3. Conflict checks design and continuous monitoring lack specification: Methods for entity/person matching and disambiguation (e.g., common names), dual checks at onboarding and per case, manual review flow for red flags, and rules for continuous mid-case monitoring and escalation are not finalized. Green/red flagging logic, firm-specific conflict databases, data models, owners, and delivery dates are missing, increasing compliance risk.
> 4. Phase 2 ownership and schedule risk threaten downstream work: Responsibilities and timelines to complete Phase 2 this week are not assigned, and the list of known frontend-service issues targeted in Phase 2 is unspecified. This creates a high risk of delay and could block Phase 3 (LLM/AI) from starting on schedule.
> 5. Stability and priority workflow updates are unclear and risk crashes: After removing client-side priority, updated priority-setting rules, error handling, and fallback behavior when agents are unavailable are not defined. Without these, workflows remain fragile and crash risk persists, impacting service stability.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: So you have, you know, the client approaches the law firm, yeah.
Speaker 2: Well, wait a minute. Before starting everything, let's see what we have done so far. And then we can start, you know, searching. So I can hit the Confirm. These are the details.
Speaker 3: AdWords. Okay. Say it's your case that we created. This is the ID. Okay. So we didn't do anything wrong. Mm-hmm. So I can get thrashed. So this is my line, but I know how to answer all.
Speaker 2: Okay, wait on that case. This crash happened because I removed the priority thing from the client side. The client cannot set the priority. Now only the agent can have to check the priority of the case. Now our client has created the case and agent have, you know, this is a new case, the personal inquiry, which he did. So he can approve or approve whatever he wants. He can set the priority.
Speaker 3: Nice. Approved. And this is by the way the agent. Yeah. Okay. So now he's.
Speaker 2: now I can you know the after accepting the case client can chat with the agent.
Speaker 3: agent yeah okay cool and they pick a description whatever they want and let's say if agent is not available the basic thing is ready you know you can see the.
Speaker 2: quality now. there's a certain things I need to fix this this one because I divided this project into the three phases the phase one is complete and I hope I'll try to complete this next phase within this week which is extremely important and and we have the third phase third phase is for the LLM and this and that artificial intelligence.
Speaker 2: surely the case that's only the other only you know and the first thing was you know the prison the break into the front end that Jack sister Jack full service how you can see that service is working they don't pretend if they're communicating with each other yeah there are my issues are coming they did they know I'll sort them out so so far I've done this usually can approach the document yeah.
Speaker 2: you.
Speaker 1: I think we need to have the onboarding for the client slightly different, the flow has to be slightly different, so at the moment we've got a client onboarding by case, what needs to happen is that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer, the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the.
Speaker 1: client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to contact the lawyer and the lawyer needs to onboard the client and at the point that the client needs to, then there'll be KYC AML so they have to provide documents there should be a way of them providing the KYC and the AML a brief description of the case and then the client or the the lawyer can determine whether or not they accept the case they'll have to tick AML check they'll have to.
Speaker 1: tick KYC check they'll have to check that the case and that there's no conflicts so that usually you.
Speaker 4: you should have if you put in the chat box like a function for that so like you know like an automated KYC do you know what I mean yeah and an automated AML thing instead of like, the client asking you know like instead of it being questioned like the agent asking the client the question you know almost like it just what does the what system does Astra use for their.
Speaker 1: KYC AML they've got they're meant to have this, I have no idea. No idea. We'll have a look at that. Yeah. So that would be really good if we could automate the KYC and the AML. Okay.
Speaker 5: Give me two seconds while I disrupt it. It's going to be really difficult. I'll let you just go over.
Speaker 2: Okay. So for the client portal, client can only be done the KYC once.
Speaker 1: Yeah. Right.
Speaker 2: Okay.
Speaker 1: So what I'd have is... It's not very good, is it? No. I don't think I've got the marker. I need to have it in my head.
Speaker 3: Maybe this one.
Speaker 1: So we've got the client and the normal process would be client. Okay. approaches the law firm right and then they have to check aml kyc conflict okay yeah so this is easy so we know how to do aml we know how to be kyc conflict they'll need to check, um from the description so they'll have to so client will provide uh hale's question.
Speaker 2: um let's say the client may not try to contact with the law firm and uh how like from online.
Speaker 1: portal what we have yeah really yeah yeah we'll just signed up so so the idea is first the idea is to start with yeah that we have let's imagine the client.
Speaker 1: Imagine the client's a start-up, okay? So we market this in conjunction with our partner law firm as a service to the start-up, yeah.
Speaker 3: So we have marketing, start-up wants to sign up with our service.
Speaker 1: It may be that they don't have a case, it may be that they want some help with structure, intellectual property, any sort of issue that, you know, sort of corporate documents, non-disclosure agreements, all of these things, so we're going to provide a full service, okay? So... they want to sign up so they get a link or they get a you know through through our marketing they sign up they get a link it's either.
Speaker 1: given to them by the law firm given to us they go to a landing page and they sign up so they sign up okay then they decide what level of service they want one tier two tier three tier four tier it's going to cost one two three okay yeah we have different types yeah, okay so that but but in order to do any of this they have to go through that process so kyc aml conflict.
Speaker 2: and what are the things in the email usually.
Speaker 1: kyc and aml they'll do together and it will be proof of, identity, proof of the business, proof of address, proof of funds these just these.
Speaker 2: sorts of general KYC and everything. Okay in a general KYC usually what I know is like your ID, your identity documents and your residential address, proof of residential address. I think they only take the photo or maybe maybe there are there are a lot of ways to because we said we have you know AI, we have to avoid the bots. Yeah. So we can create the best AI system so to do.
Speaker 1: that KYC. So this we can do or we can automate it. Yeah that's what I'm thinking. So here conflict. Conflict is the you know complex thing. No it's not that complex. You have to check, that there is no issue between this potential client and any client you already have.
Speaker 6: Okay, so what they'll need to do is to check the name of the client, name of the company.
Speaker 1: against anyone in the database already. And if this name or this company is flagged in an ongoing case, then we should red flag it for manual review. Because it makes because we couldn't take a case if we're bringing a claim against the board Yeah, what's on you can't represent both sides out the claim something like that. So this is easy This is easy. This is easy because it just requires checking the name of the client check of the name of the company.
Speaker 1: against the database and.
Speaker 2: River yeah, why can't we accept the both parties? Like for example if we have multiple lawyers and.
Speaker 1: so So you can sometimes do it. But what I'm saying is this should can all be done by AI, Okay, and then this if if there's no cable if there's no conflict issues, we have green flag, If there is a conflict issue we have red flag and then it can be manually reviewed by the lawyer.
Speaker 2: We can see our agent is reviewing your documents and then it shows to the lawyer.
Speaker 1: Red flag, the lawyer has to look at this, look at this, look at this and then they can decide whether or not we can take the case on So now I understand.
Speaker 2: I think I understand now we have to make more advanced sign-up system Before opening the case. Yeah, we need to user have to turn the KYC, AML and, But for the conflict, I guess, Conflict is come under each case that for example a I'm a user.
Speaker 1: Yes, so so this is like an initial initial onboarding, So onboard the client, so we do KYC, AML, conflict check, onboard, so then we decide whether they can access the platform or not.
Speaker 2: I think we need to separate the conflict from here. When you were, you know, trying to create a new case, and then we can, you know...
Speaker 1: There's two different points at which you have to assess conflict. You can't separate them, it's two different assessments. The first assessment is, can we take this person on as a client? So if you are, for example, say you're representing Coca-Cola, and you're representing Pepsi, and Pepsi is suing Coca-Cola. You can't represent both Pepsi and Coca-Cola. So that would be a no. If they're onboard and there's no big conflict check, then every time they open a case, there would have to be another conflict check.
Speaker 1: But that's something that you would then do. You'd run the case. You'd do the diffs. Algorithm or this check again for every case. Okay. Okay. So it's two conflict checks.
Speaker 2: How about you know, If an individual loses, I don't you know, I don't have any company or any you know relations with any company I'm not representing anything, and in my case my, I put none in my company.
Speaker 1: Mm-hmm. Well then then if there's then there's no check to make is that you'd have to check their name, Against the database. Okay to see if say, you know Oliver, Was an employee of coca-cola and all it was now suing coca-cola. Okay, we represent coca-cola Okay, Oliver tries to sign in we know his name. We know his address. We know his details We check those against the database and it says this is the Oliver that is suing our client.
Speaker 1: We can't represent, So, it's the same thing if it's a person or if it's a company.
Speaker 2: Okay. How we, for example, I'm, you know, I'm already on board with the service and I'm representing nobody. Okay. And I open a case and it seems like I have to sue the Coca-Cola for X, Y and Z reason. So, here's my document, this and that. And we have another person, X, Y, Z.
Speaker 2: He comes to the platform, he signs up, he puts his company name, Coca-Cola, now it's President Coca-Cola. And he wants to, you know, sue me or whatever.
Speaker 1: Well, then this would flag it up. We're not making the decision. So the AI isn't making the decision, the AI is checking for a potential conflict. And then it's a lawyer's job to always keep in their head the possibility of conflict. So sometimes you get cases where at the beginning of the case there isn't a conflict, and then halfway through there is a conflict. And so you have to make the decision as a lawyer halfway through that there isn't. So what we're flagging here is conflict at sign-up, question mark.
Speaker 1: We don't reject it, we flag it, so the lawyer has to decide.
Speaker 2: I guess, Oliver, at the moment of sign-up, we don't ask for the conflict. Like for example, I'm an existing customer.
Speaker 1: Well, you would have to ask for the conflict.
Speaker 2: I have one case, I tried to sue a person, ABC, a year ago. And then after a year ago, I want to sue, or my partner, you know. For what? for example i have a traffic issue or whatever case i have i reopen a new case and um now, for the new case uh you know when we signed up before one year ago i you know provided documents.
Speaker 1: that had no conflict so you'd have to you have to do it twice so this is the job that a lawyer is going to have to do when they're on board so so if i'm if if forget the platform if you come to me as a lawyer then we have i have to take your aml your kyc and i have to do a conflict check when you come to me okay okay if you want say say you want me to represent you in a divorce you come to me we do these three things to take you on board easiest way okay for example.
Speaker 2: I am the lawyer, A comes to me, I want to divorce B, and letter B comes to me, and he wants to divorce A, or whatever he wants, but the thing is, B was the existing customer, and A wasn't. And so, when A comes to us, we didn't have any B case, and we, you know, onboard the A, and later, a day, or two, a week, B comes, and he says that, I want to sue this one.
Speaker 2: a person okay and even for example the the names are similar like uh for example oliver, um john xyz and any name so they may conflict well you know we cannot check on with the names this is so hard uh yeah for example what if so we will have a database of.
Speaker 1: of clients we will have a database of companies yeah we will have the documents that relate to any particular kind that's being made yeah if you came to me as a lawyer in that situation, i would have to do a manual check to make sure that there's no conflict at the point that you're on boarded against any case that i've got okay that's the first thing if you then so you bring case a to me and i say as a client i have no conflict and in case a i have no conflict.
Speaker 1: there's a two different conflict checks, It's not the same one and then if you came to me two years later with another case, I'd have to do another conflict check, okay.
Speaker 2: then, my suggestion is to, Implement the conflict check on one side, you know we can let anybody you signs up and on board to a platform and, Once you will open the case, another conflict check then then we only.
Speaker 1: Check the conflict no because you can't take the client if there's a conflict whether they're bringing whether they're bringing a case or not If there's a conflict there may be some conflicts which means you can't take the client at all.
Speaker 2: You know the sign that means we on board the client because we didn't associate any a lawyer.
Speaker 1: Anybody else, but we're doing this in partnership with the law firm. Okay, you should think of it as as us, Doing the job of someone working at the law firm. So that's the that's that's where we fit into.
Speaker 2: Let's say you and me are lawyers. Okay, it comes to you and becomes to me Okay, we're working together Make up to you against me or to be or becomes to me against me So what we're doing this in this case? Well to start with we don't reject the cases.
Speaker 1: We accept it and we know it's not us that's accepting or rejecting the case There is the law firm because we don't act for anybody so we can't act. They're not our clients the law firm The conflict checks in the conflict check will be made against the days, device.
Speaker 2: You know, this is the tricky thing. Conflict check. How are we going to find the conflict? For example, if his name was John, he wants to sue the John and later somebody else John comes to us, and he wants to sue anybody. So, okay, so that's, let's imagine, we're using the name, we can.
Speaker 1: find. Well, so we've got, so someone, so someone apply, so we've got client one.
Speaker 2: And we've got, you know, in my back, I'm, you know, I'm thinking how the logically.
Speaker 1: things are going to work. Yeah, yeah, so client one going to law firm one, yeah, with us in the middle. What? With us here. Well, okay. Between the client, between the client and the law firm, yeah. Okay. In in order to be up for the law firm to accept and it's the law firm's decision whether they accept or not Okay, we have to do AML KYC. Yeah, and we have to do.
Speaker 1: Conflict. Okay, if there's an issue here, we red flag. Okay, okay.
Speaker 2: Give us his normal thing.
Speaker 1: Yeah, but if there's you know, they don't have the right documents or we check the documents and there's a problem with the documents or Something like that.
Speaker 2: Until use it, you know audible to complete the AML or KYC. We will not let him use the dashboard.
Speaker 1: No, no, but okay. So the decision about who uses the dashboard comes here not from us.
Speaker 2: for example we are the but we can't say okay we and center okay and here's the law firm and here the client okay the same thing and nobody suggested client to to come to this platform right okay okay so user there's some recent online.
Speaker 2: program but and he called okay this is the platform I can sign them and I can get the lawyer I can do it on my official you know things so he just signed up and the next next step is I have to turn the KYC AML in order to, complete the basic verification once we give him the basic verification take, okay so now a user can see the uh no no the user can't see the dashboard until the law firm.
Speaker 2: accepts the case there's a confusion um for example um if if uh because you're mixing two things together like case and the sign up thing okay okay yeah the the client this client doesn't.
Speaker 1: get any access to anything until the law firm takes them as a client because if it's us that's determining whether they get access to the platform that's us acting as lawyers we're not lawyers okay so we are an extension of the law firm okay so so we are. We're SaaS for the law firm, so we don't make these decisions, so if I came to you in the real world and wanted to onboard as your law firm, you're the person working at the law firm, I come to you, I say I want to sign up, you're on the front desk, so here are models on the front desk, you say to me I need to see this, I need to see this and I need to perform this check, give me these documents, we'll contact you when we can take one as a client.
Speaker 1: So this here, so if there's AML KYC which we can automate, what can we do? My suggestion is here.
Speaker 2: the the way you're suggesting the things um is um is totally dependent upon the cases, now the client uh for example if clients don't see signs that they provide documents then often decide okay we can let you sign up then you can see that dashboard and if it is fuzzy so it's totally depend the you know user portfolio or the whole thing is totally depend upon the case.
Speaker 2: the way i'm looking things like we'll let the user sign up basic email sign in phone sign up whatever he used to sign up now here the basic thing okay now the whole problem with that is.
Speaker 1: that you just get clients signing up yeah spamming the dashboard asking silly questions and things like this which is isn't what we want we want okay we want what we are offering isn't, Legal advice to members of the public. Okay, what we're offering is a sass system.
Speaker 2: Yeah, for the sass point of view like if, We got a user and he's opening his case nonsensely and doing spamming We can you know the end lawyers can you know block his account.
Speaker 1: So what we're focusing on is, Startups and businesses. This is the law firm that we're thinking of partnering with is a corporate law firm.
Speaker 2: for example, if, you know for this, Flow and seeing the problems or maybe I'm getting wrong who then let me explain that you inside.
Speaker 5: Sorry, just interrupt. I'm gonna watch from people. I'm absolutely starving. Are you hungry? Whatever, I'm not gonna get some chicken and rice or maybe I mean.
Speaker 2: okay so let's say if in future because from the SAS point of view mm-hmm in future in future we may have more than one firm connected with our platform right yeah so there's not a single authority or love from that controlling the platform if we go with this way you know the law firm can.
Speaker 2: let the user signs up it can we can we the only way of doing this is against.
Speaker 1: this okay so so say that we have a law firm that does corporate law yeah, and a law firm that does employment law yeah we'll have a partner doing this and a partner doing this, okay so they'll do the aml kyc anyway we'll have the data for the conflict check anyway.
Speaker 1: so either firm will have to do both kyc and the conflict check okay so.
Speaker 2: one more thing so we can um if we go this way usually can come to the uh visit to physically visit the person uh to the lawyer or any you know the firm he asks, uh agent or lawyer he discuss things so uh the agent team or lawyer team they said okay okay give us this so we can we we have to restrict the user sign-in process.
Speaker 2: from the, you know, we can restrict the sign up process for the clients, we can put the sign up procedure, you know, whole thing into the, in a corporate level, they can get the, you know, in person they are sitting and, you know, the agent can create the sign up procedure.
Speaker 1: Yes, I want to automate the KYC, just look at that, it's Astra's KYC.
Speaker 6: Thank you very much.
Speaker 2: Okay, it seems good, very good, but certain things, they don't have any. At least they have, this is like we are using the zero knowledge proof protocols, but. I don't think we don't have to do exactly this, but what I'd like is for us to be able.
Speaker 1: to offer effectively. So we've got the KYC, so think of it, think of our platform as being, for this purpose, the secretary to the law firm. It will be a slightly different model, dependent on the law firm.
Speaker 1: It will learn, you know, we'll have a bespoke model that the LLM will learn the law firm's particular way of doing things. So this conflict check will only be run against this law firm's database, which we have access to. So, I think we've got it. We don't have to we don't have to make it any bigger because we're not the one at the moment who decides, Where a particular piece of work goes? What we are is like the secretary for law firm one and that's the more we're going to have our you know.
Speaker 1: All of our integration with okay, so if we can do this AML KYC You know we can say top-level AML KYC whatever and then we can check for conflicts against their database At the point of onboarding. Okay, then great. Okay, so like I said.
Speaker 2: The law firm, Reception team can or lawyer can, Create a sign up detail then, you know, create a portal for the client, because if you they cannot directly signs up on to the platform, so we need to, give this kind of access to because in our case as you explained the law firm has full authority who's going to sign up and who's going to use the platform yeah they will do the you know all.
Speaker 2: details they will take that details in person and you know they could they will create a problem for the client okay they can they will share the details with the client okay here's your pass.
Speaker 1: and yeah because what because what will have to happen is when they if they pass this check and pass this check the law firm has to accept them okay one second yeah the law firm then has to issue the client with client care okay client care letters terms of service which the client has to accept okay yeah and then they're onboarded.
Speaker 1: Okay, so AML KYC goes to the law firm, green flag, green flag, the law firm accepts, gives them access to the platform, on the platform they have the client care, terms of service, they click to accept that, when it's clicked to accept we have an immutable record of the fact that they've clicked to accept it because we've recorded, then they're onboarded. So this is the point at which they'd have full access to the platform.
Speaker 1: So they can have access to something here, it doesn't have to be a platform at all, it can just be within the environment, they're provided with terms of service and letter, client care letter, terms of service, they accept it or they don't accept it, if they accept it then they get access to the platform, if they don't accept it they don't.
Speaker 2: So far the client has to visit the law firm. and then here agent will do the whole thing for him he will get the whole details and according to the platform and once the law firm or in visit law firm physically yeah no doubt is it open then how's my husband to how the client is.
Speaker 1: going to communicate with the law well so here so you know we're gonna focus on startups I'm going to market ourselves for startups in conjunction with the law firm yeah so we'll do emails social whatever it is I'll get yeah okay they haven't there's a link they use that link okay to contact us contact the law for us okay and that's the first point of contact which is here, We then respond to them, or the law firm responds to them, powered by us, and then they do AML, KYC.
Speaker 2: For example, I got the link for marketing, I got the mail, and I was even looking for help, so I clicked it, and where it will bring me.
Speaker 1: so it will bring it to not not to not to the portal but maybe like a very short version of.
Speaker 2: the very short version i was saying before like we need to let the user signs up and in the sign up we will give them very short uh but they don't need to chat they don't need okay we can restrict anything yeah they don't need any of that exactly exactly this is the you know here uh you know i just created that you know okay yeah so it's about so what we need to do is to give them access.
Speaker 1: to whatever it is to allow this flow to take place okay yeah uh and this is my suggestion.
Speaker 2: so far whatever understand um like we need to uh you know complete this whole thing we can put this thing in a single case we don't you know we will not uh um, and put a check in during the signs up but you have to distinguish between a client and a case, yeah so this is for client onboarding yeah for for the client onboarding uh this is this will come under a single case for each case we usually have to go through all of these things except for the.
Speaker 2: aml and they don't have to do this yeah exactly this is what they they may not have to do this for each for each case um the law firm will accept the case and uh user also will accept the case and terms and conditions each and everything provided by the law firm uh and once they will onboard it the case is fully approved and open yeah and then they can you know go which is that they can chat this yeah without um uh without accepting and this whole thing user can't.
Speaker 2: communicate with you, any of the law firm user can you know and, regarding the spamming and this kind of things we can plan how we can you know tackle the things and for example and like you said like we we are doing the marketing and we got the client and we the client just signed up and for example in that you said like very short version of the portal now it's in the in.
Speaker 2: this case I mean I was assuming like you think that client have to physically a you know visit not in front you know the whole idea is yeah they don't have to be talking so if if the client is from visiting physically to the lock farm, then how he knows which firms are...
Speaker 1: because at the moment when we start out it's going to be one firm.
Speaker 2: okay but but in the future we may have multiple firms right.
Speaker 1: we're likely to have firms in particular markets yeah so a corporate law firm.
Speaker 2: corporate employment.
Speaker 1: criminal yeah we'll have these different ones.
Speaker 2: yeah so.
Speaker 1: and it will be dependent on, just at the moment we can just focus on this because we've got corporate.
Speaker 2: let's let's say we have one one law firm in start and we give the limited version of the dashboard, to communicate to the law any law firm or say we we may have single or multiple even infinite law firms with us, you just have to create a case right, in order to come to this.
Speaker 1: yeah but then then that's how you would do it in the real world, If I wouldn't go to a lawyer unless I needed to go to a lawyer, so if I come to a lawyer because I've got a case, I don't go to a lawyer because I want to spend money, I go to a lawyer because I've got work, and so we're specifically pushing for this professional market, it may be that people try and sign up and we just can't help them, at which point, because this and this, which will have to be a very short explanation of what the case is, you know, like you saw in here,
Speaker 1: you know, a short, you know, I've got this problem, I want this, you know, I need this, I need that, so what's provided to the law firm at this stage is a package of data which is KYC, AML, conflict, and description.
Speaker 2: We usually have that, and just, yeah, we can understand, just move step by step, for example, we've got that. marketing and we go to the client yeah okay now client have a very short version of the dashboard to do this one yeah so now he is on the dashboard how, is going to communicate with any law firm we don't need for the moment okay.
Speaker 1: what he needs to do is provide his KYC yeah for example he's done the KYC okay.
Speaker 2: we know we are for in order to sign up with an image for the limited version you have to done the AML or the KYC things okay now he's done with the KYC and AML okay now what's now now he have the limited version of our then then there.
Speaker 1: will be need to be a description of the case. yeah and obviously he doesn't he doesn't we don't this is done by the law firm so that's going to put the law in the culmination of the name meeting five minutes i have to break five minutes

## Oliver OS Classification

**Summary:** Detailed 43-minute meeting on the Qanun legal case management portal covering client onboarding flow, automated KYC/AML verification, dual conflict checks (at onboarding and per case), access control gating, and phased development. Phase 1 is complete; Phase 2 targeted for the same week. The platform operates as SaaS inside a partner law firm's regulatory bubble, with initial focus on corporate law for startups.

**Key Decisions:**
- Clients get no platform access until the law firm formally accepts them after KYC/AML and conflict checks pass
- Two separate conflict checks required: one at client onboarding, one per new case
- AI flags potential conflicts (green/red) but lawyers make final determinations
- Platform acts as law firm's secretary, not as a legal service provider
- Phase 2 to be completed within the week; Phase 3 covers LLM/AI features

**Key Open Items:**
- Select vendor/tool for KYC/AML verification automation
- Investigate what system Astra uses for KYC/AML
- Define entity/name matching logic for conflict checks
- Assign Phase 2 completion responsibilities and timeline
- Define pricing tiers and subscription parameters
- Plan anti-spam measures for public-facing sign-up

**Projects:** Qanun-Platform, Dubai-Law-Firm
**People:** oliver-cook, tai, gabe
