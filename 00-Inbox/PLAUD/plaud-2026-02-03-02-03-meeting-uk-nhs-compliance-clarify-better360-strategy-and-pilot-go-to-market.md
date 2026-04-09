---
source: plaud
type: inbox
file_id: d79837033de50be51984fb52d029c4e4
title: "02-03 Meeting: UK NHS Compliance, Clarify/Better360 Strategy, and Pilot Go-to-Market"
date: 2026-02-03
duration: 30 min
projects: [Human8]
people: [oliver-cook, gabe, ammar, tai]
jurisdictions: [UK]
tags: [healthcare, compliance, ISO-27001, NHS, beta-testing, go-to-market, Clarify, Better360]
status: active
last_reviewed: 2026-04-09
---

# 02-03 Meeting: UK NHS Compliance, Clarify/Better360 Strategy, and Pilot Go-to-Market

## Summary
## Meeting Information
> Date: 2026-02-03 09:01:01
> Location: [Insert Location]
> Participants: [Speaker 1] [Speaker 2] [Speaker 3] [Speaker 4] [Speaker 5]
## Meeting Notes
- Topic Title: Market Context and Competitive Positioning
  - The team discussed an article highlighting fragmentation of US health record providers and the UK NHS’s unified advantage.
  - Concern raised about potential entry of US SaaS/AI companies; emphasis on moving quickly in the UK market.
  - Strategy proposed: rapid deployment into surgeries to build “stickiness,” making acquisition a more likely route for entrants.
  - Branding angle: emphasize British-built software to appeal to the local market.
- Topic Title: Product Portfolio and Regulatory Approach (Clarify vs. Better360)
  - Clarify: healthcare-regulated product focused on LLM-based compliance, document scanning, coding, triage, and NHS linking.
  - Better360: positioned as a wellness, direct-to-consumer application to reduce regulatory hurdles initially.
  - Decision to develop separately (“siloed”) now, with future integration potential for wraparound care.
  - Align Better360 with regulatory pathways (policies, security) despite not being regulated yet, to ease future accreditation.
- Topic Title: Technical Status and Integrations
  - Backend for Clarify’s LLM parsing engine completed; front-end deployable.
  - Document scanning and coding ready; ~250,000 documents referenced.
  - Need to engage Medicus for API integration; alternative is direct SNOMED access keys for international coding.
  - Twilio relaunch completed; speech-to-text engine done and to be linked with Twilio.
  - Azure templates, NHS mapping, and logic workflows prepared; request to share the internal to-do spreadsheet for team contribution.
- Topic Title: ISO and Compliance Planning
  - ISO 27001 (information security) required for AI/web security; ISO 9001 (quality management) already achieved previously.
  - UK-specific compliance referenced (including GDPR and NHS-related requirements; “DTAC” likely among them).
  - Accreditation typically takes 3–4 months; currently operate as “aligned, accreditation pending.”
  - Documentation-heavy process: create, brand, and operationalize policies with clear authors and enforcers; internal audits expected.
- Topic Title: Beta Testing Strategy and Operations Readiness
  - Aim to test the full user flow, not just the model.
  - Treat beta testers like real users: proper sign-in, verification, contracts (possibly via DocuSign), and SLAs.
  - Proposed limited initial scale: around “10 calls” sufficient for first phase to avoid overload and aid debugging.
  - Deployment considerations: web app first; local installation if needed due to NHS routers/firewalls; possible use of Mac minis.
  - Operational readiness includes receiving governance documents from the dev team (Sean/DEF).
- Topic Title: Go-to-Market Targets and Network Outreach
  - Target a small/agile clinic for initial pilot; avoid high call volumes early.
  - Potential contacts:
    - Amar’s network (including Beamer network contact awaiting a proposal).
    - Gabe’s NHS contact and a social media physician with a large doctor network.
    - Avoid conflicting channels where contacts are building similar products.
  - Clarification: Dr. Hamid discussions have stalled; current approach is to proceed independently and revisit later if needed.
- Topic Title: Team Coordination and Responsibilities
  - [Speaker 1] will share the to-do spreadsheet; team to populate responsibilities.
  - [Speaker 2] to review and assign items the team can take on, especially regulatory tasks.
  - Agreement to prepare a prioritized outreach list and terms for beta participation (e.g., free trial period, data/debugging value).
