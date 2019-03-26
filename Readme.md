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

## Background
- When you use an image as background, this will be position fixed as default.
- Background has many components, but you can reduce all of them in one element, if you know the elements order, I will give two cases that will be helpfull to work with it
```
background: url position/size repeat origin clip attachment
```
Code Example:
```
background: url("images/image.jpg") left 10% bottom 20%/cover no-repeat border-box;
```
Other example with more elements
```
background: linear-gradient, url position/size repeat origin clip attachment, one color
```
Code Example:
```
background: linear-gradient(to top, rgba(80,60,18, 0.6) 10%, transparent), url("images/image.jpg") left 10% bottom 20%/cover no-repeat border-box, #ffffff;
```

## IMG (tag)
The img tag it doesn't matter about the parent tag size has it (That's why the image shows up with the original size). To resize the img according to parent tag:
- The parent element should have this ```display: inline-block```
- Use the height or width that you wish indicated
- You can use on img tag the height or width (**Remember if you using height on img the parent have to use the same, and equally with width**).
- With this it should resize the image according the parent tag
- If the parent element has **vertical-align: middle** and also has **box-shadow** probably the image would have a white space below. To fix that you can use on child element (The img tag or image class of course) **vertical-align: top** or with **display:block**

## REM (root em) and EM
- Is normally used on Font size.
- When **rem** is used on margin, also padding has to do it, for better dynamic results. (**Be careful** when is used on margin).
- Using **rem** is a very good way to create a dinamically website, it's very recommended.
- The difference between **rem** and **em** is that **rem** use the root element as base to get the size (**The Root element could be the html or the web browser, that way if someone in their web browser has a font-size's modification on settings, this will be affect the website as well**). And **em** will take the reference size from the closest parent element, and this will affect child element differently to the rest components.

## VW & VH
- vh means **Viewport Height**
- vw means **Viewport Width**
- Besides of using percetange %. This is another good option to work with.
- Be aware about if you are using **height** and nothing happens, check on devtools if **height** is equal 0. One of the options to fix that is adding on **body** or **html** **height: 100%** (In case the height for any reason is not working).

## JS
- Added **variableName.className** will overwrite the complete class list, so **Be aware** using this.
- The best option to add and remove classes is with **variableName.classList.** (It has more components than add and remove stuff).


