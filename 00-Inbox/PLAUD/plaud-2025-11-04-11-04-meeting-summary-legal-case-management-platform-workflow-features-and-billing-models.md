---
source: plaud
type: inbox
file_id: 1af8d299225856a9f09c7a7e865c3b76
title: "11-04 Meeting Summary: Legal Case Management Platform Workflow, Features, and Billing Models"
date: 2025-11-04
duration: 86 min
projects:
  - Qanun-Platform
  - Dubai-Law-Firm
people:
  - Oliver-Cook-KC
  - Tai
  - Gabe
jurisdictions:
  - UAE
tags:
  - product-design
  - whiteboard
  - billing-model
  - subscription-tokens
  - client-onboarding
  - document-management
  - case-prediction
status: active
last_reviewed: 2026-04-09
---

# 11-04 Meeting Summary: Legal Case Management Platform Workflow, Features, and Billing Models

## Summary
> Date & Time: 2025-11-04 11:30:47
> Location: [Insert Location]
> Attendees: [Speaker 2] [Speaker 1] [Speaker 3] [Speaker 5] [Speaker 6] [Speaker 4]
## Overview
This document summarizes a series of meetings held to design and define the workflow, features, and business models for a legal case management platform as of November 4, 2025. The discussions covered the integration of an infinite whiteboard for document collaboration, onboarding and permissions flows, subscription and case-based billing models, document management, communication systems, and the use of tokens or credits for billing. Key outcomes include the adoption of a subscription-based access model, the need for flexible document and case organization, and the identification of open issues around terminology, billing for complex cases, and technical implementation. Action items focus on clarifying document ingestion, billing processes, dashboard development, and credit management.
## Platform Features and Document Management
- The platform supports an infinite whiteboard with multiple components, allowing flexible arrangement and organization.
  - Users can take segments of text, place them on the whiteboard, and link them together.
  - Linked text refers back to its original context within the source document, enabling easy reference and traceability.
  - The functionality is compared to LiquidText, highlighting similarities in how information is managed and connected.
- Users can upload PDFs, extract and annotate content, and organize multiple documents on a shared whiteboard.
  - Users can circle, crop, and drag sections from documents (e.g., witness statements, phone data, banking data) onto the whiteboard.
  - Widgets represent different data types, enabling users to switch views and interact with specific data.
- The whiteboard is envisioned as an "infinite board" or "space" where various legal materials (dashboard, telephoning, witness statements, depositions, etc.) can be managed together.
- Visual representations and links ensure all extracted content remains connected to the original documents.
- AI integration is planned to assist with tasks such as finding references, converting data (e.g., telephone records into graphs), and answering queries about case details.
- A chat system will be available for users to interact with AI or team members for support and data retrieval.
- The platform aims to support collaborative work, with permissions managed by a designated case lead who can assign editing rights to staff members.
- Output options include generating bullet-point documents or media files for presentations, with support for projecting via devices like iPad, Chromecast, or Apple TV.
- Document ingestion, including OCR and data extraction, is under consideration, with responsibilities for extraction and chunking likely assigned to specific team members.
- The onboarding process for clients includes document review and compliance checks before granting full access.
## Onboarding, Permissions, and User Roles
- The onboarding process includes client registration, KYC (Know Your Customer), AML (Anti-Money Laundering), conflict checks, and limited dashboard access.
  - After review by a lawyer and completion of terms and engagement letters, clients gain full access.
- Clients must subscribe to a law firm before opening a case; access to case creation is restricted until subscription and agreement signing are complete.
- The platform will enforce permissions, with case leads controlling access and editing rights for each case.
- There are distinct roles: client, law firm admin, agent/lawyer, and super admin.
  - Law firm admins have broad access and can assign cases to lawyers.
  - Permissions are managed so that only relevant parties can access specific cases or documents.
  - Super admin or main admin requires a key for access; issues with password/key management were briefly mentioned.
## Subscription and Case-Based Billing Models
- The platform will require all clients to have a subscription to access any services.
  - Subscription provides general legal assistance up to a defined value, measured in tokens, credits, or hours.
  - Standard legal documents (e.g., employment contracts, NDAs, IP agreements, shareholder agreements) are included under the subscription.
  - The subscription covers a set amount of work; additional work requires purchasing more tokens or upgrading the subscription.
  - Example pricing discussed: $100 per month for a subscription, with 100 tokens or credits allocated to the client account.
  - Unused tokens or credits (referred to as "Y tokens") can be carried over to the next month.
- The subscription model is likened to a retainer agreement.
  - Clients pay a fixed amount (e.g., £10,000 per year) for a set number of hours or tokens.
  - Once the included hours or tokens are used, additional work is billed at a higher rate (e.g., £150–£300 per hour).
  - All agreements and pricing are set by the law firm, not the platform.
- Access to the platform and services is only available to subscribers.
  - Clients must complete KYC and AML checks, then fund their account with credits.
  - Service requests are initiated via a chat or ticketing system, with lawyers quoting the required credits for each task.
- Clients cannot open new cases without an active subscription.
  - The system should prevent case creation unless the client is subscribed to a law firm.
- A clear distinction was made between general legal assistance (covered by subscription) and "cases," which refer to legal proceedings against individuals or companies.
  - Case-based work is not included in the subscription and is billed separately.
  - Clients must have a subscription to access case-based services, but payment for cases is handled outside the subscription model.
- The process for handling cases involves:
  - Reviewing case documents, using an AI model to summarize and predict success, and drafting advice on the merits.
  - Lawyers review AI outputs and negotiate agreements with clients on a case-by-case basis.
  - As volume increases (e.g., 100 cases per month), additional staff may be needed for negotiations.
- The admin dashboard will be required to manage:
  - Credit allocation and consumption.
  - Agreement terms and adjustments based on law firm pricing.
  - Tracking of token/credit usage and carryover.
## Payment Models and Case Agreements
- The primary payment model discussed is a subscription system, potentially using tokens (e.g., 100 tokens for $100) to represent client credit.
  - Tokens are used for standard legal services and document generation (e.g., NDAs, shareholder agreements).
- For complex or high-value cases (e.g., over 5,000 pages or £1 million), separate agreements are required outside the standard subscription.
  - These cases may involve conditional fee agreements (CFAs), where the law firm covers legal fees in exchange for a percentage of the award if successful.
  - The platform will help determine case eligibility for subscription or special agreements based on predefined criteria.
- Billing for complex cases involves cost estimation, engagement letters, and potentially charging for professional services such as case assessment.
  - Example: A KC (King’s Counsel) may charge £50,000 to review evidence and provide advice, with costs recovered from the losing party if the case is successful.
- The platform acts as an intermediary, facilitating agreements between clients and law firms and charging for its services accordingly (e.g., a percentage of the award or professional service fees).
- The system must handle both standard credit-based billing and manual processes for exceptional cases.
## Client Dashboard, File Structure, and Communication
- The client dashboard is the central hub, containing all client-related information, cases, and documents.
  - Each client has a profile page with KYC/AML details and a record of all agreements and actions.
  - All work (cases, actions, tickets) is organized under the client, with each piece of work stored in a separate folder or subfolder.
  - There was extensive discussion about terminology ("case", "action", "ticket"), but agreement that the underlying structure remains the same regardless of naming.