## Next Arrangements
- [ ] Share the action-item/to-do spreadsheet with the team for review and contributions
- [ ] Populate responsibilities and owners; prioritize items (regulatory, technical, outreach)
- [ ] Create a separate version of the plan specifically for Better360, aligned with future accreditation pathways
- [ ] Engage Medicus regarding API integration; in parallel, scope and obtain direct SNOMED access keys
- [ ] Link the speech-to-text engine with Twilio and validate end-to-end call flow
- [ ] Collect and organize governance documents from the dev team (Sean/DEF) for ISO 27001 readiness
- [ ] Define beta tester terms (trial duration, data use, SLAs; contract via DocuSign) and draft a standard beta agreement
- [ ] Identify and confirm 1–2 small “agile” clinics for the pilot; prepare deployment playbook (web vs. local install, firewall/Mac mini)
- [ ] Prepare and send proposal to Amar’s Beamer network contact
- [ ] Schedule a meeting with the social media physician contact through Gabe
- [ ] Populate the outreach list with names and contact info; assign owners and target dates; prioritize targets
- [ ] Decide on whether to re-engage Dr. Hamid after next week’s demo readiness
- [ ] Plan an internal simulation/demo for the four team members before the external pilot
## AI Suggestions
> AI Suggestions
> AI has identified the following issues that were not concluded in the meeting or lack clear action items; please pay attention:
> 1. The exact UK-specific compliance frameworks beyond ISO (e.g., DTAC and any NHS approvals) need clear identification, owners, and timelines.
> 2. The pilot participation terms (pricing, duration, data-sharing, and SLAs) are not finalized; draft a standard beta agreement.
> 3. API integration path (Medicus vs. direct SNOMED) requires a decision and technical scoping.
> 4. Operational deployment at clinics (web vs. local install, firewall constraints, Mac mini approach) needs a step-by-step playbook.
> 5. Outreach strategy prioritization is pending; risk of delay without assigned owners and target dates for each contact.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: Morning. Morning, you all right.
Speaker 2: I'm good, yeah, you.
Speaker 1: Not bad, not bad, thank you. Cheers. How was Dubai? Saudi.
Speaker 2: Yeah, good. And, you know, I'm just going to go and deliver this to my wife. Give me one second. I'll stay on the phone. It was good, yeah. I'm back again next week, next Wednesday.
Speaker 1: Get out. Just move there.
Speaker 2: Well, I think maybe that might happen soon enough. Morning.
Speaker 3: Morning, morning. You've shown your ID, right.
Speaker 2: Hi.
Speaker 3: A lady said she can bring a liaison.
Speaker 2: My ID? One second. Sorry guys, I've got another nine o'clock linked to a prison, so I'm going to do you guys first, and then I'm going to go and see someone else.
Speaker 2: Interesting article that, I don't see it as a competition, I see two things, a validation of this idea that wraparound sort of, you know, care in terms of what we're able to offer on the back end once we get better 360 going is going to be the direction of travel, and also that, you know, you guys have anticipated and dealt with the problems that the article brings up, so I mean, and also the thing that struck me is, oh God, sorry.
Speaker 2: I've just got to go and show them my face so that it matches my ID so they'll let me into the conference when we've finished. One second.
Speaker 3: Oh dear. They don't know who I am. What do they need? There's someone there. Yeah, she's on the link. Oh, hi. Thank you.
Speaker 2: Welcome to my life, guys. Two meetings at one go. Two meetings at the same time and one straight afterwards. i've pushed that one in i've got in dubai for a couple of hours so that we can have our chat and i can do it but yeah i mean the one thing about that article how many different health health record providers there are in the us i mean that's just insane because it's not unified.
Speaker 1: we've got an advantage because nxs is under one umbrella yeah i mean what uh what a massive.
Speaker 2: advantage that is i mean i suppose you know in terms it's a lot more cumbersome the nhs a lot less agile but a massive advantage to someone like us that we don't have to deal with they're talking about 5 000 different record providers 50 000 insane.
Speaker 1: No, too much, too much. It's a good article, good validation. My worry is, I'm not afraid of the UK, because the UK, I feel like there's a lot of catch-up going. The concern is, if an American company comes in, they will blow us all out of the water, because they've been, like, messing around with open AI the last 12, 24 months now, and they're more used to this kind of software as a service, you know, so...
Speaker 2: Well, I think the idea is, then, that we move quick, we get into as many surgeries as we can, and that when a US, you know, company wants to move into the market, then they see acquisition as the better and most friction-free route rather than trying to take over, because, you know, we know that these things are, you know, these systems, once they're installed, are fairly sticky, because we know how reluctant these practices are to make any changes at all. And so really what we want to do.
Speaker 2: is put ourselves in that position where if someone does want to come into the market, then they have to take us over rather than going to competition with us.
Speaker 1: Yeah, then we should always lean into the point that it's a British-made product. This is a British-built software, yeah. And, you know, hopefully people will buy us faster. So anyone heard from Ammar.
Speaker 4: No. Nah, I've been here as well, man. Let me give him a quick word.
Speaker 2: It's quite early in the morning for him, but we'll just have to crack on with it because obviously I know we're all busy. So, you know, I've got someone else on hold so that we can do this.
Speaker 3: Yeah.
Speaker 2: OK.
Speaker 1: Are you calling him, B? Yeah, yeah.
Speaker 4: That's what I'm going to call him. So just give me a sec. I'll jump back. One minute.
Speaker 2: Don't let me know once those funds hit your account.
Speaker 1: Oh, it's already in the account on yesterday.
Speaker 2: Okay, cool.
Speaker 1: Okay, so let me just share this screen.
Speaker 2: And then just shoot me a message when you need next month's Azure fees. Yeah, yeah.
Speaker 1: Got it, yeah. Let me just see. Right, right, right. I don't know how to manage Amar, to be honest. He seems to be busy. And respect to everyone, everyone's busy. You know, Elon Musk is the busiest man on earth. You know, the richest and the busiest man on earth. But if you can make time to have 12 kids, I'm sure you can.
Speaker 2: No one's got time for 12 kids, I can tell you that much. When I was out in Dubai last week and I was talking to a friend of mine, he said that his wife had come back to the UK and he was, you know, he was like daddy daycare. But I think his daddy daycare, like Elon Musk's daddy daycare, involves having two nannies for three kids and a driver. And I said, you're not really daddy daycare, are you? You've got nothing. You've got more members of staff than you have.
Speaker 1: kids and you've got you know what in singapore it's so common as well like having nannies is so common over here my parents don't mean you got no nannies it's like what kind of money do you think i'm on yeah well i mean yeah yeah uh because we signed the we signed the agreement that we should all be moving forward because i don't want to end up there only me and you are missing all the time um like if we've got to bring amar and uh on board and then tell him okay we've done this already it's it's going to slow down progress a lot like um so um he told me he's busy.
Speaker 1: with the startup incubator thing with um uh what's his name uh dr hamid in a qcs or something so yeah maybe it's worth having a private chat with him like to say um is he you know not like because, I don't want to leave him out of it, but I also have no capacity to speed him up to the progress.
Speaker 2: Let's work out what we need, and I'm confident that between us we can sort everything out that we need to sort out. Let's just forget everything else and just drive forward as quickly as we can, and whatever we need, we'll sort.
Speaker 1: The agenda list today is the Action Item List that's created to deliver us and how to move on with Dr Hamid. Gabriel, are we waiting for him.
Speaker 4: Yeah, get us back on it. I called him, he didn't answer. After I did, he dropped the text, said he couldn't join.
Speaker 2: Let's just go on with it, come on.
Speaker 1: Okay, fine. Right, so we've got a few stuff here done mostly. So look at this whole structure here. This is applicable to Clarify, but since we agree that we're going to move forward in the same direction anyway, a few of these apply to Better Health 360 as well. Say, for example, these two work streams here, need to be done. We've got the Azure templates, the mapping that I sent to you, Oli,
Speaker 1: the logic workflow, how we link to NHS. Everything is here, but I'm guessing the question is to you, Oli. Do you want us to do it all into one or do you just want to copy and paste and then do your own version of it.
Speaker 2: Well, really, that's probably a better question. Gabe's best answer because he's sort of going to be the one in terms of the actual dev of it that's driving it all forward. Obviously, on the reg side, then that's going to be me, but...
Speaker 4: dave what do you think from what i understood i thought even though these two products were under the same entity which is us as a group i thought we were separating it because and we're better 360 because of the type of product it is we don't have the same regulatory hurdles and then it's not defined as a medical product it's more angled as a wellness product so we can go about integrating it into gateway health however we don't have as strict um you know kind of obstacles to your market because it's not something for clinics it's a direct to.
Speaker 4: consumer application um so, it's both ways I feel like it might be better and faster to develop it as its own product but then kind of have them because through these applications you can have a link that can take you to another application um and kind of have it that way but maybe building it directly into, gateway might might it might be more difficult difficult it's not the right word it might be more unnecessarily complex for the type of application it is you know if we know it's.
Speaker 2: so okay then so let's do this if you can uh do we have access to this tie this this spreadsheet.
Speaker 1: um I can extract it out so this is my my own to-do list like uh so if there's more people on it to work on it good uh but it will be done if I do it myself but it will take you know six to eight months but I've got more people working on it it will take yeah yeah so let's so let's if you if.
Speaker 2: you can sort of share it with us so we can at least have a look at it and go through it and work out whether there's stuff that we can jump on at the same time what we'll do is, We will create another version of this for Better360, which will drive forward. The way I see it working, you know, given what Gabe says, which is right, is that, you know, to start with, they are separate entities effectively. But the goal is and the way that Better360 will be built is with the potential to integrate it at a point when we're ready to integrate it into sort of creating that round, you know,
Speaker 2: wrap around care that we were just talking about right at the beginning. And, you know, the same sort of thing that's been talked about in the article that I put in the group. So we will we will sort of silo development focus in terms of the regulatory setup and everything on the health care ecosystem. Better360 will follow its development path and we're pushing ahead with that. I know that Gabe's close to, you know, we're very close to being able to give you guys something that you can have a play around with, have a look at it as well. We're very excited.
Speaker 2: We're very excited about it. But for now, we'll silo it and let's focus. on this from a regulatory point of view.
Speaker 1: I think from my side, while doing this, I've got another project that's about to launch as well. It's a small-sized project. But my concern is that that product itself is not ... the other product there is not healthcare regulated and I did see the very stark comparison anything that do with healthcare, personal care, you need the confidence of the end user and you need to tell them we are regulated to hell already and internally.
Speaker 1: we know your data is not going to be sold to anyone, you know like how, what the guys called the 23andMe guys, they recently went on and the data leaked and everything and they were never thought about but I think the user behaviour now is that like, you're a private company sure, but are you following all these rules I think to have that at the front end would be healthier for you guys and to link it out of pages, it might not work unless I just thought about this is, within our policies, we add you guys in as part of our umbrella and then you can just refer back to our overall.
Speaker 1: structure and say, oh this is this workflow is following, Terrify and all the GDPR, everything is out so we need the policy.
Speaker 2: so we're not regulated but, we follow the regulatory path so that when we do get to a point when we're regulated, you know, it's baked into the system. Yeah, it makes sense to me.
Speaker 1: Yeah, yeah. But I'll just add it and the policies then. Okay, so just looking at this, this is the part that I was, happy to discuss with everyone. So this is what we've created so far. We have the code for it. It's ready to be deployed to a front end already. The back end is all done. So when we first built Clarify, it was always a complex, LLM passing engine, that's all. But how we use it to find regulations and all that stuff,
Speaker 1: that is within our back end, how we code it. But now we can use it for scanning for the documents, the coding of the documents, and even for the text, the reception, the triage software. So the main part of the engine is there. We can do it, no problem. Then now we have all the codes for the scan documents. All the... 250,000 of them. We need to speak to Medicus about how we can create an API integration with them. Maybe we might just go to Snowmed.
Speaker 1: and then get the access key. So Snowmeds are the ones who do international coding. UK just bought it, that's all. UK subscribed to one, but UK has their own specific code for everything, yeah. The Twilio stuff, we relaunched it last week. So we're just trying to build it around to make sure it stands up in Twilio properly. Speech-to-text engine, again, all done already. So we don't need to do much on it. Just link it with Twilio. Pretty much here is what we've done.
Speaker 1: And when you guys mentioned your product is almost ready, in my mind, it's already done, really. I'm more concerned about the operational side, how we're going to run it, and service level agreement to people that will send out after post-beta testers. If the product does work, what kind of contract are we sending people? Is it on DocuSign? And to me, it's the operational side already. And the thing is, when we launch a product like this, it's easier to treat the beta testers like a real user. So, you know, okay, the user journey is right.
Speaker 1: These beta testers, even if you send us the link to play around with, make sure we sign in correctly, all the verification, go back to email, all that stuff is all done. And then you can test, okay, this works now. We're ready to go out. Otherwise, you'll do it twice, you know. That's my...
Speaker 2: Yeah, so we're testing the whole flow, not just testing the model.
Speaker 1: Yeah, so the whole flow would include all of this. All this is pretty much done. I just need to get all the documents from Sean, which is the DEF team, to make sure they have all this so that when we do our governance for the ISO 27001, these are all there. So we can show the regulators. So to get ISO accreditation takes about four months. Our sell is we always publish that we are aligned to them, but accreditation is awaiting. So accreditation, it depends.
Speaker 1: The guys I work with, Citation, they took about three months to give me my ISO 9001, but I already got it since day one. So they say, okay, we'll give you it in eight weeks. But because as ISO accreditors, they must be seen doing the work to bring you there. So they don't give it to you in one day anyway. So we just know we have to have them in place and then show them that, okay, we know what we're doing. And then that's quite simple from our side. But yeah, so the rest of it is more, for the regulators. how to be operational ready once the product is ready so um if you guys can just let me know.
Speaker 1: uh what other items you have uh for um yeah so if you if you share this then i can have a look.
Speaker 2: through it myself and i'll tell you in with these ones that you've not marked in terms of who's responsible what we can take responsibility for and we'll try and shift we'll try and take as much much of the burden off you in terms of the things that we can do as we possibly can so that you guys are just focusing on you know the things that you need to focus on um but i mean i'll have a good i'll have a proper look through this this afternoon probably now and i will say we can do this we can do this we can do this and then we can crack on with it.
Speaker 4: You know the standard 27001, I think you said, or 0001, I'm not sure exactly what you referenced. What is that standard? I know the 90001 is the quality management system, which is for general companies, but what was that other one you referenced.
Speaker 1: ISO27001 is web security, so anyone who is using AI needs to have them. Okay. So ISO9001 is management, ISO27001 is for internet security.
Speaker 4: When you go about proving it, is that more about the actual system you've built and showing the regulators, or is it also to do with the documentation you've created in the building of that to prove it when you go and apply for the certification.
Speaker 1: Well, all of them are documentation. It's a paperwork exercise. But we have to link it back to our documents, our build, so to speak. So, you know, in ISO 9001, I can say I've got a business continuity plan. You know, there is a template online. You can download, you really can write it for you, but you need to feel it. Okay, what happens when I die, you know, or when the building's on fire? You've got to fill it in to a point that everyone has to understand. And within all the policy, there must be an author and someone who's enforcing it. So internally, we know we are audited.
Speaker 1: within ourselves already. So when we show the document to people, it's not just a template we bought offline, you know. This is one of the checks that they do, like, and they will interview us and say, okay, are you sure you've got this document? Say yes, how does it work? So it's about creating and filling up these policies. These are quite tedious. Takes about three, four days for each of the ISO. But once you get everything, it's about formatting it correctly, doing it in the same style so they know it's company stationary. So everything. be branded to the company so otherwise you'll say okay this is just template they don't accept.
Speaker 4: this stuff like this like so okay that makes sense i'll pay at times there's also detect and uh the.
Speaker 1: other four that i mentioned that's uk specific so at at this point uh iso 27001 is globally recognized so even if you go to australia canada europe it's okay fine but the uk that's gdpr there is the detect and the mount or whatever it is like all specifically for you um uk healthcare uh health nhs systems so to work on these two first would be the priority like so okay yeah, Yeah, okay, so for us,
Speaker 1: I think at the start of next week, we should have something to look at with the scanning of the docs. And then closer to the end of next week, we should have a trial version of the chat message reception is done already. We just need to think about how we want to make it look like. So I don't know whether you can see this. So these guys are in America. Look, there's a very simple landing page, how it looks like, stuff like this. Anyone can build this in less than, I'd say two hours. What we want is once you get this, we want to show people,
Speaker 1: you can click on it. You can call straight away. The call button should pop up somewhere on my screen, but you can't see it. But anyway, it's just to show people, all right, we're ready to deploy. Let's go. And then from there, we start pushing it out. I know Dr. Hamid have other obligations. So I don't know, Amar, do we have anyone to push this product to.
Speaker 5: Yeah.
Speaker 4: I think I do have some it's got you here yeah.
Speaker 5: sorry I'm a bit ill innit so I'm just trying to, I'm just listening sorry what was the question.
Speaker 1: if we have the product ready by next week is there other doctors within the your network that we can push this product to.
Speaker 5: yeah so I spoke to one the other day and, he's got that Beamer network so he just said to send him a proposal okay, for anything we're doing and, yeah. there's a few other people I can speak to to be honest I just need to think about it a bit more, yeah.
Speaker 1: sorry I'm not functioning.
Speaker 5: proper well but yeah, I'll think about it.
Speaker 1: I'll just put it onto here and then I'll put it as one of the to-do lists and then just put the names and then the contact information on it.
Speaker 2: I know Gabriel potentially had someone as well, didn't he, Gabe.
Speaker 4: Yeah, yeah. I've got two. I've got one which I met at an event and he's got he works within the NHS so it might be a difference depending if you want to go private or NHS, type of direction and, and, I've got a network of doctors through a guy who's also creating products within the healthcare but he's not the primary gateway I want to go through because he's also creating products although it's not completely the same but I need to fully.
Speaker 4: understand what he wants to do so I know we're not competing with him when I'm speaking to him.
Speaker 2: So let's have a think about that then, so if we're ready to do it when did you say, Ty, end of next week? End of next week, yeah So let's prioritise thinking about a network that we can put it into where we're going to put it and that means that by the end of next week we can have a meeting where we're looking at actually what we're pushing out and we can say right, we're going to approach this person, we're going to approach this person what would be useful is if we all have an idea about exactly the terms that we're going to be doing it under.
Speaker 2: what are we asking them for what are we giving them is it just, try this and we're not going to charge you for it for the first six months or try this or we just have to have a, think about um what it is that's going to make it appealing to them uh you know from our point of view really um even if we're not getting paid for it we're getting the data and the data and the debugging and everything like that you know and the credibility that that brings us is hugely valuable to the you know hugely valuable to us so we just need to have a think about how many people.
Speaker 2: because it's good you, I don't know how Ty thinks, but, you know, even if we've just got one practice with 100 patients, it's going to be more than that, I know. But it's not about, you know, getting 10,000 people involved in the first in the first sort of phase of beta testing, because that's just going to cause, you know, that's just going to cause.
Speaker 1: 10 is enough. 10 is more than enough already. 10 calls. So what we're going to do is we're going to we're going to simulate it internally first. We'll show all four of us to see how it works. So when we go out there. So most of GP will use HealthConnect anyway. Yeah. So it's about convincing them to disconnect HealthConnect. Maybe so 8 to 8.30 would be the prime time. So people would people will ring and we don't want to stop their business. So maybe we say, all right, after 8.30, disconnect HealthConnect, connect our phone call system to you.
Speaker 1: Because they know at that time, once your booking is full up already anyway, we're not afraid of anyone. I mean, we're not disturbing their business, so to speak. So 8.30 onwards, every call that happens. Log in.
Speaker 5: I was going to ask, are we going to pilot it in Dr. Armand's clinic or not.
Speaker 2: No, I mean, we're open to piloting it anywhere. But as per the discussion that we had the other night, you know, the deal isn't what the deal was. And so, you know, this is us with a product going to a potential customer, not us with a product going to a potential partner. And so, you know, I'm happy to pilot it with anyone. And, you know, frankly, you know, a relatively small practice to start with will probably be more manageable for us.
Speaker 2: And, you know, in terms of because I think it's going to be like with anything, there's going to be a lot of debugging at the beginning. You know, you know, a lot of things that the dev team and everyone needs to resolve. That's just the way these things work. So, you know, if we get any huge call volume straight off the bat, then that's, you know, it's going to be cause. More problems than it solves, I think. Well, maybe let's just think about who in our network we know that we could go to and say, look, you're a relatively small practice.
Speaker 2: I probably don't say that in those terms, but, you know, we want to get involved with you because you're, I like saying agile when I mean small. So, you know, you're an agile practice. You've got, you know, you've got this and you've got that. Let's come in and try and help you, you know, be innovators. We're innovators, blah, blah. This is how we can increase your patient base. And then just sort of have that, like Ty says, you know, not a huge amount of calls in the first instance. And then when we sort of spun it up to a position where, you know, we're not getting errors that we are going to be getting to start with,
Speaker 2: we can think about taking it to someone else or, you know.
Speaker 1: so yeah just basically a practice that's happening like so we want to know that we can appear on the home screen so that it will be deployed as a web app first and then if it needs to be localized because all of them have the nhs router or firewall around their system uh we can locally install it as well uh we just need to find how to do it like so all this kind of like nitty-gritty stuff we won't know until we sit there yeah we're in front of the practice like so.
Speaker 2: Just get one of these Mac minis. Everyone's buying them now.
Speaker 1: Send it across to them. Okay. Yeah, so, Dr. Hamid, are we going to keep on speaking to him or are we just going to... Because last week we said we're going to catch up with him, didn't we.
Speaker 2: Yeah, but I mean, I know that he was sort of, through Amar, was saying, you know, what's going on, this, that and the other. But my view is, subject to anything anyone else says, I'm not closed-minded to talking to anyone about anything. But we've gone sort of down this road. We've gone down this road, in terms of developing it and funding it internally. For me, you know, we've not lost anything by getting to the end of next week and having what is, you know, a product that we can actually demo.
Speaker 2: And then, um, you know, for me, it's a completely different conversation. I'm not close to anything, you know, I never am, but, but, you know, we could get into this round of conversations again and get nowhere. Whereas in fact, what we're interested in now is this is a sprint to the end of next week. Let's get as much done as we can. Let's get, you know, let's get a network going. Let's get someone that we think we can get this into. And then, you know, you're having a very different conversation when you're saying we've built it, we've tested it. Do you want to be involved in it? And to be involved in it,
Speaker 2: this is the ask, this is what you're going to have to give us. Then, you know.
Speaker 5: Gabe, that guy, Gabe's got a, um, that influencer kid. He does, he's like a doctor or something. Oh, the wellbeing doctors? No, no, no. He's a younger guy. He's like on social media. He sent me him last time.
Speaker 4: Oh, like the Asian guy, like the South Asian guy.
Speaker 5: Yeah, yeah, yeah.
Speaker 4: Yeah, yeah, that's who I was talking about. He's quite a good option because even if he, I don't know, for whatever reason can't, he has a massive network of doctors because he's on a lot of charities and organisations for these young professionals and older ones for investments and just for activities. So he's a very good person to reach out to, which is at the top of my mind. So I can set up a meeting with him for the end of the week so we can just, like, feel him out.
Speaker 5: There's a few doctors that I'm thinking of from the top of my head, but some of them work in hospitals and for Bupa, and that's, like, private, isn't it, Bupa.
Speaker 2: Yeah. Okay, let's not...
Speaker 5: Is that not out of what we want to do.
Speaker 2: Yeah, well, we sort of want a clinic, so let's not... you know sort of have the thought process now i think i think the purpose of this is just to set the target and we're going to do this we're going to do this let's go away and do it because i'm going to have to jump off this call in a minute because uh my client's going to be wondering where.
Speaker 1: i've been for the last half hour um yeah we cover almost everything already so i'll send this list across in the different spreadsheet and then populate as much as you guys can yeah yeah.
Speaker 2: definitely and then obviously that thought process about who we're going to approach and then you guys gabe and i can talk to one another and let's get a list of in order of priority about who we're going to approach with this and then we'll look at this spreadsheet tight and we'll fill in as much as we can and get cracking on everything that we can do our end, got it all right thanks all right guys thanks a lot yeah

## Oliver OS Classification

**Summary:** Team meeting covering the Clarify (healthcare-regulated LLM) and Better360 (wellness/consumer) product strategy, with focus on NHS compliance requirements (ISO 27001, DTAC), beta testing approach, and go-to-market targeting small GP practices. Backend development is largely complete; operational readiness and regulatory documentation are the main remaining workstreams.

**Key Decisions:**
- Better360 will be developed separately ("siloed") from Clarify but aligned with regulatory pathways for future integration
- Beta testers will be treated as real users with full sign-in, verification, contracts and SLAs
- Dr. Hamid partnership deprioritized; team will proceed independently and revisit after demo readiness

**Key Open Items:**
- Medicus API integration vs. direct SNOMED access keys decision pending
- Beta tester terms (trial duration, data use, SLAs) not finalized
- Outreach list for pilot clinics needs owners and target dates
- UK-specific compliance frameworks beyond ISO (DTAC, NHS approvals) need identification and timelines

**Projects:** Human8
**People:** oliver-cook, gabe, ammar, tai
