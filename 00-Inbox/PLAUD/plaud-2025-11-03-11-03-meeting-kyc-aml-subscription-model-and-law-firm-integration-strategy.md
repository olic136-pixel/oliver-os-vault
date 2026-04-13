---
source: plaud
type: inbox
file_id: 72061c55c6c6d60754fd4d5654550298
title: "11-03 Meeting: KYC/AML, Subscription Model, and Law Firm Integration Strategy"
date: 2025-11-03
duration: 22 min
projects:
  - Qanun-Platform
  - Dubai-Law-Firm
people:
  - Oliver-Cook-KC
  - Tai
jurisdictions:
  - England & Wales
  - UAE
tags:
  - KYC-AML
  - subscription-model
  - client-onboarding
  - law-firm-integration
  - SaaS
  - token-credits
status: active
last_reviewed: 2026-04-09
---

# 11-03 Meeting: KYC/AML, Subscription Model, and Law Firm Integration Strategy

## Summary
## 🔑 Keywords
`KYC/AML` `Legal Platform Subscription` `Law Firm Partnership`

## ⏰ Meeting Information
> Date: 2025-11-03 14:35:56
> Location: [Insert Location]
> Participants: [Speaker 1] [Speaker 2] [Speaker 3]

## 📝 Meeting Notes
- Topic Title: Current Service Focus and Target Customers
  - The platform currently provides corporate legal services for startups, covering corporate, employment, and commercial law.
  - Initial strategy is to partner with a single law firm and operate within its framework.
  - Target market is startups/SMEs; the concept is to replace or complement in-house legal via subscription.
  - Users may onboard without an immediate case, seeking reassurance and readiness for future issues.
  - Conclusion: Stage 1 focuses on integrating with one partner law firm, serving startups via subscription.

- Topic Title: Onboarding Flow and Conflict/KYC/AML Checks
  - Proposed flow: user signs up via marketing or referral link; creates an account with email/name.
  - Automated KYC/AML checks, plus simple conflict checks using the partner law firm’s database.
  - If cleared, the law firm issues a client care letter and terms of engagement through the platform.
  - Discussion on when to collect case description:
    - Speaker 1 suggests capturing service selection (tick-box) early.
    - Speaker 2 prefers separating sign-up (person-level) from case creation (case-level details).
  - Conclusion: Keep sign-up and case details separate; case description is provided when opening a case.

- Topic Title: Dashboard Access and Case Creation
  - After sign-up and KYC/AML, users receive limited dashboard access.
  - Users can create a case; suggestion to include a short case description field or service selection at case creation.
  - Ultimately, everyone gets a “full dashboard” once onboarding steps are complete.

- Topic Title: Platform Architecture and Scope (Stage 1 vs Stage 2)
  - Stage 1: Operate within a law firm’s “bubble” to avoid direct regulation and rely on firm’s insurance and compliance.
  - Stage 2 (future): Public-facing model (e.g., kai.com/kai.ai) that routes inquiries to relevant law firms.
  - Dev perspective: build a generic, upgradeable, universal system with configurable guardrails to avoid future rebuilds.
  - White-label options: law firms may brand practice areas (criminal, employment, etc.) while the platform remains SaaS to the firm.
  - Conclusion: Build an adaptable platform now, with initial deployment inside the partner law firm.

- Topic Title: Regulatory Considerations and Liability
  - The team aims to remain within the law firm’s regulatory coverage.
  - The platform should not charge clients directly to avoid liability outside the firm’s regulatory framework.
  - Payments and terms are between client and law firm; the platform facilitates but does not act as a legal service provider.

- Topic Title: Subscription and Token/Credit Model
  - Subscription proposed as a token/credit model (e.g., pay $100/month for 100 tokens).
  - Tokens represent time/usage for covered services (e.g., document drafting); large litigation is outside the subscription.
  - Tiered subscriptions offer varying token amounts; additional charges apply after token depletion.
  - Credits may expire (e.g., 6–12 months), with parameters configurable by the law firm.
  - Users must have an active subscription/credits to open cases; subscriptions are tied to a specific law firm.
  - Conclusion: Adopt a token/credit subscription managed by the law firm; engagement letter and terms define parameters.

