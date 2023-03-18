<script context="module">
  // images must load remotely from an absolute URL to be reliable
  export const imagesBaseUrl = 'https://files.ink.fish/sigmaker'
  export const fonts =
    'font-size: medium; font-family: Helvetica, Arial, sans-serif;'
  // 'font-size: medium; font-family: Helvetica, Arial, sans-serif;'
</script>

<script>
  // images must load remotely from an absolute URL to be reliable
  // let imagesBaseUrl = 'https://files.ink.fish'
  // import { onMount } from 'svelte'
  // let path = ''
  // // onMount(() => (url = window.location.href))
  // onMount(() => (imagesBaseUrl = imagesBaseUrl + window.location.pathname))

  import InkfishIcons from './InkfishIcons.svelte'

  export let name
  export let title
  export let phone

  const logoUrl = imagesBaseUrl + '/inkfish.png'
  const links = [
    { name: 'instagram', url: 'https://instagram.com/inkfishexpeditions' },
    { name: 'facebook', url: 'https://www.facebook.com/InkfishExpeditions/' },
    {
      name: 'linkedin',
      url: 'https://www.linkedin.com/company/inkfishexpeditions/',
    },
    {
      name: 'youtube',
      url: 'https://www.youtube.com/channel/UCmFIo3uaPeYxfqLNMVxtL5w',
    },
  ]
</script>

<!-- <h1>PATH: {path}</h1> -->

<!-- Horrendous HTML and CSS as recommended for email signatures. -->
<table style={fonts} cellspacing="0" cellpadding="0">
  <tbody>
    <tr>
      <td>
        <table style={fonts} cellspacing="0" cellpadding="0">
          <tbody>
            <tr>
              <td style="vertical-align: top">
                <img
                  src={logoUrl}
                  role="presentation"
                  style="display: block; max-width: 130px"
                  width="130"
                  alt="" />
              </td>
              <td style="padding-left: 29px; border-right: 1px solid #8EA5C7;">
                <div />
              </td>
              <td style="padding-left: 29px; vertical-align: middle">
                <h2
                  color="#0C0732"
                  style="
                    margin: 0px;
                    font-size: 16pt;
                    color: #0C0732;
                    font-weight: 400;
                  ">
                  {name}
                </h2>
                <p
                  color="#0C0732"
                  style="
                    margin: 0px;
                    color: #0C0732;
                    font-size: 11pt;
                    font-style: italic;
                    font-weight: 200;
                    line-height: 17px;
                  ">
                  {title}
                </p>
                <p
                  color="#0C0732"
                  style="
                  margin: 0px;
                  color: #0C0732;
                  font-size: 11pt;
                  font-weight: 200;
                  line-height: 17px;
                ">
                  {phone}
                </p>
                <p
                  style="
                    margin: 0px;
                    font-size: 11pt;
                    line-height: 37px;
                  ">
                  <span style="color: #0C0732; font-weight: 600;">Inkfish</span
                  >&nbsp; |&nbsp;
                  <a
                    style="text-decoration: none; font-weight: 200; color: #0c0732;"
                    href="https://www.ink.fish">www.ink.fish</a>
                </p>
                <p
                  style="
                    margin: 0px;
                    font-size: 11pt;
                    font-weight: 200;
                    line-height: 24px;
                    padding-bottom: 10px;
                  ">
                  <span style="color: #114C96">Deeply curious</span>
                </p>

                <InkfishIcons {links} />
              </td>
            </tr>
          </tbody>
        </table>
      </td>
    </tr>
  </tbody>
</table>

<style>
  /* Must use inline styles with email. */
</style>
