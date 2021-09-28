---
templateKey: blog-post
title: Can You Run TypeScript Directly in the Brower
date: 2021-09-01T21:35:10.888Z
description: I'm working on a new React application that uses TypeScript as the
  language of choice.  I'm well aware that TypeScript is transpiled into
  JavaScript for most, if not all, applications.  But that begs the
  question.  Can you run TypeScript directly in the browser without the extra
  step of transpiling into JavaScript?  It would definitely be nice to be able
  to save a step in the development process and just load TypeScript files
  especially when you are building large applications.
featuredpost: true
featuredimage: /img/browser.jpg
---
So can you run TypeScript directly in the browser? **Currently, web browsers don't support running TypeScript without the additional step of transpiling the code into JavaScript.** Most modern web browsers support certain features that have been defined in various versions of ECMAScript, which is the JavaScript standards definition to help ensure browsers treat code similarly. But since TypeScript is a superset of JavaScript and supports more features, TypeScript is not directly supported by browsers.

This idea can definitely seem frustrating for new and existing users of TypeScript. Especially because TypeScript and JavaScript seem to be closely related. Which they are. But the issues run much deeper than the languages themselves.

## The Future of TypeScript in the Browser

If you take a look at the evolution of the standards definition for JavaScript, known as <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-262/" target="_blank">ECMAScript</a>, you could probably deduce that eventually, that definition would catch up to the features of TypeScript. At that point, it would make sense to be able to run TypeScript in the browser.

While this is a very nice dream we have, in reality, the odds of this happening are very slim. There are a few main reasons you shouldn't hold your breath for TypeScript support in browsers.

### It's a Moving Target

The problem with this train of thought is that while the standards being defined are moving forward, so is TypeScript. TypeScript, itself, is continually evolving as a language and growing and changing as well. If it were to stand still long enough, the ECMAScript standards definitely would catch up to its list of features.

But like anything else in technology, if it slows to a standstill, it will eventually die and be taken over by something new and growing.

### Browser Feature Adoption

The fact that there is even a standards definition at all for JavaScript and features supported by browsers is definitely commendable.

But that is exactly the problem. **Feature support**.

Versions for ECMAScript are typically defined by the years that they come out. Things like ECMAScript 2015, 2016, etc are common to see. They are also given shorthand abbreviations like ES5, ES6, etc. So, you would probably think that since we are into the 2020s that all the features previously defined in a previous decade would be supported by browsers.

But you would be wrong.

Browser developers don't set out to support whatever version of the standard that came out in the current or previous year. They typically have a business to run and a product to ship, just like any other company.

So they typically go through the standards and implement the features that make the most sense for them to support and that their customers want.

So what does that mean?

It means that even though a particular version of a modern browser may support all the features of the standards definition that came out in 2016, it may only have support for one or two that came out in 2015.

## Browsers Adding Support for TypeScript

Since browser developers are spending so much time adding features, why don't they just pony up and add TypeScript support?

The wound goes pretty deep, I'm afraid.

The demand on browsers over the years has only gotten exponentially larger. Think of the amount of time you spend on the internet. What's the first thing you do if your browser starts to get slow or pages start to load very slowly?

Do you blame the site you are looking at?

Do you sit and wait patiently for the page to load?

Probably not.

You probably close your browser and try again. And if this happens too many times, you may even consider getting a new browser.

It's a war!

Browser developers don't have the time and resources to stop what they are doing and add support for TypeScript for a couple of main reasons:

### Cost

Money makes the world go 'round.

It's just a fact of life.

But when it comes to the cost of features and added support to browsers, what exactly does that mean? If you think about the time that it would take to add support for TypeScript to a browser, let's just do some crude math.

Imagine it would take a year to fully add support for TypeScript to the popular modern browsers (Chrome, Firefox, Safari, IE/Edge).

Based on the estimated salaries of mid-level software engineers, product managers, and QA engineers at those companies, this is roughly what it would cost per company to add that support.

<table><tbody><tr><td class="has-text-align-center" data-align="center"><strong>Company</strong></td><td class="has-text-align-center" data-align="center"><strong>Mid-Level Engineer Salary</strong></td><td class="has-text-align-center" data-align="center"><strong>Number of Engineers</strong></td><td class="has-text-align-center" data-align="center"><strong>Total Cost</strong></td></tr><tr><td class="has-text-align-center" data-align="center">Google</td><td class="has-text-align-center" data-align="center">$160,000</td><td class="has-text-align-center" data-align="center">10</td><td class="has-text-align-center" data-align="center">$1,600,000</td></tr><tr><td class="has-text-align-center" data-align="center">Mozilla</td><td class="has-text-align-center" data-align="center">$150,000</td><td class="has-text-align-center" data-align="center">10</td><td class="has-text-align-center" data-align="center">$1,500,000</td></tr><tr><td class="has-text-align-center" data-align="center">Apple</td><td class="has-text-align-center" data-align="center">$150,000</td><td class="has-text-align-center" data-align="center">10</td><td class="has-text-align-center" data-align="center">$1,500,00</td></tr><tr><td class="has-text-align-center" data-align="center">Microsoft</td><td class="has-text-align-center" data-align="center">$140,000</td><td class="has-text-align-center" data-align="center">10</td><td class="has-text-align-center" data-align="center">$1,400,000</td></tr></tbody></table>

Average salaries based on data at <a href="https://www.levels.fyi/" target="_blank">levels.fyi</a>

