# EXERCISM

Exercism is a platform with several coding exercises for all sorts of programming languages.

## Table of Contents

- [About](#about)
- [Getting Started](#getting-started)
- [Running Tests](#tests)
- [Community](#community)
- [Credits](#credits)
- [Author](#author)
- [License](#license)

## About <a name = "about"></a>

As I have time, I will be doing some Javascript exercises and posting the answers here. It's an interesting platform but far more confusing than it needs to be - for some reason.

### Possible improvements

A lot of times it's not clear what the exercise actually wants and you have to run the tests to grasp what kind of answer it will accept - something that a more clear question would have easily solved. I say that because it makes the learning curve to use this platform unnecessarily harder.

There is one exercise that says:

```bash
From the example above:
brown-green should return 15
```

So you would think it will take a `string` `"brown-green"` as an argument and it returns a `number`, but in reality the question will test an `array` `["brown", "green"]`. Why not say the function takes an array with each color?

If they just give an example or make it clear what kind of data they expect in the answer, it would make things much better.

## Getting Started <a name = "getting-started"></a>

You have to [install](https://exercism.io/tracks/javascript/installation) it via node.js in order to run the tests and submit your answer.

## Running the test suite <a name = "tests"></a>

I'll explain here how to run tests because their explanation is kind of confusing too.

```bash
npm test
```

This part is pretty straigh-forward but most questions have more than one test to run and you have to manually change a file in order to run the next test. In the exercise page they say you have to change the name from `xtest` to `test` but they don't say where.

There is a file with the same name as the exercise:

```bash
exercise.js
exercise.spec.js
```

Inside the second file you will find the tests:

```javascript
describe("twoFer()", () => {
  test("no name given", () => {
    expect(twoFer()).toEqual("One for you, one for me.");
  });

  xtest("a name given", () => {
    expect(twoFer("Alice")).toEqual("One for Alice, one for me.");
  });

  xtest("another name given", () => {
    expect(twoFer("Bob")).toEqual("One for Bob, one for me.");
  });
});
```

In this case, there are 3 tests. If you run `npm test` and it passes the first test, you go to this file and change the first `xtest()` function name to `test()`, run again, if it passes you change the next `xtest()` and so on and so forth.

## Community <a name = "community"></a>

Since this is a learning platform, most people post their answer on the community section. It's always interesting to check how other people solved the same problem, you can always learn something and add a few new tricks up your sleeve.

## Credits <a name = "credits"></a>

[Exercism](https://exercism.io/)

## Author <a name = "author"></a>

[@psudo-dev](https://github.com/psudo-dev)

## License <a name = "license"></a>

This project is licensed under the MIT License - see the [LICENSE.md](./LICENSE.md) file for details
