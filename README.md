# Frontend Mentor - Interactive card details form solution

This is a solution to the [Interactive card details form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-card-details-form-XpS8cKZDWw). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

-   [Overview](#overview)
    -   [The challenge](#the-challenge)
    -   [Screenshot](#screenshot)
    -   [Links](#links)
-   [My process](#my-process)
    -   [Built with](#built-with)
    -   [What I learned](#what-i-learned)
    -   [Continued development](#continued-development)
    -   [Useful resources](#useful-resources)
-   [Author](#author)

## Overview

### The challenge

Users should be able to:

-   Fill in the form and see the card details update in real-time
-   Receive error messages when the form is submitted if:
    -   Any input field is empty
    -   The card number, expiry date, or CVC fields are in the wrong format
-   View the optimal layout depending on their device's screen size
-   See hover, active, and focus states for interactive elements on the page

### Screenshot

Desktop:
![Desktop initial state](/design/desktop-init.png)

![Desktop active state](/design/desktop-active.png)

![Desktop form submission state](/design/desktop-form-submission.png)

Mobile:

![Mobile initial state](/design/mobile-init.png)

### Links

-   [Live Site URL](https://interactive-payment-ianwilk20.netlify.app/design/)

## My process

### Built with

-   Semantic HTML5 markup
-   CSS custom properties
-   Flexbox

### What I learned

-   Learned when to use a div and when to use a section. In past projects, I believe I overused sections and in places where I just wanted some kind of wrapper or container to apply styles to, I used a section rather than a div. I thought by using semantic elements like section I would be improving accessibility, but I learned that overusing/misusing semantic element could hurt accessibility rather than improve it.

-   The input type number is the worst input type for a number of reasons: numbers aren't the only valid input, inconsistency in accpeted charactersd across browsers, min and max limits are not enforced, invalid values aren't retrieved the way they are typed. The advantage of using an input of type number is that it natively allows keyboard users to increment and decrement the value with up and down arrows and it makes it easier for screen readers to read the input. The form validation I needed to perform required getting the whole value of the inputs, so I switched my input's of type number to input's of type text.

-   The floating cards took the longest time to implement because I had trouble conceptualizing how to allow them to be responsive and hover on top of each other in a static way. For the hovering of the cards I put them in a wrapper that had a `position: absolute` and the closest parent of the wrapper had a `position: relative`. This allowed me to overlay the cards over the blurred purple background. I found the best way to constrain the cards over various screen sizes was to define a `min-width` for the card wrapper class, and increase/decrease that min-width depending on the screen breakpoints. The backside of the card was aligned to the end and the frontside of the card was aligned to the start. I then transformed the card's y positions so they overlapped. I'm sure there could have been a more elegant solution to this problem by using different display grid variations over screen breakpoints, but I wasn't able to figure out that solution.

### Continued development

Going forward I look forward to improving my understanding of position types so that I can intuitively look at a project's mockup like this and identify which position types I'll use. Additionally, I would like to get better at using display types other than flex, specifically grid.

### Useful resources

-   [Why the number input is the worst input](https://stackoverflow.blog/2022/12/26/why-the-number-input-is-the-worst-input/) - An exceptional blog about the advantages and disadvantages of input's of type number and what to use instead.
-   [What is the difference between section and div tags in HTML ?](https://www.geeksforgeeks.org/what-is-the-difference-between-section-and-div-tags-in-html/) and [The Best Way to Implement a “Wrapper” in CSS](https://css-tricks.com/best-way-implement-wrapper-css/)- These two articles helped me stop my overuse of `section` and understand the differences between the div's and section's and when to use which.

## Author

-   GitHub - [ianwilk20](https://github.com/ianwilk20)
