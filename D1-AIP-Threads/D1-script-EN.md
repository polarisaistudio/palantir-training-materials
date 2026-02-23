# D1 — AIP Threads Basics: Drag a File, Ask AI

---

## YouTube Info

**Title:** Palantir AIP Threads Tutorial | Analyze Your Data with AI in 3 Minutes

**Description:**
```
Palantir AIP Threads hands-on tutorial — get started in 3 minutes.

Open AIP Threads in Foundry, drag in a CSV file, ask questions in plain English, and watch AI analyze your data and respond instantly.

Demo environment: progressbootcamp.palantirfoundry.com

⏱ Timestamps
0:00 Intro: What we're doing today
0:15 Open AIP Threads
0:40 Upload a data file
1:15 Ask the first question
1:50 Ask follow-up questions
2:40 Review AI's analysis
3:00 Wrap up

📂 Full Tutorial Series
D1. AIP Threads Basics (this video)
D2. Build an AIP Agent
B1. Create an Ontology from Scratch
C1. Build a Dashboard with Workshop

💡 Each video in this series teaches one thing. Follow along and you'll get it.

#Palantir #AIP #Foundry #AI #DataAnalytics #Tutorial
```

**Tags:**
```
Palantir, AIP, AIP Threads, Foundry, Palantir Foundry, AI, data analytics, tutorial, hands-on, artificial intelligence, LLM, large language model, Palantir tutorial, data platform, enterprise AI, no code, data analysis
```

---

## Script

> Target duration: 3-4 minutes

---

### [0:00 - 0:15] Intro

**Voiceover:**

> Today I'll show you AIP Threads in Palantir Foundry. You drag in a file, ask questions in plain English, and AI analyzes your data on the spot. Three minutes, let's go.

**[SCREEN: Foundry home page, cursor ready to click]**

---

### [0:15 - 0:40] Open AIP Threads

**Voiceover:**

> After logging into Foundry, find AIP Threads in the left sidebar and click into it.

**[SCREEN ACTION: Click left sidebar → AIP Threads entry]**

> This is the Threads interface. It looks a lot like ChatGPT — conversation area on top, input box at the bottom. But the key difference is it can directly read your data inside Foundry.

**[SCREEN: Show the empty AIP Threads conversation interface, cursor pointing at input box and attachment button]**

---

### [0:40 - 1:15] Upload a Data File

**Voiceover:**

> Now I'm going to drag in a CSV file. This is a work orders dataset with fields like work order ID, building, category, priority, status, and cost.

**[SCREEN ACTION: Drag work_orders.csv from desktop into the input box, or click the attachment button to upload]**

> You can see the file is now attached. Threads automatically recognizes the file format.

**[SCREEN: Show the file attached in the input area]**

---

### [1:15 - 1:50] Ask the First Question

**Voiceover:**

> I'll ask it a simple question: which work order category has the most entries?

**[SCREEN ACTION: Type in the input box → "Which work order category has the most entries?" → press Enter]**

> See — AI read the CSV and counted them up. It tells me Plumbing has the most, followed by HVAC, then Electrical...

**[SCREEN: Wait for AI response, show the analysis results, cursor slowly follows the response as it scrolls]**

> No code, no Excel, just ask.

---

### [1:50 - 2:40] Ask Follow-Up Questions

**Voiceover:**

> Let me ask something more complex: for all Critical priority work orders, how many days did they take to resolve on average?

**[SCREEN ACTION: Type in input box → "For all Critical priority work orders, what's the average number of days from creation to completion?" → press Enter]**

> It looks at created_date and completed_date, calculates the difference for each Critical work order, and gives me the average.

**[SCREEN: Show AI response, possibly including calculation steps or a table]**

> One more. I'll ask: give me a monthly summary of work order count and total cost.

**[SCREEN ACTION: Type → "Give me a monthly summary of work order count and total cost" → press Enter]**

> There it is — a clean table broken down by month.

**[SCREEN: Show the table-formatted response]**

---

### [2:40 - 3:00] Wrap Up

**Voiceover:**

> That's AIP Threads. Drag in a file, ask questions in plain English, AI handles the analysis. No code, no waiting for someone to pull data for you. That's it for today — three minutes, done.

**[SCREEN: Pan out to full Threads interface showing the complete conversation history]**

---

## Recording Notes

- Pre-place `work_orders.csv` on the desktop for easy drag-and-drop
- If Threads supports referencing Foundry datasets directly, use that approach instead of file upload — adapt based on the actual interface
- Ask questions in English for this version
- If AI response is slow, cut the wait time during editing
- Make sure the CSV has enough completed work orders (with completed_date) so the "average days to resolve" question works properly
