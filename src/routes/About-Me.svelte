<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins');

    :root {
        --bg-color: #121212;
        --bg-secondary: #343F4F;
        --main-txt: #610094;
        --secondary-txt: #FC6D6D;
        --heading-txt: #150050;
        --secondary-heading: #AAA;
        --paragraph: #404040;
    }
    body{
        background-color: var(--bg-color);
        margin-top: 15%;
    }
    .about-me img {
        float: right;
        width: 30%;
        height: 80%;
        margin-right: 15%;
        border: 2px solid white;
        border-radius: 50%;
    }
</style>

<body>
    <div class="about-me">
        <div class="heading">
            <h2>/ About me</h2>
        </div>
        <span>
            <img src="mail_icon.png" alt="">
        </span>
        <span class="about-me-Content">
            <p>I am currently in High School, studying at Sunway International School. Regardless of my academic
                background
                I have been able to accomplosh numerous personal projects, including motion-censor volume control, Todo
                lists,
                Arcade game developments and web developments. Last semester I excelled at Computer Science with an
                average
                of 94%.
                I am grateful to be a mentored by a UC Berkeley graduate, Saif Nizam. I am into any sort of software
                develpment that
                requires creativity and critical thinking. Some areas that peak my interest are full-stack development,
                Machine-Learning,
                and game development. On my free time I update personal websites, play video games and networking.</p>

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
</body>
 