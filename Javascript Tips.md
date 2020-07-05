# Javascript Tips

[Reference](https://gosink.in/common-javascript-promise-mistakes-beginners/)

* Using promise.all() saves time

Change this 

```
const { promisify } = require('util');
const sleep = promisify(setTimeout);

async function f1() {
  await sleep(1000);
}

async function f2() {
  await sleep(2000);
}

async function f3() {
  await sleep(3000);
}

// Running code sequentially
(async () => {
  console.time('sequential');
  await f1();
  await f2();
  await f3();
  console.timeEnd('sequential'); // Approx 6 seconds
})();
```
to

```
(async () => {
  console.time('concurrent');
  await Promise.all([f1(), f2(), f3()]);
  console.timeEnd('concurrent'); // Approx 3 seconds
})();
```
