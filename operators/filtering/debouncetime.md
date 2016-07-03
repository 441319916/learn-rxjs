# debounceTime
####signature: `debounceTime(dueTime: number, scheduler: Scheduler): Observable`
*The gist: Throw away all emitted values that take less then the specified time between output...*

( [jsBin](http://jsbin.com/kacijarogi/1/edit?js,console,output) | [jsFiddle](https://jsfiddle.net/qg6qfqLz/14/) | [official docs](http://reactivex.io/rxjs/class/es6/Observable.js~Observable.html#instance-method-debounceTime) )

```js
const input = document.getElementById('example');

//for every keyup, map to current input value
const example = Rx.Observable
  .fromEvent(input, 'keyup')
  .map(i => i.currentTarget.value);

//wait .5s between keyups to emit current value
//throw away all other values
const debouncedInput = example.debounceTime(500);

//log values
const subscribe = debouncedInput.subscribe(val => {
  console.log(`Debounced Input: ${val}`);
});
```

### How debounceTime works...
*Coming soon...*


### Additional Resources
* [Transformation operator: debounce and debounceTime](https://egghead.io/lessons/rxjs-transformation-operators-debounce-and-debouncetime?course=rxjs-beyond-the-basics-operators-in-depth) :video_camera: :dollar: - André Staltz
