
<script>
    import { onMount } from 'svelte';
  
    let e1 = '***';
    let e2 = '@';
    let e3 = '***.';
    let addi = `${e1}${e2}${e3}app`;
  
    let vn = '*****';
    let nn = '********';
    let adrs = '******';
    let adrp = '*****';
    let adrst = '******';
  
    let d = {};
  
    function handleClick() {
      e1 = d.e1;
      e3 = d.e3;
      addi = `${e1}${e2}${e3}app`;
      vn = d.adrv;
      nn = d.adrn;
      adrs = d.adrs;
      adrp = d.adrp;
      adrst = d.adrst;
    }
    onMount(async () => {
      d = await fetch('./impr.json').then((res) => res.json());
    });
  </script>
  
  <svelte:head>
    <title>Impressum - Corona-Ampel</title>
  </svelte:head>
  

<div class="container">
  <h1>Datenschutz - Corona-Ampel Website &amp; Inzidenz-Ampel App</h1>
  <p>
    Die Nutzung unserer Webseite/App ist in der Regel ohne Angabe
    personenbezogener Daten möglich. Nur teile der IP Adresse, niemals die
    komplette IP-Adresse wird zu Trackingzwecken gebraucht. Soweit auf unseren
    Seiten personenbezogene Daten (beispielsweise Name, Anschrift oder
    eMail-Adressen) erhoben werden, erfolgt dies, soweit möglich, stets auf
    freiwilliger Basis. Diese Daten werden ohne Ihre ausdrückliche Zustimmung
    nicht an Dritte weitergegeben. Wir weisen darauf hin, dass die
    Datenübertragung im Internet (z.B. bei der Kommunikation per E-Mail)
    Sicherheitslücken aufweisen kann. Ein lückenloser Schutz der Daten vor dem
    Zugriff durch Dritte ist nicht möglich. Der Nutzung von im Rahmen der
    Impressumspflicht veröffentlichten Kontaktdaten durch Dritte zur Übersendung
    von nicht ausdrücklich angeforderter Werbung und Informationsmaterialien
    wird hiermit ausdrücklich widersprochen. Die Betreiber der Seiten behalten
    sich ausdrücklich rechtliche Schritte im Falle der unverlangten Zusendung
    von Werbeinformationen, etwa durch Spam-Mails, vor.
  </p>
  <p>
    Wir verwenden keine Cookies, mit denen der Benutzer identifiziert werden
    könnte. Wir verwenden auch keine anderen Tracking-Technologien wie Pixel
    oder Fingerabdrücke.
  </p>
  <h2>Wie speichern wir Ihre persönlichen Daten</h2>
  <ul>
    <li>IP-Adresse mit verschleiertem letzten Oktett</li>
    <li>
      User Agent ohne eindeutige und möglicherweise identifizierbare Teile
    </li>
    <li>
      Nur App: Favorisierte Liste der Landkreise wird anonym, nur auf dem Gerät
      gespeichert
    </li>
    <li>
      Ein Standort kann auf klick ermittelt werden, wird aber nie gespeichert
    </li>
  </ul>
  <h2>Nutzung von Diensten Dritter</h2>
  <p>
    Google Admob Die kostenlose Version der App benutzt den Dienst Google Admob,
    um Werbeanzeigen einzublenden. Anzeigen werden basierend auf dem von Ihnen
    verwendeten Gerät personalisiert.
  </p>
  <p>
    Auf Geräten mit dem Betriebssystem iOS wird die Werbe-ID von Apple
    verwendet. Weitere Informationen zum Anzeigen-Tracking mithilfe dieser
    Werbe-ID finden Sie auf Ihrem Gerät in der App "Einstellungen".
  </p>
  <p>
    Der Google Admob Dienst wird von der Firma Google (Google Inc., 1600
    Amphitheatre Parkway Mountain View, CA 94043, USA) bereitgestellt. Google
    ist unter dem Privacy-Shield-Abkommen zertifiziert und bietet hierdurch eine
    Garantie, das europäische Datenschutzrecht einzuhalten (<a
      href="https://www.privacyshield.gov/participant?id=a2zt000000001L5AAI&amp;status=Active"
      >https://www.privacyshield.gov/participant?id=a2zt000000001L5AAI&amp;status=Active</a
    >).
  </p>
  <p>
    Allgemeine Informationen zum Umgang mit Nutzerdaten finden Sie in der
    Datenschutzerklärung von Google: &nbsp;<a
      href="https://www.privacyshield.gov/participant?id=a2zt000000001L5AAI&amp;status=Active"
      >https://www.google.de/intl/de/policies/privacy/</a
    >
  </p>
  <h2>Änderung der Datenschutzerklärung</h2>
  <p>
    Im Zuge der Weiterentwicklung der App und der Implementierung neuer
    Funktionen können Änderungen dieser Datenschutzerklärung erforderlich
    werden. Daher empfehlen wir Ihnen, sich diese Datenschutzerklärung
    regelmäßig durchzulesen.
  </p>

