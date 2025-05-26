# PostgreSQL Interview Questions 

<hr/>

<h3>1. What is PostgreSQL?</h3>
<p><strong>PostgreSQL</strong> একটি শক্তিশালী, ওপেন-সোর্স Relational Database Management System (RDBMS)। এটি ডেটা সংরক্ষণ, পুনরুদ্ধার ও বিশ্লেষণের জন্য ব্যবহৃত হয়। PostgreSQL ACID-compliant এবং উন্নত ফিচার যেমন JSON সাপোর্ট, Stored Procedures, Full-text Search ইত্যাদি সাপোর্ট করে।</p>

<hr/>

<h3>2. What is the purpose of a database schema in PostgreSQL?</h3>
<p><strong>Schema</strong> হলো ডেটাবেসের ভিতরে একটি লজিকাল কাঠামো যা টেবিল, ভিউ, ফাংশন, ইনডেক্স ইত্যাদি সংগঠিত করতে সাহায্য করে। এটি একই ডেটাবেসে একাধিক ব্যবহারকারী বা অ্যাপ্লিকেশন আলাদা আলাদা কাঠামোতে ডেটা রাখতে পারে, যাতে কনফ্লিক্ট না হয়।</p>

<hr/>

<h3>3. Explain the Primary Key and Foreign Key concepts in PostgreSQL.</h3>

<ul>
  <li><strong>Primary Key:</strong> এটি একটি বা একাধিক কলামের সমন্বয়ে গঠিত যা একটি টেবিলের প্রতিটি রেকর্ডকে ইউনিকভাবে শনাক্ত করে। এটি নাল (NULL) হতে পারে না এবং ডুপ্লিকেট থাকতে পারে না।</li>
  <li><strong>Foreign Key:</strong> এটি অন্য একটি টেবিলের Primary Key এর সাথে সম্পর্কিত হয়। এটি ডেটার integrity বজায় রাখতে সাহায্য করে।</li>
</ul>

<hr/>

<h3>4. What is the difference between the VARCHAR and CHAR data types?</h3>

<table>
  <thead>
    <tr>
      <th>CHAR</th>
      <th>VARCHAR</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ফিক্সড-লেংথ স্টোর করে</td>
      <td>ভ্যারিয়েবল-লেংথ স্টোর করে</td>
    </tr>
    <tr>
      <td>খালি জায়গা দিয়ে পূর্ণ করে</td>
      <td>খালি জায়গা সংরক্ষণ করে না</td>
    </tr>
    <tr>
      <td>কম ফ্লেক্সিবল</td>
      <td>বেশি ফ্লেক্সিবল</td>
    </tr>
  </tbody>
</table>

<hr/>

<h3>5. Explain the purpose of the WHERE clause in a SELECT statement.</h3>
<p><strong>WHERE</strong> clause ব্যবহৃত হয় ডেটাবেস থেকে নির্দিষ্ট শর্ত অনুযায়ী ডেটা ফিল্টার করতে। এটি <code>SELECT</code> statement-এর সাথে ব্যবহার করে নির্দিষ্ট রো খুঁজে বের করা যায়। যেমন:</p>

```sql
SELECT * FROM students WHERE age > 18;