<script>
  export let name
  export let title
  export let phone
  const baseUrl = 'https://files.ink.fish/sigmaker'
</script>

<!-- Inline styles required for pasting to email clients. :-( -->
<table border=0 style="font-size: 10pt; font-family: Helvetica, Arial, sans-serif; ">
  <tr>
    <td style="vertical-align: bottom; padding-right: 1.3em; border-right: 1px solid #8EA5C7" rowspan="6" >
      <img border=0 style="height: 9rem" alt="" src={`${baseUrl}/if.png`} />
    </td>
    <td style="padding-left: 1.3em">
      <strong style="font-size: 1.3rem;">{name}</strong>
    </td>
  </tr>
  <tr>
    <td style="padding-left: 1.3em">
      <em>{title}</em>
    </td>
  </tr>
  <tr>
    <td class="phone" style="padding-left: 1.3em; text-decoration: none; color: #0c0732">{phone}</td>
  </tr>
  <tr>
    <td style="padding: .5rem; padding-left: 1.3em"><strong>Inkfish</strong> | 
      <a style="text-decoration: none; color: #0c0732;" 
        onMouseOver="this.style.color='#244B91'"
        onMouseOut="this.style.color='#0C0732'" 
        href="https://www.ink.fish">www.ink.fish</a>
    </td>
  </tr>
  <tr><td style="padding-bottom: .5rem; padding-left: 1.3em; color: #244b91">Deeply curious</td></tr>
  <tr>
    <td style="padding-left: 1.3em">
      <a href="https://instagram.com/inkfishexpeditions">
        <img border=0 alt="" src={`${baseUrl}/ig.png`} /></a>
      <a href="https://www.facebook.com/InkfishExpeditions/">
        <img border=0 alt="" src={`${baseUrl}/fb.png`} /></a>
      <a href="https://www.linkedin.com/company/inkfishexpeditions/">
        <img border=0 alt="" src={`${baseUrl}/li.png`} /></a>
      <a href="https://www.youtube.com/channel/UCmFIo3uaPeYxfqLNMVxtL5w"> 
        <img border=0 alt="" src="{`${baseUrl}/yt.png`}" /></a>
    </td>
  </tr>
</table>

<style>
  /* light blue: #8EA5C7, blue: #244b91, dark purple: #0c0732 */
  /* a, a:link, a:visited {
    text-decoration: none; 
    color: #0c0732;
  }
  a:hover {
    color: #8EA5C7;
  } */
</style>
