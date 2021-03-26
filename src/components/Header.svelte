<script>
</script>

<!-- <header>
  <div class="container">
    <div class="header">
      <a class="logo" href="/">
        <img width="260"
          wrapperClass="image-wrapper"
          alt="Logo - Corona-Ampel"
          src="site-logo.png"
        />
      </a>
    </div>
  </div>
</header> -->

<header>
  <div class="container">
    <div class="header">
      <a class="logo" href="/">
        <img width="260"
          wrapperClass="image-wrapper"
          alt="Logo - Corona-Ampel"
          src="site-logo.png"
        />
      </a>
      <a class="btn fund" href="https://ko-fi.com/coronaampel" target="_blank">
        Jetzt spenden&nbsp;❤️
      </a>

    </div>
  </div>
</header>

<style>
  header {
    position: sticky;
    top: 0;
    z-index: 100;
    background-color: var(--bg-200);
    box-shadow: var(--box-shadow);
    padding: 0.2rem;
  }
  .header {
    display: flex;
    /* justify-content: center; */
    justify-content: space-between;
    align-items: center;
    
  }
  .logo {
    width:200px;
    max-width: 50%;
  }

  .fund {
    text-decoration: none;
    font-size: 0.7em;
    padding: .75rem 1rem;
    background-color: var(--bg-400);
    font-weight: bold;
    border-radius: var(--border-radius-btn);
    text-transform: uppercase;
  }
  img {
    display: block;
    max-width: 100%;
    height: auto;
  }
</style>