- Topic Title: Marketing Focus and User Access Controls
  - Marketing will target startups to keep intake manageable, though public links may attract broader users.
  - Platform-level limits suggested to prevent spam and manage case volume.
  - Keep the funnel narrow initially to learn and maintain service quality.

## 📅 Next Arrangements
- [ ] Define and document the onboarding sequence in the product: sign-up, KYC/AML, conflict check, client care letter, dashboard access.
- [ ] Decide when and how to capture case description/service selection during case creation; finalize UI fields.
- [ ] Implement token/credit subscription logic with tiering and expiry, configurable per law firm.
- [ ] Integrate law firm-issued client care letter and terms of engagement into the platform workflow.
- [ ] Set access controls: require active subscription/credits before case opening; enforce firm-specific subscriptions.
- [ ] Align marketing messaging to target startups and SMEs; prepare materials to support the narrow intake funnel.

## 💡 AI Suggestions
> AI Suggestions
> AI has identified the following issues that were not concluded in the meeting or lack clear action items; please pay attention:
> 1. Specify exact data fields for KYC/AML and conflict checks, and define the automated verification provider/process.
> 2. Decide the precise UI/UX for separating sign-up from case creation, including where tick-box service selection appears.
> 3. Establish subscription tiers, token values, covered services vs. exclusions, and credit expiry rules.
> 4. Clarify legal responsibilities: ensure the engagement letter explicitly ties payments and services to the law firm, not the platform.
> 5. Plan for scalability: define guardrails for Stage 1 and the roadmap for Stage 2 public-facing routing to multiple law firms.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: Okay, so users done the KYC and AML and then you don't have to just provide a description of what they've won. At the moment what we're offering is effectively corporate services. So the model for now is that we offer to the client, we offer corporate services for startups. So corporate law, employment law, commercial law, that sort of thing.
Speaker 2: There's all kinds of things related to the case.
Speaker 1: Yeah.
Speaker 2: Not with the client. The client has that, you know.
Speaker 1: Yeah, yeah, I get it. But we'll have to have the description.
Speaker 2: Yeah, once you try to create a new case, we will... give him the detail like we we are offering this if he wants you know for any kind of criminal or any kind of or divorce or anything we will we can say apologize okay we are not.
Speaker 1: dealing in future yeah we don't have it right now maybe so at this at the sort of onboarding stage. so he'll have to have so let's say one marketing or whatever follows link yeah two limited dashboard yeah three ask to provide details.
Speaker 1: for KYC AML for automated check KYC AML conflict and the conflict there is just the details, of the company and the person so it's a really straight forward conflict check and how it works well because we are only working with one law firm at the moment we can check the.
Speaker 1: conflict against their database. So, in the way that works now, if you come into a law firm and you want me to do some corporate work for you, you go and speak to the secretary and she says, I need your name, I need your company name, I need your KYC, KML. And then they'll take your name and the company name and they'll just type them into the database to see if they come up. That's honestly, that's how straightforward the conflict check is at this point.
Speaker 1: So, we can do this because we have access to the law firm's database. So, check KYC and then if no issues, firm sends client care letter and terms of engagement.
Speaker 1: to the platform to the limited platform yeah for example um six client accepts. seven full dashboard okay yeah the picture in my head yeah it's like um.
Speaker 2: nobody has a full dashboard everybody has a full dashboard like for example user signs up from any kind of link marketing or he heard from his friend or from finding from the search engine, yeah now he's then you know on our platform and he just signed up now after signing basically putting the details the email name and this is so, now we are asking uh for the kyc or aml once he completed those details uh which we have been.
Speaker 2: going to get really good to get the automation like we saw that i see here we have done this now, uh we have the you know user have the limited access of the dashboard now user.
Speaker 1: now user have can create the case i think maybe we have to put in here 3.5 with me or 2.1 what you have there which is a short description of what it is that they want so you had here you know describe your case or or don't go for this one this is not no no but i think that thinking about it as we're talking yeah i think it makes sense.
Speaker 1: at this stage for them to say what they want, Even if it's a tick box, do you want this, do you want these services, or these are the services we provide.
Speaker 2: It's a part of sign-up.
Speaker 1: Because I think if we ask the KYC and AML before we've told them that...
Speaker 2: You know, we need to mix two things separate, very separate. Like for signing process, sign-up process is totally, you know, related to the person, not with his case. Once he will open the case, then we will ask, okay, description. What kind of, you know, catch-up key or whatever we want to get related to the case. Because we may have returning client.
Speaker 2: Last year he's done for divos, next year he's you know finding a business.
Speaker 1: The idea is that you are onboarding a company, a start-up, and that we stay with the start-up throughout their journey. So the idea is that this combination of our platform and the law firm replaces in-house legal for the start-up. And as it grows, the services that they require from us will grow. So they're paying a subscription for this. So really it's like a system by which they have the reassurance of having the in-house legal department.
Speaker 1: And in the same way that if we have a problem, someone picks up the phone and speaks to me, this is the same thing for them. So what we're selling them... is access to a law firm with resources they couldn't afford as a start-up on a subscription basis and as it grows obviously it will become more involved and becomes more valuable to the law firm. So the idea is to scale with the company and that we onboard the company and it may be.
Speaker 1: that at the point of onboarding they don't have a particular problem, it may be that they want to onboard because if they're going for example to funding and they want to be able to say we have this resource available to us if there's a problem or it may be that they do have a problem, it may be that they don't. So I think that's the way you have to think about it, that this is, the intention is to market it to start-ups, to small businesses, SMEs and then replacing or...
Speaker 2: Having from the start a legal team. Okay, I think, If we do the limits, To the platform, you know from the developer perspective, Once you know before you know start with men.
Speaker 3: How are you doing, how are you? I'm happy trying to avoid you. It's all days. I'm doing okay. Yeah good good. No, I plan it tonight So why on the night. So how are you good I'm good just a week.
Speaker 1: He's selling me a house.
Speaker 3: Can I get in with you.
Speaker 1: No, no, I'm fine. So think of it like that.
Speaker 2: Okay. If we will put a limitation in a platform, and in future if we want to...
Speaker 1: So what you're saying is from a dev point of view, you would rather build it... Yeah, have it available and then put the guard rails in and then be able to remove the guard rails.
Speaker 2: Okay, I understand. We will make a full, you know, adoptable, upgradeable, you know, universal kind of platform, So we can you know We will not get a headache whenever we want to integrate any kind of thing or service on any kind of A law firm interrupt. So we will make a generic system or universal system for all of the Not just for the startups for everybody. Yeah, but always.
Speaker 1: We've got the law firm. Yeah, and we sit here and here's the client Yeah, so we're sitting effectively. We are working. We're part of the law firm. So it might be that we white label it, and they and they brand it and they're like the criminal law or the employment law or whatever it is, but the way that these other sort of legal AI services work is they're not a bridge between.
Speaker 1: a client and the solicitor lawyer they are effectively part of the law firm so they're sass to the law firm so I agree with you that you know from a practical dev point of view you need to build it in such a way but this is our initial focus okay we don't want to say we're never going to do this now so you have to build it but this is our this is our focus to start okay I understand.
Speaker 2: now you create a big circle and the big circle is representing representing the law firm and we are within that law firm.
Speaker 1: because what we don't want to do is get in a situation where we have to be regulated.
Speaker 2: we are not regulating anything because because we are a software service yeah we are the software service and in a software uh suit we are providing you know we are getting the clients on board for the law different law firms and and we we already then but kyc are ready for the law firms you know they usually uh user goes to the law firm they you know they do the kyc they they get the whole detail a lot of things you know office work they do and then they start working on the case in our.
Speaker 2: case we you know remove all those things as a software provider we are we have already done these kind of things by ourselves, and the case is object in my head like we are the platform and we have the law comes under us okay and but we are not uh you know um legalizing the thing, if user for example if you just open a case for for fraud for example.
Speaker 2: we, you know, redirected with the law of fraud related law firm.
Speaker 1: Okay, so that it's like stage two or stage three. Yeah. Okay, so at the moment, at the moment, we're just inside the law firm. There'll come a point where if, say, we want to go public-facing. So say we want to have like, you know, kai.com, kai.ai, and then someone can go out and question and then they can be put in touch with the law firm, the law firm that we select based on the question that they asked. Yeah, that's stage two maybe, but what we're trying to do here at stage one is get that credibility by partnership,
Speaker 1: partnering with the law firm, get the data, understand the learning and everything else. And so that when we, you know, we can go out and take this model, like you're saying, we can go and give it to an employment law firm, or we can go and give it to a... criminal law firm the marketing is different you know the the cases are different but the.
Speaker 2: structure in the process is the same thing but if we go with this uh vision um we can expand we we will be limited uh you know restricted uh in future if we even wants to upgrade the platform.
Speaker 1: we have to recreate yes no i get it i get it but this is just what we need to do yeah.
Speaker 2: uh and uh if we do the you know opposite uh we are the provider law every law firms come under us but that in that stage too after the stage yeah yeah but but you know it will fulfill whatever we wants to to get it achieve it it will you know behave like if you can say like.
Speaker 1: okay we are coming under the law firm uh or in future if we have infinite numbers of platform.
Speaker 2: with us, you, they we can say they you know we encapsulate all of the law firm or we can say okay we are dependent upon those numbers we can vice versa we can say anything like because every case related to the relevant law firm and we have nothing to do with that we have that line we redirected the client.
Speaker 1: to the law firm but this this way we sort of narrow it so that we can rather than getting 10 000 people trying to get them through a public portal, There will be some people who share the link or whatever, but we're trying to keep it narrow enough that we can manage it, narrow enough that we can use it to learn from.
Speaker 2: Okay, for example, we are doing marketing, okay, and we are getting that, how are we going to narrow it? And for example, we market specifically to start-ups.
Speaker 1: We say that this is, replace your in-house legal or in-house legal from the start, whatever you want.
Speaker 2: But we are publicly available on the market, right, on the internet.
Speaker 1: But...
Speaker 2: So anybody can come, we can do it.
Speaker 1: Yeah, yeah, but you could, yes. Obviously, that's what I said, you can't stop people from clicking on the link. Exactly. But what you can do is focus the marketing... A bit.
Speaker 2: To let you do the start-ups. Yeah.
Speaker 1: And it might be that other people...
Speaker 2: That's the part of the marketing thing, we have nothing to do. So as I've done, so far we're... developer we as a developer I'm thinking like okay we have this platform is live but we can restrict the users to do and not do the spamming you know I understand now the whole thing you want to explain me and the best way my suggestion is to you know put the limitation on the each case is you know.
Speaker 1: we are bothering the people I'm saying they might they might not have a case at the moment it might just be okay we're starting a company we want to have the reassurance of knowing that if there's a problem we can pick up the phone yeah or not pick up the phone we cannot get I mean we cannot be quite okay.
Speaker 2: As a software provider, if a law firm or any company signs up and they don't have any specific case or anything right now, but they may have in future, they have started using our platform. In future, we can use it. It's an easy way to solve things. we can put a subscription on our platform to use it for example like for.
Speaker 2: example which are the X amount of dollars yeah as a provider, no we are no we chose a law firm okay okay not we can do the.
Speaker 1: board even yeah but not stop because once we start charging the client we're outside the law firm's regulatory bubble okay okay so we went once we start charging the client ourselves we're liable to the client okay okay so we want to stay inside the law firm's bubble okay be protected by their insurance be protected by their professional indemnity be protected by.
Speaker 2: their regulator okay okay so we can do one more thing here make it more advanced like, okay user can sign up you can use it or any firm can provide is the kyc aml thing now they are verified they can use now we can um show for example here a new page or panel where uh he can get the subscription of the law okay and now he's paying judas to the ex law firm not to us but to the law firm yeah and if anything happens uh it's not the case is the subscription method.
Speaker 1: if for example yeah so you you'd have it you'd have it like this you'd have, a subscription say you pay a hundred dollars a month it'd be more than that but say because it's an easy number yeah a hundred dollars a month buys you i don't know 100 tokens or 100 something, You can use those over the course of the month and there might you know, they might accrue they might not accrue, But once you've used up all your tokens or all your time, then you have to pay additional.
Speaker 1: So there are there will be things that were covered by the subscription and things that aren't So for example, if you want documents drafting and things like that pretty straightforward. Yeah, it's going to be automated by the system Yeah, so they'll fall under the tokens that fall under, you know And the subscription if you're launching a three-year case against coca-cola That's not really because of the agent, So, there's a certain amount of time represented by tokens that you get from your subscription.
Speaker 1: Different tiers buy you different amounts of tokens. Now once you've used all of those tokens, then you have to pay additional. Or if there's a big case or something.
Speaker 2: So you're eliminating the time factor. The subscription is not dependent upon the time, but the token or credit system. Yeah, I think that it makes it easier for someone to understand. Yeah, it's good for the clients as well. They would think like, okay, if we don't have any work or anything official, so why do we have to pay like $1,000, $1,500 a month? It's insane. It's like insurance. Yeah.
Speaker 2: If we're offering like... credit system so you know okay because I have we can purchase the thousand dollars trading okay so if we have an issue we can even after two months or three months or five months we can live put limits on the credit expiry yeah yeah okay if we would not use within six months or a year they're gonna be.
Speaker 2: expired yeah so and this subscriptions and is this limitations is we're not totally provided by the law firm yeah okay. software provider we the law firm could set those parameters yeah exactly that.
Speaker 1: will be contained in the engagement letter and the terms of service okay.
Speaker 2: okay okay I understand now we need to introduce the subscription or communication without the subscription user cannot open the case yeah if user don't have any credit or subscription user cannot if I have a subscription off from law firm a I cannot go to the law firm B I only can get open the case for the law firm a right yes okay yeah okay oh we are on.
Speaker 2: same page okay so it was yeah we've got enough to be getting on

## Oliver OS Classification

**Summary:** Meeting to define the Qanun platform's client onboarding flow, KYC/AML automation, and subscription/token-credit billing model for a law firm integration. The platform will sit inside a partner law firm's regulatory bubble, targeting startups and SMEs as a subscription-based in-house legal replacement. Stage 1 focuses on a single law firm partnership; Stage 2 envisions a public-facing platform routing to multiple firms.

**Key Decisions:**
- Keep sign-up (person-level) separate from case creation (case-level) in the onboarding flow
- Adopt a token/credit subscription model managed by the law firm, not the platform directly
- Build a generic, upgradeable platform architecture from the start to support future multi-firm expansion
- Platform stays inside the law firm's regulatory bubble to avoid direct regulation

**Key Open Items:**
- Define exact data fields for KYC/AML and conflict check automation
- Implement token/credit subscription logic with tiering and expiry
- Integrate law firm-issued client care letter and terms of engagement into the platform
- Finalise UI/UX for separating sign-up from case creation

**Projects:** [[01-Projects/Qanun-Platform]], [[01-Projects/Dubai-Law-Firm]]
**People:** [[02-Entities/Oliver-Cook-KC]], [[03-People/Tai]]