<table><tbody><tr><td class="has-text-align-center" data-align="center"><strong>Company</strong></td><td class="has-text-align-center" data-align="center"><strong>Product Manager Salary</strong></td><td class="has-text-align-center" data-align="center"><strong>Number of Product Managers</strong></td><td class="has-text-align-center" data-align="center"><strong>Total Cost</strong></td></tr><tr><td class="has-text-align-center" data-align="center">Google</td><td class="has-text-align-center" data-align="center">$180,000</td><td class="has-text-align-center" data-align="center">2</td><td class="has-text-align-center" data-align="center">$360,000</td></tr><tr><td class="has-text-align-center" data-align="center">Mozilla</td><td class="has-text-align-center" data-align="center">$130,000</td><td class="has-text-align-center" data-align="center">2</td><td class="has-text-align-center" data-align="center">$260,000</td></tr><tr><td class="has-text-align-center" data-align="center">Apple</td><td class="has-text-align-center" data-align="center">$170,000</td><td class="has-text-align-center" data-align="center">2</td><td class="has-text-align-center" data-align="center">$340,000</td></tr><tr><td class="has-text-align-center" data-align="center">Microsoft</td><td class="has-text-align-center" data-align="center">$140,000</td><td class="has-text-align-center" data-align="center">2</td><td class="has-text-align-center" data-align="center">$280,000</td></tr></tbody></table>

Average salaries based on data at <a href="https://www.levels.fyi/" target="_blank">levels.fyi</a>

<table><tbody><tr><td class="has-text-align-center" data-align="center"><strong>Company</strong></td><td class="has-text-align-center" data-align="center"><strong>QA Engineer</strong></td><td class="has-text-align-center" data-align="center"><strong>Number of QA Engineers</strong></td><td class="has-text-align-center" data-align="center"><strong>Total Cost</strong></td></tr><tr><td class="has-text-align-center" data-align="center">Google</td><td class="has-text-align-center" data-align="center">$140,000</td><td class="has-text-align-center" data-align="center">3</td><td class="has-text-align-center" data-align="center">$420,000</td></tr><tr><td class="has-text-align-center" data-align="center">Mozilla</td><td class="has-text-align-center" data-align="center">$120,000</td><td class="has-text-align-center" data-align="center">3</td><td class="has-text-align-center" data-align="center">$360,000</td></tr><tr><td class="has-text-align-center" data-align="center">Apple</td><td class="has-text-align-center" data-align="center">$130,000</td><td class="has-text-align-center" data-align="center">3</td><td class="has-text-align-center" data-align="center">$390,000</td></tr><tr><td class="has-text-align-center" data-align="center">Microsoft</td><td class="has-text-align-center" data-align="center">$120,000</td><td class="has-text-align-center" data-align="center">3</td><td class="has-text-align-center" data-align="center">$360,000</td></tr></tbody></table>

Average salaries based on data at <a href="https://www.levels.fyi/" target="_blank">levels.fyi</a>

If you were to look at this as a whole per company, we're talking about anywhere between 2 and 3 million dollars!

And I haven't even factored in time from designers, architects, program managers, etc. As you can see this could get very expensive!

### Time

So what is happening to the existing browser that these companies have built and support while TypeScript is getting added into the mix?

Not much, that's what.

Yes, I know that there are more than 10 software engineers that work at these companies. But you can't continue to add a bunch more features to these browsers while you are trying to add native support for TypeScript.

Why not?

We get back to the whole moving target analogy that I mentioned earlier.

If you start adding support for TypeScript _and_ continue adding new features to the browser that these engineers have to support with TypeScript, the two ends will never meet.

Not to mention the fact that what is more important to these companies when it comes to users of their product? End-users or developers? I'm sure you probably know the answer to that one.

## Workarounds

So if there is currently no native support for TypeScript in the browser AND these companies aren't going to add support for it anytime in the near future, is there at least a workaround?

Well....sort of.

At the end of the day, the browsers NEED your code to be in JavaScript so it can run "correctly". But that doesn't necessarily mean that you have to feed it JavaScript.

What does that mean?

There are actually ways that you can have the heavy lifting of <a href="https://github.com/harrysolovay/ts-browser" target="_blank">transpiling the TypeScript to JavaScript handled inside the browser</a>.

The typical flow of web applications looks something like this:

![TypeScript in Browser](/img/typescript-deploy.jpg)

<br/>

The web application is written in TypeScript. The build process takes place either on a development machine or more typically on a build server somewhere and the resulting application, transpiled into JavaScript is hosted in a CDN somewhere.

Then, when the user opens the application in the browser, the browser downloads the application code from the CDN, loads it in the browser, and everyone is happy.

This flow can change to something like this:

![TypeScript in browser](img/typescript-direct-deploy.jpg)


Where the TypeScript code is not transpiled in advance and just loaded into the CDN directly. From there, when the user opens the application in the browser, the browser downloads the application code from the CDN, transpiles it into JavaScript, loads the resulting JavaScript, and everyone is happy.

That may not seem like a big jump, but web browsers were never designed to handle that type of processing where it would need to transpile potentially hundreds of thousands of lines of code and then run it.

I'm sure you could image how long something like that would take.

Users would be none-to-pleased.

## What to do as a TypeScript Developer

So, what exactly are we, as TypeScript developers, to do about this mess we are in?

Wait...

Patiently...

And stay the course.

Over the years some really good tools and build processes have been created for just such times. There may come a time when we don't have to do the extra step of transpiling our code into JavaScript, but unfortunately that time doesn't look to be that close.