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