- Document management should allow for clear separation of files related to different actions or cases.
  - Subfolders within the client vault help prevent mixing documents from different requests.
  - The system should enable retrieval of all documents and communications for a given client, regardless of how many cases or actions exist.
- The platform will include a chat or messaging system for client-law firm communication.
  - Clients can submit queries via chat or ticket, which are flagged by AI and routed to the appropriate lawyer or agent.
  - Communication does not need to be real-time; asynchronous messaging (similar to email or Slack) is acceptable.
  - Admins can add or remove lawyers from chat channels as needed, ensuring oversight and proper assignment.
- The admin dashboard allows assignment of cases or tickets to specific lawyers or agents.
  - All communications and documents related to a ticket or case are accessible to assigned personnel.
## Legal and Regulatory Considerations
- All legal documents and advice generated by the platform or AI must be approved and signed off by the law firm.
  - The platform itself is not regulated and does not provide legal services directly.
  - Agreements are always between the client and the law firm.
## Open Issues & Risks
- The process for manual billing and the platform’s exact role as an intermediary in complex case agreements remains unclear.
- Criteria for determining when a case falls outside the standard subscription model need further definition.
- The integration of AI for data extraction, reference finding, and case prediction requires additional planning and technical validation.
- Responsibilities for document ingestion, extraction, and onboarding steps are not fully assigned.
- The terminology for tokens/credits and their management remains somewhat unclear and may need further simplification.
- It is not fully resolved how agreements will dynamically adjust to different law firm pricing structures.
- The process for distinguishing between general assistance and case-based work in the user interface needs further clarification.
- The terminology for organizing work ("case", "action", "ticket") remains a point of confusion and needs final alignment.
- There is some uncertainty about how document versioning and organization will scale with large numbers of files.
- Password and key management for admin and super admin accounts may need further attention to prevent access issues.
- The integration of the subscription model with the current file and case structure requires further technical validation.
## Action Items
- [ ] Discuss document ingestion process and potential use of OCR models.
- [ ] Define infrastructure setup to ensure smooth data and permissions flow.
- [ ] Clarify manual billing processes for complex case agreements.
- [ ] Develop an admin dashboard to manage the credit/token system and agreement terms.
- [ ] Define and implement the process for credit carryover and consumption tracking.

