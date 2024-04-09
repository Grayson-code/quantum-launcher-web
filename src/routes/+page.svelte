<script>
  import oss from "../lib/oss.svg";
  import gplv3 from "../lib/GPLv3_Logo_filled.png";
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="true" />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap"
    rel="stylesheet"
  />
  <title>Quantum</title>
</svelte:head>

<body>
  <div id="bg">
    <div id="wrapper">
      <nav>
        <a id="nav-home" href="#home">QUANTUM</a>
        <a id="nav-oss">
          <img src={oss} alt="Open Source Initiative Logo" />
          <!-- <img
            id="gpl"
            src={gplv3}
            alt="GNU General Public License V3 Free as in Freedom"
          /> -->
        </a>
        <a id="nav-download">Download</a>
        <a id="nav-upcoming">Upcoming</a>
  
        <a id="nav-contact">Contact</a>
      </nav>
      <section id="section-introduction">intro</section>
    </div>
  </div>
  <section id="section-download">downloads</section>
  <section id="section-features">planned features</section>
  <footer></footer>
</body>

<style>
  :root {
    --border-color: rgb(6, 11, 25);
  }

  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    height: 100vh;
    background-color: black;
    color: white;
    text-decoration: none;
    font-family: "Inter", Arial;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    font-variation-settings: "slnt" 0;
    display: flex;
    flex-direction: column;
  }
  #bg {
    height: 100vh;
    background-image: url("../lib/bg.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  nav {
    display: flex;
    width: 100%;
    flex-direction: row;
    /* justify-content: center; */
    height: 116px;
    flex-basis: 116px;
    background: black;

  }
  nav > a {
    padding: 3rem 2rem;
    display: flex;
    justify-content: center;
    color: white;
    text-decoration: none;
    font-weight: bold;
    opacity: 1;
  }
  #nav-home {
    flex-basis: calc(100% / 2.4);
    justify-content: left;
    font-size: 40px;
    box-sizing: border-box;
    padding: 2rem;
  }
  #nav-download,
  #nav-upcoming,
  #nav-oss,
  #nav-contact {
    flex-grow: 1;
  }
  nav > a > img {
    box-sizing: border-box;
    max-width: 60px;
  }
  nav > #nav-oss {
    display: flex;
    border-left: none;
    align-items: center;
    gap: 1rem;
    padding-bottom: 1rem;
    padding-top: 1rem;
  }
  nav > a > #gpl {
    width: 115px;
    height: 46.5px;
    max-width: none;
  }
  #section-introduction {
    height: 100vh;
    position: relative;
    width: 100%;
  }
  #section-introduction::after {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0) 0%,
      rgba(255, 255, 255, 1) 100%
    );
    height: 40%;
  }
  #section-download {
    height: 100vh;
  }
</style>
