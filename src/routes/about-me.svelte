<script>
    let src = "about-me-image.jpeg"
</script>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins');

    body{
        background: #01012b;
        margin: 0%;
        max-height: 100vh;
    }
    .heading {
        display: block;
        margin: 5%;
        transform:translateX(85%);
        color: #05d9e8;
        text-shadow: 0px 0px 500px #dadcdd;
        margin-right: 30%;
        font-size: 150%;
        margin-bottom: 0;
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
        overflow: hidden;
        margin-right: 10%;
        margin-left: -10%;
    }
    .about-me-Content p {
        float: right;
        width: 70%;
        color: #d1f7ff;
        text-align: justify;
        padding-top: 5%;
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
</style>

<body>
    <div class="about-me">
        <div class="heading">
            <h2>/ About me</h2>
        </div>
        <span>
            <img src="https://media3.giphy.com/media/l0IpXgEBZ3y3UEljO/giphy.gif?cid=790b76116e6fe86933e15c420b871ae23b6b8ee88565ca36&rid=giphy.gif&ct=s" alt="" width="30%" height="20%">
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
 