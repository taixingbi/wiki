### improve-performance
resize, scroll, and keyup/keydown events


### debounce
delays the processing of the keyup event until the user has stopped typing for a predetermined amount of time.

     // ES6
    function debounced(delay, fn) {
      let timerId;
      return function (...args) {
        if (timerId) {
          clearTimeout(timerId);
        }
        timerId = setTimeout(() => {
          fn(...args);
          timerId = null;
        }, delay);
      }
    }


### throttle
cause the event listener to ignore some portion of the events while still firing the listeners at a constant (but reduced) rate

    // ES6 code
    function throttled(delay, fn) {
      let lastCall = 0;
      return function (...args) {
        const now = (new Date).getTime();
        if (now - lastCall < delay) {
          return;
        }
        lastCall = now;
        return fn(...args);
      }
    }


### reference
[1] [Debounce in JavaScript — Improve Your Application’s Performance](https://levelup.gitconnected.com/debounce-in-javascript-improve-your-applications-performance-5b01855e086)     
[2] [Throttling and debouncing in JavaScript](https://codeburst.io/throttling-and-debouncing-in-javascript-646d076d0a44)