> **AI Suggestion**
> AI has identified the following issues that were not concluded in the meeting or lack clear action items; please pay attention:
> 1. The process for manual billing and the platform’s exact role as an intermediary in complex case agreements remains unclear and requires further definition to ensure accurate billing and prevent disputes between users and law firms.
> 2. Responsibilities for document ingestion, extraction (including OCR), and onboarding steps are not fully assigned; the process and team roles need to be clarified to avoid delays and ensure efficient data handling.
> 3. The integration of AI for data extraction, reference finding, and case prediction requires additional planning and technical validation to ensure reliability, compliance, and that the system meets user needs.
> 4. Criteria for determining when a case falls outside the standard subscription model need to be clearly defined to avoid ambiguity in billing and access, which could lead to user confusion and revenue leakage.
> 5. The terminology for organizing work ("case", "action", "ticket") remains a point of confusion and needs final alignment across the platform to prevent user misunderstanding and workflow errors.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: It was the best way that I come up with infinite whiteboard with the multiple components.
Speaker 2: So we were just looking at this and you saw how that liquid text worked.
Speaker 1: I've seen it.
Speaker 2: Yeah.
Speaker 1: You know.
Speaker 2: So it's the same sort of thing. So I can take bits of text, put them here, link them together. Yeah, it refers back to the original text.
Speaker 1: Original context, which is in the document.
Speaker 2: Yeah, yeah. And then...
Speaker 3: How do I go back to my UI perspective? How does that work.
Speaker 2: How does it work? You upload the PDF, and then you can take extracts out of the PDF, circle bits in the document, and then draw it out to your whiteboard side of it. You can link multiple documents to the same whiteboard so that you can sort of see this. So we're talking about, I think, this, but on a scale where we have dashboard, banking, telephoning, witness statements, depositions, everything in the same whiteboard.
Speaker 1: And if, let's say, we didn't implement a component that can handle, for example, a telephone directory kind of data, and we have other components. So we thought, okay. Our... Dashboard, you know. infinite board, I call it space. Our space cannot handle the telephone data. So, we will create a separate component for the space.
Speaker 1: and then implement it and we'll start adopting the new way of telephone data. So, the possibilities are infinite in this way, and that's how lots of people works. That makes sense how the logically things are working.
Speaker 3: Yeah, yeah, yeah, I do like the idea.
Speaker 2: And then you can take the ideas from the whiteboard, and output them to, you know, a presentation, or to your notes or talk to the court or when you're drafting documents and things like this.
Speaker 1: You're gonna make a rough picture of that, right.
Speaker 4: Yeah, if you want. I've got my pen.
Speaker 1: Oh, that's a good thing.
Speaker 3: Yeah, I'm trying to figure out how we... It'll be just like that, won't it? Like a whiteboard.
Speaker 2: Yeah, so the way I see it, if you've got. your workspace.
Speaker 1: your whiteboard, it's now going to have to be a working monarchy's.
Speaker 5: infinite.
Speaker 2: whiteboard, and then like it is on here, and then you might have like a sort of... You've got your widgets in here.
Speaker 6: yeah? So you've got witness statements, you've got phone data, banking data, and what else? Expert evidence, exhibits...
Speaker 2: filings, orders and then you can go through these things and you see on your widget you know on its phone widget and then maybe the phone widget will come up here so you can see it bigger and then you can select a piece of data drag the piece of data onto your whiteboard then you click on the witness statement widget that will replace the telephone data and then you can read the witness statement yeah you can circle a part of the witness statement and drag it onto your.
Speaker 2: whiteboard yeah and then when you see it on the whiteboard you can you know there'll have to be some kind of visual representation of it if it's the witness statement you can have the text if it's the witness statement.
Speaker 1: we can you know crop the certain portion yeah link to the.
Speaker 2: and then you should you need to be able to click on this and it'll take you back to this yeah or you know back to this but it's always yeah, It's always grounded in the original material.
Speaker 1: There will be, you know, in the bottom, there will be a, you know, chat system. Chat here? Yeah. Yeah, okay. We can ask the AI as well to find the references and these kind of things or help us out. If we want to convert, for example, like on the left side, we have a document for the phone data, for example. And we ask the AI, what, okay, convert the, you know, telephone data into the historical graph or whatever graph it wants, whatever the position wants.
Speaker 1: So he will, you know, grab the data and, you know, convert to it and display here. And it will, you know, points to the original document as well. Yeah.
Speaker 2: I mean, look, I mean, if we can do it, it would be great to be able to, like, say, here, you know, the questions we were asking yesterday, you know. what day did X call Y, or what did Mr Smith say about something on this day, or something like that, and then it can bring it up here. Are we going to make this collaborative so that anyone who's got access to the case can see that on the whiteboard.
Speaker 1: But we have to send the privileges who can.
Speaker 2: So there should be a lead on the case, and then there should be...
Speaker 3: Aren't we setting it up like that anyway? each case you have lead and then you have your staff members yeah yeah so it should be a case lead.
Speaker 2: and it should the case lead should be the one who is able to give permission to you know a junior or one junior to edit the whiteboard yeah and then at the end of it we should be able to select from here what we want to output and then we can help out i don't know some kind of you know either you know a bullet point document or a media file that's like some kind of presentation yeah what they do on that trial pad you can output it and then you can use the.
Speaker 2: ipad to um with either chromecast or um apple tv and you can you can project it onto the screens, So that you can use your ipad to do the presentation. You know what they build their software over.
Speaker 1: I don't know how many years and months, with the X team, I don't know, but we This is.
Speaker 2: This is what we can say the last page. Yeah. Yeah. I mean this is where we were talking yesterday We were saying let's plan from the start, To build in the possibilities. Yeah to have the integrations that we want at the end Yeah, I mean that if we can if in the end we can get from start from case to presentation.
Speaker 1: Yeah, then it's sort of possible. Yeah. Initially we can can do all of these functionality at once. Yeah, We don't have a big team.
Speaker 2: I'm not saying you should be able to do that presentation thing in six weeks, maybe seven. Okay so this is what we're thinking yeah and then in terms of um yeah we just need to think.
Speaker 3: clearly how we're going to set up in terms of the infrastructure so everything can flow from there. Are you looking at sort of document ingestion at the moment or just permissionings onboarding.
Speaker 1: I don't think so, I don't think so. Okay.
Speaker 3: Say that again? George? Yeah we need to we need to have a chat about document ingestion uh maybe using like a OCR model.
Speaker 2: Yeah we looked at that briefly yesterday didn't we.
Speaker 3: That's extraction um then chunking but that probably falls within my remit.
Speaker 2: So you are looking at the onboarding process at the moment, what we talked about yesterday.
Speaker 3: Yeah.
Speaker 2: So how are you doing that? You want to look at this document.
Speaker 3: What is the job onboarding.
Speaker 2: So our onboarding flow is client, and then we talked about KYC, AML, conflict, and then.
Speaker 6: access to limited dashboard, then we have review by lawyer, issues.
Speaker 3: What does the client do.
Speaker 6: TC and letter of engagement. How do you do that? Yeah.
Speaker 1: and it doesn't take their access to dashboard okay i i think there's an issue here there's always an issue uh yesterday um we planned like if if our client is coming from the marketing and he you know came to our uh platform and he just signed up he processed the kyc at that time uh he have to.
Speaker 1: make a purchase or subscribe to the certain um you know law firm uh instant because when he signs up nobody's lawyer with him no there's nothing nobody knows so he had to subscribe to certain firm, then he can open the cases then the lawyer will be assigned on based on that you know the case but he's got to be onboarded he's gone before he opens the case yeah not onboarded but a partial.
Speaker 2: uh you can say yeah so you can't you can't open the case without subscription without subscription yeah and without him signing the letters and the terms of agreement exactly exactly which is.
Speaker 1: provided you know uh by the law firm uh for the subscription yeah once he would agree with this.
Speaker 2: terms of conditions and what we were talking about was sort of the subscription being like a sort of, tokenized thing so you're getting a certain amount of tokens for a certain amount of money and those tokens count for a certain amount of work or maybe you can we can only basis token.
Speaker 3: like one token or like yeah when you think about the payment model but we could do payment model based on, The thing that kind of cost us are document storage, potentially a case to charge them on their number of documents to help on each case.
Speaker 2: Well you see, in my head, the way that it works is this, because we're focusing on start-ups, SMEs, and the plan is to replace in-house legal teams or to be the in-house legal before they bring in in-house legal. So we want the subscription model and in certain circumstances, at the outset, it might be, and...
Speaker 2: it's more like it's a big part but they don't have a case to open I mean they're just they're subscribing in the same way they have insurance in the same whether you have an accountancy team in the same way that you have you know so that if they're going for example on the raise or if they're doing or if they're scaling they've got access to this and we can say that we've got access to it yeah so that's the first you know that's the sort of subscription model then it might be that they need more time with some of the payment yeah so I think I think monthly but I mean it might be that so that's it might be that we're.
Speaker 2: guided to a certain extent by the lawyers that we partner with because they're gonna want to have a say in how things are built from there and but the way I see is initially you're going to need like document production rather than document storage so you're going to need like, NDAs, shareholders agreements, intellectual property protection, employment contracts, those sorts of things. So we're generating documents. And these things generally aren't, you know, shareholders agreement in a really complicated.
Speaker 2: case is going to be like 50 pages long. So it's a tiny amount of, it's a tiny amount of data. So in terms of billing the client, then, you know, billing them on documents, but the outset isn't going to work. There aren't going to be huge amounts of it. So I think have this sort of token either that's ours or whether it's token and then build into the agreement. if you have a case the case is dealt with on a separate basis you know that you know that you don't you don't get a three-year multi-million pound lawsuit for 150 quid a month and it just.
Speaker 2: doesn't work like that and so you know then we can switch to working out how much it's going to cost to store the documents and things like that and you build that into the quote that the law firm.
Speaker 1: gives yeah i just have an idea yeah like if i open i plan and i open a case against for example the google and then when our case will be received by the law firm they will you know sort of the case and based on that they will set the how much you know they're gonna cost early or yeah yeah so.
Speaker 2: because because there will be different kinds of agreement yeah so if you're, say you're suing coca-cola.
Speaker 1: It's a big case, and they won't have two, three, four, five, maybe a large scam, or five cent people who want to work together.
Speaker 2: They'll have what's called a CFA, so they'll have a conditional fee agreement. So the client might not necessarily pay the money upfront, they might say to them, we will cover your legal fees, because we think you're going to win the case, but we want 50% of the money that you get from Coca-Cola at the end of the case. So that's quite often how you fund big litigation, is the client doesn't pay upfront. Then we can have an agreement with the law firm about that. And also, one of the parts of the model is this case prediction.
Speaker 2: So part of what we're doing is, one of the things is that we're helping the law firm to decide whether or not the case is going to be successful or unsuccessful, by taking their data that they have about cases, that they've won, lost, and settled, and using... AI to read a case against the data and then produce a, you know, a predicted success. So and, you know, that's all a loop there, so we can be involved in all of that. But on the front end, charging the client, you know, it's just going to be this subscription,
Speaker 2: when I say tokens or something like that, works quite well.
Speaker 1: Yeah. If we, you know, using the token system, for example, a client have a hundred tokens, $100, for example, and his case is, you know, very big or complex one. So the law firm needs a lot of people to work on this single case to make success or whatever. So the law firm, before approving the case or accepting the case,
Speaker 1: they will, you know, they can set all the basis rate.
Speaker 2: Yeah well, so what they generally do is, in a case like that, you would, there'd be a separate letter of engagement, to deal with the case, yeah.
Speaker 1: These cases have a different engagement.
Speaker 2: Yeah, because, so, and then they'll set the hourly rate, they will, let me just, I'll show you, you've got a letter of engagement.
Speaker 5: erm, ch-ch.
Speaker 2: And except how. Subtitles by the Amara.org community, case, they set out the terms and conditions, money laundering, data protection, they say who's going to be working on the case, they set out the instructions and then at the bottom this is the fees and estimate costs. Different people charge different rates, depending on how senior they are. You'll then set out what's going to happen, here disbursements, expenses, who's liable to pay them, the CFA which is the conditional fee agreement.
Speaker 2: So what they're saying here is, what generally happens is that they do this, they take the case on, once they've issued this letter of engagement and that will say, fees equal x, and then they'll say, we'll give you a conditional fee agreement and at that point, the case is sent to someone to review it.
Speaker 2: and that review results in a percentage success, so if they say it's a 70% chance of success then this determines the proportion of the award, they're saying 50% success rate because they're taking on risk, they'll say we want 90% of your award, so if it's a 90% success rate they might say we want 20% of your award, 90% you won't get 90%, but the logic shows you, so we're doing this as well.
Speaker 1: but if they are going to try on this percentage, how is the platform going to deal with this.
Speaker 2: So here, we onboard the client. This is the normal onboarding of the client for the subscription model, for doing the start-up, for doing all the things that you would have. I do in-house legal for Phoenix. If there's an issue, I have emails every day saying, I need the contract, or I need this. This falls under this. Now, day-to-day work falls under this. If they've got a case that's going on, say an employee falls out of a window and they're getting sued for a million pounds,
Speaker 2: because, I don't know, he wants to keep selling, he's going to turn up and then he never does and he's going to push him out of the window. But say that happens, right? Then that doesn't fall under this agreement. It would be a separate agreement. And part of this... would say, you know, if there's a case where there's more than 5,000 pages or the value is more than 1 million pounds, it's not covered by the terms of this agreement or has to be covered by a separate agreement.
Speaker 2: So when they're in the dashboard, when they have access to the dashboard and they start a case, that case will be checked. to see whether or not it meets these criteria and falls outside the main agreement that's.
Speaker 1: for the lawyers to make a decision about. We can do this like single cases falling into the certain criteria. Yeah that's for the lawyer to make a decision. For every case we need a, letter of agreement between the law firm and the client and in that agreement they will put just like you showed me they would have you know cost estimation cost yeah how many people want to work. The way it's going to be funded. But it will be based on our credit system.
Speaker 1: not just the dollars but they will you know charge based on the credit.
Speaker 2: Well yeah yes but then there will be circumstances where it falls outside them.
Speaker 1: if in case or in these cases like the person did this has to be.
Speaker 2: absolutely yeah well that will not deal because the lawyers need to charge the money or they won't get the money back so if you win a case against someone the person that loses pays your fees and if they're paid if the client is paying fees in tokens then the person loses is gonna say I don't know you any money.
Speaker 1: because I'm saying like the game you know of the cases whose comes under the certain criteria yeah so so.
Speaker 2: This will be one client care letter, then if they open a case, like you say, separate client care letters for every case, determined by the lawyer, and the lawyer makes a decision about whether it falls in the token scheme or it falls in the different scheme. If it falls in the different scheme, they have to have a different agreement, and that's between them. We get our money then from the lawyer, because they're going to use our system to have them use the case. So they're going to use the other scientists and the data analytics and all of this, so.
Speaker 2: we've got a subscription from the client and a subscription from the lawyer.
Speaker 1: But how are we going to charge? We got the agreement, because we are the middle party, and we know what kind of agreement happened between the client and the lawyer, and based on that agreement, how are we going to charge? So you have a client, yeah.
Speaker 2: Yeah. this case is a subscription so we can we can that's easy we can take this.
Speaker 1: shortly based on the credit system we don't need to do anything mainly so say.
Speaker 2: we get a case that falls outside it yeah yeah okay so the contract the contract is between the client and the law firm yeah this is a case that falls outside this it's a big case okay the law firm then is under an agreement to pay us for, professional services okay and in this so this the amount that they pay us will.
Speaker 2: depend on this okay so we can charge them for so in this document I just showed you okay the lawyers in this document say. The first thing we need to do is to assess the prospects of success. We're going to go to a KC to get an advice, we're going to read all the papers and go to a KC to get advice. That's likely to cost you about £50,000 still to assess the case, but if we say that there's.
Speaker 2: a prospect of success and if you decide to go ahead with us, that £50,000 will come from the people who lose. If we say it's not going to succeed, you don't pay anything. But this is the risk. This is the risk. So they recover their costs because they will say it's going to win. So say the case has actually got a 90% prospect of winning.
Speaker 2: In order to make sure they recover their costs, including the £50,000 from the costs, they start reading. It's really going to cost them £50,000. Because they have lawyers that work for them and they'll have a KC who does work for them and gets instructive. He's getting paid for doing 10 cases. They get 20 cases in, he gets paid for 10 cases. And on the basis that he's getting 10 cases, he'll do this. But they say that this is going to cost you £50,000. The actual prospect of success is 90%. They evaluate the prospect of success at 70%.
Speaker 2: So that they can increase the amount of money they're getting for the award. Which over the course of 100 cases balances out and means that they're making a profit. Now they say that this work costs them £50,000. It doesn't cost them. But when they go to the other side and say we've done all this work as being the case. It's going to cost, let's just cost £50,000. They know they're probably going to get knocked down to £40,000 or maybe £30,000. Which is why they start at £50,000.
Speaker 1: So we need a member team as well for these kind of agreements. No, the lawyers do it. How are they going to do it? For example, they created that, you know, agreement. So the client and the law firm reached an agreement. How do we, as an intermediate party...
Speaker 2: So client and the law firm reached an agreement on the case. This agreement is, say, that there's a 70% chance of success and they're going to take 50% of the award plus cost.
Speaker 1: That's cost.
Speaker 2: So they get paid everything they spend plus 50% of the value of the claim. Okay, I'm getting to it. Give me a second. Okay, so first thing is we charge them for producing this number. Okay, so just like this KC here is charging them fifty thousand pounds to read the evidence and do an advice, We charge them here. We charge the law firm. Okay on a conditional agreement Okay, this is 70% hold on. We also have an agreement that we get a percentage of the award.
Speaker 2: Okay, okay, so we can reach this agreement with the law firm for professional services.
Speaker 1: So for this kind of work, we need a manual team as well A manual team? Yeah. To do what? To charge on this kind of bill Yeah, because I'm not understanding.
Speaker 3: Unless you want to use algorithms in the backend to figure it out, but then we can miss out. You mean the prospect of success? Yeah, yeah, well in terms of like the payment to you. The percentage? Yeah.
Speaker 1: yeah and that's what I mean like we need a man oh this is a girl this negotiates yeah the case was outside from the law firm platform so our member team will you know do the work yeah they will review the each agreement yeah and they know so the way I see it happening is that because the things are happening outside the platform nor within the platform so the.
Speaker 2: way I see it you have what the Alaska's for you the law firm asked us to review a case we already have the papers yeah and we have our so we have the papers that'll be reviewed by the papers as in the document already.
Speaker 2: So we have the papers, because the clients will learn from them, and we have access to them. We have the papers, we have our AI model that will summarise and will give us prediction of success. It'll also draft advice on the merits. So that's really just a legal way of saying how likely is the chances that the prospect case is going to succeed.
Speaker 2: Then, I'll review this to make sure that we're happy with it. We'll then send it to the lawyers, and me and the lawyers will negotiate. the agreement on a case-by-case basis now you know in five years time if we're doing a hundred cases a month then we'll need somebody else to do it yeah.
Speaker 2: but at the start yeah you can do it'll be me because this is going to be the emotional the heavy lifting yeah if I can see this and it's summarized the case papers and then I can see the prediction and understand why it's predicted it then you know that's that's a job of half a day maybe to do that rather than two weeks which is what it would normally take yeah so we so we can.
Speaker 3: do it and then we'll have an agreement with the law firm yeah turn into like a spread.
Speaker 2: betting firm yeah well that's what it is yeah that's what litigation funding is except that yeah so yeah but there's no risk to us because we're just a difference between, yeah the plan is that we at some point we become the funder as well okay yeah so if we can get this.
Speaker 3: right we can set up funds but here we're just taking about the delta between the ai prediction.
Speaker 1: and the legal prediction yeah why don't you live like if if law firm asking you for what a lot of them uh you know study the case based on the documents the client provided and they.
Speaker 2: prepared an argument and they sent to no it's okay so we have this advice on the merits here okay.
Speaker 1: So, let's see, we go through Glowthal.
Speaker 2: Glowthal, Glowthal.
Speaker 3: I can't believe you could buy a whiteboard and bring it on.
Speaker 2: It is good. Yeah, but it's like got a chisel or a marker. He's having like a bullet in there. Here we go. Okay, subscription model, yeah? It seems to be getting there. Anyway, subscription. We understand the subscription model, yeah.
Speaker 1: Yeah.
Speaker 2: Yeah? We're happy with that.
Speaker 1: Yeah, yeah. Okay, so then... Let's have one other one.
Speaker 2: So then here is case by case.
Speaker 3: Well, everyone needs a subscription to be...
Speaker 2: Everyone needs a subscription to get into this.
Speaker 3: Yeah, yeah.
Speaker 2: Okay, okay. Yeah. Okay, so case by case.
Speaker 1: Let's put it into the subscription.
Speaker 3: Yeah, draw that.
Speaker 1: Yeah? No, no, under the subscription. That won't make sense.
Speaker 3: Yeah, draw that.
Speaker 4: Okay, done.
Speaker 3: And then, say, there's a subscription on the client side, on the legal side, and then we've got to branch it through to your...
Speaker 2: Say, subscription.
Speaker 3: Yeah.
Speaker 2: Okay, that's number one.
Speaker 6: And then, off the subscription, we can have document, crafting, et cetera, startups, yeah.
Speaker 1: Ah, you're missing something.
Speaker 6: Yeah.
Speaker 1: In the subscription, we have the cases. Next branch... That's what's coming here. Yeah, then documents, you know, will come under the cases, not within the subscription. No.
Speaker 2: This is document drafting. This isn't us. This isn't the client sending us documents. This is us writing documents for the client.
Speaker 1: It's confusing. If subscription, in this when user will subscribe to X firm, now he wants, he can open the case for the head for the certain type.
Speaker 2: Yeah, let's go. So what you're saying is, no, no, it's principle. Okay, so subscription, the subscription. Yeah.
Speaker 3: Okay. And for, like, $100 client, $100 legal, this is just a proxy figure, obviously. We need to, we need to essentially go first thing, so the first thing what happens in the flow is that the client pays the subscription. Yeah. And we go from there.
Speaker 5: okay okay are we happy with this client page subscription yeah okay okay yeah okay now.
Speaker 1: what's the description like i guess you like the word subscription i think it's quite long.
Speaker 2: i'm just going to start writing s in this so covers so the subscription covers x.
Speaker 1: forget about subscriptions thing we can you know user did subscribe you just bought a token and, whenever he needs help he can open a case and the law firm will charge based on that case or we can do other thing as well so I think the problem is we're using the word you're using case isn't the.
Speaker 2: right word to you you don't need to use the key or no no there is a case there are cases yes but.
Speaker 3: there's but there's different so sound okay let me say no one wants to be clear about subscription okay let me talk with you is driver free yeah and then buy tokens from there and when you open up a case, The demanded tokens must then be transferred into that case that I paid for.
Speaker 2: Let me write out the flow in my head, and then you can ask me to do what you've done at the moment. I'm getting past stage 1 every five minutes. Am I? Because you're asking me so many fucking questions before I even get past stage 5.
Speaker 1: Okay, go ahead Ray.
Speaker 5: You finish it, I'll let me. Alright mate, okay.
Speaker 3: Yeah, we just need to, in every explanation we do, just bring it down to first principles.
Speaker 5: Hm? This is what it is. Oh, it's a lego. Well...
Speaker 1: Right he's so complex and so small. Everyone's a fucking critic. Okay the subscription. Come on I'm.
Speaker 2: going to sort you through it. Okay okay. We'll take questions at the end. Okay so we started with a client who subscribes. Okay. the subscription covers general legal assistance up to the value of x whether that we measure it in tokens or whether we measure it in hours and we can work that out okay it includes drafting standard documents agreements and stuff like that standard stuff that you'd use employment contracts, nda ip agreements shareholder agreements that sort of thing that you need day in set day out so this.
Speaker 2: is us we're placing the legal services well the law firm through us okay so okay obviously, everything's signed off by the law firm, Did this one as well? Yes, because we're not regulated so this is all this is all it's generated by us Okay, but has to be approved by the law firm to be sent out So that that way we don't have to be insured. We don't have to be regulated.
Speaker 1: They're doing has their name at the top of it. Okay. Yeah, everything will be done by the AI or by us.
Speaker 2: Yeah, but with them with their name. Yeah. Yeah. Okay, so that's under the subscription Yeah, they have an amount of work that they need doing of X value If they need any more of this work doing though, I'd have to purchase more tokens or increase the level of subscription However, you want to work. Okay. Okay, so this we can call it a call it agent mode or call it something Okay, okay, because in my head, it's not a case. Okay, so a case is, A set of proceedings against an individual or a company. Okay. Okay. So that's what we call a case.
Speaker 2: Okay, on a case-by-case basis, Fees are determined separately, you need a subscription to access, but it doesn't fall under the subscription model.
Speaker 1: So what kind of subscription is this then.
Speaker 2: We have two models here. You have to be a subscriber to access any of the system.
Speaker 1: Okay.
Speaker 2: So all I've written here is, need subscription to access, because you have to be a subscriber to go down this route.
Speaker 1: Okay, so what kind of subscribe is it and how much is it going to cost to use it.
Speaker 2: If you're subscribing for say $100 a month. Now that gives you access to this. Okay, and access to this board. Yeah, okay But you know you don't pay you don't pay time for the cases. Yeah, you know pay tokens to go down this route.
Speaker 1: Okay, but you just need to have a subscription to access the system. Okay, okay And for this subscription user account, for example, I'm a client at that purchase and I subscribe well, I got hundred tokens and, that hundred tokens going to be, Consumed by all based on all the pieces, If we subscribe for this kind of things, right? Let me make it more simple.
Speaker 1: If I'm a client, I signed up, I provide KYC, AML, I've done everything, now I put my credit card or debit card to put a credit into the platform, now I have like thousand credit in my account now, so, and I want a few works like general area assistance and drafting documents. So that's it. So, how is going to be work, like for example, I got the thousand credit and how he going to work, make it work?
Speaker 1: I don't understand.
Speaker 3: Just give me how the thousand...
Speaker 2: Are you saying how much does an NDA cost or how much does this cost.
Speaker 1: For example, I'm a client, I signed up, done everything by KYC, ML, etc. Now I have subscribed to work and what kind of services, how I'm doing, you know. For example, I have a startup and I want somebody, I don't have anything right now, but I may have in future, yeah, and at the other end, we're calling case for any kind of work.
Speaker 1: okay but here we have a subscription model like for example if I have a new startup and I bought a thousand credit in my account and I don't have work right now okay and I just subscribe for the X firm with X firm to cover me or provide assistant in future if I need it so my credit will be consumed based on hourly basis for example if we the law firm charging like one credit per hour.
Speaker 1: or two credit per hour so based on that it will consume based on hourly basis and if after ten days he needs some kind of work how he going to, make a, you know, request, what kind of terminology he can, like, he can open tickets, how he going to...
Speaker 2: So he's going to come through the, so he's subscribed, he's got X number of credits, he has got access to the platform now, because he's subscribed, then he can ask in the dialogue with the AI, I need help with this, then that will send the flagged ticket for the lawyer, and then the lawyer will be able to write back in the chat and say, hey, we can help with this, it's going to cost you this number of credits to do it. They can say, yes, I agree to that. And then...
Speaker 1: That's the case as well, right? Or not.
Speaker 2: No. So a case, a case is a set of proceedings against a person or a company.
Speaker 6: Okay.
Speaker 2: So, if Olay versus Coca-Cola is a case, drafting a document... it's not a case but what kind of technology we can that's what i'm saying agent mode you want.
Speaker 1: to call it whatever you want to call it but if we call an agent uh for it if he have a book and at the moment i don't i didn't write yeah okay yeah yeah it's much better now if um let's say generally subscription uh if you know i signs up for the let's say that take the example of chat gpd if i do not put my debit card subscription and i'm not using it uh it's up to me yeah but.
Speaker 1: they're going to charge me on based on monthly basis yeah and if i once i can open the platform put a query in the chat box and i got you know responsive yeah and here we have um like. uh here we have a subscription model for our based on uh we will charge on pay you know, for example client subscribe to the firm two they are charging uh for drafting this kind of things.
Speaker 1: uh five tokens per hour uh x uh firm one charging three tokens per we're not turning into a.
Speaker 2: marketplace where we are like we were talking about yesterday we are working law firm powered by car we are law firm powered by car so this all of it is bespoke to the law firm that is attached, So we're not a marketplace, we're not saying this one's cheaper than that one, or this one's better than that one, or this one's better than that one, because we don't want to get into a situation where we're recommending law firms, because again, that leads to issues potentially with liability if the law firm focks up, so we're not doing that.
Speaker 2: So what we're doing is, we are going inside the law firm to replace the law firm's secretary, or the law firm's junior, or something like that. So here, there will be, just let me say this, let's call them tokens from now, so then X number of tokens will burn every month. Y number of tokens will remain in the account.
Speaker 2: So you can carry them over. Okay. What are the Y tokens? Say again.
Speaker 1: What are the Y tokens.
Speaker 2: It's just X and Y. It's a number.
Speaker 1: No, no. Do we have two different kinds of tokens like X and Y.
Speaker 2: No, no. X is a number. It's an amazing number.
Speaker 1: Okay, okay.
Speaker 2: We've got 100 tokens.
Speaker 1: Okay, I got it. 10 more birds. Yeah.
Speaker 3: We've got 90.
Speaker 1: Yeah, I understand.
Speaker 2: 10 is X and 90 is Y.
Speaker 1: Yeah, I got it. Okay. So... like for example I got I just want to open a case against the Coca-Cola wouldn't fall yeah so then we'll go down this route yeah for in the subscription because in my head like there's two projects for the client to work like one subscription model in this subscription model we we offering okay if you subscribe we will cover you this but how are chilling actually is going to.
Speaker 1: work like am I going to open a ticket like to get some sport yes that's what.
Speaker 2: that's what we're saying so follow it down the subscription so think about it as a retainer you know our retainer it so so I work for a company I get paid I, won't say X I get paid fifty thousand pounds a year store, I get ten thousand pounds a year, to work for this company. This company pays me £10,000 a year, whether I pick up the phone to them or not. They pay £10,000 a year because they know that if they need to pick up the phone to.
Speaker 2: me, I'll answer the phone. So that's this here. So you're paying a certain amount of money every month because it means that you get me, or you get this law firm. So that's this burn. The second thing is, I would say to them, the retainer agreement I have is, I'm going to charge you £10,000, that £10,000 gets you 10 hours of work over the course of the year. If you use 10 hours of work, I'm going to charge you £150 an hour, £200 an hour.
Speaker 2: That's the same sort of thing as we've got here.
Speaker 1: We need a general agreement for the subscription. That's the same sort of thing as we've got here. but it could be you know but it's an agreement with the law firm not with us not with us but.
Speaker 2: they've they've issued when we went through the the process the flow before the law firm accepts the client they have the clients to accept terms of engagement and the lesser in the terms of engagement it will explain this is what it's going to cost you a month for this amount of money a month you get the provision of our services and you get 10 hours of work or you get 10 tokens or whatever it is okay when you've used up this 10 hours work it's going to cost you 300 pounds an.
Speaker 2: hour or something like that yeah but that you know so but all of those numbers are set by the law.
Speaker 1: firm yeah okay so i we have to create a uh admin dashboard that can control this kind of yeah, you know the credit system and it will affect the credit system as well also agreements this thing as well because if they said like 100 period per hour so the, agreement would be changed accordingly yeah yeah well why are the tokens being.
Speaker 2: transferred to which I think we transfer this burn so they have a minute they have them I don't know whether we want to call it tokens until I know when he's over complicated I think we definitely are but you know it's just about met a measure because what we want to be able to make what we want to make it clear is that you're getting for your hundred pounds and a portion of that hundred pounds a month goes to just having us available to you yeah and you can spend another portion of that hundred pounds a month and getting work and the work.
Speaker 2: portion will carry over to the next month. So that's why we sort of thought of this.
Speaker 3: But how's the illegal company getting paid then.
Speaker 2: Well then the subscription will be a subscription that we divide between us and the law firm. Okay. This subscription isn't really where we're going to make the money.
Speaker 3: Yeah, I know. What I'm saying is these, the tokens, if you call it a token, will have to transfer to the law firm then, won't they? If we've got an agreement in place between us and the law firm.
Speaker 2: Only if they're really a measure of value. It's just an indication of how much time that they've got in the bank, isn't it.
Speaker 1: Let's say, put it hours instead of token.
Speaker 2: Call it hours. Hours, yeah. Call it whatever you want. I mean, I just think that tokens is easier for, if we're going to be targeting startups in DIFC, then I think tokens is...
Speaker 1: you know it makes us look but I guess we do at work basis which I said if they don't have work how the token going to be consumed if if we are consuming the token based on the hour or time then what it accurate hours or minute do what is I mean if we doing one based on minutes but like there has to be a.
Speaker 2: certain amount of the subscription that just is the subscription it's a lot we talk about a retainer so if I'm on a retainer I'm getting that ten thousand pounds whether I never speak to these people or though I do sense that sweet sweet speed I'm getting it whether I send one email or whether I send 20 emails yeah so that's the point the point is that is to have the person available on the end of the phone okay or through the map okay so.
Speaker 1: uh in in the subscription model um flying is going to open their different tickets.
Speaker 2: based on his uh uh yeah can you in the chat he'll say can you have it can you have it with it can you draft this document for me i need this i need that okay so subscription model uh.
Speaker 1: would work like this uh he will have a chat box for the ai and uh the real agent as well mm-hmm he can ask the question okay i need to complete this uh can you help me this is the document name yeah and uh the legal uh guy will help him okay yeah so they put say.
Speaker 2: they put in the chat box okay we've developed this great software we need to protect the intellectual property can you help okay and then that will flag up to the lawyer, So the AI agent will say to the lawyer, this is the query, and then they'll be able to have a chat with this person and explain, this is how many correct tokens are ours, where it's going to cost, this is what it's going to do, are you happy for us to carry on? Yes, and have this dialogue.
Speaker 1: Okay, so the client paid 10,000 pounds annually and now he has a subscription. He just made a query by the chat, like I need an IP against my software. Can you help me out? Then the law firm, the agent will connect with him.
Speaker 2: So it goes in the AI, the AI flags it on the lawyer's dashboard and it says Client A needs help with this. And then within the lawyer's dashboard, they can assign someone to deal with it. And then that person will contact the client. How are they going to contact the client? Through the client's dashboard. Okay.
Speaker 4: So I need to be able to contact the communication system. Okay. So that's what I've done. That's what I've done.
Speaker 1: yeah I thought we had a chat in the dashboard yeah but the thing is, which I implemented in a dashboard I open a case case goes in all of the agent dashboards and whoever accept the case will know you can check so it.
Speaker 2: witness like it needs to the clients does the client has subscribed we can.
Speaker 4: pop this yeah define my query into the AI and I like to admin dashboard.
Speaker 1: I think we should introduce a discrete chat system just like the mail like they. don't need to be you know online at the same time for for discussion so the yeah.
Speaker 2: sort of an email email yeah so so asks the AI the AI flags to the lawyers admin.
Speaker 1: dashboard okay it will create a new ticket for the AI firm yeah they will.
Speaker 2: review it they will assign a certain person yeah yeah so the AI will show it type in the query and client it will give them the information okay they the admin and assigns lawyer yeah. contacts the client via what yeah what what is it say again uh five by the client's.
Speaker 2: dashboard so you can either have it as a chat or you can have it as a message or an email like an email sort of thing or whatever whatever you want doesn't have to be a live chat okay like slack.
Speaker 1: messaging system yeah yeah like that you know in a slack or any chat system uh two person have to be uh on the same under the same channel yeah in order to communicate if if the admin assigned certain person uh to to help the client, how they're going to communicate, they don't have, how they're going to, I'm thinking logically.
Speaker 3: Can they not add this lawyer, this channel? So the client query will be a chat between the client and the admin account, and then the admin adds the lawyer to that chat, if that makes sense.
Speaker 2: Okay, yeah, that makes sense, because it means that the admin should be able to see the contents of everything, so all the chats and everything like that, because you have to make sure that.
Speaker 1: Okay, okay, yeah, I got it now. When the client will subscribe, it will connect with the admin, and once he'll make a query or open a ticket, now admin will assign somebody to assist the client. they can communicate with a live chat or whatever we have in our platform and so.
Speaker 1: admin can remove or add persons from the chat yeah okay because it might be that you know.
Speaker 2: so i imagine the way it would work in the law like in real life is that, you know someone will come in and ask a question to the to the admin, they would then say, okay, it's a contract question. They would then go to a junior person in the contract department. That person would then speak to the client, get the information, make sure that, you know, if there needs to be another agreement, then all of that, they'd do all that. Then, only then, would a more senior person become involved.
Speaker 2: when this person, or in our case, the AI, has looked at the case, has done this, and settled that.
Speaker 1: Yeah, the issue, what I'm seeing here, I you know give power to the cases in the dashboard so far you've seen yesterday in the dashboard so now our case is you know our powerful object just like a home object oriented yeah it is oriented here yeah and in this case we don't have any case okay so it's picture model so and the problem.
Speaker 1: but I've seen okay let's think about it this way that we have to create a case.
Speaker 2: is in this one so just think about this one that's that's the moment this way, When a client comes to a firm here, in the real world, they will open a file for the client. So imagine like a filing cabinet, and in that filing cabinet, it's every piece of work, every communication, everything that's to do with that client. So whether they open a case, whether they ask someone to draft a contract, whether they do anything like this, everything's in that client file. So when they come into the system,
Speaker 2: we open a client file for that client. And then everything underneath that.
Speaker 1: let's not get hung up on the term, call it a case if you want, you know, call it, you know, call it. Let me explain one thing, like for example, if you subscribe to...
Speaker 2: Let's call these, let's call these... actions okay yeah and so you have an action we have a case okay but they're.
Speaker 1: all in the client file okay for example user subscribe and he request he opened a ticket for for IP thing and then later after a month he again opened a new ticket for second software everything and the problem is like if we, make all things at one place there'd be you know some kind of each one of those.
Speaker 1: two things would be a separate action for example if he uploads a 50 or 60 documents for in a subscription panel and now he wants another software the things will be you know mixed with each other so every new ticket we need.
Speaker 2: separate panels for you know you know what do to do make it yes so like if you open a clock you have a client file imagine the client for like a filing cabinet in every case of the different drawer and fine cover yeah so.
Speaker 3: if you think of like a other like it the data warehouse.
Speaker 1: The data was essentially like how we're going to distribute and distinguish between different kind of requests, like if he, You know open a ticket for for software one and then after a month he wants I and their five I could get for software to yeah, we can mix the files together Now if it will be under come the subscription thing, Everything is here. So it.
Speaker 2: You know, you know, yeah, I've got the client file Yeah, and then underneath the client file you'd have, IP1, IP2 shareholders agreement and, NDA and then you have say they open a case They have case and then you have and the things under the case documents, so this is the client file and then under each file for every action is a.
Speaker 1: separate folder okay okay if if but if user wants user you know upload the new documents these documents will be mixed together if we were here but I'd be one I'd be two I'd be a three as before the government I mixed I don't understand.
Speaker 3: what it is mixed together well not with when the documents, form part of the vault. Yeah.
Speaker 2: So in the vault is a client file, is the main folder, or subfolders.
Speaker 1: Yeah, let's say we have one cabinet, and I put one document in the cabinet. If I put the second, that's easy if we have two different documents. If we put 10, 20, 50, 50, 100, then it would be hard for me to find which file is relevant. But then on my laptop.
Speaker 3: You'll be able to file the documents. You'll be able to file the documents by subfolders within the vault.
Speaker 2: But on my laptop I have a case, I have a client name, and on the client name I have case 1, case 2, case 3, case 4, case 5, separate folders.
Speaker 1: Now you're referring to this case.
Speaker 2: Yeah. Because I'm talking about a case. But whether you call it a case or an action, it's the same thing. It's a different...
Speaker 1: piece of work yeah you know we i just in my mind i you know initially when uh sofa but i've developed uh is based on the case by case thing okay but okay so now we have two different models we've.
Speaker 2: got we've got stuck in this thing now about using the word case yeah okay let's call it whatever you want call each one of these different case well everything should permission off the client.
Speaker 3: dashboard though shouldn't it so it's one client dashboard yeah and then within uh vault or data warehouse and documents you have a following system like we have on a laptop i don't like.
Speaker 1: you having let me bring my laptop then we can um you know what i'm going from there though don't.
Speaker 3: you where you have like one you have like one client i can't we actually really suck on the.
Speaker 2: fact that it's not called a case because we're using a different word for it yeah i know well.
Speaker 3: i think we've got to make it clear to him, that everything should be permissioned off the client dashboard so the client dashboard is the god.
Speaker 2: and then everything comes yeah and so everything any interaction with that client yeah has to be within that dashboard and within that client as well yeah exactly every letter doesn't matter if it's a case or an option yeah so here we go here's the client dashboard yeah here's the client's vault yeah in the vault it's action case yeah action action whatever.
Speaker 3: whatever it is i think where from i think the way in his mind he wanted to set it up is a case by case basis so instead of the client dashboard being the sort of number one i think the client the case is number one so a client may have different cases are you different definitely yeah yeah so that's that's why we need to be aligned here just to just make sure that.
Speaker 5: okay, Thank you. that's very Bitcoin okay we take it you know this is the agent portal okay this.
Speaker 1: is a client in dashboard she's the client dashboard yeah yeah right now what we have we have a key system we don't have a subscription model like these let me have one see this one is closed, This is pending not approved by the law firm. This is approved. This is ongoing case like they said They have the you know chat system here did, Okay, and I have the documents here.
Speaker 1: This is a version when I can upload no updated documents But it it would come under the different version like two three four. Yeah, okay. Yeah with a sequence Okay, and, but now We got different, thing our model subscription if if, But the stroke the structure doesn't have to be any different.
Speaker 1: But how is my how the subscription going to work with the current? Land like how we come to charge.
Speaker 3: I think that the way it's structured at the moment, from what I can see, is you have a client dashboard at the top, then you have underneath client dashboard are the cases, and then you have different document vaults for each case. That's what I'm seeing at the moment. I think we're just getting confused around the word case, to be honest.
Speaker 2: Yeah, so there's nothing wrong with this. No. So whether you have one vault for the client, or whether you have a case-by-case or action-by-action vault, as long as if the law firm needs, or the regulator comes in and says, we want to see all the vaults relating to client X, as long as you're able to pull up all of the contact and communication, with client x then that's fine yeah it doesn't matter if it's ten a thousand volts i had one.
Speaker 3: vote with a thousand just stay like this just change the word case to something i don't know yet and this document right there it's okay to be tagged to a case but it ultimately also needs to be tagged to a client dashboard so we may have another tab here called vault which shows.
Speaker 2: all documents from all cases yeah yeah see when you go into a file when you go into when you when you bring a client up you should be able to see in relation to that client every contact communication every case that um the client so you know the fact that they've signed up the fact that they've signed this letter of agreement the fact that they've done this you know all of these things.
Speaker 1: now in development we have certain limitations how the law firm and the client can communicate with each other like let's say with this model we cannot achieve the subscription thing like for example okay we have a client we have a model so we have single model right now but the file structure is the same.
Speaker 1: whether it's whether yeah inscription or whether it's my model is the same let me explain we have gazed in here right now yes okay this is my cases yeah and in.
Speaker 2: your head if we're asking to draft a document that you that's a case, yeah yeah okay so it's any word that we do any piece of work we do okay yeah.
Speaker 1: okay that's fine okay so how is how the law firm can charge the line based on subscription how you know yesterday but I understood like you use it client can not open a case without subscription yeah okay so I said okay now client.
Speaker 1: cannot open a new case without any subscription to the any law firm and now we are planning to charge based on all the basis okay instead of based on work.
Speaker 2: for example you know yeah yeah i get it i don't tell me what the issue is i don't understand what the problem is uh you know we we're discussing different kind of models uh this is just a different way of charging somebody it's not a different file structure the file structure is the same call it cases call it whatever you want as long as every every piece of work that you do as a as a is separate in a separate vault in a separate folder however you want to structure it in and as long as all of that is accessible under the client name yeah so if you want to see.
Speaker 2: all of the pieces of work that are ongoing will have concluded in relation to that one client, you can see all of that as long as you can see all of the interactions between that client and the firm so all chats conversations letters correspondence and stuff like that yeah then that then this is fine there's no issue with this, They call it a case, call it a piece of work, call it whatever you want, it doesn't really matter, that's just me being pedantic, because as a lawyer, we use a different way of saying it, but as long as we're saying each piece of work is separate, then this isn't affected by the subscript, how they're paying for it.
Speaker 1: Here is the agent dashboard, the client uploaded the document, the agent can see his documents, everything, once he will update the document, he will see the conversion, the agent can see everything, but it's also based on the cases he accepted. yeah or he involved in which cases he can see his cases.
Speaker 2: for each client yeah you need to have like a you need to have the first sort of a front page imagine that sets out you know their details their KYC their AML make sure everything has like the I don't know what you want to call it you know what I mean like a front page for every client that shows they've signed this letter.
Speaker 1: they've done this I guess the signing and each and everything will be based on the case yeah but the initial onboarding that we're talking yeah we are the check mark here like if you agreed the okay you.
Speaker 2: need a client profile page is that the wrong way to put it no do you know what I'm trying to say what are you trying to articulate yeah, So, in the real world, when you open a client on a really old piece of case management software.
Speaker 1: In the real world, the case management works very differently.
Speaker 2: I'm just trying to articulate the idea. So, in the real world, you would have a client and everything flows down from the client. So, at the top of the structure is the client's identity and then everything flows from that. So, you need to be able to see everything under the client. And the way of doing it is to have the client's identity first and then you click through to the case management.
Speaker 3: There's an overview.
Speaker 1: it just shows you is that everything active cases are completed when you so when you click on.
Speaker 2: clients uh it's not a thematic yeah okay so that's what i mean okay so this i think this is what i'm.
Speaker 1: talking about if uh then this is the agent portal you know the admin one okay okay and uh agent you.
Speaker 2: mean the lawyer yeah a single yeah yeah okay but then the lawyer has to have an admin so the lawyer.
Speaker 1: yeah it has to be someone at the lawyer's office you can do you know we need uh two different things like uh law firm account uh admin account yeah that i'll finish it i don't know okay they will assign a agents or lawyers based on the case yeah yeah then it's this these need to have access to everything yeah yeah so they need to have this yeah they need uh they can see uh super rights.
Speaker 1: i you know i also built it.
Speaker 5: It means yeah, okay. Okay. I created this one.
Speaker 5: I don't know.
Speaker 1: I saved the key and I forgot the password. I saved the password but admin, super admin, like the law firm, main admin requires a key as well.
Speaker 4: We lost Oswald. We lost the boss over on our own set still.

