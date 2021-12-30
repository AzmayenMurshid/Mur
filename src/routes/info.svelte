<script>
    const title="about me";
</script>
<svelte:head>
    <title>{title}</title>
</svelte:head>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins');

    body {
        overflow: scroll;
    }

    #About-Me {
        margin-bottom: 10%;
    }
    .navBar {
        transform: translateX(80%);
        margin-top: 30px;
        margin-right: 10%;
    }

    .navBar a {
        text-decoration: none;
        color: white;
        margin-right: 25px;
        transform: translateY(-20%);
    }

    .navBar a:hover {
        color: #05d9e8;
    }

    .heading {
        display: block;
        margin-top: 7%;
        transform:translateX(85%);
        color: #05d9e8;
        text-shadow: 0px 0px 500px #dadcdd;
        margin-right: 30%;
        font-size: 150%;
        margin-bottom: 0;
        animation: fadeIn 7s cubic-bezier(0, 1.07, .72, 1.42);
    }
    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
    .about-me img{
        float: left;
        margin-left: 5%;
        border: 5px solid #05d9e8;
        border-radius: 10px;
        margin-right: -10%;
    }
    .about-me img:hover{
        transform: translateY(-5%);
    }
    .about-me-Content {
        display: block;
        margin-right: 10%;
        margin-left: -10%;
    }
    .animatedTexts{
        animation: fadeAndScale 7s cubic-bezier(0, 1.07, .72, 1.42);
        transform-origin: center bottom;
        animation-iteration-count: 1;
    }

    @keyframes fadeAndScale {
        from {
            opacity: 0;
            transform: translateY(10%);
        }
        to {
            opacity: 1;
            transform: translateY(2%);
        }
    }

    .about-me-Content p {
        float: right;
        width: 50%;
        overflow: hidden;
        color: #d1f7ff;
        text-align: justify;
        padding-top: 2%;
    }

    .about-me-Content h3 {
        clear: both;
        display: block;
        padding-top: 7%;
        transform: translateX(50%);
        font-size: 130%;
        color: #05d9e8;
        opacity: 0.5;
    }
    .about-me-Content ul {
        list-style-type: none;
        display: inline-block;
        color: #d1f7ff;
        margin-top: 2%;
        margin-right: 10%;
        margin-bottom: 10%;
    }
    .about-me-Content ul li::before {
        content: "\2022";
        color: #05d9e8;
        display: inline-block;
        font-weight: bold;
        width: 1em;
        margin-left: -1em;
    }
    #BackEnd {
        margin-top: 2%;
        margin-left: 40%;
        transform: translateX(60%);
    }
    .about-me-Content #FrontEnd{
        margin-top: 2%;
        transform: translateX(70%);
    }
    .about-me-Content #Databases{
        margin-top: 2%;
        transform: translateX(80%);
    }

    #Experiences {
        margin-bottom: 10%;
    }

    #Experiences .heading {
        float: left;
        margin-bottom: 5%;
        margin-left: 25%;
    }
    #ex-info table {
        clear: both;
        margin-bottom: 10%;
        transform:translateX(-2%);
    }
    .titles {
        width: 20%;
        background-color: var(--bg-secondary);
        border: none;
        transform: translateX(90px);
        color: #d1f7ff;
        font-size: 100%;
        text-align: right;
        padding: 20px;
    }
    .titles:hover{
        border-right: 2px solid rgb(22, 139, 128);
    }
    .descriptions{
        width: 80%;
        display: block;
        margin-left: 300px;
        padding: 20px;
        border: 2px solid white;
        transform: translateX(-17%);
    }
    .descriptions:hover{
        border-left: 2px solid rgb(22, 139, 128);

    }
    .ex-info .descriptions ul li::before{
        content: "\2022";
        color: #05d9e8;
        display: inline-block;
        font-weight: bold;
        width: 1em;
        margin-left: -1em;
    }
    #Projects {
        margin-top: 10%;
        margin-bottom: 10%;
    }
    #Projects .heading h2 {
        transform:translateX(-30%);
    }
    .project-Container {
        display: inline-flex;
        float: left;
        width: 25%;
        height: 50%;
        margin-left: 2%;
        margin-bottom: 10%;
        background: #151542;
        border-radius: 20px;
        padding: 20px;

    }
    .project-Container:hover{
        opacity: 2;
        transform: translateY(-40px)
    }
    .project-Container h4 {
        text-align: left;
        opacity: 0.85;
    }
    .project-Container a {
        text-decoration: none;
        color: #d1f7ff;
    }
    .project-Container p{
        margin-top: 50px;
        text-align: left;

    }
    .project-Container h5 {
        margin-top: 50px;
    }
    @media (min-width: 100px) and (orientation: portrait){
        body{
            width: justify;
            overflow-y: scroll;
        }
        .navBar {
        transform: translateX(40px);
        }
        nav{
            width: 150%;
        }
        .navBar a{
            font-size: 8px;
            padding-left: 5px;
        }
        span img {
            transform: translateX(-2000px);
        }

        .about-me .heading {
            transform: translateX(90px);
        }
        .about-me .heading h2 {
            margin-top: 100px;
            margin-bottom: -100px;
        }

        .about-me-Content {
            overflow: none;
        }

        .about-me-Content p {
            clear: both;
            float: none;
            overflow: scroll;
            width: 90%;
            border: 3px solid white;
            padding: 20px;
            transform: translateX(60px);
            margin-top: 20px;
        }
        .about-me-Content h3 {
            font-size: 20px;
            width: 150%;
            transform: translateX(80px)
        }

        .about-me-Content ul {
            margin-right: 20px;
        }

        .about-me-Content #BackEnd {
            margin-left: 60px;
        }

        #Experiences .heading h2 {
            margin-top: 100px;
            width: 150%;
            transform: translateX(-190px);
            margin-bottom: 20px;
        }

        #Experiences .titles {
            transform: translateX(-1000px);
        }
        #Experiences .descriptions {
            width: 80%;
            transform: translateX(-400px);
        }

        #Projects .heading h2 {
            transform: translateX(-125px)
        }

        .project-Container {
            display: block;
            float: none;
            width: 80%;
            margin: 20px;
            margin-left: 40px;
        }
    }

    @media (min-width: 1000px) and (orientation: landscape) {
        body{
            background: var(--bg-secondary);
            opacity: 1;
        }
        .navBar {
            transform: translateX(450px)
        }
        .about-me-Content h3 {
            width: auto;
            padding-top: 0;
            transform: translateY(-30px);
            margin-left: 600px;
            text-align: center;
        }
        .about-me-Content ul {
            margin-top: -50px;
        }
        .about-me-Content ul li{
            transform: translateX(120px);
        }
        .titles {
            transform: translateX(60px);
        }
        .titles:hover {
            border-right: 3px solid cyan;
        }
        .descriptions {
            transform: translateX(-150px);
        }
        .project-Container h5 {
            margin-top: 50px;
        }
    }
    @media (min-width: 1500px) and (orientation: landscape) {
        body{
            background: var(--bg-secondary);
            opacity: 1;
        }
        .navBar {
            transform: translateX(1100px);
        }
        .about-me-Content h3, .about-me-Content #BackEnd{
            margin-left: 50%;
        }
        .about-me-Content h3{
            transform: translateY(-150px);
        }
        .about-me-Content #BackEnd {
            transform: translateY(-150px)
        }
        .about-me-Content #FrontEnd {
            transform: translateY(-150px)
        }
        .about-me-Content #Databases {
            transform: translateY(-150px)

        }
        #Experiences {
            margin-top: -10%;
        }
        .titles:hover {
            border-right: 3px solid cyan;
        }
    }
