<script lang="ts">
    const title = 'Mur';
</script>
<svelte:head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>{title}</title>
</svelte:head>
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

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Poppins', sans-serif;
    }

    body {
        background:#01012b;
        min-height: 100vh;
        margin-top: 0%;
        overflow-y: auto;
        width: 100%;
    }

    .Mobile-Wrapper{
        display: none;
    }

    #blobSvg {
        display: block;
        float: left;
        position: relative;
        margin-top: 5%;
        margin-left: 1.5%;
    }

    #svgWaves {
        position: absolute;
        transform: translateX(0%);
        transform: translateY(5%);
    }

    .wrapper {
        display: inline-flex;
        align-items: center;
        transform: translateX(82%);
        margin-top: 5%;
        position: absolute;
    }

    .wrapper .static-txt {
        color: #fff;
        font-size: 50px;
        font-weight: 400;
    }

    .wrapper .dynamic-txts {
        margin-left: 15px;
        height: 90px;
        line-height: 90px;
        overflow: hidden;
    }

    .dynamic-txts li {
        color: #6B9FED;
        list-style: none;
        font-size: 60px;
        font-weight: 500;
        position: relative;
        top: 0;
        animation: slide 6s steps(4) infinite;
    }

    @keyframes slide {
        100% {
            top: -360px;
        }
    }

    .dynamic-txts li span {
        position: relative;
    }

    .dynamic-txts li span::after {
        content: "";
        position: absolute;
        left: 0;
        height: 100%;
        width: 100%;
        background: #01012b;
        border-left: 3px solid var(--bg-secondary);
        animation: typing 1.5s steps(10) infinite;
    }

    @keyframes typing {
        100% {
            border-left-color: #A1A7C8;
            left: 100%;
            margin: 0 -35px 0 35px;
        }
    }

    .intro {
        display: block;
        width: 50%;
        transform: translateX(50%);
        color: white;
    }

    .intro h2 {
        transform: translateY(400%);
        font-size: 200%;
        color: var(--secondary-heading);
        opacity: 0.7;
    }

    .intro p {
        transform: translateY(270%);
        font-size: 100%;
        text-align: left;
    }

    nav ul li {
        list-style: none;
        display: inline-block;
        margin-right: 30px;
        margin-top: 50px;
        transform: translateX(-100px);
    }
    nav ul li a{
        text-decoration: none;
        color: white;
        font-size: 14px;
    }
    .navBar a:hover {
        color: #05d9e8;
    }

    @media (min-width: 100px) and (orientation: portrait) {
        body {
            overflow-y: auto;
            overflow-x: hidden;
            opacity: 1;
        }
        #blobSvg {
            display: none;
        }
        nav ul {
            display: flex;
            justify-content: space-between;
            margin-left: 7px;
            padding: 10px;
            width: 100%;
            position: absolute;
            top: -10px;
            left: 45px;
            transform: translateX(60px);
            z-index: 2;
        }
        nav ul li a {
            color: #6B9FED;
            font-size: 17px;
        }
        #blobSvg, #svgWaves, #Parent-Wrapper{
            display: none;
        }

        .Mobile-Wrapper{
            display: block;
            width: 100%;
            text-align: center;
            margin-top: 175px;
            color: #6B9FED;
        }

        .intro{
            display: block;
            width: 100%;
            text-align: center;
        }

        .intro h2 {
            font-size: 25px;
            text-align: center;
            transform: translateX(-210px);
            margin-top: 50px;
        }
        .intro p {
            width: 350px;
            font-size: 15px;
            margin-top: 50px;
            margin-left: -180px;
            border: 3px solid white;
            padding: 20px;
            transform: translateX(0);
            text-align: center;
        }
        #Contact-Me{
            text-align: center;
            margin-top: 70px;
            margin-bottom: 30px;

        }
        #Contact-Me a{
            border: 2px solid cyan;
            border-radius: 10px;
            padding: 20px;
            text-decoration: none;
            color: cyan;
            margin-bottom: 30px;
        }
    }

    @media (max-width: 800px) and (orientation: landscape){

        body{
            height: 100vh;
        }

        nav ul {
            display: flex;
            justify-content: space-between;
            margin-left: 200px;
            padding: 10px;
            width: 60%;
            background-color: none;
            position: absolute;
            top: -10px;
            left: 45px;
            transform: translateX(60px);
            z-index: 2;
        }
        nav ul li a {
            color: #6B9FED;
            font-size: 17px;
        }

        #Parent-Wrapper{
            transform: translateY(100px);
        }

        .wrapper{
            transform: translate(80px, 50px);
        }
        .intro{
            margin-right: 100px;
        }
        .intro h2{
            width: 125%;
            margin-top: 250px;
            transform: translateX(-60px);
            margin-bottom: -250px;
        }
        .intro p{
            width: 150%;
            text-align: left;
            margin-right: 200px;
            margin-left: -57px;
            margin-top: 80px;
            font-size: 15px;
        }

        #Contact-Me{
            display: none;
            width: 100%;
            text-align: center;
        }
        #Contact-Me > a {
            border: 2px solid cyan;
            border-radius: 10px;
            padding: 20px;
            text-decoration: none;
            color: cyan;
            margin-bottom: 30px;
        }
        #svgWaves{
            position: fixed;
            height: auto;
            bottom: 0;
        }
    }

    @media(min-width: 1000px) and (orientation: landscape){
        body{
            overflow-y: auto;
            opacity: 1;
            height: 100%;

        }
        #blobSvg {
            transform: translateY(-25px);
            margin-left: 20px;
        }
        #navigation{
            display: flex;
            justify-content: space-between;
        }
        #navigation > a > svg {
            transform: translate(0, 10px);
            width: 70px;
        }

        .wrapper{
            transform:translate(350px, 0);
        }

        .intro h2 {
            transform: translateX(25px);
            margin-top: 170px;
        }
        .intro p{
            width: 100%;
            margin-left: 10px;
            margin-bottom: 20px;
            padding: 20px;
            transform: translateY(0px);
        }
        #svgWaves {
            width: 100%;
            height: auto;
            bottom: 0;
            position: fixed;
        }
        #Contact-Me{
            display: none;
            width: 100%;
            text-align: center;
            margin-top: 40px;
            cursor: pointer
        }
        #Contact-Me > a {
            border: 2px solid cyan;
            border-radius: 10px;
            padding: 20px;
            text-decoration: none;
            color: cyan;
            margin-bottom: 30px;
        }
    }

    @media (min-width: 1500px) and (orientation: landscape) {
        body {
            overflow-y: auto;
            opacity: 1;

        }
        #navigation{
            display: flex;
            justify-content: space-between;
        }
        /* #navigation > a > svg {
            transform: translate(0, -50px);
        } */
        .wrapper {
            margin-left: 50%;
            transform: translate(-65%, 0);
        }
        #Contact-Me{
            display: none;
            width: 100%;
            text-align: center;
        }
        #Contact-Me > a{
            border: 2px solid cyan;
            border-radius: 10px;
            padding: 20px;
            text-decoration: none;
            color: cyan;
            margin-bottom: 30px;
        }
        #svgWaves{
            width: 100%;
            height: auto;
            bottom: 0;
            position: fixed;
        }
    }
