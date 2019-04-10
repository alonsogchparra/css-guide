# CSS Guide

This a repo to keep the knowledge from the udemy tutorial [CSS - The Complete Guide](https://www.udemy.com/css-the-complete-guide-incl-flexbox-grid-sass/) by Maximilian Schwarzmüller and Manuel Lorenz

Will be divide in modules to move the basics topics to advance ones.

Only need to have basic knowledge about HTML and CSS3 to follow this.

# Reminders IMPORTANT

## Outline
We use **outline** to avoid the blue border the web browser has for default. Use it on pseudo class **focus** and to avoid the blue border put **none**.
Example:
```
.fooclass:focus {
  outline: none;
}
```

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

## Media Queries
- Mobile First (**VERY RECOMMENDED**).
- If you going with **Mobile First** the original CSS code will be use for mobile and the queries will be use for bigger dispositives.
- To find a correct **Break Point**. You could check this site [mydevice.io](www.mydevice.io). Check which width are more usual (or more repetitive), this will apply for mobiles, tablets and desktops and take that as a reference.
- The **OR** operator in Media queries is with comma (,) and the **AND** operator with ```and```.
- If the media query will have more than one condition, please check these make sense.
- You can work with portrait and landscape oritantion. But the best way si usin a height (Example: ```min-height: 40rem```).
- **NOTE**: If you problem to fix the footer, keep it in the bottom of the page. The best recommendention is stablish a **minimum height** (```min-height```) with calculation. Example:

```
min-height: calc(100vh - 3.5rem - 8rem);
```
The first value on the calculation will take the viewport height, teh second one will take the height of nav and the third one of the footer. The value of nav and footer are taken using the devtool. You have to check the original height with the padding and margin (if the nav or footer have them).

Example: The nav from module 10 has a padding the height of the nav according the devtool is **47.938(px)** and the padding top and bottom is **8px** if we sum these values will be **55.938px**. Taking a rounded number will be **56px**. Taking this value to **REM** will be **3.5rem** (The second value of the previous calculation).

## Checkbox

- To make the style on checkbox works, you have to add **appearance:none;**. But remember to add the condition to make work on all web browser
```
-webkit-appearance: none;
-moz-appearance: none;
appearance: none;
```

## Fonts

- It's better work with fonts import them on css file. And if the font will be in all the project you have to create an shared.css file to only be use for that propouse (Not only for font, it's good to have a shared file where the changes are the same in different parts).
- **line-height** is asociate with **font-family** so when you have to work with this, you have to use int numbers like 1, 2... the line-height will take the int part of you font-size and take that as reference to add the line-height you want. For example your font-size is **19px** and you going to use **line-hegiht: 2** the height will be **38px**. You can check that on devtools.