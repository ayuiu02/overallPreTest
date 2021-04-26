**Name : Ayu Isnaini <br/>
Position Applied : Software Engineer in Test<br/>**

**Basic Programming**<br/>
1.	What is the data-type usually used in arithmetic operation? <br/>
Answer: <br/>
Data-type usually used in arithmetic operation are: integer, float, and double.<br/>

2.	What is the data-type usually used in word and character? <br/>
Answer:<br/>
Data-type usually used in word and character are: string, char, and text.<br/>

3.	Output: 113<br/>
Operation that happened in manual:<br/>
a = 100 + (3 x 5) – (10 / 5);<br/>
a = 100 + 15 – 2;<br/>
a = 100 + 13;<br/>
a = 113;<br/>

4.	Output: 2<br/>
Operation that happened in manual:<br/>
When i = 0 -> a = 2;<br/>
When i = 1 -> a = 4;<br/>
When i = 2 -> a = 6;<br/>
When i = 3 -> a = 8;<br/>
When i = 4 -> a = 10;<br/>
When i = 5 -> a = 12;<br/>
So a / 6 = 12 / 6 = 2<br/>

5.	Output: 3566GoldenStreetMiami<br/>
Reason: because the system replacing “ “ with “” while showing the address using replace() method.<br/>

**Flaky Test**<br/>
1. What is a flaky test?
Answer:<br/>
Flaky test is testing which produced inconsistent result. Sometimes the testing got failed while in the other time it got passed.<br/>

2. An element in a website is using ajax/javascript to show the data (processed as asynchronous). What do you do to test that element?
Answer:<br/>
Based on what I read, to test website which has ajax/javascript on it, one of the way is we could use implicitlyWait() in Selenium. So if we have a form using AJAX to shows the data, then we could set timeout in our script for several second so then we could ensure certain component is there or not.<br/>

3. A website page can only be accessed with CAPTCHA. How do you test that page?
Answer:<br/>
Based on what I read, to handle captcha testing we could set static captcha in our testing environment.<br/>

**Essay Question Topic**<br/>
1. Create automation test script to test these end-point:<br/>
a. GET -> https://jsonplaceholder.typicode.com/posts -> To make sure this
end-point have a correct data-type below:
- userId -> Integer<br/>
- id -> Integer<br/>
- title -> String<br/>
- body -> String<br/>
Answer:<br/>
>const schema = {<br/>
  "type": "array",<br/>
  "items": [<br/>
    {<br/>
      "type": "object",<br/>
      "properties": {<br/>
        "userId": {<br/>
          "type": "integer"<br/>
        },<br/>
        "id": {<br/>
          "type": "integer"<br/>
        },<br/>
        "title": {<br/>
          "type": "string"<br/>
        },<br/>
        "body": {<br/>
          "type": "string"<br/>
        }<br/>
      },<br/>
      "required": [<br/>
        "userId",<br/>
        "id",<br/>
        "title",<br/>
        "body"<br/>
      ]<br/>
    }<br/>
  ]<br/>
};<br/>
pm.test('Schema is valid', () => {<br/>
    pm.response.to.have.jsonSchema(schema);<br/>
});

2. To create input in this endpoint https://jsonplaceholder.typicode.com/posts, I use the 'Body' > 'form-data' section in Postman and input the data based on these following data:<br/>
- key : title, value : recommendation
- key : body, value : motorcycle
- key : userId, value : 12

3. For web automation test, I choosed to create scenario for 'Login' functionality using integration between Eclipse (Java Language), Cucumber, Selenium WebDriver, and I created the report too in html format. I've stored my code in this following repository: https://github.com/ayuiu02/webAutomationPreTest

5. For mobile automation test, I choosed to create scenario for 'Login' functionality too using integration between Eclipse (Java language), Cucumber, Appium. I've stored my code in this following repository: https://github.com/ayuiu02/mobileAutomationPreTest
