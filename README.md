# LIA-Questions

### Questions

<p><strong> 1. Explain what is Long polling.<strong></p>
<p>Long Polling is a technique that simulates a server outage to keep an HTTP connection open. This technique was created from the need for real-time communication with a web server.</p>

<ul>
  <li> a) Provide a example implementation of long polling</li>
  <p> Imagine a page that sends an AJAX request every 5 seconds to a specific endpoint in order to find out if there have been changes in notifications, for example. This does not become a problem with few users simultaneously connected. But let's say the application grows from 10 users to 100 concurrently connected users.

Let's think bigger. Imagine 1000 connected users. In 5 seconds, 1000 requests will be sent to the same endpoint. After another 5 seconds, another 1000 and so on. Depending on the architecture of the application, this starts to overload the server. Specifically that endpoint. The solution here would be long polling. When a client makes a request, the server simulates a data unavailability and makes the HTTP request unresponsive while there are no changes in the application data model.

Does this solve the problem? Yes and no. Yes, because it is not necessary to keep sending requests from time to time to check these changes. No, because that caused another performance issue. HTTP requests were not specified for this. Extending an HTTP request may "seem" to solve the problem of the number of requests sent to the same endpoint, but in fact it also consumes a lot of resources precisely because it is being used inappropriately.</p>
  <li> b) What other alternatives are available instead of long polling explain at least one if any.</li>
  <p>WebSocket. WebSocket is the name given to the technology that allows establishing a bidirectional connection between a client and a server. By bidirectional, it can be said that both sides send messages simultaneously, through full-duplex channels, without worrying about ports shared by HTTP requests or proxy/firewall.
The famous inflexible relationship between request and response is over. With an active websocket connection, the client can send messages to the server via a single TCP socket.</p>
  <li> c) Provide positive and negative impact of using long polling.</li>
  <p>Positive: Long Polling it always keeps an open connection with a long timeout (55 seconds), as soon as a new message arrives, is sent or the request times out, it opens another request with the same characteristics.
  <p>Negative: Requires user interaction or periodic polling to load new data from the server.</p>
  </p>
</ul>
<br>
<p> 2.Explain the difference between cookies and local storage.</p>
Cookie information is stored in the browser and in the origin server of the service referred to it. Local Storage and Session Storage use only the browser as the data storage location.
<p>3. How many HTTP Methods are there? Explain each of them.</p>
<p>GET: Request a representation of the specified resource (The same resource can have several representations, for example services that return XML and JSON).</p>
<p>HEAD: Returns the headers of a response (without the body containing the resource)</p>
<p>POST: Sends an entity and requests that the server accept it as a subordinate of the resource identified by the URI.</p>
<p>PUT: Request that an entity be stored under the given URI. If the URI refers to a resource that already exists, it is modified; if the URI does not point to an existing resource, then the server can create the resource with that URI.</p>
<p>DELETE: Deletes the specified resource.</p>
<p>TRACE: Echoes back the received request so the client can see if there have been changes and additions made by intermediary servers.</p>
<p>OPTIONS: Returns the HTTP methods the server supports for the specified URL.</p>
<p>CONNECT: Converts the connection request to a transparent TCP/IP tunnel, usually to facilitate SSL encrypted communication (HTTPS) through an unencrypted HTTP proxy.</p>
<p>PATCH: Used to apply partial modifications to a resource.</p>
<br>
<p> 4. Explain the difference between an object and an array.</p>
Array is used to store multiple values in a single variable, "very good when you have large batches of data to be stored and analyzed etc.. and object is used to store only the values that contain within the used contain, also used for few values to be stored.</p>

<p>5. What is reactjs? </p>
It is a library used with the JavaScript programming language in front-end development.

<ul>
  <li>What is react hooks used for?</li>
  React Hooks are simple JavaScript functions that we can use to isolate the reusable part of a functional component, instead of using classes.
  <li>Name 3 rules of hooks and why they exists.</li>
    <ul>
       <li>We shouldn't declare hooks, be it for state management, lifecycle, etc., inside repeating loops or conditional structures.</li> 
       <li> When invoking a function, we shouldn't do it according to regular JavaScript. We must create custom hooks or components using already created functions.</li>
       <li> A good practice for creating hooks is to always start with the prefix use before the name of the function (it is from this prefix that hooks such as useEffect, useCallback, etc. arose). From there you can use it to call other hooks.</li>
    </ul>
  <li>What is jsx?</li> JSX is a syntax extension for JavaScript. JSX allows React to show more useful error and warning messages, for example when using files with the .js extension in VS Code you don't have an autocomplete option. Now, when using files with a .jsx extension, VS Code already shows suggestions for completing HTML tags, for example.
  <li>What are environment variables and how do you use them in react?</li>
  They are variables that can store information that cannot be leaked to the outside world, for example, keys and passwords of APIs or database, as well as more specific configurations of them as well.
  <li>What are props?</li>
 Props, which is short for properties, or properties, are pieces of information that can be passed to a component. It can be a string, a number, even a function. This value can then be used by the receiving component.
 <li>How do you update state in react?</li>
 <li>Can you return multiple element from a component?</li>
 <li>Describe Component Driven Development and how it applies in react</li>
 <li>provide an example implementation of the following components</li>
  i.
</ul> 
<p> 6. Complete the following challenges </p>
<p>a. </p>
<p>b. </p>
<p>c. </p>

<p>7. What is typescript?</p>
TypeScript is a superset of JavaScript, that is, a set of tools and more efficient ways to write JavaScript code, adding features that are not natively present in the language.
<ul>
  <li>What are the benefit of typescript?</li>
  Typescript adds new functionality to JavaScript. JS, for example, does not allow you to create classes or work with modules, as its typing is dynamic, which can cause many errors. And these errors are not pointed out at the time of implementation.
  <li>Provide positive and negative of typescript</li>
  Negative: The creators of TypeScript designed the language and its tools to avoid some potential problems, but still, it's not pure JavaScript.
  Positive: Typescript enhances the characteristics of JS. Because it has static typing, developing in TS ends up being safer, because while the application is being implemented, errors are identified, differently from what happens with JS.
  <li>Provide a code snippet in both javascript and typescript</li>
  JS: const product = {
  id:  1,
  name:  "glas",
};
  TypeScript -> interface Product {
  id: number;
  name: string;  
}
</ul>

<p>What is a user Story?</p>
User Stories are written specifications of how a person would use a product's functionality.

