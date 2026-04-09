---
source: plaud
type: inbox
file_id: 77d00dabf466186044b1a6e7d59e02b5
title: "11-05 Meeting: AI Document Processing and Whiteboard Feature Design"
date: 2025-11-05
duration: 52 min
projects:
  - Qanun-Platform
people:
  - oliver-cook
  - gabe
  - tai
jurisdictions:
  - UAE
tags:
  - AI-document-processing
  - OCR
  - LLM-evaluation
  - whiteboard
  - source-traceability
  - product-design
status: active
last_reviewed: 2026-04-09
---

# 11-05 Meeting: AI Document Processing and Whiteboard Feature Design

## Summary
Date & Time: 2025-11-05 11:33:21
Location: Building 5, 26th floor
Attendees: [Speaker 1], [Speaker 2], [Speaker 3], [Speaker 4]
## 1. Technology Stack: AI Document Processing, OCR, and LLM Selection
The team discussed the foundational technology for the application, emphasizing that the quality of the entire system depends on the initial data processing pipeline. A powerful LLM cannot function effectively if the input context from documents is poor due to a "crappy" OCR. Therefore, selecting the best OCR is a high-priority task.
The proposed AI flow for drafting documents involves a pre-processing layer using Redicto AI, which utilizes the Realm OCR model. This model, built on QWEN 2.5 with a planned upgrade to QWEN 3, is favored because it provides context to documents by intelligently splitting contracts, automatically tagging titles, separating clauses, and performing chunking. This structured data allows the LLM to retrieve content more effectively. The process involves converting uploaded documents into a textual version to be stored in a database. This converted text, not the original document, will be passed to the LLM for analysis to avoid compatibility issues. In parallel, the team will evaluate various open-source LLMs to find the most suitable one for legal reasoning tasks.
### Action Items
- [ ] Finalize the document processing pipeline to a state where work can begin on it. -- *[Speaker 1]* by the end of this week
- [ ] Implement Redicto AI with the Realm OCR model for the pre-processing layer to parse and structure uploaded documents. -- *[Speaker 1]*
- [ ] Evaluate the performance of Realm OCR, comparing it against the "Romo" model and exploring alternatives like the DeepSeq model if it is not satisfactory. -- *[Speaker 1]*
- [ ] Set up the system to automatically convert uploaded documents to a textual version and store them in the database for the LLM to access. -- *[Speaker 4]*
- [ ] Test and evaluate several open-source LLMs, including Minimax, Qwen, and GLM, to assess their reasoning capabilities. -- *[Ollie]*
## 2. Whiteboard Feature Design and Workflow
A central discussion point was the design of the "whiteboard" feature. The main challenge is defining a user workflow that is both powerful and simple, avoiding clutter. A key disagreement emerged regarding its core functionality. Speaker 2, a lawyer, advocated for a clean "mind map" approach where the whiteboard contains only curated information manually placed by the user. Conversely, Speaker 4 argued for a more dynamic approach where AI generates all analytical components (charts, tables) within a grouped section on the whiteboard, allowing the user to select and discard elements as needed. The consensus leaned towards ensuring the final design keeps the whiteboard clean and user-controlled. To move forward, a basic version will be developed to facilitate more concrete discussions.
### Action Items
- [ ] Develop a basic version of the whiteboard to enable further discussion and refinement of its features. -- *[Speaker 4]* one and a half week
## 3. Source Document Traceability and Referencing
A critical system requirement is the ability to trace all generated content back to the original source document. This is essential for lawyers to verify information and build trust in the model, as inaccuracies can have severe legal consequences. The proposed solution is to implement a referencing system, similar to footnotes, where a user can click on a reference number in the output to view the corresponding section of the original source document. This traceability must be integrated into all outputs, including drafted documents and whiteboard presentations.
### Action Items
- [ ] Ensure all outputs from the system, including drafted documents and whiteboard presentations, contain references that link back to the original source documents.
- [ ] Implement a user interface feature, similar to footnotes or clickable reference pointers, that allows users to easily navigate from a piece of generated content to the exact location in the original source.
> **AI Suggestions**
> AI has identified the following issues that were not concluded in the meeting or lack clear action items; please pay attention:
> 1.  **Whiteboard Workflow and Architecture:** There is a fundamental disagreement on the whiteboard's core architecture. The conflict between a "clean, curated space" (Speaker 2) and a "dynamic, all-in-one workspace" (Speaker 4) was not resolved and is critical to the user experience.
> 2.  **Source Referencing Implementation:** The technical plan for the source document referencing feature is not finalized. It is unclear how and when this feature will be fully automated, especially for the whiteboard, where it was suggested initial linking might be manual.
> 3.  **Collaborative Whiteboard Model:** The team discussed a complex collaborative model with personal, shared, and approval-based whiteboards. However, the technical implementation, permission model (who can edit, push, approve), and the process for merging data between boards remain undefined.
> 4.  **Interactivity of Whiteboard Elements:** It is undecided whether elements on the whiteboard (e.g., charts) will be static images or fully interactive components. A decision is needed to balance user experience with development capacity.
> 5.  **OCR Evaluation and Methodology:** The team lacks direct experience with the proposed Realm OCR model. A formal evaluation plan with success criteria should be established. Additionally, a suggestion to run the OCR process multiple times and overlay the results for accuracy needs its technical feasibility, cost, and methodology defined.
> 6.  **Scope of "Phase One":** The plan to complete a basic whiteboard in "one and a half week" for "phase one" lacks a detailed scope of deliverables, which could lead to misaligned expectations.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: I don't like the whiteboard. You don't, you don't? I don't understand it, I don't write anymore.
Speaker 2: Do you want to connect, do you want to connect to the TV? Yeah. Amazing.
Speaker 1: You have a seat? Yeah, I have a seat, yeah. Thank you.
Speaker 2: It's the generation gap.
Speaker 1: Yeah, this is much better. Interactive thoughts.
Speaker 2: No, I like this. Honestly, still now, when I'm doing casing stuff, I have a notebook and I have to write stuff down.
Speaker 1: I've never written in my life.
Speaker 2: It works in my head. It's just, I suppose, like the way of working, isn't it? Yeah, it's the industry.
Speaker 1: It's good. What does it do? Does it tokenise real stocks or something like that.
Speaker 2: It doesn't, yeah, so stocks, you can trade in tokenised versions of the underlying asset. Great. Yeah. When he says he's here on the 26th floor, just send me a message two seconds ago by saying,
Speaker 2: two seconds, what building? I say, building 5. He says, what floor? 26th, and I'm here. Not here.
Speaker 3: What's that? That's it.
Speaker 3: Might as well get a whiteboard.
Speaker 2: I like my version. It's a bit laggy though. What? It's a bit laggy. I like that. There's no lag on my whiteboard. I can't. What you need is Zaheib's infinite whiteboard. Yeah, dude. I like that word as well, and that's what we're going to call it. Infinite whiteboard.
Speaker 1: So this at the moment I'm just going to look at document uploads and then the drafting version. I am not going to take a look at the interactive dashboards we'll do that together at a later date but this is just going to be like the bread and butter of the of the model ie drafting documents from uploaded documents from the team etc. Essentially the Harvey and McGorrett sort of the bread.
Speaker 1: and butter stuff which is obviously very important for what we do. So this is the flow I propose to use self-explanatory pre-processing layer. Is it the flow or the visuals for the body parts? No, no, this is just my AI flow, so what I propose, so I've stocked, this is my AI stock.
Speaker 1: Okay. The first three are pretty simple, I've got a pre-processing layer. For parsing out OCI, I'm going to use Redicto AI, which uses a free open source model called Realm OCR, which is very similar to the way, it's a visual learning model, so it's like the DeepSeq OCR, it's built on top of the QWEN 2.5, but I know they're going to update that to QWEN 3 visual learning model, so it's going to get even better.
Speaker 1: Okay. But the good thing about Realm OCR compared to other OCR models, it gives context to the document, so Harvey AR uses it as part of their sort of processing layer, and for example, if you drop a contract, it's able to split the contract. intelligently so it's able to tag the title automatically, separate different clauses and it does all the sort of chunking for you and yeah it's used a lot by.
Speaker 1: sort of like legal AI systems so I'm going to start using that and see see how it works for us. If not we can always try different other things like the deep-sea model but I think real multi-I is probably the best one to use for our.
Speaker 4: purposes. Okay in my mind yeah I plan in this way like whenever a user will upload the document yeah without you know doing anything once the document will be uploaded, Our agents are hurting the convert the document. Yeah, and to using all your orders. Yeah Yeah, it took texture. Yeah, one two three times to make sure everything. Yeah, it's correct. Yeah.
Speaker 4: Yeah, so and you know keep the, Textual version of that document. Yeah, and, that, Textual version document can be passed to any, You know LLM without, you know, without requiring any OCR model. OCR model just we will use To recognize a convert the document. Yeah.
Speaker 2: Yeah, that's that's what I was planning on. And we will be able to, Refer back to the original document that's been uploaded. Yeah, we sort of like citations. Yeah Yeah, so that's that's gonna be critically important because obviously thinking of it, Backwards from the point at which we have to present this document present the presentation in court We need to be able to follow the route back to the original. Yeah, you know for the bike. I'm not stuck mother by phone.
Speaker 4: No, no, I get it I get it We will use the biggest model and you know, the best model, for for, Technical analysis and this and that we will use the texture model, which is the best out, for us but the textual model is you know mostly not compatible with the images and the documents the reason they they only expose text they are not you know they are not multi-models.
Speaker 1: no they're not it's because the way they sort of pass the documents it's all flat file isn't it so they don't have any concepts around what the title is what a table is and that's what that role most guy does really well yeah they're able to sort of like chunk the document into intelligent parts and yeah um put that in the embedding model so the llm can retrieve solve better content.
Speaker 4: and ultimately produce better answers yeah so um what we will do uh in the whiteboard yeah.
Speaker 1: yeah this is separate to the whiteboard obviously just drafting um research etc.
Speaker 4: the conversion will be not will not be shown to anybody but will be kept separately in the database uh to provide um you know once the agent or in-law guy wants to do something and one instruct the llm to do something it will not go to the original document it will uh you know use the converted text with documents to to understand what are the contexts and.
Speaker 2: yeah when we get to the end of the flow right at the end yeah so when we get in your scenario when we get the drafted document yeah yeah or, In the other scenario when we're using the whiteboard, when we get to the presentation at the end, you have to be able to trace everything back to the original document that's uploaded.
Speaker 4: Yeah, in the whiteboard, LLM will not point everything to the documents, or maybe we can integrate, but initially LLM cannot point the documents to the original documents, or it cannot create what we call the lines. What are the terminologies.
Speaker 1: Paragraphs.
Speaker 4: No, the lines we see in the... In liquid text. Yeah, in liquid text, what we call the lines, the points, pointers.
Speaker 2: Points, connectors. References, I would call it a reference maybe. Yeah, reference pointers.
Speaker 4: Yeah. Okay, so those pointers, reference pointers, I think that's pretty much it. Initially, we will not integrate with LLM. It can be linked manually by the log-by, but the agents, the real agents, the log-by, can get the converted visuals using the AI, and you can manually link.
Speaker 2: So, say I'm a lawyer working on a case. I would always want to be able to go straight back to the original material. So, if I'm preparing something and I'm looking at a big load of telephone evidence, then I might use something to scan through it to find me a particular thing. I'll look at it, but then I'll always want to go back and check before I get further on down the line, because the biggest worry for a lawyer, I'll tell you this. is standing up in court and saying this is what this witness says or this is what this line of.
Speaker 2: data is and the other guy sitting next to you going no it's not and then you looking like a right idiot and then your case disappearing however good your case is your case falls apart, at the point that the judge can't can't trust what it is that you're saying and then you sort of go oh i've got all of this wrong and then everything becomes on demand so for me that's the paranoia that i need to know and i need to be able to check throughout the process the original document.
Speaker 2: okay i need to be able to look at it myself okay and you know you know all this oci and everything like that super duper but i don't you know i don't i'm the one at the end of the day having to stand up and present the case and you know this could be the difference between, winning a 50 million dollar case and losing a 50 million dollar case, So, you know, that's that's how important is so every step of the process whether it's document drafting or whether it's the whiteboard There has to be a way of going back and looking at the original document.
Speaker 2: Okay, because that's how you build the truck because there's a problem where this is going to be not the problem but the you know, it's a friction here is, That the law is the lawyer trusting the model Yeah And so if I'm working with something if I'm working with chat GPT and I ask you a question and he gets it wrong And I'm thinking well, you know, this isn't I can't trust it. I can't trust it to analyze it And then I don't trust it at all. Yeah, and what's that trust in broken then? It's really difficult Yeah, so I need to and it it's better if it gives me the wrong answer and I can go back and work out.
Speaker 2: Why it's giving me the wrong answer because then I can change it, So that's why everything has to be able to be referable back to the original document about every stage.
Speaker 4: So, we need multiple iterations for creating any output from that, or a single iteration. Because in a single iteration, it can make mistakes, and it can cost a lot of Ks for it.
Speaker 3: Okay.
Speaker 1: So... We'll just reference it. We're going to reference all the answers back to the source document then. Yeah. Like, ChaiGPU doesn't do well in that sort of...
Speaker 2: So, you say to the... If you say, let's take the whiteboard and use it as an example.
Speaker 1: It does the output, and then it has source numbers or something. You just hover over the source number.
Speaker 2: Yeah, you just click on the... It's like a footnote in a document. Yeah. You know what a footnote is, yeah? Right. So, when you're saying... and you're reading it and then it's like a number and then at the bottom of the page it says. something so you're reading a document and it's got this little number next to it and then you look at the bottom of the page and at the bottom of the page yeah okay okay you do all your references.
Speaker 2: yeah what we call a footnote because it's at the foot of the page, and it's a note put the page at the bottom of the page yeah uh for this kind of thing.
Speaker 4: reference yeah we need a very good ocr models uh parallel with the.
Speaker 2: extra models yeah you need a very good one or a good one that you can you can roll the eyes of us, you run 10 times or whatever and then overlay the answers on top of one i think. Yeah.
Speaker 1: Okay. I love a Reef. But Roam LCI is definitely the best at it. But I don't know from personal experience that.
Speaker 2: That's what Harvey uses it.
Speaker 1: Harvey uses it. Yeah.
Speaker 4: Can you explain and show me how they are working? The how-be.
Speaker 1: What? The Roam? Hm? What Roam? The LCI model.
Speaker 2: Oh, the whole thing.
Speaker 4: Yeah, the whole thing. How they are working.
Speaker 2: What? Harvey.
Speaker 4: What.
Speaker 3: What Roam.
Speaker 4: Okay, based on the documents, they start answering my questions, okay? Well, we can, you know, get some idea, you know, use the same pattern, you know.
Speaker 2: You can even be when you were doing work for that. Yeah, what were you doing like this.
Speaker 1: Well, I just got into. investment banks. Well, yeah the way they saw stuff is. You know, when you click on this number two, they don't bring it back to the original video, to get into like a little sort of context window like this and highlights it.
Speaker 3: Okay, I guess I think we found it is way better than they have.
Speaker 1: Yeah, yeah. Well, this is, well, Harvey's essentially like ChatGPT, so you just...
Speaker 4: Yeah, yeah, they made a static main...
Speaker 1: Yeah, yeah, you upload documents, the map with like a draft mode and the way you want to draft, draft like a shared purpose agreement. You attach relevant documents to your company, Harvey sort of looks at all the documents, puts it in the pipeline and drafts the SBA based on the knowledge you give it. Yeah.
Speaker 4: And user clients can request an answer based on the document.
Speaker 1: Yeah, yeah, it's all based on Q&A stuff. They have draft mode, they have Q&A. They have things called workflows, which are essentially just combined agents. And then they have, I think, one of their most popular features is bulk document analysis. So you can bulk upload a load of them. This is more relevant to sort of like in-house legal teams. They're not in-house legal, they're like legal firms where you can upload a load of documents.
Speaker 1: And then you can, it's in like a grid format. And the columns of the grid are sort of like separate agents. And they run queries on a bulk basis on all the documents. Let's see if they actually do it digitally.
Speaker 3: Let's have a video.
Speaker 1: What's all these sprout no music trying to get Okay.
Speaker 4: Do we do we have any decisions? What kind of what kind of poverty is I can approve as a PDF.
Speaker 2: What kind of what and what kind of follow they're gonna go become be.
Speaker 1: missing anything cut the image of, notes, unwritten notes, here, powerpoint excel what we what what will you actually do probably integrating the part into their um to a local environment right okay well yeah there's our principal architectures pretty um.
Speaker 4: and what kind of board they have like yeah yeah this is what i'm sorry about now it's a.
Speaker 1: voltage of like the document management system you just upload documents in a standard way you um yeah then analyze the document types of document metadata and document types, industry etc yeah okay and then you can run sort of bulk queries on all the documents so if you have all the documents here in a grid bar map next to industry here you.
Speaker 1: may have um clause extraction can you put it over here so we can it's it's not this is that's the same video we saw before i just tested it then um but here they might have a agent called clause extraction and i'll extract all the clauses from each document into this these cells there.
Speaker 4: so each one of those are the tops and different agent and yeah they have you know the workflow concept but we are we have a space concept yeah then that's space i'm wrapping to the whiteboards okay. each project have a you know one or maximum two spaces to work on I guess one.
Speaker 2: one's probably easier because if you even if you're collaborating you want to.
Speaker 4: have you can if you know collaborating with anyone and when you can share the.
Speaker 2: same space yeah that's that's better because then you know everyone all the works in the same place yeah you're working on one case you're not got a bit over here and a bit yeah so yeah I'm trying to visualize how we're going to work though although it might be problematic in that maybe can can every.
Speaker 2: can each user have a separate whiteboard for every case, Yeah. Okay. And then if you're going to collaborate, can you have one collaborative whiteboard? And then a whiteboard, say that we're working together on a case, case A and case A, we both have our own case A whiteboard. And then there's a collaborative whiteboard, because it might be that we're doing different parts of the same case.
Speaker 2: So if I'm working together on a case with someone, I'll say to him, you go look at the telephone data, and I'll look at the banking data, or you look at the witness statements and I'll look at the exhibits. And then you can work that on your own whiteboard. And then when you've got to the point where you think that this is going to be, this is in the right space for the case, you can take that part of it and push it to the joint whiteboard. Because otherwise I think you might just get, if both people can edit the whiteboard.
Speaker 2: And I'm running the case.
Speaker 1: What are we going to pull into the whiteboard? What are the sources? Is it going to be like that liquid test.
Speaker 4: Yeah, so the way I see it, we need the sources. I guess, you know, if we have two different whiteboards, you know, combining would be a headache for us. Yeah. I'm thinking how the algorithm will work. You know, it's so complex to merge different spaces because these spaces have...
Speaker 4: There are also a lot of components, so migrating those components to a different site is going to be a headache. I guess we can do one thing, we can give certain limitations instead of infinite if the two persons are working together.
Speaker 2: So what I'd say is this, just because this is how the workflow would work if I was doing it in real life. So say we have the whiteboard, Ollie's whiteboard here, and Ollie's whiteboard here. That's helpful, isn't it? Ollie with a Y and Ollie with an I. So this is Ollie's whiteboard, and this is my whiteboard, and this is the Colab whiteboard. One of us has to be in charge of this. So if I'm the senior lawyer on the case,
Speaker 2: I'm the person that can I'm the person that can delete stuff or move stuff on this whiteboard and no one else can do that okay now I'm so say Ollie's working on the telephone stuff and I'm working on the banking data and then this is the collab case whiteboard yeah so I and I'll show you what my visualization of the board is in a minute once we look to the flow but so.
Speaker 2: say I'm doing it I can, do my work, create a product on the whiteboard and then push that product to the Colab whiteboard. So this is the case preparation. So this is where we take the final notes and things like that, the final results from. And then Ali's working on the telephone evidence and he can sort of, whether he can push it or whether he can sort of...
Speaker 4: Automatically reflect, like whenever he's drawing or anything here, it will be reflected in the.
Speaker 2: collaborative board as well. No, I think that only, I think when he pushes it... Pick and choose. Yeah, when he pushes it to the collaborative whiteboard it can. Okay. Because otherwise you might as well just have one big whiteboard. So what I want here is like a cleaner, more finished product. Okay. Which I control, he can push stuff to it. And what would the sources be? I'll do the sources in a second. But this is how I see it. So one person has to be in control of this.
Speaker 2: They can push it and maybe it'll come up on here and I can decide whether I accept it or whether I reject it. I can look at the product that he's pushing and I can say, knock on the chat, and I'll go back and look at this in a different way or go and look at that in a different way. And so one person's in charge of this. So I can work here and do the banking stuff. He can work here and do the telephone stuff. He can then say, push the product to here, say in the chat, have a look at this. What do you think? I can look at it.
Speaker 2: I can say, no, go back and go back and do this, go back and do it differently. You can push it again, have a look at this and say yes. And then I'll put it in the privacy whiteboard.
Speaker 3: Okay.
Speaker 2: I see the...
Speaker 4: This whiteboard thing is becoming complex and complex and complex. But you know, once we've been finished, it's gonna be alright.
Speaker 2: Well I say, if it's simple then there's no point, you might as well use liquid text or you might as well use something else. This is a different level. What is liquid text? Liquid text is our own company.
Speaker 3: Yeah.
Speaker 2: Erm, I think what we do is, once we get funding, the first thing we're gonna do is buy some pens for this fucking game. Right. So this is our fucking app. Right, I'm gonna start throwing the ones that don't work away, because I think I'm ghost going. I'm just fucking the same fucking pens every time. So, I see the whiteboard working like this, a bit like the liquid text thing.
Speaker 2: So down, you have the whiteboard in the middle, and down each side you've got the widgets. And then you'll have like, you know, like you have in your room in your dashboard. Yeah, Like different banking data and then if I click on this banking data here It will take me to the, you know, the dashboard, The banking data dashboard and I can say I want a pie chart of this and I can drag and drop the pie chart.
Speaker 2: Onto the thing or the telephone data.
Speaker 1: Does it still have to be interactive? How do you mean? Once you've dragged and dropped the pie chart, it's slightly interactive here Does it still have to be interactive in there? Or do you just want it for visual representation? Could be a lot easier, for example, to transfer a photo or something of the pie chart into that That would be a lot quicker.
Speaker 1: you know what I mean because in the dashboard the pie chart here is generated by code yeah.
Speaker 2: I think that if if you can drag and drop a visual representation yeah rather than the actual interactive dashboard yeah that's for the whiteboard yeah as long as it will tell the interaction.
Speaker 1: probably is a way of doing it but in terms of getting it done quick it'll be a lot easier just to drag and drop a static version it would be much cooler yeah definitely definitely it is.
Speaker 2: probably possible then that's then that's your sort of um idea of when you were talking about you know what's about minority report or something like that where you're checking this bit of this and putting it here and like you've got this sort of vr sort of thing moving moving parts and stuff like that it would be mega to be able to do like that but it's that it's beyond our capability for, it to be able to do that but it's that it's beyond our capability for it to be able to do that.
Speaker 4: I'm a little bit confused. On the whiteboard, on the left side, we have the documents, right? Yeah, so the documents here as well.
Speaker 1: So why do we have the banking? So these are the dashboards. For example, when we plug in NSL data, raw data, banking or telephone data, we then use AI to generate code to build the interactive banking dashboard.
Speaker 2: You've seen the demo? Yeah.
Speaker 1: And the interactive telephone data. And on the whole dashboard, you have different widgets like a pie chart, a data table, etc. And then the user will be able to sort of pick and choose those widgets. On the dashboard and drag it onto the whiteboard. So that would be one element, and then the second element is documents, which I presume is an output from the AI.
Speaker 2: Yeah, so you can have, say you'd have drafted documents wouldn't you.
Speaker 1: Yeah.
Speaker 3: And then you'd have statements, exhibits, and then whatever else.
Speaker 2: So statements are documents written by witnesses.
Speaker 4: From my perspective, it's becoming complex. Yeah. Because if we create a complex product, and we present to any company, they need to, you know, train their resource accordingly. Then there's the big challenge.
Speaker 2: But it's no more complex to use.
Speaker 1: It's just a drag-and-drop feature, isn't it.
Speaker 2: It's no more complex than that.
Speaker 1: Try to make it as simple as possible.
Speaker 2: Actually, we have drag-and-drop. And I think if we've got, this is your whiteboard, and you can drag-and-drop the visual representation of it, if you think that's easier, then as long as when you click on this, it takes you back to this, and you can change it or edit it. Because, you know, you might sort of say...
Speaker 4: Instead of going back to the banking, it should go back to the original document.
Speaker 2: No, no, I'm talking about two... Yes, I'm talking about two different things. So for these ones, if you're going to click on here, say, and you're going to be taken to the banking dashboard... And I want this chart from the banking dashboard, so I want to be able to see how many transactions there have been in two.
Speaker 4: No, these all, we don't have different dashboards as we plan. We plan everything will be shown into the whiteboard because we create the infinite board. So whenever we like, for example, we ask the AI to convert the document banking statement into the visual representation. So it will create a whole, you know, charts and details and, you know, each element in the whiteboard.
Speaker 4: So you can you will have the full dashboard based on the document in the whiteboard, not, you know, in a separate tab. Thank you. first banking telephone no it will be in within a whiteboard with with the separate thread like banking data analysis and there's a whole group of, components that represents that document which was well then do that with the.
Speaker 1: might not be able to get a bigger picture of everything because quite, whiteboard any UI perspectives for night you can't for example the things you have AI to produce in the whiteboard or the banking data etc making the.
Speaker 2: overall dashboard if I make sense so for me this you know as a as a lawyer my way of working right in like. In the old days, before the invention of the infinite whiteboard, I'd be there and I'd have boxes of papers and imagine that these things on the side are boxes of papers and in one box I've got the telephone data and in one box I've got the banking data. So I would go to the box of the telephone data and look at everything in it.
Speaker 2: and then I would look at the banky data and I would think okay I want this piece of the Telefo data, I don't want all of it I want this piece I'm going to put that in my in my whiteboard yeah I've got I've looked through the bank statements this is what's relevant to me I take this down so for me the whiteboard is like almost a mind map of my case exactly and so I don't want but really I.
Speaker 4: want too much I only want information on the whiteboard which I put there yeah that requires.
Speaker 2: wires for to make success yeah so when I'm talking about this it doesn't have to be iterated exactly like this but I think that you know we don't need the depth and the document in the whiteboard it's almost like actually here I think right I'm going to look at the banking data all right if you want you can do it through the prompt you know to take me to the banking data it takes you the bank data I want a chart of this but I think what's really helpful about what you've done with the dashboard, is that sometimes it's helpful to have the information without asking the question,
Speaker 2: if that makes sense. So the way that it's been done in the demo, you put the banking data in and it shows you all of this information in charts. That's not because you've said, I want this chart or I want that chart. Sometimes only by looking at it, you think, oh, that's a really good point. Well, that's a really good piece of information. Oh, I didn't think of it like that. I'll tap that and I'll have this. And then when you look at the big picture, you can start asking other questions. But for me, we need to keep the whiteboard as clean as we can. So you have to.
Speaker 2: take it out of the box, put it on the table. Yeah. I'm seeing the same thing like we did.
Speaker 4: before. He did already, but in a totally different way. Things will be the same. Right. it you know um it adopts uh each component will be a sorted and positioned by the ai, uh in a whiteboard without with a group setting yeah and um okay when you ask the ai uh okay give.
Speaker 4: me the visual representation or analysis of this banking it gives you the group of components and, each conference has the uh data whatever we you know similar to the uh dashboard uh we saw in the video you did already and um okay you saw all data is there yeah the whole analysis is there okay you need this component you need this component you need this kind piece of data you can just.
Speaker 4: drag you know click and copy yeah and you know rest of that you can you know which pocket, So now you have your relevant components whenever you require or any textual information, you just move from the group component and now you can use and you can remove the rest of the components.
Speaker 2: Yeah, I mean as long as it's sort of we're keeping the whiteboard focused. What we need to avoid is getting too much clutter, too much information in the whiteboard.
Speaker 4: Because you know what the problem with static dashboards is that like, for example, if we statically mention like banking, telephone, because in real world there's an infinite kind of data format. So we cannot, okay, we have banking now, we have telephone, we have now the criminal, you know, there's a lot of branches and now we have to think about. So. But I'm thinking to make, you know, combine any kind of information in, you know, in a very standard way. So if any kind of data comes to us, we can, you know, represent in our own file, you know, ways that's posed by the whiteboard and that can help the, you know, agent, they can find the ideas and, you know, make that, you know, the logic.
Speaker 4: In the case, very, very fast. Okay. Okay. They don't have to waste time. Okay. Looking to this one, this one. very simple, user, you know UX, Then that's you know, even the child's can't understand very easily. Yeah, and, But it can help out, you know, they it can produce the productivity, If you know they are searching, Right now if they are searching for you know, making logics and finding references and you know patterns in different files.
Speaker 4: They just ask. Okay. Yeah, fine, Did I'm graphing when a pilot pilot PCP now find this kind of pattern in these files It will do for you and give you the complex. Okay, you can see. Okay, okay Okay, and it will you know even points to the ocean document reference very from it got, Yeah, got it. And okay, you saw okay when you click the data, okay fine. I don't need this, rest of the you know conference keeping the whiteboard you will remove that.
Speaker 4: response okay and your data and you go according to your music that's how I'm thinking they're making more standard version is if we go with the static way it can cause a lot of issues like design in future we have this one we have to integrate the full project become you know so complex because for each kind of data we need different you know sort of dashboard and the elements that's that's.
Speaker 4: that those thing I want to buy what do you say.
Speaker 2: I think however you do it, I think as long as you have the ability to be able to control what's on the whiteboard without it being cluttered, so for me this is...
Speaker 4: I think it's better if we can start discussing once we will have a whiteboard, a basic version, and being good.
Speaker 1: So you know I love the Q&A function. When you ask a question about a page or a document, you get obviously the AI output which embeds the source. If you can drag that AI response onto the whiteboard, it's like a little snippet of the response and within the snippet you can look at the source directly. i think that'll be great and then obviously when lawyers look at that they can see a response which.
Speaker 1: may help them on the case but also see the grounded information behind it like we've talked about before going back to the source pdf but if you want to sort of export this whiteboard to pdf for example you don't really need the underlying source because the library already knows it's there without being sort of like one potential yeah whiteboard would be great all right it's, just the one in the ui perspective i just don't know how possible it is because i'm not i'm not.
Speaker 2: i'm not big on ui um what why don't we get what you say let's get a it's in the phase two yeah.
Speaker 4: so working on phase one once it will be completed, i'll start working maybe one and a half week requires to complete our basic version okay, okay so if there will be no birth of the sturdy platform can i see your liquid test how much is it.
Speaker 3: i used it in one case it's quite limited to functionality because.
Speaker 1: oh so is it just you write notes and you link it to the but then you can also.
Speaker 2: um when you plot the full functionality you can like a circle a bit tatter you can. you can like select text yeah and then you can drag it onto here yeah and then it will reference you back to that text really good and then um you can lasso select then you can like do this.
Speaker 2: put it here but then with the lasso you can just circle it up a bit or and you can download these are these are pds but they're not ocr okay yeah there's pdf yeah yeah yeah it's just like reading the witness statement um and then let's see so these are the extracts from the witness statement you can move them around and then you know wherever they are.
Speaker 2: it will take you you click on it back to the original yeah.
Speaker 1: we weren't very similar don't we we can just circle around yeah look around a widget for.
Speaker 4: example connect it to the whiteboard yeah so it's that sort of no they built a very good one, but we need a different one yeah but that's the sort of general concept the certain concept we need from them like yeah referring yeah yeah to those in documents um but uh you know i'll i'll give my 100 percent uh to to make it according to my experiences um i'll put 100.
Speaker 4: percent to get the best yeah product of course i think you'll like it i'm sure because i'm, When I was a kid, I used to, you know, use a booties, Macs, and a lot of, you know, Autodesk products, if you've heard of them. Yeah. So, when I was a kid, as far as the whole machine software, there's thousands and thousands of components, and, you know, I was lost, okay, where can I start, what did it do, what did it do, so it was so complex.
Speaker 4: So, and when I, you know, came to the software industry, so I thought we should create the softwares that are more UX-friendly, if we will not create a software user-friendly, and the people stop, even if they are, you know, more extremely useful, people stop using them, because...
Speaker 2: Yeah, that's all I know. Well, our target is to create a more user-friendly, more complete version of Bars.
Speaker 4: Simplest version and the best for me.
Speaker 1: Yeah, but you've got to remember that the mass use of these products, I'm not really big into technology, so you just need to make it as easy as possible for them to use.
Speaker 2: Once I was going to... I'm fairly unusual as a lawyer in that I use technology more than most lawyers do, most lawyers don't.
Speaker 4: Then this will give you the element and you can help me out to reshape the whiteboard according to... Because I'm a developer, I can create and think how it can help the user and make it more simplified. But what are the desired results, you can...
Speaker 2: Yeah, no, exactly. That's what I'm here for. Okay, cool. Does everyone know what they're doing then? Everyone is happy. Yeah. Okay, you just quickly do that I think I wants me to test out a few yeah.
Speaker 4: Did you take The deep-sea cause you know, that's my.
Speaker 1: Day, so I'm gonna compare that against the Romo and see how the top could be against.
Speaker 4: It's good. Yeah.
Speaker 1: Yeah, so I'm extra. Yeah, I'm gonna I'm gonna give it a couple of different sort of documents like contract tables and I want to give them a big financial accessories perhaps done, Tables and see how that's all, The output, um so that's my to-do list this yeah this by the end of this week i want to get sort of the, document pipeline sort of in a place where we can start work start working i totally depend on you.
Speaker 4: because you have to select the best possible version yeah it's not a bit it is.
Speaker 1: for the lm to work it doesn't matter how good the lm work so obviously our process has to be the best and to vote for it to give it the the best the best concepts you could have had the best hello and llm in the world but if the sort of context you give it it's muddled up if we just use a crappy ocis it's never going to work properly um by then we should give ollie a, couple of um open source lms to test like mini maps um quen doesn't mean it makes uh glm i suppose.
Speaker 4: Does Minimax have the OCR version.
Speaker 1: No, it doesn't. No, no, no, I don't think so.
Speaker 4: They have a lot of products, that's all.
Speaker 1: Yeah.
Speaker 4: If I look into it, I guess they have...
Speaker 1: But when we use the NLLM, it doesn't have to be an OCR.
Speaker 4: No, no, I'm talking about the OCR. The OCR is extremely important for us.
Speaker 1: Yeah, yeah, yeah, well, that's on my side to pick the best OCR for us. We need the sort of reasoning model to be tested. Okay.
Speaker 2: Useful for something then, good. I said I am useful for something. You are the boss. Right, so you want me to test those? Yeah. I'll test those models, and then you're cracking on with the... phase one that we were talking about yesterday yeah and then we know where we're going now with phase two so ollie's gonna work on the yeah ollie and i work together on the lm yeah yeah okay.
Speaker 4: perfect and you're gonna go on with the death yeah i want to see this uh training platform.
Speaker 1: okay we really have a meeting like one two hours oh yeah yeah perfect so you get it on your iphone.
Speaker 4: technology guy and you know he helped me uh the other day uh i was entering the room and he said okay use these system problems and this sign. they're using it but they don't know how yeah they don't have to use it.
Speaker 2: Well, I like to know about things. Yeah, that's good. Alright, good meeting you guys.

