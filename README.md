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

# Q4	

A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

## A4
For any project there are a diverse range of skills required. Similarly, in case of web application development different kind of technical and non-technical skills are required to successfully sail through the conception to production deployment phase. 

Following is a list of essential skills that are required to implement a website for a small business.

1. Requirement Analysis
2. Project Management and Planning
3. Wireframing
4. Frontend Design
5. Database Design
6. Backend Design
7. SEO
8. Testing
9. Deployment

**References**
1. https://onextrapixel.com/12-skills-you-need-to-develop-a-website/

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