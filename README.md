# WDI-PROJECT-3 - [team:up](http://bytemeteamup.herokuapp.com)

## Local Setup
1. Clone or download the repository and navigate to `WDI_TEAM_PROJECT` in terminal.
2. run `npm i`, `bower i`, `mongod`, `node db/seed.js` and `gulp`.
3. Navigate to [http://localhost:7000](http://localhost:7000/).

## Technologies Used

### Back-end

Node.js, Express.js, gulp.js, MongoDB, Mongoose, JSON web tokens, Bcrypt, ES6.

### Front-end

JavaScript, jQuery, AngularJS, HTML, CSS, SCSS, Materialize, AJAX requests, User Authentication.

## Brief

We were challenged as a group to develop an app with an AngularJS front end, a Node.js / Express.js back end and a MongoDB database.

As an MVP, the app needed to be served by our own Express.js web server, allow user authentication via JSON Web Tokens, Bcrypt and our own Web API linked via Mongoose to a MongoDB database and use at least two models with restful routes from an Express.js API outputting JSON.

## Overview

After considering a few ideas, we decided to build a platform where a lead freelancer would be able to build a team of other freelancers to help them tackle a project which required more time or skills than the lead freelancer could handle alone. 

The lead freelancer would be able to post the job and accept or reject applicants from other freelancers on the platform (of varying skill sets) until the team was fully populated. In this way the lead freelancer could construct their own small agency from project to project and capture all the benefits that come with working in a team a diverse set of skills.

We also decided that the freelancers would be organised into 9 different types (Back-end Developers, Front-end Developers, etc).

## User Journey

**Step One:** The user is greeted by team:up's landing page.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796135/4f63c350-0591-11e7-866f-4932ce463e9b.png">

**Step Two:** The user can filter and search all the projects on the platform to find a project and position to apply for.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796140/4f65c36c-0591-11e7-9339-0709121957dd.png">

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796137/4f640518-0591-11e7-8816-7e5715e66ca7.png">

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796935/6949b172-0595-11e7-872c-c59dc891f98d.png">

**Step Three:** The user can view the profiles of other freelancers currently involved with a project.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796798/bd775732-0594-11e7-8502-c0db436a3aca.png">

**Step Three:** Before the user can apply they must register or login.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23796964/886767c0-0595-11e7-8948-1054deeb56d0.png">

**Step Four:** The user can now apply to a specific project and role.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23797108/21d4e8ce-0596-11e7-976f-df4a3774b596.png">

**Step Five:** The user can also post a new project to the platform, specifying how many of each freelancer type the project requires.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23797156/57c147de-0596-11e7-9a80-7a9787476aef.png">

**Step Six:** The user is then able to accept of reject the applications from other freelancers.

<img width="1269" alt="screen shot 2017-02-06 at 09 58 18" src="https://cloud.githubusercontent.com/assets/20629455/23797183/78bfd32e-0596-11e7-9575-b98379ad507a.png">

## Favourite parts

### Dynamic application buttons

Once the user presses apply on a listed vacancy the button is disabled and it's inner text is changed from "Apply" to "Applied".

This was achieved by using AngularJS's $event object and although the logic is relatively simple I feel the end result adds a good level of polish to our app.

### Team creation form

The user is able to select the required roles for their new project.  Once a role is selected a new box appears with the roles title and a tag showing the sum for that type of role already assigned to the project.

This was achieved with AngularJS's two-way data binding. The project object (which is later saved to the database) is being directly interacted with by the user, once a role is selected the view automatically updates to the change in the data / model.

Again, although relatively simple logic I feel enjoyed the added level of polish it added to our app.

## Challenges

The biggest challenge for our team was how to handle applications. This included how to store and display vacancies, filed positions, active applications and rejected applications. In hindsight we should have used more than two models (Freelancer and Project) however we managed to overcome this challenge with some creative Mongoose models and use of AngularJS's two-way data binding.

## Wins

Producing a polished app dispite this being our first team project, our first AngularJS app and our first Materialize App.

## Known issues to be addressed
1. Login is currently buggy.
2. Sometime our views do not correctly display the correct text given the data they are representing. For example if there are currently no vacancies on a project then "no vacancies" should be displayed.
3. Our model titles are being used as display information. This leads to camel case text being displayed instead of properly formatted words (e.g. UIDeveloper vs UI Developer").

## Features which could be added

1. A way for the freelancers to contact each other on our platform.
2. Email notifications of application updates (acceptation or rejection).
