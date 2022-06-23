---
title: The Story of React
authors: 
year: 2022
---
url:  https://www.youtube.com/watch?v=Wm_xI7KntDs
zot: [See in Zotero](zotero://select/items/@uidotdevStoryReact2022)
status:
# The Story of React

jQuery -> Backbone

# AngularJS
reduce DOM manipulation
updating view without manualy manipulating DOM

# Reacting
When something changes renrender it from scratch in a way thats performant. 

view is funciton of aplication state
V = fn()

Different view on separation - anything that has something to do with UI its one component.  -> JSX

**Before**: imperative code - ![[Pasted image 20220619121927.png]]

**After** abstracted behind declarative API - <Btn/>

What is react? 
Create components that contain or recieve everythin they need to render the UI. Than you compose those components. How react is used to create single page applications - then NEXT.js used react for UI and outsourcing global state management fetching froms servers. 