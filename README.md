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

## A2

There could be many aspects of a quality software from technical and non-technical perspectives however from end user's perspective following qualities would be at top of the list.

- User Experience

    The term "User experience (UX)" is used to define user's experience while using the software. For example how well organized the UI is, how well the the navigation is structured or even how quick the percieved speed of the application is. It collectively defines how good the user's experience is compared to using other similar applications.

    Generally user-friendly softwares that are easy to use provides better user experience which helps in achieving higher adaption of the application, increased productivity for users of the application, and better results for the business of the organization. 

- Reliability

    Any software application is prone to failures which might be due to varied number of reasons. Reliability of application is defined as the number and amount significant failures the user experiences while using the application. The less the number and criticality of the failure the more reliable the application.

    Reliability of the application plays most important part if the application is being used for implementing realtime or business critical processes. For example a Banking Transaction software.

- Secure

    In connected world of today application security is becoming much more critical as more and more computers are interconnected through internet. It is important that the software application handles the user's credentials and data securely to make sure that the data handled by the application can be used only by its intended users and the users who should have access to the information are not deined the access by the application.

    In current competitive world information security plays a big part in success of the entities using the software application.

- Portable

    Portability of application from end user perspective is the different kind of environments the applicatio can run correctly. The environment can be varied number operating systems supported by the application or different kind of browsers in which the application can be run even the different kind of devices on which the application can run.

    Portablity gives users flexibility to use the application in different situations for example on desktop while working in office or home, along with at least limited critical functionality on mobile device while on the move.

    Portablity gives agility to the software when better and/or new hardware devices are created.

- Efficient

    The software applications must be efficient enough to be able to make optimum use of available resources to provide better user experience without interfering with functionality of other applications running in the same environment.

    Efficiency results improving end user productivity as well as cost reduction.
- Flexible

    Flexibility is the measure of how easily changes can be introduced in the application to respond to changes of needs of the users. Flexible applications not only helps in reducing overall cost of the software development but also it helps in providing consistent user experience since the users can still use other features of the application in the same as they have always used.

**References**
1. https://www.softwaresuggest.com/blog/five-characteristics-make-excellent-software/
2. https://courses.cs.vt.edu/csonline/SE/Lessons/Qualities/index.html
3. http://www.idc-online.com/technical_references/pdfs/data_communications/Characteristics_of_good_software.pdf
4. https://uxplanet.org/how-user-experience-shapes-custom-software-development-78490943b0fc
5. https://www.quora.com/What-are-some-characteristics-of-good-software



# Q3	
Outline a standard high level structure for a MERN stack application and explain the components

# Q4	

A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

## A4
For any project there are a diverse range of skills required. Similarly, in case of web application development different kind of technical and non-technical skills are essential to successfully sail through the conception to production deployment phase. 

Following is a list of essential skills that are required to implement a website for a small business.

1. Requirement Analysis

    Most of the project whether big or small starts with Requirements Analysis in some form to understand what is required to be built.

    Having the skills to analyse the requirements helps to figure out
    - What are the requirements and the major usecases?
    - How the new application will help the customer to solve a problem?
    - Set the boundries terms what needs to be delivered?

2. Project Management and Planning

    Management and Planning are essential for any kind of project to make sure the project is delivered within optimal time frame and the issues are addressed timely.
    Project management is required to make sure the resources are utilized optimally, the team sticks to the defined timelines, all the goals of the project are achieved.
    It is one of major skill that helps to make sure the project is completed successfully. Project management skills requires knowledge of at least one of the project management framework such as Agile Project Management.

3. UI Design and Wireframing

    UI Design involves the process of creating intituitive and easy to follow user interfaces. UI designers uses wireframing to sketch and communicate various visual components that might be availalbe to the user to interact with the software application. It helps in communicating and deciding flow of the interaction and what componentes will be present on actual user interface when its ready. For customers it also helps in figuring out if the application can provide all the desired functionality without building the entire application.

4. Programming

    Programming skills are the collective technical skills required to implement UI design, Business Logic, persistence of data in a storage medium, deployment etc...
    It involves knowledge of frontend technologies, programming languages, database management applications, server deployment and many other relevant technologies that is required to design and implement software applications.
    
5. Testing

    Testing is process of verifying if the web application works correctly for all the use cases that are defined during the requirement gathering. Investigative testing skills important to deliver a good quality website and to make sure that all the required standards of performance are maintained. 

**References**
1. https://onextrapixel.com/12-skills-you-need-to-develop-a-website/
2. https://en.wikipedia.org/wiki/Requirements_analysis
3. https://www.wrike.com/project-management-guide/faq/what-are-project-management-skills/
4. https://balsamiq.com/learn/courses/intro-to-ui-design/what-is-ui-design/
5. https://www.guru99.com/web-application-testing.html

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