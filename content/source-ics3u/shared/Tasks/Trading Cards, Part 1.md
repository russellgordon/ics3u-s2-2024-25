---
draft: true
draftSectionTwo: false
enableToc: false
excludeBacklinks: true
created: 2024-10-17T00:00:00.000-0400
createdForSectionTwo: 2024-11-11T07:00:00.000-0400
tags:
---
## Objective

Create your own *unique* trading card that has the look and feel of the broader examples of trading cards for [sports](https://duckduckgo.com/?q=baseball+trading+cards&iax=images&ia=images#), [board games](https://duckduckgo.com/?q=board+game+trading+cards&t=osx&ia=images&iax=images), [video games](https://duckduckgo.com/?q=video+games+trading+cards&t=osx&ia=images&iax=images), or other areas of interest.

![[Screenshot 2023-01-12 at 10.07.50 AM 1.png]]

## Purpose

An opportunity to demonstrate your understanding of key concepts. Specifically, using structures to:

- describe related data
- build user interfaces

## Success criteria and exemplar

1. Made a rough plan where you have identified how various structures (`VStack`, `HStack`, `ZStack`, `Image`, et cetera) might be used to create part of your design.
   
   For example:
   
   ![[Pasted image 20230112102153.png]]
   
   And:
   
   ![[Pasted image 20230112102253.png]]
   
2. Created a static layout where the look and feel of a trading card is reproduced.
   
   ![[Screenshot 2024-01-22 at 5.48.12 PM.png]]
   
3. Created a structure named `TradingCard` (or similar) using appropriate property names, capitalization, and selection of data types that will allow you to store the data shown on your cards' static layout.
   
   ![[Screenshot 2024-01-18 at 7.57.49 AM 1.png|275]]
   
4. Created instances of your structure to hold information for cards.
   
   Here is one example:
   
   ![[Screenshot 2024-01-18 at 8.00.02 AM.png|600]]
      
5. Applied abstraction by converting your static layout to use a property named `card` (or similar) that accepts an instance of your `TradingCard` structure.
   
   To demonstrate even more mastery of abstraction, use *helper views* to make the layout more concise and easier to understand:
   
   ![[Screenshot 2024-01-22 at 5.51.05 PM 1.png]]
   
7. Written code that is well-formatted and easy to read.
   
8. You have used source control well by [[Pushing Commits|committing and pushing]] your work to a remote on GitHub at regular intervals.
   
   ![[Screenshot 2023-01-12 at 10.39.33 AM.png|500]]
   
   ==NOTE:== This is not a complete list of commits; your actual list of commits would be much longer.

## What you'll need to begin
- [ ] Xcode
- [ ] the [SF Symbols App](https://developer.apple.com/sf-symbols/) installed on your computer, also for reference
- [ ] your copy of SwiftUI Views Mastery, downloaded to your computer, so you can look up examples as needed
      
## Getting started

1. Create a new iOS app:
   
   ![[Screenshot 2023-01-12 at 9.18.08 AM.png]]
   
2. Name the app `TradingCards`:
   
   ![[Screenshot 2023-01-12 at 9.18.22 AM.png]]
   
3. Save the app in your Computer Studies folder, ensuring that source control is enabled:
   
   ![[Screenshot 2023-01-12 at 9.18.37 AM.png]]
   
4. Then create a public remote on GitHub:
   
   ![[Screenshot 2023-01-12 at 10.06.32 AM.png|400]]
   
5. Now work to complete each item described above in the [[Trading Cards, Part 1#Success criteria and exemplar|success criteria]].
   
   > [!IMPORTANT]
   > 
   > Remember to [[Pushing Commits|commit and push]] your work regularly.

## Progress and due date

The task is due by 11 PM this Monday, November 18, 2024.

After each class, [on Notion](https://notion.so), be sure to:
- [ ] Share progress regularly
	- [ ] Be sure to post screenshots
	- [ ] ==Be sure to post the address of your GitHub remote at some point==

> [!NOTE]
> Your work is not considered as handed in until the GitHub remote has been shared *and* you have [[Pushing Commits|committed and pushed]] all your work.

## Further examples

Here are some examples of possible layouts that you could aim to reproduce, or use as inspiration for a similar layout:

![[Trading Card Template Examples-7 (dragged).png|400]]

![[Trading Card Template Examples-3 (dragged).png|400]]

![[Trading Card Template Examples-2 (dragged).png|400]]

![[Trading Card Template Examples-1 (dragged).png|400]]

![[Trading Card Template Examples-4 (dragged).png|400]]

![[Trading Card Template Examples-5 (dragged).png|400]]

![[Trading Card Template Examples-6 (dragged).png|400]]

![[Trading Card Template Examples-8 (dragged).png|400]]

![[Trading Card Template Examples-9 (dragged).png|400]]

## Typefaces

You can use other typefaces in iOS applications.

Consult the [iOS Fonts](http://iosfonts.com) website for a quick reference.

![[Screenshot 2024-01-18 at 8.35.40 AM.png]]

> [!TIP]
> 
> Page 478 in [[SwiftUI Views Mastery]] has examples of how to use custom fonts, as well.

## Final advice

> [!IMPORTANT]
> 
> Do *not* use frames for positioning. Your layout should work well on multiple screen sizes.
> 
> Put another way, use frames only to size the width or height of an image, but not both.

