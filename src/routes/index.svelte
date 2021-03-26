<script>
  import Card from "../components/Card.svelte";
  import Image from "svelte-image";
</script>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<div class="container">
  <Card>
    <p>
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
          Inzidenz, Impffortschritt, Fallzahlen und mehr …
        </span>
      </h1>

      <p><small>Ohne Download und Installation…</small></p>
      <div>
        <a class="btn cta" href="https://corona-ampel.netlify.app/#/">
          Jetzt starten ›
        </a>
      </div>

      <p><small>Bald auch auf: Windows, MacOS, Linux</small></p>
    </div>
    <div class="column desktop-right">
      <div class="device">
        <img width="200" src="mockup.png" alt="Borat" />
      </div>
    </div>
  </div>
</div>

<div class="bg-lighter">
  <div class="container">
    <h1>dskfaslkjdhfaslkjfh</h1>
  </div>
</div>

<style>
  h1 {
    display: block;
    padding: 0 0 1rem;
    font-size: 2.5em;
  }
  .fat {
    display: block;
    margin-bottom: 1rem;
  }
  .light {
    display: block;
    font-weight: 200;
    font-size: 0.8em;
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
      padding: 3rem;
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
    padding: 0.5rem 2rem;
    font-size: 1.5rem;
    font-weight: 500;
    border-radius: var(--border-radius);
    text-transform: uppercase;
    margin-top: 0.75rem;
    margin-bottom: 1rem;
  }

  .device {
    perspective: 10px;
    opacity: 0;
    animation: fadeDeviceIn 2s 1s ease-out forwards;
      top: 100px;
  }

  .bg-lighter {
    background-color: var(--bg-200);
  }

  @media (min-width: 768px) {
    .device {
      position: relative;
    }
    .desktop-wrapper {
      flex-flow: row;
    }
    .column {
      text-align: left;
    }
  }
  @keyframes fadeDeviceIn {
    from {
      opacity: 0;
      transform: scale(1) rotate3d(1, 1, 1, 60deg) translate3d(0, 50%, 0);
    }
    to {
      opacity: 1;
      transform: scale(1.4) translate3d(0, 0%, 0);
    }
  }
</style>
