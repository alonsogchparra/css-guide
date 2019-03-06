# CSS Guide

This a repo to keep the knowledge from the udemy tutorial [CSS - The Complete Guide](https://www.udemy.com/css-the-complete-guide-incl-flexbox-grid-sass/) by Maximilian Schwarzmüller and Manuel Lorenz

Will be divide in modules to move the basics topics to advance ones.

Only need to have basic knowledge about HTML and CSS3 to follow this.

# Reminders IMPORTANT

## Outline
We use **outline** to avoid the blue border the web browser has for default. Use it on pseudo class **focus** and to avoid the blue border put **none**.

## Float
We use **clear** to affect **float**, this will correct the way how will behaviour (Will move the direction as we want without affecting others).

## Position
- Every element has **position:static** as default.
- Adding **position:relative** to the element *father* and adding **position:absolute** to the element child. The element child position will take the element father as guide for the position that we want put the child element
- If the element has **position:relative** (without child element). Will take the initial position where it is. And the movement of the element will take from the initial position.

## Overflow
- Adding **overflow:hidden** to a element, will affect the child element

