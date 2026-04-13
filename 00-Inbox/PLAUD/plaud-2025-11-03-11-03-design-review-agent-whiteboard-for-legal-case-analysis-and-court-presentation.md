---
source: plaud
type: inbox
file_id: aa07088f99a4444532a57340bf500939
title: "11-03 Design Review: Agent Whiteboard for Legal Case Analysis and Court Presentation"
date: 2025-11-03
duration: 7 min
projects:
  - Qanun-Platform
people:
  - Oliver-Cook-KC
  - Tai
jurisdictions:
  - England & Wales
tags:
  - product-design
  - whiteboard
  - case-analysis
  - court-presentation
  - AI-agent
  - data-visualization
status: active
last_reviewed: 2026-04-09
---

# 11-03 Design Review: Agent Whiteboard for Legal Case Analysis and Court Presentation

## Summary
## Agent Dashboard and Case Whiteboard Concept
- Introduces a conceptual “space” per case: an infinite, whiteboard-like environment serving as the central hub for analysis, visualization, and presentation.
- Purpose: unify multi-source data (banking, telephone records, witness statements, location traces) into a visual, manipulable canvas suitable for legal preparation and court presentations.
- Core capability: dynamic placement and linking of data elements to express relationships, timelines, and patterns (e.g., linking payments to calls, calls to movements, movements to witness statements).

### Interactive Data Handling
- Drag-and-drop interactions: analytics outputs can be placed, rearranged, and grouped.
- Visual linking: circle and connect related text or data points to show cross-source associations.
- Manual updates: lawyers and agents can reposition and annotate items directly.
- Agent/AI assistance:
  - Update specified components of the board on command (e.g., “update this to that”).
  - Enrich with supplemental information.
  - Run pattern-finding on selected elements and return structured results to the whiteboard.

### Court Presentation Use Cases
- Build narratives with dated facts:
  - Tuesday: specific amount spent or cash deposit made.
  - Wednesday: specific call made.
  - Thursday: specific travel or location data.
  - Friday: witness statement content.
- Assemble evidentiary slices: select relevant items (banking data, phone logs, witness excerpts) and position them for courtroom storytelling.

## Reference Inspiration and Tools
- LiquidText (PDF-focused tool):
  - Functionality: circle text, link across document sections, visually connect related points.
  - Suggestion: download and experiment for interface inspiration (acknowledging the envisioned system is broader in scope with more data sources).
- Visual metaphors from films:
  - Marker/pen-based linking of clues and facts aligned with investigative workflows.

## Design Decisions and Preferences
- Preference for a whiteboard over a static dashboard to better:
  - Populate and reorganize data.
  - Reflect investigative thought processes.
  - Expand scope as cases evolve.
- Compatibility with pen/pencil input to draw directly on the board enhances usability.

## Development Approach and Phasing
- Current work aligned with “Phase One” completion as the initial priority.
- Conceptual exploration of the whiteboard planned to begin after Phase One tasks are completed.
- Flexibility endorsed:
  - Proceed in whatever sequence accelerates progress (“do however it works in your brain faster”).
  - Start whiteboard work when productive, even if earlier than originally planned.

## Stakeholder Positions
- Positive reception to the whiteboard concept.
- Emphasis on usability for lawyers to mentally adjust and reorganize evidence.
- Approval to explore LiquidText for UI/UX ideas while recognizing the broader system vision.

## Data Types and Examples to Handle
- Banking transactions: amounts, cash deposits.
- Telephone records: calls by date/time.
- Movement/location logs: places visited.
- Witness statements: text excerpts.
- Analytical outputs: patterns identified across these sources, displayed as linked visual artifacts.

## Functional Requirements Summary
- Infinite canvas per case.
- Drag-and-drop modules for analytics results.
- Visual connectors and annotations.
- Agent/AI functions to:
  - Update elements upon request.
  - Add external/contextual information.
  - Perform pattern detection on selected items and surface findings on the canvas.
- Pen/pencil drawing support.
- Easy assembly of court-ready presentations from board components.

## 📅 Next Arrangements
- [ ] Complete Phase One tasks as the initial priority.
- [ ] Begin conceptual whiteboard exploration once Phase One is done, with flexibility to start earlier if it speeds progress.
- [ ] Download and experiment with LiquidText to extract UI/UX ideas applicable to multi-source data linking.
- [ ] Define the whiteboard’s data modules for banking, telephone, witness statements, and location logs.
- [ ] Implement drag-and-drop placement and visual linking (circles, connectors) on the infinite canvas.
- [ ] Enable agent/AI controls to update specific board elements, add information, and run pattern detection.
- [ ] Integrate pen/pencil drawing tools for direct annotation on the whiteboard.
- [ ] Prepare an example courtroom presentation flow using dated evidence slices (Tue–Fri sequence) to validate usability.