</style>

<body>
    <div id="About-Me">
        <nav class="navBar">
            <a href="/">home</a>
            <a href="#About-Me">about me</a>
            <a href="#Experiences">experience</a>
            <a href="#Projects">projects</a>
        </nav>
    </div>
    <div class="about-me">
        <div class="heading">
            <h2>/ about me</h2>
        </div>
        <span>
            <img src="https://media3.giphy.com/media/l0IpXgEBZ3y3UEljO/giphy.gif?cid=790b76116e6fe86933e15c420b871ae23b6b8ee88565ca36&rid=giphy.gif&ct=s" alt="" width="30%" height="20%">
        </span>
        <span class="about-me-Content animatedTexts">
            <p>I am currently in High School at Sunway International School. Regardless of my academic
                background
                I have been able to accomplosh numerous personal projects, including motion-censor volume control, Todo
                lists,
                Arcade game developments and web developments. Last semester I excelled at Computer Science with an
                average
                of 94%.
                I am grateful to be mentored by a UC Berkeley graduate, Saif Nizam. I am into any sort of software
                develpment that
                requires creativity and critical thinking. Some areas that peak my interest are full-stack development,
                Machine-Learning,
                and game development. On my free time I update personal websites, develop video games and networking.</p>
                
                <h3>Technologies I have worked with</h3>

                <ul id="BackEnd">
                    <li>Python</li>
                    <li>Java</li>
                    <li>C++</li>
                </ul>
                <ul class="techList" id="FrontEnd">
                    <li>HTML & CSS</li>
                    <li>Javascript</li>
                    <li>Svelte</li>
                </ul>
                <ul id="Databases">
                    <li>PostgreSQL</li>
                    <li>MySQL</li>
                    <li>SQL</li>
                </ul>
        </span>
    </div>
    <div id="Experiences">
        <div class="heading">
            <h2>/ experience</h2>
        </div>

        <div id = 'ex-info'>
            <table>
                <tr>
                    <td class = "titles">ICS2O</td>
                    <td class = "descriptions" style='text-align: justify'>ICS2O is a Canadian grade 10 Computer science course that teaches:
                        <ul style="padding-left: 7%; padding-top: 2%; padding-bottom: 2%;">
                            <li> Fundamental of Computer Science</li>
                            <li>Python</li>
                            <li>HTML & CSS</li>
                        </ul>
                         At <a href="https://sis.sunway.edu.my/frontpage" style="color: cyan; text-decoration: none;" target="_blank">Sunway International School</a> I worked with hands on projects with fundamental syntax.
                          In addition, our teacher gave me the apportunity to assist him to tutor the students struggling. through out the semester we worked on various projects which enabled me to understand algorithms, syntax, error handling and debugging more in depth.
                        we had to create a personal website which summarized our whole course. i was able to code a retro arcade game to go above and beyond.</td>
                </tr>
                <tr>
                    <td class = "titles">Summer Projects</td>
                    <td class = "descriptions" style="text-align: justify">Through out the summer I worked on multiple personal projects. Some of them include:
                        <ul style="padding-left: 7%; padding-top: 2%; padding-bottom: 2%;">
                            <li>Motion Sensor Voice Control</li>
                            <li>Andoid app development</li>
                            <li>game development</li>
                            <li>full stack web development</li>
                        </ul>
                          and many more. Couple of codes are released on 
                        <a href="https://github.com/AzmayenMurshid" style="color: cyan; text-decoration:none" target="_blank">Github</a> I also had an opportunity to learn about Android app development through <a href="https://developer.android.com/studio" style="color: cyan; text-decoration:none" target="_blank">Android studio</a>, Java, SQL and MySQL. Cross platform app development through <a href="https://flutter.dev/" style="color: cyan; text-decoration:none" target="_blank">Flutter</a>.
                            Game development was one of the most challenging field as I worked with  <a href="https://www.unrealengine.com/en-US/?sessionInvalidated=true" style="color: cyan; text-decoration:none" target="_blank">Unreal Engine</a> and I am still learning about it to this day. As for full stack development, I have worked with <a href="https://kit.svelte.dev/" style="color: cyan; text-decoration:none" target="_blank">SvelteKit</a> framework. Alongside Sveltekit I had to work with HTML, CSS, Javascript, TypeScript and Postgres.</td>
                </tr>
                <tr>
                    <td class = "titles">Bootcamp</td>
                    <td class = "descriptions">Everything I have learned so far were through online courses which even prepared me for school. Everything I learned from basic python syntax to full stack web development, were through:
                        <ul style="padding-left: 7%; padding-top: 2%; padding-bottom: 2%;">
                            <li><a href="https://www.freecodecamp.org/" style="color: cyan; text-decoration:none" target="_blank">FreeCodeCamp</a></li>
                            <li><a href="https://www.w3schools.com/" style="color: cyan; text-decoration:none" target="_blank">Code Academy</a></li>
                            <li><a href="https://www.codecademy.com/" style="color: cyan; text-decoration:none" target="_blank">W3schools</a></li>
                        </ul>
                    </td>
                </tr>
            </table>
        </div>
    </div>
    <div id= "Projects">
        <div class= 'heading'>
            <h2 style = "margin-bottom: 10%">/ projects</h2>
        </div>
        <div class = "project-Container" style="margin-left: 10%">
            <span>
                <h4>Motion sensor Volume Control</h4>
                <a href = "https://github.com/AzmayenMurshid/Motion-Sensor-VolumeControl">
                <p>Change your volume with hand gestures and hovering your hand. Done with external modules such as cv2, mediapipe, math, and many more</p>
                <h5>Python</h5>
                </a>
            </span>
        </div>
        <div class="project-Container">
            <span>
            <h4>Todo List</h4>
            <a href = "https://github.com/AzmayenMurshid/Motion-Sensor-VolumeControl">
            <p>An User friendly app to contain your checklists, todos, and reminders. Consisting of database to store data.</p>
            <h5>Svelte, Javascript, TypeScript, HTML, CSS, Prisma, Postgres</h5>
            </a>
            </span>
        </div>
        <div class="project-Container">
            <span>
            <h4>Muricle Game</h4>
            <a href = "https://github.com/AzmayenMurshid/Motion-Sensor-VolumeControl">
            <p>A pixelated Retro game inspired from Mario. Contains 3 levels and player has to fight enemies and go thorugh obstacles to win!</p>
            <h5>Python</h5>
            </a>
            </span>
        </div>
        <div class="project-Container" style = "clear: both; margin-left: 10%">
            <span>
            <h4>Maze Game</h4>
            <a href = "https://github.com/AzmayenMurshid/MazeGame">
            <p>Retro pixalated game inpired from pacman. Objective is to get to the vortext before the terminators get you! External turtle, math, random and time libraries</p>
            <h5>Python</h5>
            </a>
            </span>
        </div>
        <div class="project-Container">
            <span>
            <h4>Personal Website</h4>
            <a href = "https://github.com/AzmayenMurshid/Personal-Website">
            <p>The code to this very website. Done with Svelte framework. consisting of Javascript, HTML and CSS and deployed through vercel.</p>
            <h5>Svelte, Javascript, HTML, CSS</h5>
            </a>
            </span>
        </div>
        <div class="project-Container">
            <span>
            <h4>Ping pong</h4>
            <a href = "https://github.com/AzmayenMurshid/Ping-Pong">
            <p>Retro Arcade 2 player ping pong game created with Turtle and time library. player 1 key bindings are "w" and "s", player 2 key bindings are "up", "down".</p>
            <h5>Python</h5>
            </a>
            </span>
        </div>
    </div>
</body>
 