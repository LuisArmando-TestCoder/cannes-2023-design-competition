<main class="main">
    <header class="header">
        <img src="bamboo-logo.png" alt="Bamboo Logo">
        <nav>
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Cans</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
      </header>
    <img class="img" src="{src}" alt="">
    <div class="column">
          <main class="sections">
            <section>
                <h2>The Electric Souls</h2>
                <nav>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#music">Music</a></li>
                    <li><a href="#tour">Tour</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                </nav>
            </section>

            <section id="about">
              <h2>About The Electric Souls</h2>
              <p>The Electric Souls is a four-piece rock band from Los Angeles, California. They formed in 2015 and have been making music together ever since. Their sound is a mix of classic rock, blues, and punk, with influences ranging from The Rolling Stones and Led Zeppelin to The Stooges and The Clash.</p>
            </section>
            
            <section id="music">
              <h2>Music by The Electric Souls</h2>
              <ul>
                <li><a href="#">"Electric City"</a></li>
                <li><a href="#">"High Voltage"</a></li>
                <li><a href="#">"Rock 'n' Roll Rebellion"</a></li>
              </ul>
            </section>
            
            <section id="tour">
              <h2>The Electric Souls on Tour</h2>
              <p>The Electric Souls are currently on tour in support of their latest album, "Electric City." Check out the tour dates below:</p>
              <ul>
                <li>June 1 - Los Angeles, CA</li>
                <li>June 5 - San Francisco, CA</li>
                <li>June 10 - Portland, OR</li>
                <li>June 15 - Seattle, WA</li>
              </ul>
            </section>
          </main>
    </div>
</main>
<script>
    import { browser } from '$app/environment'

    let src;

    if (browser) {
        (function () {
            const i = new URLSearchParams(window.location.search).get('i')
            src = `p${i}.jpg`
        })()
    }
</script>
<style>
    * {
        box-sizing: border-box;
    }

    .nav-title {
        display: block;
        text-align: center;
    }

    .column {
        /* background: #fff; */
        color: white;
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        padding: 25px;
    }

    .column li {
        padding-bottom: 10px;
    }

    h1, h2 {
        margin-top: 0;
    }

    h2 {
        padding-top: 50px;
    }

    .main {
        padding: 100px clamp(0, 10vw, 200px);
        min-height: 100vh;
        background: #0e0722;
        display: grid;
        grid-gap: 25px;
    }

    .img {
        width: 100%;
        padding-top: 60px;
        /* clip-path: inset(7.5% 5% 7.5% 5%); */
    }

    a {
        color: #69b9ff;
    }

    p {
        max-width: 500px;
    }

    .header {
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        background-color: #c46361;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 1;
    }

    .header img {
        height: 40px;
        margin: 0 20px;
    }

    .header ul {
        display: flex;
        list-style: none;
        margin: 0;
        padding: 0;
    }

    .header li {
        margin: 0 10px;
    }

    .header a {
        color: #333;
        text-decoration: none;
        font-weight: bold;
        text-transform: uppercase;
    }

    .sections {
        display: grid;
        grid-template-columns: repeat(2, minmax(1fr, 400px));
    }
</style>