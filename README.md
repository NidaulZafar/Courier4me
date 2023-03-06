# Courier4me - Class 39 final project

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://c39-hyf.herokuapp.com/">
    <img src="https://res.cloudinary.com/dl44q0v9r/image/upload/v1678096794/logo_cipz5l.png" alt="Our Logo" width="250" height="150">
  </a>
  </div>

## About the Project
This is the final project for the HackYourFuture curriculum we did as a class using the MERN stack by following the agile methodology with our team and a group of mentors. The web version of this project can be seen on [Heroku](https://c39-hyf.herokuapp.com/). A quick guide to what we built:


<div align="center">
<img src="https://res.cloudinary.com/dl44q0v9r/image/upload/v1675943679/ezgif.com-gif-maker_nsilhc.gif" width="800" height="400" alt="WelcomeScreen">
</div>

## Description

This app is built to provide a platform to deliver your packages for the cheapest price with the fastest delivery time anywhere in the Netherlands. To make use of this platform users need to register as a Sender or a Courier too. As a sender, users can make delivery requests for their packages. As a courier, the users can make deliveries by selecting one of the pending requests entered in the system according to their suitability.

## Usage
* User can register as a sender only or a sender as well as a courier.
* Users can reset their password in case they forget the current password.
* When the users log in, they can request a delivery by entering the package details, pick up address and destination address.
* Any available courier can self-assign the request from the system. It saves the history on their respective accounts.
* In case the courier cancels the request, the sender can make a new request for the same package again.
* In the details of the delivery, couriers can see the addresses where the package will be received and delivered on the map.
* Users can edit their profile pictures and information on their account dashboard.
* Users can see their delivery history on their account dashboard and can delete the history if they want.
* Users can see courier4me news in the press page and also access the frequently asked questions on the FAQ page to find answers to some common questions.
* The user can reach out to the customer support team through call, email or contact form at the contact page.


## 2. Code structure

```
client
├── public
└── src
|   └── __tests__
|   └── __testUtils__
|   └── assets
|   |      └── celebration.mp4
|   |      └── contactVideo.mp4
|   |      └── courier4me.png
|   |      └── color.png.jpg
|   |      └── logo.png
|   |      └── pt.png
|   └── components
|   |     └── __tests__
|   |     └── buttons
|   |     |      └── button.css
|   |     |      └── ClearButton.jsx
|   |     |      └── MainButton.jsx
|   |     |      └── SignButton.jsx
|   |     └── courier
|   |     |      └── ActiveDeliveriesForCourier.jsx
|   |     |      └── ActiveDeliveriesForCustomer.jsx
|   |     |      └── ApprovedDelivery.jsx
|   |     |      └── DeclinedDelivery.jsx
|   |     |      └── PendingDelivery.jsx
|   |     └── footer
|   |     |      └── footer.css
|   |     |      └── Footer.jsx
|   |     └── homepage_sections
|   |     |      └── AppWorks.jsx
|   |     |      └── CourierFeatures.jsx
|   |     |      └── FirstSec.jsx
|   |     |      └── home.css
|   |     |      └── SenderServices.jsx
|   |     |      └── Services.jsx
|   |     |      └── WhyUs.jsx
|   |     └── loadErr
|   |     |      └── Error.jsx
|   |     |      └── loadErr.css
|   |     |      └── Loading.jsx
|   |     └── navbar 
|   |     |      └── Nav.jsx
|   |     |      └── Nav.testid.js
|   |     |      └── navbar.css
|   |     └──input.jsx
|   └── context
|   |     └── AuthContext.js
|   └── hooks
|   |     └── __tests__
|   |     └── useFetch.js
|   └── pages
|   |   └── __tests__
|   |   └── account
|   |   |       └── account.css
|   |   |       └──Account.jsx
|   |   └── contact 
|   |   |       └── contact.css
|   |   |       └── Contact.jsx
|   |   └── delivery
|   |   |       └── delivery.css
|   |   |       └── Delivery.jsx
|   |   |       └── deliveryHistory.css
|   |   |       └── DeliveryHistory.jsx
|   |   |       └── yourPackage.css
|   |   |       └── YourPackage
|   |   └── deliveryRequests
|   |   |       └── deliveryRequest.css
|   |   |       └── DeliveryRequest.jsx
|   |   └── faq
|   |   |       └── faq.css
|   |   |       └── Faq.jsx
|   |   └── home
|   |   |       └── __tests__
|   |   |       └── Home.jsx
|   |   |       └── Home.testId.
|   |   └── loginSingup
|   |   |       └── login.css
|   |   |       └── Login.jsx
|   |   |       └── signUp.css
|   |   |       └── Signup.jsx
|   |   |       └── signupSuccess.css
|   |   |       └── SignupSuccess.jsx
|   |   └── press
|   |   |       └── press.css
|   |   |       └── Press.jsx
|   |   └── resetpassword
|   |           └── ResetPassword.jsx
|   └── util
|   |   └── __tests__
|   |   |       └── createTestIdFilePath.test.js
|   |   └── createTestIdFilePath.js
|   └── App.jsx
|   └── AppWrapper.jsx
|   └── index.css
|   └── Index.jsx
|
└── .babelrc
└── .eslintrc.js
└── jest.config.js
└── setupTests.js
└── webpack.config.js
cypress
|   └── fixtures
|   └── integration
|   └── plugins
|   └── support
server
└── src
|   └── __tests__
|   |       └── createUser.test.js
|   |       └── user.test.js
|   └── __testUtils__
|   |       └── dbMock.js
|   |       └── userMocks.js
|   └── controllers
|   |       └── delivery.js
|   |       └── message.js
|   |       └── photo.js
|   |       └── user.js
|   └──db
|   |   └── connectDB.js
|   └── images
|   └── models
|   |      └── Delivery.js
|   |      └── Message.js
|   |      └── User.js
|   └── routes
|   |      └── delivery.js
|   |      └── message.js
|   |      └── photo.js
|   |      └── user.js
|   └── util
|   └── index.js
|   └── app.js
|   └── testRouter.js
└── views
    └── index.ejs
└── .eslinttrc.cjs
└── babel.conflig.js
└── jest.config.js
└──prettierrc.json
└── cypress.json
```

### 2.1 Client structure

- `public` || public facing client code
- `components` || all of our shared components that are used over multiple pages
- `hooks` || all of our custom hooks
- `pages` || the page components of our app, all routing goes between these components
- `pages/components` || components used specifically on those pages
- `util` || any utility functions that can be used anywhere on the client side
- `index.jsx` || the start point of the client


### 2.3 Server structure
- `controllers` || all of our controller functions that interact with the database
- `db` || all of our configuration for the database
- `models` || all of our `mongoose` models are placed here
- `routes` || code to match up the API with our controllers
- `util` || any utility functions that can be used anywhere on the server side
- `index.js` || the start point of the server

## 3. Stack / external libraries

The app was built in MERN stack (Mongoose, Express, React, Node) using the knowledge gained by studying different modules of Web Development at HackYourFuture curriculum especially:

 <img src="https://img.shields.io/badge/-HTML:5-750000?logo=html5" height="30" alt="HTML:5">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-CSS-4c9ee8?logo=css3" height="30" alt="CSS:3">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-Javascript-000000?logo=javascript" height="30" alt="JavaScript">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-Visual%20Studio%20Code-0cc0e7?logo=visual-studio" height="30" alt="VSC">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-React-gray?logo=react" height="30" alt="React">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-MongoDB-000000?logo=mongodb" height="30" alt="MongoDB">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://img.shields.io/badge/-NodeJs-ffffff?logo=nodedotjs" height="30" alt="MongoDB">

Next to that we make use of the following extras:

### 3.1 Configuration libraries

- `dotenv` || To load the .env variables into the process environment. See [docs](https://www.npmjs.com/package/dotenv)
- `webpack` / `html-webpack-plugin` || To bundle our React app and create a static app to host. See [docs](https://webpack.js.org/)
- `husky` || To run our tests and linter before committing. See [docs](https://typicode.github.io/husky/#/)
- `eslint` || To check our code. We have different configurations for frontend and backend. You can check out the configuration in the `.eslintrc.(c)js` files in the respective `client` and `server` folders. See [docs](https://eslint.org/)
- `prettier` || To automatically format our code. See [docs](https://prettier.io/)
- `concurrently` || To run commands in parallel. See [docs](https://github.com/open-cli-tools/concurrently#readme)

For more information on how these work together including the automatic deployment to heroku, have a look at our detailed [DEV](./DEV.md) file.

### 3.2 Client-side libraries

- `jest-fetch-mock` || To mock out the backend for our testing purposes. See [docs](https://github.com/jefflau/jest-fetch-mock#readme)
- `prop-types` || To type-check our components. See [docs](https://github.com/facebook/prop-types)

### 3.3 Server-side libraries

- `nodemon` || To automatically restart the server when in development mode. See [docs](https://nodemon.io/)
- `jest` || To run our tests and coverage. See [docs](https://jestjs.io/)
- `supertest` || To more easily test our endpoints. See [docs](https://github.com/visionmedia/supertest#readme)
- `mongodb-memory-server` || To mock out our database in our backend tests. See [docs](https://github.com/nodkz/mongodb-memory-server)
- `cors` || To open up our API. See [docs](https://github.com/expressjs/cors#readme)
- `mongoose` || To add schemas to our database. See [docs](https://mongoosejs.com/)


## Roadmap

This is a basic app that fulfills the requirements for the graduation project at HackYourFuture. However, the team intends to keep improving upon it with the following roadmap. 

- [x] Responsive app
- [x] Follow the MERN stack
- [x] Have a frontend connected to the backend alongwith the Database.
- [x] Loading/error handling.
- [ ] Additional Options
    - [ ] Payment system
    - [ ] Star based reviewing system for the provided services.

## Contributing

This is in no way a perfect application. We, as a team, are in the process of learning and implementing knowledge. Therefore, contributions, suggestions and feedbacks are **heartily welcome**. If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Our Team

[<img src="https://img.shields.io/badge/-Asiye Gokalp-000?logo=github" height="30" alt="Github">](https://github.com/AsiyeGokalp)
[<img src="https://img.shields.io/badge/-Betul Yasar-222?logo=github" height="30" alt="Github">](https://github.com/betysr)
[<img src="https://img.shields.io/badge/-Heba Salem-444?logo=github" height="30" alt="Github">](https://github.com/hebaMak)
[<img src="https://img.shields.io/badge/-Nida ul Zafar-444?logo=github" height="30" alt="Github">](https://github.com/nidaulzafar)
[<img src="https://img.shields.io/badge/-Nuha Azazi-222?logo=github" height="30" alt="Github">](https://github.com/noshacode)
[<img src="https://img.shields.io/badge/-Yusuf Demir-000?logo=github" height="30" alt="Github">](https://github.com/yusufDemir9110)

## Acknowledgments

The team would like to acknowledge a number of people who helped us get through this project. 


* DevOps for the project [Rob van Kruijsdijk](https://github.com/robvk)
* TechLead [Josja Heerema](https://github.com/J05J4)
* Scrum Master [Larissa Sharkie](https://www.linkedin.com/in/larissa-sharkie-6a888553/)
* Product Owner [Michelle Audiffred](https://www.linkedin.com/in/michelleaudiffred/)
* Last but not least the numerous mentors and the [HackYourFuture Team](https://github.com/HackYourFuture) for their untiring guidance and efforts.