## Oliver OS Classification

**Summary:** Technical meeting on the Qanun platform's AI document processing pipeline and whiteboard feature design. Key topics included selecting Redicto AI with Realm OCR for document pre-processing (used by Harvey AI), the critical requirement for source document traceability via footnote-style references, and whiteboard architecture debates between a clean curated mind-map approach vs a dynamic AI-generated workspace. Oliver stressed that lawyers must be able to trace every output back to the original document for court credibility.

**Key Decisions:**
- Use Redicto AI with Realm OCR model (QWEN 2.5, upgrading to QWEN 3) for document pre-processing
- All system outputs must include source references back to original documents (footnote-style)
- Whiteboard should be clean and user-controlled, not cluttered with auto-generated content
- Drag-and-drop will use static visual representations rather than interactive components initially
- Oliver to test open-source LLMs for reasoning capabilities; Gabe to finalise OCR pipeline

**Key Open Items:**
- Finalise document processing pipeline by end of week
- Evaluate Realm OCR performance vs alternatives (DeepSeq model)
- Test open-source LLMs (Minimax, Qwen, GLM) for legal reasoning
- Develop basic whiteboard version within one and a half weeks
- Resolve collaborative whiteboard model (personal, shared, approval-based)
- Define whether whiteboard elements will be static or interactive

**Projects:** Qanun-Platform
**People:** oliver-cook, gabe, tai
