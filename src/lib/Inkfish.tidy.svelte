<!-- Tidy styles but but loses styles when pasted into email client -->
<script>
  export let name
  export let title
  export let phone
</script>

<table border="0">
  <tr>
    <td id="logo" rowspan="6">
      <img alt="" src="https://files.ink.fish/sigmaker/if.png" />
    </td>
    <td id="name">
      <strong style="font-size: 1rem;">{name}</strong>
    </td>
  </tr>
  <tr>
    <td id="title">
      <em>{title}</em>
    </td>
  </tr>
  <tr>
    <td id="phone">{phone}</td>
  </tr>
  <tr>
    <td id="company"
      ><strong>Inkfish</strong> |
      <a id="url" href="https://www.ink.fish">www.ink.fish</a>
    </td>
  </tr>
  <tr><td id="tagline">Deeply curious</td></tr>
  <tr>
    <td id="social">
      <a href="https://instagram.com/inkfishexpeditions">
        <img alt="" src="https://files.ink.fish/sigmaker/ig.png" /></a>
      <a href="https://www.facebook.com/InkfishExpeditions/">
        <img alt="" src="https://files.ink.fish/sigmaker/fb.png" /></a>
      <a href="https://www.linkedin.com/company/inkfishexpeditions/">
        <img alt="" src="https://files.ink.fish/sigmaker/li.png" /></a>
      <a href="https://www.youtube.com/channel/UCmFIo3uaPeYxfqLNMVxtL5w">
        <img alt="" src="https://files.ink.fish/sigmaker/yt.png" /></a>
    </td>
  </tr>
</table>

<style>
  /* light blue: #8EA5C7, blue: #244b91, dark purple: #0c0732 */
  :root {
    --lightBlue: #8ea5c7;
    --blue: #244b91;
    --darkPurple: #0c0732;
  }
  table {
    margin: 0;
    padding: 0;
    color: var(--darkPurple);
    font-family: Helvetica, Arial, sans-serif;
    font-size: 0.8em;
  }
  a,
  a:link,
  a:visited {
    text-decoration: none;
    color: var(--darkPurple);
  }
  a:hover {
    color: var(--blue);
  }
  #logo {
    padding-right: 1.8rem;
    border-right: 1px solid var(--lightBlue);
    text-align: center;
  }
  #name,
  #title,
  #phone,
  #company,
  #tagline,
  #social {
    padding-left: 2rem;
  }
  #phone {
    color: var(--darkPurple);
    text-decoration: none;
  }
  #tagline {
    color: var(--blue);
  }
  #social img {
    padding-right: 2px;
  }
</style>
