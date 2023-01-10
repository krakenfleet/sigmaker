<script context="module">
  // images MUST load remotely to be reliable
  export const imagesBaseUrl = 'https://files.ink.fish/sigmaker'
</script>

<script>
  export let email
  export let phone
  export let name
  export let title

  const logoUrl = imagesBaseUrl + '/rocinante/rocinante.png'
  const yachtUrl = imagesBaseUrl + '/rocinante/yacht.jpg'
</script>

<table>
  <tr
    ><td colspan="2" style="padding-bottom: .3rem;">
      <b><i>{name}</i></b><br />
      {title}<br />
      <img style="margin: .3rem 0;" src={logoUrl} alt="" /><br />
      <i>{email}</i>
    </td>
  </tr>
  <tr><td>Mobile:</td> <td>{phone}</td></tr>
  <tr><td>VoIP:</td> <td>+1 954 672 6594</td></tr>
  <tr><td>VoIP:</td> <td>+1 954 672 6595</td></tr>
  <tr><td colspan="2"><img src={yachtUrl} alt="" /></td></tr>
</table>

<style>
  /* Must use inline styles with email. */
</style>
