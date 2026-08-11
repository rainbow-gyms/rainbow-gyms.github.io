[![Rainbow Gyms CI](https://github.com/rainbow-gyms/rainbow-gyms-nextjs/actions/workflows/ci.yml/badge.svg)](https://github.com/rainbow-gyms/rainbow-gyms-nextjs/actions/workflows/ci.yml)

## Table of Contents

* [Overview](#overview)
* [Team](#team)
* [Team Contract](#team-contract)
* [Github Organization and Repositories](#github-organization-and-repositories)
* [Rainbow Use Cases](#rainbow-use-cases)
* [User Guide](#user-guide)
* [Developer Guide](#developer-guide)
* [Deployment](#deployment)
* [Milestones](#milestones)
   * [Milestone 1](#milestone-1)
   * [Milestone 2](#milestone-2)
   * [Milestone 3](#milestone-3)

## Overview

Rainbow Gyms is a gym session scheduling application designed to help University of Hawaiʻi students balance fitness goals with their academic responsibilities. The app allows students to find workout partners, create gym sessions, and build a supportive fitness community within the campus environment.

## Team Contract

Our team contract can be found [here](https://docs.google.com/document/d/1algRmpXW86wuj2J9FpdIfrhPnD4kGLlib5fFAoGzR6E/edit?usp=sharing).

## Team

Rainbow Gyms is designed, implemented, and maintained by [Joshua Abrogena](https://jabrogena5100.github.io/), [Joshua Koerte](https://jkoerte.github.io/), and [Tayten Yau](https://tayten0.github.io/).

## GitHub Organization and Repositories

* [Rainbow Gyms organization](https://github.com/rainbow-gyms)
* [Next.js application repository](https://github.com/rainbow-gyms/rainbow-gyms-nextjs)
* [Project home repository](https://github.com/rainbow-gyms/rainbow-gyms.github.io)

## Rainbow Use Cases

* Students can browse and filter available gym sessions by day, time, and availability.
* Students can view gym session details including the creator's profile picture, session time, location, fitness level, and number of available spots.
* Students can create gym sessions through a calendar-based scheduling system for other students to join.
* Students can join or leave gym sessions based on their availability and fitness goals.
* Students can view user profiles containing information such as profile picture, fitness level, session history, and progression level.
* The app includes a leveling system where users gain points from creating and joining gym sessions, unlocking profile improvements and future features.
* Users can manage their account through sign-up, log-in, profile settings, and logout functionality.
* Administrators may manage users, sessions, and reported content to maintain a safe and welcoming campus fitness community.

## User Guide

When a user first visits Rainbow Gyms, they'll be greeted by our landing page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/LandingPage.png">  
  
This page gives a brief overview of our website's goals, purpose, and features.  

If a user is new and doesn't have an account, they can create one via our sign-up page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Sign-Up-m3.png">  
  
Alternatively, if they already have an account, they can use the sign-in page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Sign-In.png">  

Once a user creates a new account, they'll be greeted by our profile creation page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Setup-Profile-m3.png">  
  
On this page, users can enter their account name, major, select their year and experience level, provide a short bio about themself, and link an image to use as their profile icon.  

After entering the required details and completing their profile, users will be greeted by our directory page.  
<img width="576px" class="rounded float-start pe-4" src="/images/Browse-m3.png">  
  
Users will be able to browse through all of the open and available workout sessions and filter them by workout type, experience level, location, and/or date. This page also serves as the landing page if you're logged in to an account.  

If a user wants to see more details for any given workout sessions, they can click a session card's "More Info" button, which will redirect them to the session's profile page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Session-Profile-m3.png">  
  
The session profile page displays the session's name, location, date and time, as well as the session type, the host's experience level, it's capacity and capacity status, and the current participants who have signed up. They can also join by clicking the "Join" button, or return to the directory by clicking the "Back to Browse" button.  

If instead a user wants to create their own workout session rather than join one, they can click on "Create" in their navbar. This will redirect them to the "Create a Session" page.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Create-Session-m3.png">  

A user can view all of the sessions they created by clicking on "My Sessions" in their navbar.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/My-Sessions-m3.png">  

If a user would like to browse through workout sessions using a calendar view, they can do so by clicking on "Calendar" in their navbar.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Calendar-m3.png">  
  
They can see which days have workout sessions scheduled, easily determine which sessions are full, and just like the directory page, there are filters users can apply to help them find the right workout session.  

If a user wants to learn more, they can just click on any of the session badges. This will trigger a pop-up that displays the session details and has a join button.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Popup-Join.png">  
  
If the session is full, the join button will be replaced with a "Session Full" warning instead.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Popup-Full.png">  

Users can view their profile details by clicking on their profile email in the top right of their navbar and selecting "Profile." They will be redirected to the page below.  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Profile-m3.png">  
  
Finally, there are two informational pages that users can access should they want to. These include our "Contact Us" page:  
  
<img width="576px" class="rounded float-start pe-4" src="/images/Contact-Us.png">  
  
And our "About Us" page:  
  
<img width="576px" class="rounded float-start pe-4" src="/images/About-Us.png">  

## Developer Guide

If you're interested in running this project locally, please follow the instructions below.  

1. Install PostgreSQL and create a database for your app:
```
createdb rainbow-gyms
```
<small>Note: Your database can be named anything. It doesn't have to be rainbow-gyms.</small>

2. Clone this repo locally on your own device.  

3. cd into the app directory and install the required dependencies.
```
npm install
```
4. Create your `.env` file
    * Copy `sample.env` to `.env` and update the `DATABASE_URL` to match your PostgreSQL setup.  
  
5. Run database migrations:
```
npx prisma migrate dev
```

6. Generate Prisma client:
```
npx prisma generate
```

7. Seed the database with some default data:
```
npm run seed
```

8. Start the development server:
```
npm run dev
```

The app will be available at [http://localhost:3000](http://localhost:3000).

## Deployment 
[View our live deployment of Rainbow Gyms on Vercel](https://rainbow-gyms-nextjs.vercel.app/)

## Community Feedback
We'd like to thank the people who were willing to help us out by testing the final deployment of Rainbow Gyms.
* Curtis Y., Senior Undergradaute Student, UH Manoa
* Aleena B., Senior Undergradaute Student, UH Manoa
* Danil K., Senior Undergradaute Student, UH Manoa
* Norah K., Undergraduate Student, UH Manoa

### Summary
Overall, the project's main features work properly. Users are able to create sessions, view session details, and join sessions through both the Directory page and the Calendar page. However, our testers encountered several bugs and provided us with several suggestions for improvement.

### Likes
The overall design and layout of the website is great, featuring an appealing theme that is easy on the eyes and mostly simple to navigate. Users appreciated the clear and organized footer design as well as the ability to filter through many options for workout sessions. The core concept behind the platform is seen as very useful if more people adopt it, and the general aesthetic receives high praise.

### Bugs
Several functional issues and broken elements were identified across the site. Multiple links fail to go anywhere, including a cluster of broken links in the footer such as the Testimonies page and UH Gym links. Clicking the "Join Session" button for a session a user has already joined displays a React error message instead of handling the action correctly. Additionally, a photo in the footer drops its image and displays only its alt text when a user is signed in, the Rainbow Gyms logo fails to show up in the footer on mobile devices, the calendar page layout is messed up on mobile, and the calendar component itself is slightly weird as it clips through the footer. Finally, the feedback form on the contact us page lacks a confirmation or error notification event upon submission.

### Improvement Suggestions
Users recommend adding comprehensive profile editing features, such as changing profile pictures, adding bios, and including optional personal or contact info to simplify coordination for profiles or workout sessions. To improve data input, minimum open spots should be changed to a slider or text box to accommodate up to 40 participants, and form layouts should be made more dynamic rather than restricted to a single column. Additional feature requests include a title search, a host search, a dark mode setting, Google Maps integration or location links, a password strength checker for new accounts, and changing the redundant join button into an unjoin session button. Finally, users requested different images on the about us tab.

## Milestones

### Milestone 1

[See our team's M1 project page](https://github.com/orgs/rainbow-gyms/projects/2)

#### Landing Page
<img width="576px" class="rounded float-start pe-4" src="/images/LandingPage.png">

#### Calendar (<i>Main Page</i>) Mockup
<img width="576px" class="rounded float-start pe-4" src="/images/Main-Page-Calendar.png">

#### My Sessions Mockup
<img width="576px" class="rounded float-start pe-4" src="/images/My-Sessions.png">

#### Create a Session Mockup
<img width="576px" class="rounded float-start pe-4" src="/images/Create-Session.png">

#### Profile Page Mockup
<img width="576px" class="rounded float-start pe-4" src="/images/Profile.png">

### Milestone 2

[See our team's M2 project page](https://github.com/orgs/rainbow-gyms/projects/3/views/1)

#### Sign In Page
<img width="576px" class="rounded float-start pe-4" src="/images/Sign-In.png">

#### Sign Up Page
<img width="576px" class="rounded float-start pe-4" src="/images/Sign-Up.png">

#### Setup Profile Page
<img width="576px" class="rounded float-start pe-4" src="/images/Setup-Profile.png">

#### Profile Page
<img width="576px" class="rounded float-start pe-4" src="/images/Profile-2.png">

#### Landing Page (After Login)
<img width="576px" class="rounded float-start pe-4" src="/images/Browse.png">

#### Session Details Page
<img width="576px" class="rounded float-start pe-4" src="/images/Session-Profile.png">

#### Create Session Page
<img width="576px" class="rounded float-start pe-4" src="/images/Create-Session-2.png">

#### My Sessions Page
<img width="576px" class="rounded float-start pe-4" src="/images/My-Sessions-2.png">

### Milestone 3

[See our team's M3 project page](https://github.com/orgs/rainbow-gyms/projects/4/views/1)

#### Sign Up Page
<img width="576px" class="rounded float-start pe-4" src="/images/Sign-Up-m3.png">

#### Setup Profile Page
<img width="576px" class="rounded float-start pe-4" src="/images/Setup-Profile-m3.png">

#### Profile Page
<img width="576px" class="rounded float-start pe-4" src="/images/Profile-m3.png">

#### Landing Page (After Login)
<img width="576px" class="rounded float-start pe-4" src="/images/Browse-m3.png">

#### Session Details Page
<img width="576px" class="rounded float-start pe-4" src="/images/Session-Profile-m3.png">

#### Create Session Page
<img width="576px" class="rounded float-start pe-4" src="/images/Create-Session-m3.png">

#### My Sessions Page
<img width="576px" class="rounded float-start pe-4" src="/images/My-Sessions-m3.png">

#### Calendar Page
<img width="576px" class="rounded float-start pe-4" src="/images/Calendar-m3.png">

#### Session Details Pop-Up (Available)
<img width="576px" class="rounded float-start pe-4" src="/images/Popup-Join.png">

#### Session Details Pop-Up (Full)
<img width="576px" class="rounded float-start pe-4" src="/images/Popup-Full.png">

#### Contact Us Page
<img width="576px" class="rounded float-start pe-4" src="/images/Contact-Us.png">

#### About Us Page
<img width="576px" class="rounded float-start pe-4" src="/images/About-Us.png">