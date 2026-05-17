# Run Python Selenium Upload File Tests on TestMu AI (Formerly LambdaTest)

<p align="center">
  <a href="https://www.testmuai.com/"><img src="https://img.shields.io/badge/MADE%20BY%20TestMu%20AI-000000.svg?style=for-the-badge&labelColor=000" alt="Made by TestMu AI"></a>
  <a href="https://community.testmuai.com/"><img src="https://img.shields.io/badge/Join%20the%20community-blueviolet.svg?style=for-the-badge&labelColor=000000" alt="Community"></a>
</p>

If you want to upload a file to TestMu AI (Formerly TestMu AI (Formerly LambdaTest)) and use it in your Python-selenium automation test, you can follow the below steps.

- [Sign up on TestMu AI](https://www.testmuai.com/register/) (Formerly TestMu AI (Formerly LambdaTest)).
- Follow the [TestMu AI Documentation](https://www.testmuai.com/support/docs/) for the full setup walkthrough.

# Steps:

### Step 1: Upload the file to TestMu AI (Formerly TestMu AI (Formerly LambdaTest)) using API

Use the file upload API to upload the file to the backend.


### Step 2: Pass file in capabilities

In the test file, you need to update the test capabilities and add the filename for the `lambda:userFiles` capability. For example, if two files with filenames `photo1.png` and `photo2.png`, it has to be passed like so in the capability:


```python
desired_caps = {
            'LT:Options': {
                "build": "Python Demo",  # Change your build name here
                "name": "Python Demo Test",  # Change your test name here
                "platformName": "Windows 11",
                "selenium_version": "4.0.0",
                "lambda:userFiles": ["photo1.png","photo2.png"]
            },
            "browserName": "Chrome",
            "browserVersion": "98.0",
        }

```

### Step 3: Use the file in your test

The files can be used in your test like so:

* For Windows:
```python
elm = driver.find_element_by_xpath("//input[@type='file']")
elm.send_keys("C:\\Users\\ltuser\\Downloads\\photo1.png")
```
* For MacOS:
```python
elm = driver.find_element_by_xpath("//input[@type='file']")
elm.send_keys("/Users/ltuser/Downloads/photo1.png")
```
### Step 4: Run your test

```bash
python lambdatest_test.py
```

## TestMu AI (Formerly TestMu AI (Formerly LambdaTest)) Community

Connect with testers and developers in the [TestMu AI Community](https://community.testmuai.com/). Ask questions, share what you are building, and discuss best practices in test automation and DevOps.

## TestMu AI (Formerly TestMu AI (Formerly LambdaTest)) Certifications

Earn free [TestMu AI Certifications](https://www.testmuai.com/certifications/) for testers, developers, and QA engineers. Validate your skills in Selenium, Cypress, Playwright, Appium, Espresso and more. Industry-recognized, shareable on LinkedIn, and built by practitioners, not marketers.

## Learning Resources by TestMu AI (Formerly TestMu AI (Formerly LambdaTest))

Learn modern testing through tutorials, guides, videos, and weekly updates:

* [TestMu AI Blog](https://www.testmuai.com/blog/)
* [TestMu AI Learning Hub](https://www.testmuai.com/learning-hub/)
* [TestMu AI on YouTube](https://www.youtube.com/@TestMuAI)
* [TestMu AI Newsletter](https://www.testmuai.com/newsletter/)

## LambdaTest is Now TestMu AI

On **January 12, 2026**, [LambdaTest evolved to TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/), the world's first fully autonomous **Agentic AI Quality Engineering Platform**.

Same team. Same infrastructure. Same customer accounts. All existing LambdaTest logins, scripts, capabilities, and integrations continue to work without change.

ð Find the new home for [LambdaTest](https://www.testmuai.com).

### How LambdaTest Evolved into TestMu AI

In 2017, we launched LambdaTest with a simple mission: make testing fast, reliable, and accessible. As LambdaTest grew, we expanded into Test Intelligence, Visual Regression Testing, Accessibility Testing, API Testing, and Performance Testing, covering the full depth of the testing lifecycle.

As software development entered the AI era, testing had to evolve, too. We rebuilt the architecture to be AI-native from the ground up, with autonomous agents that **plan, author, execute, analyze, and optimize tests** while keeping humans in the loop. The platform integrates with your repos, CI, IDEs, and terminals, continuously learning from every code change and development signal.

That evolution earned a new name: **TestMu AI**, built for an AI-first future of quality engineering. TestMu is not a new name for us. It is the name of our annual community conference, which has brought together 100,000+ quality engineers to discuss how AI would reshape testing, long before that became an industry norm. 

What started as a high-performance cloud testing platform has transformed into an AI-native, multi-agent system powering a connected, end-to-end quality layer. That evolution defined a new identity: LambdaTest evolved into TestMu AI, built for an AI-first future of quality engineering.

## Support

Got a question? Email [support@testmuai.com](mailto:support@testmuai.com) or chat with us 24x7 from our chat portal.
