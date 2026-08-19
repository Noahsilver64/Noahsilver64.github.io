<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>The World of Noah Silver</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=DM+Mono&family=Pacifico&display=swap" rel="stylesheet">

<style>

/* =========================================================
   BASE
========================================================= */

* {
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    margin: 0;

    background: #f4e3a6;
    color: #40251c;

    font-family: "DM Mono", monospace;
}


/* =========================================================
   LANDING PAGE
========================================================= */

.landing {
    height: 100vh;
    min-height: 650px;

    position: relative;
    overflow: hidden;

    background: #f4d56a;

    display: flex;
    justify-content: center;
    align-items: center;

    text-align: center;
}


/* =========================================================
   SUN
========================================================= */

.sun {
    position: absolute;

    width: 430px;
    height: 430px;

    border-radius: 50%;

    background: #f58232;

    top: 50%;
    left: 50%;

    transform: translate(-50%, -57%);

    overflow: hidden;

    z-index: 1;
}


/*
    The stripes are deliberately NOT a gradient.
    They give the sun that old 70s printed-ad look.
*/

.sun::before,
.sun::after {
    content: "";

    position: absolute;

    left: 0;
    width: 100%;

    background: #f4d56a;
}

.sun::before {
    height: 9px;
    bottom: 145px;

    box-shadow:
        0 22px #f4d56a,
        0 44px #f4d56a,
        0 66px #f4d56a,
        0 88px #f4d56a,
        0 110px #f4d56a;
}


/* =========================================================
   MOUNTAINS
========================================================= */

.mountains {
    position: absolute;

    bottom: 0;
    left: 0;

    width: 100%;
    height: 240px;

    background: #613326;

    clip-path: polygon(
        0 100%,
        0 75%,
        12% 58%,
        20% 73%,
        34% 37%,
        46% 67%,
        60% 43%,
        72% 72%,
        86% 47%,
        100% 69%,
        100% 100%
    );

    z-index: 2;
}


.mountains::after {
    content: "";

    position: absolute;

    bottom: 0;
    left: 0;

    width: 100%;
    height: 55px;

    background: #40251c;
}


/* =========================================================
   TITLE
========================================================= */

.landing-content {
    position: relative;

    z-index: 5;

    margin-top: -80px;
}


.small-title {
    font-family: "Pacifico", cursive;

    font-size: 28px;

    color: #613326;

    transform: rotate(-3deg);

    margin-bottom: 5px;
}


.main-title {
    margin: 0;

    font-family: "Archivo Black", sans-serif;

    font-size: clamp(55px, 8vw, 105px);

    line-height: .9;

    letter-spacing: -5px;

    color: #fff1bb;

    text-shadow:
        7px 7px 0 #613326;
}


.subtitle {
    margin-top: 28px;

    font-size: 13px;

    letter-spacing: 4px;

    color: #40251c;
}


/* =========================================================
   SCROLL BUTTON
========================================================= */

.scroll-button {
    position: absolute;

    z-index: 10;

    bottom: 175px;
    left: 50%;

    transform: translateX(-50%);

    text-decoration: none;

    color: #fff1bb;

    background: #40251c;

    padding: 13px 25px;

    font-size: 12px;

    letter-spacing: 3px;

    border: 3px solid #fff1bb;

    transition: transform .25s;
}

.scroll-button:hover {
    transform:
        translateX(-50%)
        translateY(-5px);
}


/* =========================================================
   NAVIGATION
========================================================= */

nav {
    position: sticky;

    top: 0;

    z-index: 100;

    background: #40251c;

    display: flex;

    justify-content: center;

    gap: 45px;

    padding: 18px;
}

nav a {
    color: #f4e3a6;

    text-decoration: none;

    font-size: 12px;

    letter-spacing: 2px;
}

nav a:hover {
    color: #f58232;
}


/* =========================================================
   GENERAL SECTIONS
========================================================= */

.section {
    padding: 100px 8%;

    max-width: 1200px;

    margin: auto;
}

.section-title {
    text-align: center;

    font-family: "Archivo Black", sans-serif;

    font-size: 52px;

    color: #d94f25;

    text-shadow: 4px 4px 0 #40251c;

    margin-bottom: 60px;
}


/* =========================================================
   PROJECTS
========================================================= */

.project-grid {
    display: grid;

    grid-template-columns:
        repeat(2, 1fr);

    gap: 30px;
}

.card {
    background: #fff1bb;

    border: 4px solid #40251c;

    padding: 30px;

    box-shadow:
        9px 9px 0 #d94f25;

    transition: .2s;
}

.card:hover {
    transform:
        translate(-4px, -4px);
}

.card h3 {
    margin-top: 0;

    font-family: "Archivo Black", sans-serif;

    color: #d94f25;

    font-size: 27px;
}

.card p {
    line-height: 1.8;

    font-size: 14px;
}

.card-date {
    font-size: 11px;

    letter-spacing: 2px;

    opacity: .7;
}


