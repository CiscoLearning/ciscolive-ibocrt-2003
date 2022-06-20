# IBOCRT-2003

* Can I use any tool or any language?

We initially thought to do this.  We could offer a numb er of languages/frameworks, and then the candidate would choose what they want to use, create a wrapper of a known name, and we'd run the code and measure the output.  In practice, though, this is very hard to do.  It's not really hard on us per se (though there are challenges in grading such things), but try this as an exercise:

> Open up a text editor of your choice.  Write an app that gathers the output of `show ip route` on a variable number of devices and commits those to a git repository.  You have 15 minutes to do this, and you cannot use Google or Stackoverflow.  You can, however, use direct documentation for your language and libraries of choice, as well as all of Cisco.com and DevNet.

Were you able to do it?  Maybe you were in your own chair in your own workspace.  But would you have been able to do it with the added pressure of the CCIE lab testing room?

We ultimately thought the general answer would be, "this is too hard."  We opted to provide starter code for tasks and have the candidate complete/fix/optimize that code.  While this made things more doable in the alotted time, it limited our choices of libraries and frameworks.  We landed on Python with a number of accompanying libraries that are fairly popular in the wild.  We stipulate reading other's code and being able to extend it is very much expert-level.  Add on top of that the context switches between tasks, and we feel our exam is both challenging and defensible.

* Are there interdepencies?

Questions are generally independent.  Some design questions may build on each other in the same overall question frame, though.  Design questions may also share resources.  So if you misread an email or chat communication it can result in bad design choices on multiple questions.

* What tips can you give to help us with the exam?

    * Practice on the CWS and work to the blueprint in depth (meaning all of the sub-options)
    * Practice and quize others
    * Learn to read the documentation for each of the items in the software list.  Know their format and layout.
    * Taking more than five minutes to read questions will hurt your overall chances to get through the exam
    * Take time to read through the whole DTDM (five hour) part before you start to understand all of the high-level concepts being asked

* Constraints

Many questions, especially in design, come with constraints.  This may mean your presented with a set of potentially correct answers and based on the resources, you have to determine the best design.  Pay _very_ close attention to constraints and check them off as you implement your solution or arrive at your conclusion.

* How to write good bad answers

As said above, in an expert-level exam, multiple choice, drag and drop, and matrix questions generally have multiple right answers.  As an example, here is a multiple choice answer you might get on a non-expert-level exam:

Which HTTP verb is used by REST APIs to create a resource?

A. POST
B. GET
C. PATCH
D. PUT

There is one right answer (A).  Now take an example expert-level design question:

Which method will improve use experience?

A. Deploy app in geographically disperse data centers to reduce latency
B. Add more instances of the backend process to service more simultaneous requests
C. Introduce a load balancer for the app frontend
D. Use async API operations between the frontend and backend

All the answers are plausible.  You won't know from the answers themselves which is right or which is wrong.  This is where those constraints come in and why question (or item) writing is considered an art.

* How long-lived is the blueprint?

We will provide a six month warning before any blueprint changes are made.  In general, small changes happen at least once per year.

* Ansible

Ansible played a huge part in the build of this exam.  We use over 6000 plays each time we spin up a pod.  Exam grading is also driven by Ansible.

* Collab with other tracks

Some of what we did for DevNet Expert has been used in the Data Center track already (thanks to Ramses being involved in both).  We also learned a number of lessons from this build that we will take back to the exam team.

* Grading
    * **Code Hygiene**
In general, the format of the code is not considered when grading.  We try and look at the product of the code rather than the code itself.  However, if the question specifically calls out elements of code style or a specific approach, that _will_ be graded.

    * **Differing input**
Keep in mind that when we grade, we often switch the input from what is given to the candidate while taking the exam.  This ensures the code does what is expected and doesn't just hardcode assumptions based on the question input.  Focus on the question tasks and the constraints to know you did everything correctly.
    

