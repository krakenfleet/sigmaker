<script context="module">
  // images MUST load remotely to be reliable
  export const imagesBaseUrl = 'https://files.ink.fish/sigmaker'
</script>

<script>
  export let email
  export let phone
  export let name
  export let title

  // const logoUrl = imagesBaseUrl + '/rocinante/rocinante.png'
  const yachtUrl = imagesBaseUrl + '/sportsfisher/yacht.png'
</script>

<table border="0" style="font-weight: bold;">
  <tr>
    <td colspan="2" style="padding-bottom: .3rem; color: #5856D5;">
      {name}<br />
      {title} &bullet; SF-108
    </td>
  </tr>
  <tr><td>{email}</td></tr>
  <tr><td>{phone}</td></tr>
  <tr><td><img src={yachtUrl} alt="" /></td></tr>
</table>

<style>
  /* Must use inline styles with email. */
</style>
