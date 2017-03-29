# #eggheadADay

## How do I #eggheadADay?
- Watch one [egghead.io](egghead.io) lesson a day
- Tweet about it for personal accountability
- Reinforce your knowledge of what you learned by creating a pull request adding to this readme.

##### Note: Click the tweet share button from the [egghead.io](egghead.io) lesson to easily tweet about the lesson.

##### Note: Use the templates in the templates directory to save time. Embed your tweet into the template. Click the tweet options menu, select embed tweet, copy the provided code. Paste it into your post and strip out the script tag. DONT FORGET TO ADD #eggheadADay to the tweet.

### Contributions are encouraged to better this project!

# Daily Lessons

## [ES6 Rest Parameters](https://egghead.io/lessons/javascript-es6-rest-parameters?course=learn-es6-ecmascript-2015)

### Example
```javascript
/* ES6 Rest parameters vs ES5 arguments keyword */

(function () {
  /* ES5 arguments keyword example */
  var personalInfo = function (name, cellNumber, address, twitterHandle) {
    // The arguments keyword provides access to the functions parameters using array like syntax
    // Note: Not all array methods are available to arguments as arguments is "array like"
    console.log(arguments); // Output:
    // { '0': 'Bob Dole', '1': '555-555-5555', '2': '123 Main St. Chicago, IL 87654', '3': '@bobdole' }

    console.log(arguments[0]); // Bob Dole
    console.log(arguments[3]); // @bobdole
    console.log(arguments.length); // 4
  }

  personalInfo('Bob Dole', '555-555-1234', '123 Main St. Chicago, IL 87654', '@bobdole');

  /* ES6 Rest parameters example */
  const personalInfo2 = (name, ...theRestOfPersonalInfo) => {
    // Arrow functions cannot use the arguments keyword.
    console.log(arguments); // { }

    // Rest parameters are litterally "The rest of the parameters"
    console.log(name, theRestOfPersonalInfo); // Output:
    // 'Bob Dole', ['555-555-1234', '123 Main St. Chicago, IL 87654','@bobdole']
    console.log(name, theRestOfPersonalInfo[1]); // 'Bob Dole' '123 Main St. Chicago, IL 87654'
  }

  // Notice in the function declartion I have one named parameter 
  // then a Rest Parameter to grab the rest of values passed to this function.  
  personalInfo2('Bob Dole', '555-555-1234', '123 Main St. Chicago, IL 87654','@bobdole');
})();
```


### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="es" dir="ltr">ES6 Rest Parameters - js Video Tutorial <a href="https://twitter.com/hashtag/pro?src=hash">#pro</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/OyVWzYccBp">https://t.co/OyVWzYccBp</a> <a href="https://twitter.com/hashtag/eggheadaday?src=hash">#eggheadaday</a> <a href="https://twitter.com/hashtag/js?src=hash">#js</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/842435671621042177">March 16, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/16/2017
___

## [Promises with ES6](https://egghead.io/lessons/ecmascript-6-promises-with-es6)

### Example
```javascript
/**
 * Promises with ES2015
 * Promises allow you to perform async behaviors in a sync manner.
 */

//Promise accepts a callback function, the callback has 2 parameters, resolve & reject.
const p = new Promise((resolve, reject) => {
  // switch true to false to test Promise reject()
  if (true) {
    resolve('Success');
  } else {
    reject('Rejected');
  }
});

// When a Promise is resolved the .then() will fire.
// then() accepts a callback method (I know....just use .then() and .catch() though :P)
p.then((data) => {
  // data is the argument passed into the resolve() method.
  console.log(data);
});

// When a Promise is rejected the .catch() will fire.
// if an Error occurs ANYWHERE in the Promise the .catch() will fire.
p.catch((error) => {
  // error is the argument passed into the catch() method.
  console.log(error);
});

/**
 * Let's chain the Promise methods
 */
const d = new Promise((resolve, reject) => {
  // switch true to false to test reject and the catch method.
  if (true) {
    resolve('Promise was resolved!');
  } else {
    reject('Promise was rejected :(');
  }
})
  .then((data) => {
    console.log(`Success : ${data}`);
    return 'foo bar';
  })
  .then((data) => {
    // What will data be here? What if there was no return statement in the previous .then() ?
    console.log(`I wonder what data will be? : ${data}`);
  })
  .catch(error => console.log(`Error : ${error}`));
```


### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Promises with ES6 - js Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/SpIvnk4UAq">https://t.co/SpIvnk4UAq</a><a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a> <a href="https://twitter.com/hashtag/js?src=hash">#js</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/842757415695278080">March 17, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/17/2017
___

## [Search the contents of files using grep](https://egghead.io/lessons/tools-search-the-contents-of-files-using-grep)

### Example
```
Grep returns all instances of lines found from the search phrase. Grep is CMD + F on steroids.

  $ grep gulp package.json

This will return all instances found of the term "gulp" within the package.json file. You can include multiple files to search through.

  $ grep gulp -r my_fake_project/js

This will recursively search everything in the js directory and return all instances found of the term "gulp"
```


### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Search the contents of files using grep - otherjs Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/BAbCQcnM09">https://t.co/BAbCQcnM09</a><br>by: <a href="https://twitter.com/brindelle">@brindelle</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a> <a href="https://twitter.com/hashtag/grep?src=hash">#grep</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/843873498862968833">March 20, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/20/2017
___
## [Manage Angular 2 Elements with Events and Refs](https://egghead.io/lessons/angular-2-using-events-and-refs?series=angular-2-fundamentals)

### Example
```javascript
/**
 * Angular 2 Elements with Events and Refs
 */

import { Component, OnInit } from '@angular/core';

@Component({
  // The DOM element type
  selector: 'app-simple-form',
  /* The View */
  /* The #myInput is how you place a reference on a DOM element */
  /* To place an event on an element you surround the Angular event with parenthesis */
  /* You then assign it a method and call the method */
  /* ex. (click)="onClick(myInput.value) */
  /* This calls the onClick Class method and passes the <input>'s value */
  template: `<div>
    <input #myInput type="text">
    <button (click)="onClick(myInput.value)">Click me!</button>
  </div>`,
  styles: []
})
export class SimpleFormComponent implements OnInit {

  constructor() { }

  ngOnInit() {
  }

  onClick(value) {
    console.log(`Input value is - ${value}`); // -> Whatever you type in #myInput text input.
  }
}
```

### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Manage Angular 2 Elements with Events and Refs - Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/xDWGJLdWc9">https://t.co/xDWGJLdWc9</a><br>By: <a href="https://twitter.com/johnlindquist">@johnlindquist</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/844935679012474880">March 23, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/23/2017
___
## [Adding badges to your README](https://egghead.io/lessons/javascript-how-to-write-a-javascript-library-adding-badges-to-your-readme)

### Example
Badges provide a quick and easy way for anyone to see the status of your project on Github.

Adding badges is extremely easy thanks to [shields.io](shields.io)
From [shields.io](shields.io) select a badge you want to place in your readme markdown file and simply copy/paste the image url into image mardown.
```
ex. ![travis build](https://img.shields.io/travis/rust-lang/rust.svg)
This gives you the badge seen below!
```
![travis build](https://img.shields.io/travis/rust-lang/rust.svg)

From here you can easily wrap the badge in a markdown link linking to your build status page!

### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Adding badges to your README - js Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/1NOdyhKUVT">https://t.co/1NOdyhKUVT</a><br>Now I know 🤘<br>By: <a href="https://twitter.com/kentcdodds">@kentcdodds</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/845293051539062786">March 24, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/24/2017
___
## [Observables are almost like Functions](https://egghead.io/lessons/rxjs-observables-are-almost-like-functions?series=rxjs-beyond-the-basics-creating-observables-from-scratch)

### Example
```javascript
// Observables are almost like functions
const plainFunc = () => {
  console.log('Hello!');
  return 7;
};

console.log(plainFunc());

// RxJS Observable
const foo = Rx.Observable.create((observer) => {
  console.log('Observable!');
  // .next() returns a value
  observer.next(5);
  // .next() can be called more than once to return multiple values!
  observer.next('Whoa, more values returned!');
  // async works just fine too
  setTimeout(() => observer.next(`I'm asynchronous!`), 1000);
  observer.next('Functions can only return a single value, I can return all the things!');
});

