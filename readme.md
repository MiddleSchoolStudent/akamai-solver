# Akamai Solver

We have successfully used our **[BotBrowser](https://github.com/MiddleSchoolStudent/BotBrowser)** for extensive testing with Akamai V2, V3 and were able to get very good \_abck without failing for a long time. Check out the video demo at playstation.com. The test code is [here](https://github.com/MiddleSchoolStudent/BotBrowser/blob/main/tests/tests/antibots/akamai.spec.ts).

<video src="https://raw.githubusercontent.com/MiddleSchoolStudent/BotBrowser/main/tests/test-results/akamai-test-playstation-com-BotBrowser-antibots/video.webm"></video>

---

The purpose of this repo is to analyze how Akamai bot manager collects fingerprints, analyze how it works, and based on playwright, write some code to bypass it.

This file is the [Akamai bot manager](akamai-bm.js) after de-obfuscation.

**Note** that it is not wise to use Python / nodejs / go to write code that puts together sensorData and POSTs the data directly, as Akamai detects TLS fingerprints, see [here](https://www.blackhat.com/docs/eu-17/materials/eu-17-Shuster-Passive-Fingerprinting-Of-HTTP2-Clients-wp.pdf).

So we can use playwright and combine it with bypass code to make the request using the browser.
