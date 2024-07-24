# Hello👋, I’m Sai Ricky
`- 👀 I’m interested in Dev.`
`- 🌱 I’m currently fresh graduate`

  Welcome to my GitHub profile! I'm a front-end developer from Myanmar. My academic background has equipped me with a solid understanding of modern web technologies and good practices in front-end development. I am passionate about creating visually appealing and highly functional user interfaces. My attention to detail and commitment to delivering high-quality code ensure that I can contribute effectively to your development team. Additionally, my ability to quickly adapt to new technologies and teamwork.

<details>
  <summary>My Contents</summary>
  <ol>
    <li>
      <a href="#about-me">About ME</a>
      <ul>
        <li><a href="#-languages-and-tools">Languages and Tools</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#deploy">Deploy</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT ME -->
## About Me

  I am Mr. Sai Reacky. I am from Myanmar and I fresh graduate of Computer Science, Major SOFTWARE ENGINEER, School of Information Technology from <a href="https://en.mfu.ac.th/home.html">Mae Fah Luang University</a> in Thailand.


### 💻 Languages and Tools:

Languages and Tools I have been to use.

| [![Git][Git]][Git-url] | [![GitHub][GitHub]][GitHub-url] | [![GitLab][GitLab]][GitLab-url] | [![Lucid][Lucid]][Lucid-url] | [![Adobe XD][Adobe XD]][Adobe XD-url] | [![Figma][Figma]][Figma-url] | [![C++][c++]][c++-url] | [![JAVA][JAVA]][JAVA-url] |
|---------------|-----------------------------------|-----------|-----------|-----------|-----------|-----------|-----------|



[![Node][Node.js]][Node-url]

[![React][React.js]][React-url]

[![Tailwind CSS][Tailwind]][Tailwind-url]

[![Vite][Vite]][Vite-url]

[![Firebase][Firebase]][Firebase-url]

[![Express.js][Express.js]][Express-url]





[![JavaScript][JavaScript]][JavaScript-url]

[![TypeScript][TypeScript]][TypeScript-url]

[![NetBeans][NetBeans]][NetBeans-url]

[![Eclipse][Eclipse]][Eclipse-url]

[![VisualStudioCode][VisualStudioCode]][VisualStudioCode-url]

[![Vuetify][Vuetify]][Vuetify-url]

[![Vue.js][Vue.js]][Vue.js-url]







[![Wix][Wix]][Wix-url]

[![XAMPP][XAMPP]][XAMPP-url]

[![HTML5][HTML5]][HTML5-url]

[![CSS3][CSS3]][CSS3-url]

[![Bootstrap][Bootstrap]][Bootstrap-url]

[![Postman][Postman]][Postman-url]

[![Next.js][Next.js]][Next.js-url]

[![React][React]][React-url]

[![Flutter][Flutter]][Flutter-url]

[![Python][Python]][Python-url]

[![Docker][Docker]][Docker-url]

[![MySQL][MySQL]][MySQL-url]

[![phpMyAdmin][phpMyAdmin]][phpMyAdmin-url]

[![MongoDB][MongoDB]][MongoDB-url]











<!-- GETTING STARTED -->
## Getting Started

### Installation

How you can instruct our audience on installing and setting up our app.

1. First, in git repository press code button and select HTTPS and coppy link
2. Clone the repo by type this command in terminal
   
   ```sh
   git clone https://github.com/ricky2001/SP_2023_loyaltychat0.3.git
   ```
   
After you clone this project open terminal, you have to go in two folders.
this cd into frontend folder
  ```sh
  cd FE_FRONTENDV2
  ```
after you go in frontend folder you have to open new cmd for go in to backend folder and this cd into backend folder
  ```sh
  cd BE_FROMCHECKINV2
  ```


### Prerequisites

After you go into root folders of backend and frontend, you have to type npm command for install package.
* npm
  ```sh
  npm i
  or
  npm install
  ```

In backend folder, you have to create `.env` file that contain the api key from openai and resend.
* .env
  ```sh
  OPENAI_API_KEY="your openai api key"
  JOB_ID="your job model from fine tuning openai"
  RESEND_API="your resend apik key"
  ```