</style>
<header>
    <div id="navigation">
        <a href = "mailto: azmayen.murshid@gmail.com" title="Contact Me" >
            <svg viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="5%"
                    id="blobSvg">
                <defs>
                    <linearGradient id="gradient" x1="0%" y1="0%" x2="0%" y2="100%">
                        <stop offset="0%" style="stop-color: rgb(76, 161, 175);"></stop>
                        <stop offset="100%" style="stop-color: rgb(196, 224, 229);"></stop>
                    </linearGradient>
                </defs>
                <path id="blob"
                    d="M434.5,336Q422,422,336,437.5Q250,453,181,420.5Q112,388,59,319Q6,250,52,174Q98,98,174,58Q250,18,333.5,50.5Q417,83,432,166.5Q447,250,434.5,336Z"
                    fill="url(#gradient)"></path>
            </svg>
        </a>
        
        <nav class= navBar>
            <ul id ="Menu-List">
                <li><a href="/info#About-me">about me</a></li>
                <li><a href="/info#Experiences">experience</a></li>
                <li><a href="/info#Projects">projects</a></li>

            </ul>
        </nav>
    </div>
    <div id="Parent-Wrapper">
        <div class="wrapper">
            <div class="static-txt">I'm a</div>
            <ul class="dynamic-txts">
                <li><span>Developer</span></li>
                <li><span>Designer</span></li>
                <li><span>CS Student</span></li>
                <li><span>High Schooler</span></li>
            </ul>
        </div>
    </div>
