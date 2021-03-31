<script>
  import Card from "../components/Card.svelte";
  import Image from "svelte-image";
import Osoveriew from "../components/Osoveriew.svelte";
</script>

<svelte:head>
  <title
    >Corona-Ampel - Fallzahlen, Impfstatistik, Intensivstation und vieles mehr</title
  >
</svelte:head>

<div class="container">
  <Card>
    <p class="fundingtext">
      <small>
        Damit diese App weiterhin kostenlos, ohne Werbung und ohne
        Datenweitergabe an Dritte bleibt, erwäge bitte eine Spende. Vielen Dank!
        <!-- Ich habe mehrere Monate diese App programmiert. Sie
          ist kostenlos, ohne Werbung, keine Cookies, keine Daten werden
          weitergegeben, alles ist Self-Hosted. Viel Liebe, Schweiss und Tränen
          sind hier reingeflossen… eine kleine Spende wäre deshalb echt toll! -->
      </small>
    </p>
  </Card>

  <div class="desktop-wrapper">
    <div class="column desktop-left">
      <h1>
        <span class="fat">Corona-Ampel</span>
        <span class="light">
          Inzidenz, Impffortschritt, Fallzahlen und mehr&nbsp;…
        </span>
      </h1>

      <p><small>Ohne Download und Installation&nbsp;…</small></p>
      <div>
        <a class="btn cta" href="https://start.corona-ampel.app/">
          Jetzt starten ›
        </a>
      </div>

      <p><small><a href="#download">Bald auch auf: Windows, MacOS, Linux</a></small></p>
    </div>
    <div class="column desktop-right">
      <div class="device">
        <img width="200" src="mockup.png" alt="Borat" />
      </div>
    </div>
  </div>
</div>

<div class="bg-lighter">
  <div class="spacer" />
  <div class="container fadein">
    <div class="second">
      <h2>
        <div class="fat">Mehr als nur Inzidenz!</div>
        <div class="light">
          Fallzahlen, Impfstatistik, Intensivstationbelegung ...
        </div>
      </h2>


        <picture>
          <source media="(min-width: 800px)" srcset="mockups.png" sizes="100vw"/>
          <source media="(min-width: 300px)" srcset="mockups_low.png" sizes="100vw"/>
          <source srcset="mockups_low.png" sizes="100vw"/>
          <img src="mockups_low.png" loading="lazy" alt="Screenshots der App"/>
        </picture>
    </div>
  </div>
</div>

<div id="download">
  <div class="container">
    <div class="spacer" />
    <Osoveriew />
    <div class="spacer" />
  </div>
</div>

<!-- <div>
  
  <script src='https://storage.ko-fi.com/cdn/scripts/overlay-widget.js' ✂prettier:content✂="" ✂prettier:content✂="e30=">{}</script>
  <script ✂prettier:content✂="CiAgICBrb2ZpV2lkZ2V0T3ZlcmxheS5kcmF3KCdjb3JvbmFhbXBlbCcsIHsKICAgICAgJ3R5cGUnOiAnZmxvYXRpbmctY2hhdCcsCiAgICAgICdmbG9hdGluZy1jaGF0LmRvbmF0ZUJ1dHRvbi50ZXh0JzogJ1NQRU5ERU4nLAogICAgICAnZmxvYXRpbmctY2hhdC5kb25hdGVCdXR0b24uYmFja2dyb3VuZC1jb2xvcic6ICcjZmZmZmZmJywKICAgICdmbG9hdGluZy1jaGF0LmRvbmF0ZUJ1dHRvbi50ZXh0LWNvbG9yJzogJyMzMjM4NDInCiAgICB9KTsKICA=" ✂prettier:content✂="e30=">{}</script>

</div> -->
<style>
  h1 {
    display: block;
    padding: 0 0 1rem;
    font-size: 2.5em;
  }
  h2 {
    font-size: 2em;
  }
  .fat {
    display: block;
    margin-bottom: 1rem;
  }
  .light {
    display: block;
    font-weight: 200;
    font-size: 0.75em;
    /* line-height: .8em; */
  }

  .desktop-wrapper {
    display: flex;
    flex-flow: column;
  }
  .column {
    display: flex;
    flex-flow: column;
    justify-content: center;
    flex-basis: 1;
    flex: 1;
    text-align: center;
    padding: 3rem 0;
  }
  .desktop-left {
    animation: fadeInBuehne 1s 0.5s ease-out forwards;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    will-change: transform;
  }
  .desktop-right {
    align-items: center;
  }
  .cta {
    display: inline-block;
    /* --focus-ring-color: var(--info-contrast); */
    background-color: var(--info-bg);
    color: var(--info-contrast);
    text-align: center;
    text-decoration: none;
    padding: 1rem 2rem;
    font-size: 1.5rem;
    font-weight: 500;
    border-radius: var(--border-radius-btn);
    text-transform: uppercase;
    margin-top: 0.75rem;
    margin-bottom: 1rem;
  }
  p {
    margin: 0;
  }

  .device {
    will-change: transform;
    perspective: 10px;
    opacity: 0;
    animation: fadeDeviceIn 1s 1s ease-out forwards;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    top: 100px;
  }

  .spacer {
    height: 4rem;
  }
  .second {
    padding: 2rem 1rem;
    text-align: center;
  }

  .bg-lighter {
    background-color: var(--bg-200);
  }

  .fadein {
    animation: fadeInBuehne 1s 0.5s ease-out forwards;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    animation-delay: 1.5s;
    will-change: transform;
  }

  @media (max-width: 1024px) {
    .desktop-left {
      padding-top: 0;
    }
  }

  @media (min-width: 768px) { 

    .fundingtext {
    text-align: center;
  }

  }
  @media (min-width: 1024px) {
    .device {
      position: relative;
    }
    .desktop-wrapper {
      flex-flow: row;
      font-size: 1.4em;
    }
    .column {
      text-align: left;
      padding: 3rem;
    }
  }
  @keyframes fadeDeviceIn {
    from {
      opacity: 0;
      transform: scale(1) rotate3d(1, 1, 1, 60deg) translate3d(0, 50%, 0);
    }
    to {
      opacity: 1;
      transform: scale(1.4) translate3d(0, 0, 0);
    }
  }
  @keyframes fadeInBuehne {
    from {
      opacity: 0;
      transform: translate3d(0, 10%, 0);
    }
    to {
      opacity: 1;
      transform: translate3d(0, 0, 0);
    }
  }
</style>