// Observables are like functions in that if you don't express interest 
// by calling a function or subscribing to an observable nothing will happen.

// subscribing to an Observable is like calling a function
// A function returns a single value immediately
// Subscribing to an observable says give me values, maybe just one value, immediately, or asynchronously.
foo.subscribe((x) => {
  // x will always be the value passed through .next() in the Observable
  console.log(x);
});
```


### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">GREAT EXPLANATION!<br>Observables are almost like Functions: rx Tutorial <a href="https://twitter.com/hashtag/pro?src=hash">#pro</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/vhNyLhtoRU">https://t.co/vhNyLhtoRU</a><br>By: <a href="https://twitter.com/andrestaltz">@andrestaltz</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a></p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/846375330415869954">March 27, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/27/2017
___
## [Introducing the Observable](https://egghead.io/lessons/javascript-introducing-the-observable)

### Example
```javascript
/* Introducing the Observable */

/**
 * An Observable is like an Array.
 * With an Array all data is stored in memory and has the data ready to pop-out synchronously.
 * An Observable is a collection of data where no data is stored in memory and the items arrive over time asynchronously.
 */

/* DOM Event Example */

// DOM events are very similiar to Observables.
const button = document.getElementById('btn');

// Event handler
const handler = (e) => {
  console.log('clicked');
  // removes or "Unsubscribes"
  button.removeEventListener('click', handler);
}

/**
 * @param Name of event
 * @param callback function
 */
button.addEventListener('click', handler);

/* Observable Example */

const obsButton = document.getElementById('obsBtn');

// An Observable is more powerful because it gives us an object to represent that Event Stream!
const clicks = Rx.Observable.fromEvent(obsButton, 'click');

// Since Observables are asynchronous unlike Arrays the native Array forEach method will not work. Subscribe accepts 3 callbacks.
const subscription = clicks.subscribe(
  // 1) onNext
  (e) => {
    console.log('click!');
    // We don't care about anymore onNext method or any callbacks
    subscription.unsubscribe();
  },
  // 2) onError
  (err) => console.log('ERROR! ', err),
  // 3) onCompleted
  () => console.log('Done!')
);
```

### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Introducing the Observable - js Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/OxxBAKtdCv">https://t.co/OxxBAKtdCv</a><br>By: <a href="https://twitter.com/jhusain">@jhusain</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a> <a href="https://twitter.com/hashtag/RxJs?src=hash">#RxJs</a><br>Observables are 🔥‼️</p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/846751030138327040">March 28, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/28/2017
___
## [Using the map method with Observable](https://egghead.io/lessons/javascript-using-the-map-method-with-observable)

### Example
```javascript
/* Observable Map Example */

const obsButton = document.getElementById('obsBtn');

// Creates an Observable from a click event
// Maps over each click event projecting an object
const clicks = Rx.Observable.fromEvent(obsButton, 'click')
  .map(e => ({ x: e.clientX, y: e.clientY }));

// Subscription to the clicks Observable
// pass the onNext callback to the subscribe method
const subscription = clicks.subscribe((point) => {
    console.log('clicked! ', JSON.stringify(point))
    subscription.unsubscribe();
  });

/**
 * Just like Arrays we can .map, filter, concat, etc on Observables to project new Observables!
 **/
```

### Tweet
<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Using the map method with Observable - js Video Tutorial <a href="https://twitter.com/hashtag/free?src=hash">#free</a> <a href="https://twitter.com/eggheadio">@eggheadio</a>: <a href="https://t.co/9BVcF4J7Te">https://t.co/9BVcF4J7Te</a><br>By: <a href="https://twitter.com/jhusain">@jhusain</a> <a href="https://twitter.com/hashtag/eggheadADay?src=hash">#eggheadADay</a> 🗺️</p>&mdash; Sean Groff (@_SeanGroff) <a href="https://twitter.com/_SeanGroff/status/847106884582719488">March 29, 2017</a></blockquote>

### Github Contributor
[@SeanGroff](https://github.com/SeanGroff) :koala:

##### Date - 03/29/2017
___
