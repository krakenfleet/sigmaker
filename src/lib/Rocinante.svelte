<script context="module">
  // images must load remotely to be reliable
  export const imagesBaseUrl = 'https://files.ink.fish/sigmaker'
  export const fonts =
    'font-size: medium; font-family: Helvetica, Arial, sans-serif;'
</script>

<script>
  export let name
  export let title
  export let phone

  const logoUrl = imagesBaseUrl + '/rocinante.png'
  const yachtUrl = imagesBaseUrl + '/yacht.jpg'
</script>

<table>
  <tr
    ><td colspan="2">
      <b><i>{name}</i></b><br />
      {title}<br />
      <img src={logoUrl} alt="Rocinante Logo" /><br />
      purser@yacht-rocinante.com
    </td>
  </tr>
  <tr><td>Mobile:</td> <td>{phone}</td></tr>
  <tr><td>VoIP:</td> <td>+1 954 672 6594</td></tr>
  <tr><td>VoIP:</td> <td>+1 954 672 6595</td></tr>
  <tr><td colspan="2"><img src={yachtUrl} alt="Yacht Logo" /></td></tr>
</table>

<style>
  /* Must use inline styles with email. */
</style>
