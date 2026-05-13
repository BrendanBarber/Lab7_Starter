# Lab 7 - Unit & E2E Testing



**1) Where would you fit your automated tests in your Recipe project development pipeline?**

Within a Github action that runs whenever code is pushed. This way the test always happens, it's not a choice or something that can be forgotten. It will also catch things early in development, as opposed to during deployment when it's already causing users issues. It also avoids a lot of the "it works on my machine" bugs by standardizing the testing environment.

**2) Would you use an end to end test to check if a function is returning the correct output? (yes/no)**

No. End-to-end tests are designed to emulate real user interactions with the application from start to finish (clicking buttons, navigating pages, filling out forms, etc.). To check whether a single function returns the correct output, a unit test is the right tool because it isolates that function and runs much faster than spinning up a browser.

**3) What is the difference between navigation and snapshot mode?**

Navigation mode analyzes a page right after it loads, providing an overall performance metric for the initial page load (but it cannot analyze user interactions or changes in content after the page has loaded). Snapshot mode, on the other hand, analyzes a page in its current state at the time the audit runs, good for finding accessibility issues.

**4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.**

1. Add proper image dimensions / use `width` and `height` attributes on `<img>` tags to prevent layout shifts
2. Add descriptive alt text to images and interactive elements so the page is more accessible to screen readers.
3. Optimize images by compressing them and serving them in smaller to reduce page load time and improve the Performance score.