## Oliver OS Classification

**Summary:** Comprehensive 86-minute meeting covering the Qanun platform's infinite whiteboard feature for legal case analysis, client onboarding and permissions flow, subscription/token billing model, document management, and communication systems. Key outcomes include agreement on a subscription-based access model with tokens, distinction between subscription-covered general legal assistance and separately-billed case work (including CFAs), and plans for AI-driven case prediction and document ingestion.

**Key Decisions:**
- Subscription required before clients can open cases; tokens/credits represent work entitlement
- Standard legal documents (NDAs, shareholder agreements, employment contracts) covered by subscription; litigation billed separately
- Case lead controls whiteboard editing permissions; collaborative work supported with role-based access
- AI integration planned for case prediction, reference finding, and data conversion
- All legal outputs must be approved and signed off by the law firm, not the platform

**Key Open Items:**
- Define document ingestion process and OCR model integration
- Clarify manual billing processes for complex case agreements (CFAs)
- Develop admin dashboard for credit/token management and agreement terms
- Define criteria for when cases fall outside standard subscription model
- Resolve terminology confusion between "case", "action", and "ticket"
- Assign responsibilities for extraction, chunking, and onboarding steps

**Projects:** [[01-Projects/Qanun-Platform]], [[01-Projects/Dubai-Law-Firm]]
**People:** [[02-Entities/Oliver-Cook-KC]], [[03-People/Tai]], [[03-People/Gabe]]
