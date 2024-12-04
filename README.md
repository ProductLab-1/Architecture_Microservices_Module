## Architecture and Microservices Module
 Welcome to the Architecture and Microservices Module of ProductLab. We're going to build on your knowledge of databases and APIs to move onto more complex topics. This module will walk you through concepts you should consider when making architecture decisions such as how to right size a service, when to use event driven architecture, the benefits of containers and whether to use cloud, edge or on-prem computing. You'll also learn skills like building sequence diagrams and containerizing applications. Finally, at the end of this module there will be a number of hands on projects to choose from. Some projects will reinforce topics from this module. Other projects will give you the opportunity to expand on projects you started in the API module. This is really where the opportunities in ProductLab expand, because at the end of this module you'll be dangerous enough to develop basic web-applications and knowledgeable enough to comfortably explain how complex applications function! 

 ## Housekeeping
 Please watch this repo by selecting the "watch" button, which is directly above the bright green "Code" button. This will help us keep track of participation.

 To keep a central record of your accomplishments you will need to create a repository called 'Architecture_Microservices_yourname' and then upload each project to the repository. This will allow your instructors to easily review your work! Your final project will also link to this repo to demonstrate your Data skillset. 

 This repo will serve as both your solution files as well as the rubric for how you should name and structure your files. 

 ## Assignments: Academic 
 Before working on the hands on material please review the following: 

1. [An intro to microservices](https://www.linkedin.com/pulse/demystifying-apis-product-managers-erin-howell/)

2. [The twelve-factor app](https://12factor.net/) 
    * This will run you through methodology used to build SaaS architecture. It will provide a strong foundation for the rest of the module, but there will be terminology / concepts you may not be familiar with. Google is your friend. For example: they'll take about "daemons." Don't breeze over it, look it up! 

3. [Domain Driven Design](https://www.youtube.com/watch?v=4rhzdZIDX_k)
    * There is an argument that Domain Driven Design is at its root all about making it easier for Developers and Business to coordinate. Thats part of the job description of a PM, so definitely pay attention. 

4. [Event Driven Architecture](https://solace.com/what-is-event-driven-architecture/)
    * Have you used Apply Pay or Google Pay recently? Then you've benefitted from EDA. In fact almost any project you work on will likely have an event driven aspect to it.
    * If you're still struggling with the concept after reading the above, check out [this youtube video](https://www.youtube.com/watch?v=ogoztX51-Xg)

5. Next read this brief article on [different types of computing](https://www.simplilearn.com/edge-computing-vs-cloud-computing-article), you've likely heard all these terms before. But it is good to be familiar with the details

6. An important aspect of development are containers and virtual machines. Its important to understand these topics well. First review [this high level comparison of containers vs virtual machines](https://learn.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm)
    * [Next review this article](https://www.backblaze.com/blog/vm-vs-containers/). EY security may ask if you're sure if you want to continue, if so hit continue, its fine its just a blog post. 

6. Now we know enough to start considering the problem of [right sizing services](https://thenewstack.io/the-right-sizing-problem-in-cloud-computing-and-how-to-solve-it/), which as a PM is a skill you can leverage to directly reduce your client's overhead
    * Watch [this youtube video](https://www.youtube.com/watch?v=k1AZeAsTna0) to get an idea of the real-world implications of right sizing and how you might implement it 

7. [A deeper dive into Architecture styles](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/)
    * Read the first page. If you're interested you can go through the deep dive pages if you would like (Big compute through Web-queue-work) but it is not required.

8. Ok, we're almost done with the academic material, but pay attention to this next one. It'll be in the homework! Watch [this tutorial on sequence diagrams](https://www.youtube.com/watch?v=zid-MVo7M-E)
    * Don't use lucidchart, the application in the tutorial, we would recomend using Mural. 

9. Finally, lets dive back into containers. Watch [this video](https://www.youtube.com/watch?v=simtBse5s9k) which gives a detailed view without becoming too technical


## Assignments: Hands On
Enough reading! Time to make some stuff! 
1. Create a new repository in your Github called "Architecture_Microservices_yourname"
    * This is where you will store your work for the module. 
    * Make sure the repo is "public"
        * go to settings, scroll down to the "Danger Zone" section and change the repo to public

2. Create a sequence diagram of a process within your favorite (or least favorite) mobile app
    * A real-world sequence diagram would likely include technical details such as API references. For this assignment don't worry about it and keep it high level. It also doesn't need to be 100% right, instead leverage what you've learned so far in ProductLab to take a best guess of how the backend of your chosen process would work! 
        * Example: a sequence diagram of selecting a ticket and then checking out on Ticketmaster 
        * Example: a sequence diagram of opening up a friends instagram profile, opening a picture and then liking it
    * also remember to think through the impact of your process beyond the user
        * for example in the instagram example, there would also be a notification sent to the friend 

3. Lets dive into Docker, in this project we'll follow along with the ['getting started' tutorial](https://www.docker.com/101-tutorial/)
    * Follow the instructions for the Docker Desktop option
    * open your terminal and navigate to your Architecture_Microservices_Module repo
    * run the command `docker run -dp 80:80 docker/getting-started`
    * open your [local host](http://localhost)
        * remember, even though this page is open on your browser and looks like a normal website. It is not on the internet, your browser is pulling a file from your local computer and running it. This is an important distinction to understand. 
    * read through the "getting started" page, then navigate to the "our application" page (hint: check the right side of the page for the directory)
    * **Remember** if you edit something in VScode, save it before running it or it won't work 
    * "our application" page
        * after you unzip the file, move the 'app' file to your Architecture_Microservices_Module repo
        * make sure you are running the docker terminal commands in the 'app' directory
        * **IMPORTANT** in your `Dockerfile` update the first line to read `FROM node:lts`
            * if you don't do this you will get an error where your YARN package does not run 
        * after you run the `docker build -t getting-started .` it will take a while to finish in your terminal, just be patient
    * continue through each page until you finish the tutorial
    * Send a ping of your Docker repo to the group so others can try running it on their local machines! 

## Challenges

3. Fullstack Applications: These will be tough and don't need to be finished this week, but they will look great in your final portfolio! We encourage you to at least get started if you want and see how far you can get this week
    * If you worked on the Strapi project in the last module this will be a logical extension of that work. Follow along with [this tutorial to build a fully functional full stack website!](https://strapi.io/blog/nextjs-react-hooks-strapi-food-app-1)
    * If you want a little more of a challenge try out the [graphQL Library project](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Tutorial_local_library_website#in_this_module)

4. [Using a different language to build a microservices application](https://spring.io/guides/gs/spring-boot/)
    * This project is not in practice overly difficult. However, it will require you to use Java, a new langauge, and will also require you to navigate downloading new dependencies and troubleshooting a variety of issues.
    * This is completely optional

## Assignment Format 
At the end of the week we expect your Github repo to have the following files: 

1. A screenshot of your sequence diagram
2. the entire file structure of your docker project
3. a screenshot of your docker desktop running your docker containers 

In addition, ping your Docker repo in the [Teams Channel](https://teams.microsoft.com/l/channel/19%3aD9im-uR3ngSILSIGGMgORJVeWvwsI6KPz0SeYu-h5m81%40thread.tacv2/General?groupId=144988bd-3c1d-41e0-a2db-d300554d9f1c&tenantId=5b973f99-77df-4beb-b27d-aa0c70b8482c)

## Troubleshooting

If you have any trouble navigating the GitHub repo or working on the exercises, please don't hesitate to ask for help. The Admin Team and your Instructors are always happy to help.
