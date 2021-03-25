<script>
  import Card from "../components/Card.svelte";
  import Image from "svelte-image";
</script>

<svelte:head>
  <title>Sapper project template</title>
</svelte:head>

<Card>
  <p>
    <small>
      Damit diese App weiterhin kostenlos, ohne Werbung, und ohne
      Datenweitergabe an Dritte bleibt, erwäge bitte eine Spende. Danke
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
      Corona-Ampel <br />
      <span class="light">
        Inzidenz, Impffortschritt, Fallzahlen und mehr …
      </span>
    </h1>

    <p><small>Ohne Download und Installation…</small></p>
    <a class="cta" href="https://corona-ampel.netlify.app/#/">
      Jetzt starten ›
    </a>

    <p><small>Bald auch auf: X X X</small></p>
  </div>
  <div class="column desktop-right">
    <div>
		<img src="great-success.png" alt="Borat" width="320">

    </div>
  </div>
</div>

<p>
  <strong
    >Try editing this file (src/routes/index.svelte) to test live reloading.</strong
  >
</p>

<style>
  h1 {
    display: block;
    padding: 0 0 1rem;
  }
  .light {
    font-weight: 200;
  }

  .desktop-wrapper {
    display: flex;
    flex-flow: column;
  }
  .column {
	  flex-basis:1;
	  flex:1;
    text-align: center;
  }
  .desktop-left {
    display: block;
    padding: 2rem 0;
  }
  .cta {
    display: inline-block;
    /* --focus-ring-color: var(--info-contrast); */
    background-color: var(--info-bg);
    color: var(--info-contrast);
    text-align: center;
    text-decoration: none;
    padding: 0.5rem 1rem;
    font-size: 1.5rem;
    font-weight: bold;
    border-radius: var(--border-radius);
    text-transform: uppercase;
	margin-top: 0.75rem;
	margin-bottom: 1rem;
  }
  @media (min-width: 768px) {
    .desktop-wrapper {
      flex-flow: row;
    }
	.column {
	  padding: 2rem;
      text-align: left;
  }
  }

</style>