## Highlights
- No highlights extracted.

## Transcript
Speaker 1: okay I understand the whole idea yeah now for the agent dashboard yeah and for the document analysis and you know yeah I was I planned a lot of things in my.
Speaker 1: life since we planned this whole thing, i come up with a result i just want to show you if it's a good or not about it we give the agent, portal uh a space concept conceptual space for example each case may have one space and, that space is like a whiteboard but infinite whiteboard and where the analysis of.
Speaker 1: the models will be there and can be updated by manual as well as you can ask the element to update the certain things as well and you can just literally like we see in movies yeah, they uh you know the ci here they're linking things or okay this links with this thing this thing i think with this thing and they they you know process the things visually so how about.
Speaker 2: this one yeah i really like them i like a whiteboard you know that i like that so i like that so you would have and when you do the data analytics you would have the results of the data analytics sort of here here and here you can drag it and you can drag and drop you can take a piece from here yeah and put it in here so so if you're doing a presentation to court you can have well this is important this bit of banking data this bit of telephone data this bit of witness statement this bit of uh this here and here yeah yeah no that makes sense because because that's.
Speaker 2: what you'd have to do in the end anyway if i'm addressing the court i say, on Tuesday he spent this amount of money or on Tuesday this big amount of cash was paid into his bank account yeah on Wednesday he made this call on Thursday he went here on Friday this witness statement says this.
Speaker 1: yeah we heard of a program called liquid text liquid test liquid text.
Speaker 3: text text it just it just does PDF documents.
Speaker 2: But have a look at it because you might get some ideas from it in terms of that's how I see it but on a much bigger scale with much more data sources. So here you can circle it and link it to another piece of text here and circle it and link it to this sort of piece of text here. So download it and have a play with it and see what you think of it because that might give you some ideas.
Speaker 1: Okay, so I didn't saw any concept but I just saw some movies and I saw them working using markers or pens. Okay, this matches with this one.
Speaker 2: Yeah, that's exactly what I'm talking about.
Speaker 1: It really helps that we can even the element can control your whiteboard thing as well. We can just help you. The agent can just help you. It's very important. like okay update this one to this one and extra disinformation or fine pattern in this one and give me the result it will give the result in the whiteboard yeah sounds perfect and our lawyer can adjust the positions of.
Speaker 1: things mentally as well okay yeah yes it's a good idea instead of having the static dashboard like we have in the video to popular the data I guess the whiteboard you know you know it's much better than yeah no I like it okay.
Speaker 2: perfect I would have a look at this and see what you think oh it's nothing it's nowhere near as big is what you're thinking you know have a look at the way that they do it because then you use your pen your pencil and you can like draw on the whiteboard so I'm looking at okay.
Speaker 1: so okay because it was in the now we have you know this one this phase one thing to complete and this white working in my mind having a piece to and the piece three is one I thought I would start working on with the whiteboard today yeah I have to complete this one so then I was don't start work from the.
Speaker 2: whiteboard this is easy you you do however it works in your brain faster.
Speaker 1: that's the way to do it okay okay once I've done there according to this thing, then I started working with a whiteboard and I also would like because whiteboard can you know expand our things.
Speaker 2: Yeah, I really like him, he's a great man.

## Oliver OS Classification

**Summary:** Design review for an AI-powered infinite whiteboard feature within the Qanun legal case management platform. The whiteboard would allow lawyers to visually link multi-source evidence (banking, phone records, witness statements, location data) for case analysis and court presentations. LiquidText was identified as UI/UX inspiration.

**Key Decisions:**
- Adopt whiteboard concept over static dashboard for case analysis and evidence presentation
- Phase whiteboard development after Phase One completion, with flexibility to start earlier
- Use LiquidText as reference for visual linking and annotation UX patterns

**Key Open Items:**
- Complete Phase One tasks as priority
- Download and experiment with LiquidText for UI/UX ideas
- Define data modules for banking, telephone, witness statements, and location logs
- Implement drag-and-drop, visual linking, and AI agent controls on the canvas

**Projects:** [[01-Projects/Qanun-Platform]]
**People:** [[02-Entities/Oliver-Cook-KC]], [[03-People/Tai]]
