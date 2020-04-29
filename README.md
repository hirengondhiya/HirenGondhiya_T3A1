# Q1	

Provide an overview and description of a standard source control process for a large project.

## A1

For any software development project the source code is one of the most important asset that entire project team nurture over time. As the code base grows it becomes very critical to track what changes were made for which functionality and how new changes will affect current codebase. In a large project where a number of developers are working on a single codebase it also gets challanging and critical to track single source of working and tested codebase. 

To manage all of the above challanges a souce control or version control mechanism is required that can make sure the code integrity is maintained all the time. The software application that aids in effective source control mechanism is called **Source Code Management (SCM) Application**.

There two main approaches for source control **Centralized** and **Distributed**. As the name suggests in the Centralized approach there is only one working copy of the source code and the version control is performed on that copy, whenever changes are required to be made on files, developers need to aquire exclusive rights to update the code in a file by checking out and then commit the changes using check-in. However this approach leads to inefficiencies and many other issues, since only one developer can make changes to a file at a time.

In a Distributed source control system such as Git developers aquire copy of the codebase (source of truth) locally and then make and commit changes to the local copy. When the developer is satisfied with the newly created or updated functionality the changes are synced back to the main shared codebase (new source of truth).

Following text describes above process in more detail,

1. Branching
Whenever a new feature is to be developed or an enhancement has to be done the developer starts with creating a new branch from the remote master branch of the respository.
2. Commit
All the changes related to the feature are commited to the new branch locally and each working day at least one push is performed on remote copy of the feature branch.
3. Merge
When the functionality is ready the developer pulls the changes from remote master branch to local master branch and then merges the changes to the feature branch. This makes sure that all the changes made to the repository after developer first aquired local copy of the repostory are accomodated in the local working copy of the code.
4. PR
After making sure everything is working on the new feature branch and the code from master branch is merged correctly the developer opens a Pull Request (PR) to add the new functionality to the master branch.
Once the PR is approved the code from feature branch is copied to the master branch with all the commits from the feature branch.

**References**
1. https://www.atlassian.com/git/tutorials/what-is-version-control
2. https://confluence.atlassian.com/get-started-with-bitbucket/types-of-version-control-856845192.html
3. https://www.perforce.com/blog/vcs/what-source-control
4. https://lonewolfonline.net/source-control/

# Q2	
What are the most important aspects of quality software?
# Q3	

Outline a standard high level structure for a MERN stack application and explain the components

## A3

In context of software applications the term stack describes the technologies that are used to build the application functionality. For example **LAMP** stack which refers group of technologies Linux, Apache, MySQL and PHP that can be used to build web applications.

In past few years JavaScript has matured to the level that it can not only be used to develop frontend but backend as well, collectively called fullstack applications. However the web applications built using javascript still needs to use a group of technologies that perform distinct functions. MERN stack is one of such javascript based technology stack which can be used for building fullstack web applications.

The acryonym MERN refers to four components that could be used to build fullstack web applications.

Following modified version of the original diagram from the blog ["The Modern Application Stack - Part 1: Introducing The MEAN Stack"](https://www.mongodb.com/blog/post/the-modern-application-stack-part-1-introducing-the-mean-stack) illustrates the location of each component in a fullstack app.

![Mern Stack Components](./docs/images/mern-components.svg)

1. **MongoDB**

    One of the first component of the MERN stack in the acrynym is the MongoDB. As the name suggests it is a database management system. Though MongoDB not built using JavaScript but its query language and the form of datastorage is JavaScript based.

    MongoDB is a no-sql database which means its not a relational database and hence it does not store the data in form of tables of rows and columns. Instead the data is stored as a document that is nothing but a BSON object. BSON objects are similar to JSON objects of javascript but the distinction is that they are Binary objects unlike JSON. 

    The data from MongoDB can be queried using JavaScript, that is interpreted by MongoDB using Shell using JavaScript Run time and then the data is returned as a JSON object which eliminates the need to peform translate the data into object at web application level.

4. **Node.js**

    Node.js is server side JavaScript runtime which uses Google Chrome's V8 engine to parse and execute the javascript code at server side. It also bundles modules to interact with server resources such as file system, networks etc...

    Until advent of Node.js JavaScript code could only be executed by the Browser at the frontend of the application by refering the javascript code in the HTML. However with Node.js the JavaScript can not only be used for frontend but also for backend of the application. Due to efficiency of the Google's V8 engine the JavaScript code executes much faster using Node.js compared to other traditional server side languages. It is also more easier for application developers to master one language and deliver fullstack functionality.

    Node.js functionality can be extended by building custom modules, that is one of the most popular feature of Node.js besides other popular features.

2. **Express**

    Express is Node.js webserver framework module that enables Node.js to respond to http requests. It can be used to serve HTML documents, rest apis, as well as other types of media using http protocol. Like any webserver it handles routing, request url, header & body parsing and it can also be used to send http responses, set response codes & cookies, custom headers etc... 
    
    Express can also be extended using Node.js modules called middleware. Middleware can be used to perform many of the common tasks performed by web servers such as request body parsing, logging, authentication etc...

    With combination of Node.js, Express and MongoDB one can easily create apis that can respond to request to retrieve and manipulate data in MongoDB over http that is commonly known as backend of the application.

3. **React**

    React is a javascript library maintained by Facebook which can be used to create **Single Page Applications (SPAs)**. One of the notorious characteristics of a SPA is that the page transitions are performed asynchronously without reloading of the entire page. This helps in building applications with superior user experience as the page transitions are faster compared to the web applications that user server side rendering. React uses concept of Virtual DOM which is React equivalent of DOM of an HTML page. React uses optimized alogrithms to update UI aka HTML DOM using Virtual DOM. 
    
    The developers create frontend of the application using React library which contains logic to render the initial UI for application, logic to fetch data from backend based on user interaction with application, and the logic to update UI using the data returned by the api.
    


**References**
1. https://www.apress.com/gp/blog/all-blog-posts/why-mern/12056000
2. https://www.geeksforgeeks.org/mern-stack/
3. https://medium.com/nybles/switching-to-the-modern-day-mern-stack-574bb478fc64
4. https://www.iamtimsmith.com/blog/what-is-the-mern-stack-and-how-does-it-work/
5. https://www.mongodb.com/blog/post/the-modern-application-stack-part-1-introducing-the-mean-stack

# Q4	
A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
# Q5	
With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges
# Q6	
With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature
# Q7	
Explain control flow, using an example from the JavaScript programming language
# Q8	
Explain type coercion, using examples from the JavaScript programming language
# Q9	
Explain data types, using examples from the JavaScript programming language
# Q10	
Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language
# Q11	
Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language
# Q12	
Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language
# Q13	
For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes 

**Q13 Code Snippet**
```
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]
    
  mycar = new Model(make, model);
  console.log(mycar.show())
}
```