<script>
  import { imagesBaseUrl, fonts } from './Signature.svelte'
  console.log({imagesBaseUrl, fonts})
  export let links
</script>


<table
  id="socialLinks"
  style={`display: inline-block; ${fonts}`}
  cellspacing="0"
  cellpadding="0"
>
  <tbody>
    <tr style="text-align: center">
      {#each links as link}
        <td>
          <a
            href={link.url}
            style="
              display: inline-block;
              padding: 0px;
            "
            ><img
              src={`${imagesBaseUrl}/${link.name}.png`}
              alt=""
              style="
                max-width: 24px;
                display: block;
              "
              height="24"
          /></a>
        </td>
        <td width="5"><div></div></td>
      {/each}
    </tr>
  </tbody>
</table>

<style>
  /* Must use inline styles with email. */
</style>
