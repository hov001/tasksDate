# __Date API, Descriptors, Getters / Setters__

## Source map

* Source
  * jsInfo
    * 1.date
      * 1.createDate.js
      * 2.getWeekDay.js
      * 3.howManyDays.js
  * 1.objWithGetSet.js
  * 2.bestAverageScore.js
  * 3.getMonths.js
  * 4.dayOfYear.js
  * 5.getWeekName.js
  * 6.formatDate.js
  * 7.getWeekOfMonth.js
* README.md

---

1. Write an object with getter/setter field name.

```js
  const obj = {
    name: [], // ['name', length][]
    set name,
    get name,
  }
  console.log(obj.name)
  obj.name = 'Vrezh, Artavazd';
  console.log(obj.name) // [['Vrezh', 7], ['Artavazd', 10]]
```

[Decision](./src/1.objWithGetSet.js)

---

2. The input is object, which `keys` are student's names and `values` are `array` of their scores. Find the student with the best average score.

```js
  getBestStudent({
    John: [100, 90, 80],
    Bob: [100, 70, 80],
  });
  // OUTPUT => "John"
  // John's avg = 90
  // Bob's avg = 83.33
```

[Decision](./src/2.bestAverageScore.js)

---

3. The function should produce the same output even if `dateStart` is greater than `dateEnd`.

| Input | Output |
| ----- | ------ |
| let january = new Date(2017, 0, 1); let march = new Date(2017, 2, 1); monthsInterval(january, march) | ['January', 'February', March'] |
| let december = new Date(2017, 11, 1); let january = new Date(2018, 0, 1); monthsInterval(december, january) | ['January', 'February', March'] |
| let january2017 = new Date(2017, 0, 1); let january2018 = new Date(2018, 0, 1); monthsInterval(january2017, january2018) | ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'] |

[Decision](./src/3.getMonths.js)

---

4. Each year has 365 or 366 days. Given a string date representing a Gregorian calendar date formatted as month/day/year,return the day-number of the year. All input strings in the tests are valid dates.

| Input | Output |
| ----- | ------ |
| dayOfYear("12/13/2020") | 348 |
| dayOfYear("12/17/2020") | 352 |
| dayOfYear("11/16/2020") | 321 |
| dayOfYear("1/9/2019") | 9 |
| dayOfYear("3/1/2004") | 61 |
| dayOfYear("12/31/2000") | 366 |

[Decision](./src/4.dayOfYear.js)

---

5. Write a function that, given a date (in the format MM/DD/YYYY), returns the day of the week as a string. Each day name must be one of the following strings: `Sunday`, `Monday`, `Tuesday`, `Wednesday`, `Thursday`, `Friday`, or `Saturday`.

To illustrate, the day of the week for "12/07/2016" is "Wednesday".

[Decision](./src/5.getWeekName.js)

---

6. Implement following function.

```js
  const formatDate = (date) => {
    return date;
  };

  console.log("Actual output: ", formatDate(new Date("2020-05-14")));
  console.log("Expected output", "14 May 2020");
```

[Decision](./src/6.formatDate.js)

---

7. Implement following function.

```js
  const getWeekOfMonth = () => {};
  const result = getWeekOfMonth(new Date(2017, 10, 9)); // => 2
```

[Decision](./src/7.getWeekOfMonth.js)