<p align="right">(<a href="#hello-im-sai-ricky">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

After you install in each folders finished, you have to run this command for running our project.
* npm run dev
  ```sh
  npm run dev
  ```
You can use this command(npm run dev) in both frontend and backend. 

You can use this username `test1@gmail.com`, `test2@gmail.com` and password `12345678` for use our web app.

If you want to see the database, you can see on firebase.

[![Firebase][Firebase]][Firebase-url] (click this to go see our firebase)

<p align="right">(<a href="#hello-im-sai-ricky">back to top</a>)</p>



<!-- ROADMAP -->
## Deploy
If you want to deploy this project, you have to do by step:

First you have to open Visual Studio Code, then open project folder.

For frontend

1. Open folder `FE_FRONTENDV2`, then go into `src\utils\api`

2. You will see `axiosIntance.js` file, then open it.

3. You will see code in line 6 and 7,
  ```sh
  const baseURL = 'http://localhost:3000/';
//  const baseURL = 'https://us-central1-loyalty-e5fdd.cloudfunctions.net/api';
  ```
Change to be this.
```sh
//  const baseURL = 'http://localhost:3000/';
  const baseURL = 'https://us-central1-loyalty-e5fdd.cloudfunctions.net/api';
  ```

4. Open terminal and go into frontend folder.
  ```sh
  cd FE_FRONTENDV2
  ```

5. After that run this command for deploy frontend.
  ```sh
  firebase deploy
  ```
  Then wait until it finish.

For backend

1. Open folder `BE_FROMCHECKINV2`, You will see `app.js` file, then open it.

2. You will see code in app.js,
  ```sh
const express = require("express");
const bodyParser = require("body-parser");
const cors = require('cors');
const app = express();

// Routes
const authRoutes = require("./routes/auth");

app.use(bodyParser.json({ extended: false,limit:'10mb' }));
app.use(cors()); 

// Routes
app.use("/api", authRoutes);

// PORT
const port = 3000;

// Starting a server
app.listen(port, () => {
  console.log(Start server : ${port});
});

//for deploy
// const express = require("express");
// const bodyParser = require("body-parser");
// const cors = require('cors');
// const app = express();
// const functions = require('firebase-functions');
// const authRoutes = require("./routes/auth");

// app.use(bodyParser.json({ extended: false ,limit:'10mb'}));
// app.use(cors()); 

// // Routes
// app.use("/api", authRoutes);

// exports.api = functions.https.onRequest(app);
  ```
Change to be this.
```sh
// const express = require("express");
// const bodyParser = require("body-parser");
// const cors = require('cors');
// const app = express();

// Routes
// const authRoutes = require("./routes/auth");

// app.use(bodyParser.json({ extended: false,limit:'10mb' }));
// app.use(cors()); 

// Routes
// app.use("/api", authRoutes);

// PORT
// const port = 3000;

// Starting a server
// app.listen(port, () => {
//   console.log(Start server : ${port});
// });


// for deploy
const express = require("express");
const bodyParser = require("body-parser");
const cors = require('cors');
const app = express();
const functions = require('firebase-functions');
const authRoutes = require("./routes/auth");

app.use(bodyParser.json({ extended: false ,limit:'10mb'}));
app.use(cors()); 

// Routes
app.use("/api", authRoutes);

exports.api = functions.https.onRequest(app);
  ```

4. Open terminal and go into frontend folder.
  ```sh
  cd BE_FROMCHECKINV2
  ```

5. After that run this command for deploy frontend.
  ```sh
  firebase deploy
  ```
  Then wait until it finish, After you done every steps it is mean you deploy successful.


<p align="right">(<a href="#hello-im-sai-ricky">back to top</a>)</p>



<!-- LICENSE -->
## License

MFU

IT school, SE major(Gen 16) 

ID:6331305002 Mr. JIRAWAT RATSAMEE (Loyalty Program group)

ID:6331305007 Mr. CHINDANAI POTIJUNTAJINDA (Loyalty Program group)

ID:6331305014 Mr. NUNTAWAT PRANGSANGWILAI (Chat Bot group)

ID:6331305023 Mrs. RISA SIRIROT (Chat Bot group)

ID:6331305037 Mr. PHEERAPHOL MEKKHARACH (Chat Bot group)

ID:6331305048 Mr. Sai Reacky (Loyalty Program group)


<p align="right">(<a href="#hello-im-sai-ricky">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Email Adress - [![Gmail]][gmail-url]

My LinkedIn - [![LinkedIn]][linkedin-url]


<p align="right">(<a href="#hello-im-sai-ricky">back to top</a>)</p>




<!-- MARKDOWN LINKS & IMAGES -->

[GitHub]: https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=fff&style=flat
[GitHub-url]: https://github.com/
[GitLab]: https://img.shields.io/badge/GitLab-FC6D26?logo=gitlab&logoColor=fff&style=flat
[GitLab-url]: https://about.gitlab.com/
[Git]: https://img.shields.io/badge/Git-F05032?logo=git&logoColor=fff&style=flat
[Git-url]: https://git-scm.com/
[MongoDB]: https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=fff&style=flat
[MongoDB-url]: https://www.mongodb.com/
[phpMyAdmin]: https://img.shields.io/badge/phpMyAdmin-6C78AF?logo=phpmyadmin&logoColor=fff&style=flat
[phpMyAdmin-url]: https://www.phpmyadmin.net/
[MySQL]: https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=fff&style=flat
[MySQL-url]: https://www.mysql.com/
[Docker]: https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=fff&style=flat
[Docker-url]: https://www.docker.com/
[Python]: https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff&style=flat
[Python-url]: https://www.python.org/
[Flutter]: https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=fff&style=flat
[Flutter-url]: https://flutter.dev/
[React]: https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=000&style=flat
[React-url]: https://react.dev/
[Next.js]: https://img.shields.io/badge/Next.js-000?logo=nextdotjs&logoColor=fff&style=flat
[Next.js-url]:https://nextjs.org/
[Postman]: https://img.shields.io/badge/Postman-FF6C37?logo=postman&logoColor=fff&style=flat
[Postman-url]: https://www.postman.com/
[Bootstrap]: https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=fff&style=flat
[Bootstrap-url]: https://getbootstrap.com/
[CSS3]: https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=fff&style=flat
[CSS3-url]: https://www.w3schools.com/css/
[HTML5]: https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=fff&style=flat
[HTML5-url]: https://www.w3schools.com/html/
[XAMPP]: https://img.shields.io/badge/XAMPP-FB7A24?logo=xampp&logoColor=fff&style=flat
[XAMPP-url]: https://www.apachefriends.org/
[Wix]: https://img.shields.io/badge/Wix-0C6EFC?logo=wix&logoColor=fff&style=flat
[Wix-url]: https://www.wix.com/
[Lucid]: https://img.shields.io/badge/Lucid-282C33?logo=lucid&logoColor=fff&style=flat
[Lucid-url]: https://www.lucidchart.com/pages/
[Adobe XD]: https://img.shields.io/badge/Adobe%20XD-FF61F6?logo=adobexd&logoColor=fff&style=flat
[Adobe XD-url]: https://adobexdplatform.com/
[Figma]: https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=fff&style=flat
[Figma-url]: https://www.figma.com/
[Vue.js]: https://img.shields.io/badge/Vue.js-4FC08D?logo=vuedotjs&logoColor=fff&style=flat
[Vue.js-url]: https://vuejs.org/
[Vuetify]: https://img.shields.io/badge/Vuetify-1867C0?logo=vuetify&logoColor=fff&style=flat
[Vuetify-url]: https://vuetifyjs.com/en/
[VisualStudioCode]: https://img.shields.io/badge/Visual%20Studio%20Code-1B6AC6?logo=apachenetbeanside&logoColor=fff&style=flat](https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?logo=visualstudiocode&logoColor=fff&style=plastic
[VisualStudioCode-url]: https://code.visualstudio.com/
[Eclipse]: https://img.shields.io/badge/Eclipse%20IDE-2C2255?logo=eclipseide&logoColor=fff&style=flat
[Eclipse-url]: https://eclipseide.org/
[NetBeans]: https://img.shields.io/badge/Apache%20NetBeans%20IDE-1B6AC6?logo=apachenetbeanside&logoColor=fff&style=flat
[NetBeans-url]: https://netbeans.apache.org/front/main/index.html
[TypeScript]: https://shields.io/badge/TypeScript-3178C6?logo=TypeScript&logoColor=FFF&style=flat-square
[TypeScript-url]: https://www.typescriptlang.org/
[JavaScript]: https://shields.io/badge/JavaScript-F7DF1E?logo=JavaScript&logoColor=000&style=flat-square
[JavaScript-url]: https://www.javascript.com/
[JAVA-url]: https://www.java.com/en/
[JAVA]: https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white
[c++-url]: https://cplusplus.com/doc/tutorial/
[c++]: https://img.shields.io/badge/-C++-blue?logo=cplusplus
[Node.js]: https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[Node-url]: https://nodejs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vite]: https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white
[Vite-url]: https://vitejs.dev/
[Express.js]: https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white
[Express-url]: https://expressjs.com/
[Tailwind]: https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white
[Tailwind-url]: https://tailwindcss.com/
[Firebase]: https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black
[Firebase-url]: https://console.firebase.google.com/u/1/project/loyalty-e5fdd/overview
[LinkedIn]:https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url]:https://www.linkedin.com/in/sai-ricky-chan-3264a0288
[Gmail]: https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white
[gmail-url]: mailto:saireacky@gmail.com

