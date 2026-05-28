# Sarek

## App Title: WikiConflict
> A web extension that visualizes conflict and editing activity behind Wikipedia articles to help users interpret information more critically.

---

## Overview

WikiConflict explores how transparency around editing activity and conflict on Wikipedia can help users better understand how information evolves online. The project focuses on politically sensitive or controversial topics where narratives are frequently negotiated and revised through ongoing edits and discussions.

The solution visualizes conflict-related signals from Wikipedia articles directly in the user’s browsing experience without attempting to determine whether information is true or false.

---

## Schema fields

- **Group name:** Sarek
- **Challenge:** *Polarization*  
- **App title:**  WikiConflict
- **One-liner:** A web extension that visualizes conflict and editing activity behind Wikipedia articles.
- **Live URL:** https://chromewebstore.google.com/detail/wiki-extension/bfieikokodfkpepggengbijmkpopmfgc?authuser=2&hl=en&fbclid=IwY2xjawSE-0tleHRuA2FlbQIxMQBzcnRjBmFwcF9pZAEwAAEexDqgaEMxTlE76uodHIRWpLl-6Rudyx9RyqRImGE2Q0LHmM1wRV3zzXlW1mQ_aem_8UBBlrs3qrAFReZB6sxygQ
- **Repo URL:** https://github.com/SVP-GU/group-project-sarek.git
- **Team members:** Fredric Jonsson, Marcus Serrander, Klara Nordén, Amina Kenjar, Summer Furniss
- **Target users:** Wikipedia readers and contributors
- **Core functionality:** Visualizing conflict levels and editing activity on Wikipedia articles using revision analysis and machine learning
- **Tech stack:** Python, TypeScript, Plasmo, Render, Wikipedia API, Scikit-learn

---

## Problem Space

Wikipedia is widely used as a source of information, especially for political and societal topics. However, readers often lack visibility into how stable or conflict-driven an article actually is. Articles connected to controversial topics may undergo constant revisions, discussions, and edit wars without users being aware of it.

This makes it difficult for readers to identify polarization, bias, or ongoing information conflicts behind the content they consume.

---

## Our Solution

WikiConflict analyzes revision history, editing behavior, protection status, and discussion activity from Wikipedia articles to generate a conflict score that visualizes potential conflict levels behind an article.

The extension integrates directly into Wikipedia and provides users with contextual information about editing activity and article stability in a lightweight and intuitive interface.

Rather than deciding what is true or false, the solution focuses on transparency and helping users approach information more critically.

---

## Key Features

- Conflict score visualization directly on Wikipedia articles
- Analysis of revision history and editing activity
- Detection of conflict-related signals such as discussion tone and protection status
- Highlight feature showing recent changes in article text

---

## User Flow

1. User opens a Wikipedia article
2. The extension fetches revision and activity data through the Wikipedia API
3. The ML model analyzes conflict-related signals
4. The user receives a visualized conflict score and contextual information directly on the page

---

## Demo

<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/f4d75fb9-2564-4dbd-8025-e189188144fe" />


---

## Design & Development Process

The project followed an iterative design thinking process including interviews, brainstorming, prototyping, user testing, and expert validation. Early project stages focused broadly on political polarization and journalism before the problem space was reframed toward transparency and edit conflicts on Wikipedia.

The solution evolved through paper prototypes, digital mockups, Streamlit prototypes, and finally a functional Chrome extension integrated directly with Wikipedia.

---

## Challenges & Learnings

One of the main challenges was narrowing down the problem space and identifying a clear target group. The project also involved several technical challenges related to revision analysis, machine learning, and Chrome extension development.

A key learning was the importance of balancing transparency and functionality with simplicity and usability. Early versions of the prototype visualized too many metrics simultaneously, which made the interface difficult to understand for users.

---

## How we differ from peers

- vs. **Peer 1:**  
- vs. **Peer 2:**  
- vs. **Peer 3:**  

---

## Future Improvements

- Improved talk-page and sentiment analysis
- Larger training datasets for the ML model
- Better comparison between related articles and topic categories

 
