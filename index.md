# ETS

(still pending group & project name)

## About ETS

ETS gives ease of access for ETS employees to review and create projects reports sent in by the state's Independent Verification and Validation (IV&V) vendors by standardizing the information sent in by each vendor.

You can read more in the HACC proposal listed [here](https://hacc.hawaii.gov/wp-content/uploads/2025/10/Challenge-Use-Case-2025-ETS-Project-Review-Web-Application.pdf).

## Deployment

Our app's live demo is currently deployed [here](https://pseudo-hacc-ets.vercel.app/), and is hosted by Vercel.

## Maintainers
* [Kyler Ching](https://github.com/kylersm)
* [Courtney Hisamoto](https://github.com/CourtneyHisa)
* [Zhanpeng Lin](https://github.com/zhanpenglin9)
* [Shuto Nishida](https://github.com/shuton-gif)

[*bound by agreement contract*](https://docs.google.com/document/d/1umOiaQro4WNHh2q9xjLKDcvKRWewYVYl2126YHVgowA)

## Tools

Our solution is based upon the [nextjs-application-template](https://github.com/ics-software-engineering/nextjs-application-template). For our stack, we are using:
* NextJS as our React framework
* Typescript for our backend and frontend
* React-Bootstrap for styling
* Prisma for ORM
* ESLint and Prettier for internal readability

## Tracking Our Progress

Our project management is [issue driven](https://courses.ics.hawaii.edu/ics314f25/morea/project-management/reading-guidelines-idpm.html). You can see our issues (tasks) associated with each milestone here:

* [Milestone 1](https://github.com/orgs/oh-yeah-ics-314-final-project-7-lets-go/projects/1): November 5th – November 19th
* [Milestone 2](https://github.com/orgs/oh-yeah-ics-314-final-project-7-lets-go/projects/2): November 19th – December 1st
* [Milestone 3](https://github.com/orgs/oh-yeah-ics-314-final-project-7-lets-go/projects/3): *Planned, for December 1st – December 10th*

## User Guide

This section aims to guide the user through how to use our website. Account creation is accessible to ETS employees only.

### Public View
This view is for the general public to see. They will be able to view:
* Search through existing reports and projects 
* A list of every project submitted by the vendors. These projects will include issues, progress, budgets, and an overall timeline of the project.
* Users can also log in, given that they are just a vendor or employee that's logged out. Otherwise, users cannot create their own account.

<img src="mockup_images/homepage.png">
<img src="mockup_images/dashboard.png">

### Vendor View
This view is for the IV&V vendors. They can also see items listed under [public view](#public-view). They will be able to:
* Create and edit projects
* Append, edit, or delete issues and timeline events to existing projects
* Receive feedback from ETS employees

<img src="mockup_images/submit_report.png">
<img src="mockup_images/reports.png">
<img src="mockup_images/report.png">
<img src="mockup_images/comment.png">
<img src="mockup_images/event.png">
<img src="mockup_images/issue.png">
<img src="mockup_images/change_password.png">


### ETS Employee View
This view is for the ETS employees. They can also see items listed under [public view](#public-view). They will be able to:
* View submissions of new projects and issues from vendors
* Approve/reject existing projects
* Create and manage ETS or vendor accounts
* Provide feedback to vendors on issues and projects

<img src="mockup_images/users.png">

## Developer Guide

If you are interested in contributing to ETS, or running the website locally, follow the next sections.

### Installation

Make sure that you have [Node.js](https://nodejs.org/en) and [PostgreSQL](https://www.postgresql.org/) installed before continuing.

Now, fetch the source code from our [repository](https://github.com/oh-yeah-ics-314-final-project-7-lets-go/ets). Change your working directory to the folder containing the project and run the following command:
```
$ npm install
```

Make a copy of the `sample.env` file and adjust the `DATABASE_URL` key to point to a (presumably local) PostgreSQL database server. If you are not sure how to setup a PostgreSQL database, read [chapter 1](https://www.postgresql.org/docs/current/tutorial-start.html) of the documentation.

Now, you can run the project with
```
$ npm run dev
```

The website will be accessible at http://localhost:3000, NextJS will also show where the website is being hosted in the console window.
