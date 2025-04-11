---
draft: true
draftSectionTwo: false
created: 2024-12-11T07:00:00.000-0400
createdForSectionTwo: 2025-04-10T07:34:55.000-0400
tags:
---

## Introduction

Please [fork and clone this repository](https://github.com/lcs-rgordon/SpellingMobile) to obtain the code for this project:

![[RocketSim_Screenshot_iPhone_16_Pro_6.3_2025-04-10_08.14.04.png|300]]

Play the game with a partner.

What are some possible *beneficial effects* of this app?

What *audience* of users might this app target?

## Filtering and searching

With Mr. Gordon, we will work together in class to understand, using cards, what it means to filter and search a list.

Remember, when writing an *algorithm* (a recipe), we have three programming concepts to work with:

1. sequence
2. selection
3. iteration

## Exercises

In class, you have just learned how to filter the list of outcomes in this game.

### Fix the buttons

Do you notice anything about the buttons in this game that feels incorrect?

Use boolean variable(s) in the view model, and the `.disabled` view modifier on the buttons, to control when different buttons are enabled or disabled.

### Use tabs

The interface feels a bit crowded with the scrollable list right below the main user interface of the game.

You have [[Swipe Gestures and Persisting Data#Sharing data|previously learned]] how to share data between screens (views) in an app using the *environment*.

Use that same approach to put the array of previous results on one view within this app, and the main user interface of the quiz on its own view.

### Add search

Instead of filtering, what if the user could search the list of outcomes based on text they type in?

Write a function to allow for this. Use the `.searchable` view modifier on the scrollable list to allow the user to type in a search string.

> [!NOTE]
> 
> As mentioned in class today, this exercise will be done in our next class (Friday). Mr. Gordon will provide a hint to help everyone get started.