<div class="impressum">
    <h1>Impressum</h1>
  
    <div>Hinweis:</div>
    <ul>
      <li>Absolut keine Daten werden weitergegeben</li>
      <li>Es werden keine Cookies gespeichert</li>
    </ul>
  
    <p>
      <small><strong>Hinweis:</strong>
        Spenden sind in diesem Fall Schenkungen da ich eine Privatperson bin.</small>
    </p>

    <p>Angaben gemäß § 5 TMG</p>
    <p>{vn} {nn} <br /> {adrs}<br /> {adrp} {adrst} <br /></p>
    <p><strong>Vertreten durch: </strong><br /> {vn} {nn}<br /></p>
    <p><strong>Kontakt:</strong> <br /> E-Mail: <span class="email">{addi}</span> <br /></p>
    <p>
      <strong>Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV:</strong><br />
      {vn}
      {nn}
      <br />
      {adrs}<br />
      {adrp}
      {adrst}
      <br />
    </p>
    <p><button on:click="{handleClick}">Daten im Klartext anzeigen</button></p>
    <small>
      <p>
        <strong>Haftungsausschluss: </strong>
        <br />
        <br /><strong>Haftung für Inhalte</strong>
        <br />
        <br />
        Die Inhalte unserer Seiten wurden mit größter Sorgfalt erstellt. Für die Richtigkeit,
        Vollständigkeit und Aktualität der Inhalte können wir jedoch keine Gewähr übernehmen. Als
        Diensteanbieter sind wir gemäß § 7 Abs.1 TMG für eigene Inhalte auf diesen Seiten nach den
        allgemeinen Gesetzen verantwortlich. Nach §§ 8 bis 10 TMG sind wir als Diensteanbieter jedoch
        nicht verpflichtet, übermittelte oder gespeicherte fremde Informationen zu überwachen oder
        nach Umständen zu forschen, die auf eine rechtswidrige Tätigkeit hinweisen. Verpflichtungen
        zur Entfernung oder Sperrung der Nutzung von Informationen nach den allgemeinen Gesetzen
        bleiben hiervon unberührt. Eine diesbezügliche Haftung ist jedoch erst ab dem Zeitpunkt der
        Kenntnis einer konkreten Rechtsverletzung möglich. Bei Bekanntwerden von entsprechenden
        Rechtsverletzungen werden wir diese Inhalte umgehend entfernen.<br />
        <br />
        <strong>Haftung für Links</strong><br />
        <br />
  
        Unser Angebot enthält Links zu externen Webseiten Dritter, auf deren Inhalte wir keinen
        Einfluss haben. Deshalb können wir für diese fremden Inhalte auch keine Gewähr übernehmen. Für
        die Inhalte der verlinkten Seiten ist stets der jeweilige Anbieter oder Betreiber der Seiten
        verantwortlich. Die verlinkten Seiten wurden zum Zeitpunkt der Verlinkung auf mögliche
        Rechtsverstöße überprüft. Rechtswidrige Inhalte waren zum Zeitpunkt der Verlinkung nicht
        erkennbar. Eine permanente inhaltliche Kontrolle der verlinkten Seiten ist jedoch ohne
        konkrete Anhaltspunkte einer Rechtsverletzung nicht zumutbar. Bei Bekanntwerden von
        Rechtsverletzungen werden wir derartige Links umgehend entfernen.<br />
        <br />
        <strong>Urheberrecht</strong><br />
        <br />
  
        Die durch die Seitenbetreiber erstellten Inhalte und Werke auf diesen Seiten unterliegen dem
        deutschen Urheberrecht. Die Vervielfältigung, Bearbeitung, Verbreitung und jede Art der
        Verwertung außerhalb der Grenzen des Urheberrechtes bedürfen der schriftlichen Zustimmung des
        jeweiligen Autors bzw. Erstellers. Downloads und Kopien dieser Seite sind nur für den
        privaten, nicht kommerziellen Gebrauch gestattet. Soweit die Inhalte auf dieser Seite nicht
        vom Betreiber erstellt wurden, werden die Urheberrechte Dritter beachtet. Insbesondere werden
        Inhalte Dritter als solche gekennzeichnet. Sollten Sie trotzdem auf eine
        Urheberrechtsverletzung aufmerksam werden, bitten wir um einen entsprechenden Hinweis. Bei
        Bekanntwerden von Rechtsverletzungen werden wir derartige Inhalte umgehend entfernen.<br />
        <br />
        <strong>Datenschutz</strong><br />
        <br />
  
        Die Nutzung unserer Webseite ist in der Regel ohne Angabe personenbezogener Daten möglich.
        Soweit auf unseren Seiten personenbezogene Daten (beispielsweise Name, Anschrift oder
        eMail-Adressen) erhoben werden, erfolgt dies, soweit möglich, stets auf freiwilliger Basis.
        Diese Daten werden ohne Ihre ausdrückliche Zustimmung nicht an Dritte weitergegeben.
        <br />
  
        Wir weisen darauf hin, dass die Datenübertragung im Internet (z.B. bei der Kommunikation per
        E-Mail) Sicherheitslücken aufweisen kann. Ein lückenloser Schutz der Daten vor dem Zugriff
        durch Dritte ist nicht möglich.
        <br />
  
        Der Nutzung von im Rahmen der Impressumspflicht veröffentlichten Kontaktdaten durch Dritte zur
        Übersendung von nicht ausdrücklich angeforderter Werbung und Informationsmaterialien wird
        hiermit ausdrücklich widersprochen. Die Betreiber der Seiten behalten sich ausdrücklich
        rechtliche Schritte im Falle der unverlangten Zusendung von Werbeinformationen, etwa durch
        Spam-Mails, vor.<br />
      </p>
    </small>
  </div>
  
</div>