</header>
<body>
    <div class="Mobile-Wrapper">
        <h1>I'm a developer</h1>
    </div>

    <div class='intro'>
        <h2>I create stuff sometimes</h2>
        <p>I am a high school student based in Lubbock, Texas with a passion for Full-Stack development,
            Machine Learning, Ai-Human interactions, and everything in between.</p>
    </div>

    <div id="Contact-Me">
        <a href = "mailto: azmayen.murshid@gmail.com" >Contact Me</a>
    </div>
</body>
<footer>
    <svg width="100%" height="100%" id="svgWaves" viewBox="0 0 1440 500" xmlns="http://www.w3.org/2000/svg"
        class="transition duration-300 ease-in-out delay-150">
        <style>
            .path-0 {
                animation: pathAnim-0 4s;
                animation-timing-function: linear;
                animation-iteration-count: infinite;
            }

            @keyframes pathAnim-0 {
                0% {
                    d: path("M 0,500 C 0,500 0,250 0,250 C 60.36211340206185,249.52945508100146 120.7242268041237,249.05891016200295 184,242 C 247.2757731958763,234.94108983799705 313.465206185567,221.2938144329897 375,233 C 436.534793814433,244.7061855670103 493.4149484536083,281.7658321060383 539,299 C 584.5850515463917,316.2341678939617 618.875,313.64285714285717 690,317 C 761.125,320.35714285714283 869.0850515463917,329.6627393225331 931,306 C 992.9149484536083,282.3372606774669 1008.784793814433,225.7061855670103 1062,224 C 1115.215206185567,222.2938144329897 1205.7757731958766,275.51251840942564 1275,289 C 1344.2242268041234,302.48748159057436 1392.1121134020618,276.2437407952872 1440,250 C 1440,250 1440,500 1440,500 Z");
                }

                25% {
                    d: path("M 0,500 C 0,500 0,250 0,250 C 47.09849042709867,209.1529823269514 94.19698085419734,168.30596465390278 165,158 C 235.80301914580266,147.69403534609722 330.3105670103093,167.9291237113402 393,173 C 455.6894329896907,178.0708762886598 486.5607511045656,167.9775405007364 528,173 C 569.4392488954344,178.0224594992636 621.4464285714287,198.16071428571425 692,224 C 762.5535714285713,249.83928571428575 851.65353460972,281.3796023564065 909,286 C 966.34646539028,290.6203976435935 991.9394329896909,268.32087628865975 1054,275 C 1116.0605670103091,281.67912371134025 1214.5887334315169,317.3368924889544 1285,318 C 1355.4112665684831,318.6631075110456 1397.7056332842417,284.3315537555228 1440,250 C 1440,250 1440,500 1440,500 Z");
                }

                50% {
                    d: path("M 0,500 C 0,500 0,250 0,250 C 70.51675257731958,288.55283505154637 141.03350515463916,327.1056701030928 206,295 C 270.96649484536084,262.8943298969072 330.3827319587629,160.13015463917526 387,173 C 443.6172680412371,185.86984536082474 497.43556701030934,314.37371134020617 552,335 C 606.5644329896907,355.62628865979383 661.875,268.375 722,225 C 782.125,181.62500000000003 847.0644329896907,182.12628865979386 912,213 C 976.9355670103093,243.87371134020614 1041.8672680412371,305.11984536082474 1104,310 C 1166.1327319587629,314.88015463917526 1225.466494845361,263.3943298969072 1281,244 C 1336.533505154639,224.6056701030928 1388.2667525773195,237.3028350515464 1440,250 C 1440,250 1440,500 1440,500 Z");
                }

                75% {
                    d: path("M 0,500 C 0,500 0,250 0,250 C 74.87518409425626,264.84628129602356 149.7503681885125,279.6925625920471 202,280 C 254.2496318114875,280.3074374079529 283.87371134020617,266.07603092783506 327,282 C 370.12628865979383,297.92396907216494 426.7547864506628,344.0033136966127 508,317 C 589.2452135493372,289.9966863033873 695.1071428571428,189.91071428571428 751,156 C 806.8928571428572,122.08928571428571 812.8166421207659,154.3538291605302 872,198 C 931.1833578792341,241.6461708394698 1043.6262886597938,296.673969072165 1109,282 C 1174.3737113402062,267.326030927835 1192.678203240059,182.95029455081 1240,166 C 1287.321796759941,149.04970544919 1363.6608983799706,199.524852724595 1440,250 C 1440,250 1440,500 1440,500 Z");
                }

                100% {
                    d: path("M 0,500 C 0,500 0,250 0,250 C 60.36211340206185,249.52945508100146 120.7242268041237,249.05891016200295 184,242 C 247.2757731958763,234.94108983799705 313.465206185567,221.2938144329897 375,233 C 436.534793814433,244.7061855670103 493.4149484536083,281.7658321060383 539,299 C 584.5850515463917,316.2341678939617 618.875,313.64285714285717 690,317 C 761.125,320.35714285714283 869.0850515463917,329.6627393225331 931,306 C 992.9149484536083,282.3372606774669 1008.784793814433,225.7061855670103 1062,224 C 1115.215206185567,222.2938144329897 1205.7757731958766,275.51251840942564 1275,289 C 1344.2242268041234,302.48748159057436 1392.1121134020618,276.2437407952872 1440,250 C 1440,250 1440,500 1440,500 Z");
                }
            }
        </style>
        <defs>
            <linearGradient id="gradient" x1="50%" y1="100%" x2="50%" y2="0%">
                <stop offset="5%" stop-color="#6b9fedff"></stop>
                <stop offset="95%" stop-color="#24f9f9ff"></stop>
            </linearGradient>
        </defs>
        <path
            d="M 0,500 C 0,500 0,250 0,250 C 60.36211340206185,249.52945508100146 120.7242268041237,249.05891016200295 184,242 C 247.2757731958763,234.94108983799705 313.465206185567,221.2938144329897 375,233 C 436.534793814433,244.7061855670103 493.4149484536083,281.7658321060383 539,299 C 584.5850515463917,316.2341678939617 618.875,313.64285714285717 690,317 C 761.125,320.35714285714283 869.0850515463917,329.6627393225331 931,306 C 992.9149484536083,282.3372606774669 1008.784793814433,225.7061855670103 1062,224 C 1115.215206185567,222.2938144329897 1205.7757731958766,275.51251840942564 1275,289 C 1344.2242268041234,302.48748159057436 1392.1121134020618,276.2437407952872 1440,250 C 1440,250 1440,500 1440,500 Z"
            stroke="none" stroke-width="0" fill="url(#gradient)"
            class="transition-all duration-300 ease-in-out delay-150 path-0"></path>
    </svg>
</footer>