/* =========================================================
   NOTES / ANNOUNCEMENTS
========================================================= */

.notes {
    max-width: 850px;

    margin: auto;
}

.note {
    border-top: 4px solid #40251c;

    padding: 25px 0;
}

.note:last-child {
    border-bottom: 4px solid #40251c;
}

.note h3 {
    font-family: "Archivo Black", sans-serif;

    color: #d94f25;

    margin-bottom: 5px;
}

.note p {
    line-height: 1.9;

    font-size: 14px;
}


/* =========================================================
   MEDIA
========================================================= */

.media-grid {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 25px;
}

.media-item {
    aspect-ratio: 1 / 1;

    background: #613326;

    color: #f4e3a6;

    display: flex;

    justify-content: center;
    align-items: center;

    text-align: center;

    border: 4px solid #40251c;

    font-family: "Archivo Black", sans-serif;

    font-size: 20px;

    transition: .2s
}

.media-item:hover {
            transform: translate(-4px, -4px);
        }


/* =========================================================
   FOOTER
========================================================= */

footer {
    background: #40251c;

    color: #f4e3a6;

    text-align: center;

    padding: 60px 20px;

    font-size: 12px;
}


/* =========================================================
   MOBILE
========================================================= */

@media(max-width: 750px) {

    .sun {
        width: 320px;
        height: 320px;
    }

    .main-title {
        letter-spacing: -3px;
    }

    nav {
        gap: 15px;
    }

    .project-grid,
    .media-grid {
        grid-template-columns: 1fr;
    }

}

</style>
</head>


<body>


<!-- =======================================================
     LANDING
======================================================= -->

<section class="landing" id="top">

    <div class="sun"></div>

    <div class="mountains"></div>


    <div class="landing-content">

        <div class="small-title">
            Welcome to
        </div>

        <h1 class="main-title">
            NOAH'S<br>
            CORNER
        </h1>

    

    </div>


    <a href="#home" class="scroll-button">
        ENTER THE CORNER ↓
    </a>

</section>


<!-- =======================================================
     NAV
======================================================= -->

<nav>

    <a href="#home">HOME</a>

    <a href="#projects">PROJECTS</a>

    <a href="#notes">NOTES</a>

    <a href="#media">MEDIA</a>

</nav>


<!-- =======================================================
     HOME
======================================================= -->

<section class="section" id="home">

    <h2 class="section-title">
        WELCOME
    </h2>

    <div style="text-align:center; max-width:750px; margin:auto; line-height:2;">

        <p>
            This is my very own corner of the internet.
        </p>

        <p>
            Here you'll find the things I'm working on,
            things I've made, things I'm thinking about,
            and lots of other things.
        </p>

    </div>

</section>


<!-- =======================================================
     PROJECTS
======================================================= -->

<section class="section" id="projects">

    <h2 class="section-title">
        PROJECTS
    </h2>


    <div class="project-grid">


        <article class="card">

            <div class="card-date">
                PROJECT / 001
            </div>

            <h3>
                Reaching High
            </h3>

            <p>
                A synthpop song I'm writing. 
                Here you can see the most recent version!
            </p>

            <a href="#">
                VIEW PROJECT →
            </a>

        </article>


        <article class="card">

            <div class="card-date">
                PROJECT / 002
            </div>

            <h3>
                TBD
            </h3>

            <p>
                TBD
            </p>

            <a href="#">
                VIEW PROJECT →
            </a>

        </article>


    </div>

</section>


<!-- =======================================================
     NOTES
======================================================= -->

<section class="section" id="notes">

    <h2 class="section-title">
        NOTES
    </h2>


    <div class="notes">


        <article class="note">

            <div class="card-date">
                AUGUST 18, 2026, 11:13 PM AKST
            </div>

            <h3>
                Welcome to the site
            </h3>

            <p>
                Hopefully I'll be able to update these without coding them
                manually soon :sob:
            </p>

        </article>


        <article class="note">

            <div class="card-date">
                AUGUST 18, 2026, 11:04
            </div>

            <h3>
                First Note!
            </h3>

            <p>
                The note system now exists.
                Entirely manually coded.
                Thank you ChatGPT for helping code this cool
                design but WHY didn't I decide to make
                these automatically posted??
            </p>

        </article>


    </div>

</section>


<!-- =======================================================
     MEDIA
======================================================= -->

<section class="section" id="media">

    <h2 class="section-title">
        MEDIA
    </h2>


    <div class="media-grid">

        <div class="media-item">
            PHOTOGRAPHS
        </div>

        <div class="media-item">
            MUSIC
        </div>

        <div class="media-item">
            VIDEOS
        </div>

    </div>

</section>


<!-- =======================================================
     FOOTER
======================================================= -->

<footer>

    THE WORLD OF NOAH

    <br><br>

    © 2026 — ALL RIGHTS RESERVED

</footer>


</body>
</html>
