---
title: What is WebAssembly and Is It Better Than JavaScript?  |  WASM Breakdown for Beginners and Web Devs
authors: 
year: 2021
---
url:  https://www.youtube.com/watch?v=sR22HtWztrY
zot: [See in Zotero](zotero://select/items/@lowlevellearningWhatWebAssemblyIt2022)
status:
# What is WebAssembly and Is It Better Than JavaScript?  |  WASM Breakdown for Beginners and Web Devs

# JS 
human readable interperetd language, JIT compiler - just in time compiled
**just in time** - parts of code are put into compiler while running - performance hit

![[Pasted image 20220622163045.png]]
Code is slower than compiled native languages.

# WASM
binary format - is precomipled before browser gets hold of it 

## files
.wasm - browser readable
.wat - human readable

## how to 
C code into WASM - ![[Pasted image 20220622163324.png]]
Write JS wrapper that calls C functions ![[Pasted image 20220622163409.png]]

## What it will be
Performant backend for demanding funcitons such as coputer vision or games on the  Web




