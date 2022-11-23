<script>
  import Signature from './lib/Signature.svelte'
  const urlParams = new URLSearchParams(window.location.search)

  let name = urlParams.get('name') ?? 'Randolf Carter'
  let title = urlParams.get('title') ?? 'Legendary Dreamer'
  let phone = urlParams.get('phone') ?? '+1 234 567 8900'

  let buttonMessage = 'Copy Signature'
  function updateButtonMessage() {
    // let the user know
    let oldMessage = buttonMessage
    buttonMessage = 'Copied!'
    setTimeout(() => {
      buttonMessage = oldMessage
    }, 1500)
  }

  let signature
  function copySignature() {
    var range = document.createRange()
    range.selectNode(signature)
    window.getSelection().removeAllRanges()
    window.getSelection().addRange(range)
    document.execCommand('copy') // deprecated but works on all tested browsers
    window.getSelection().removeAllRanges()
  }
</script>

<main>
  <div id="wrapper">
    <div bind:this={signature}>
      <Signature {name} {title} {phone} />
    </div>
    <button on:click={copySignature} on:click={updateButtonMessage}
      >{buttonMessage}</button>
    <div id="form">
      <form>
        <label for="name">Name</label>
        <input type="text" name="name" bind:value={name} />
        <label for="title">Title</label>
        <input type="text" name="title" bind:value={title} />
        <label for="phone">Phone</label>
        <input type="text" name="phone" bind:value={phone} />
        <button>Save to URL</button>
      </form>
    </div>
  </div>
</main>

<!-- 

// other copy paste methods saved for posterity
function copySig() {
  // only copies text/plain not text/html
  const output = document.getElementById("signature").innerHTML;
  const theClipboard = navigator.clipboard;
  theClipboard.writeText(output).then(() => console.log('Copied signature to clipboard: ', {name, title, phone}));  
}

async function copySig() {
  // provides text/plain fallback, best solution but no Firefox support :-(
  // https://www.nikouusitalo.com/blog/why-isnt-clipboard-write-copying-my-richtext-html/
  // https://github.com/nikouu/Web-API-Clipboard.write-Examples 
  const richTextDiv = document.getElementById("signature");

  // Works in Safari (macOS & iOS) and Chrome/Brave
  // Is supposed to (but doesn't) work in Firefox 87+ with about:config thedom.events.asyncClipboard.clipboardItem = true
  const clipboardItem = new ClipboardItem({
    "text/plain": new Blob(
      [richTextDiv.innerText.trim()],
      { type: "text/plain" }
    ),
    "text/html": new Blob(
      [richTextDiv.outerHTML],
      { type: "text/html" }
    ),
  });

  await navigator.clipboard.write([clipboardItem]);
 }

// <div bind:this={signature}>
let signature
async function copySignature1() {
  await navigator.clipboard.writeText(signature.innerHTML); // or outerHTML
}

-->
<style>
  :root {
    --darkPurple: #020035;
    --fontSize: 12pt;
  }
  div#wrapper {
    display: flex;
    flex-direction: column;
    font-family: Helvetica, Arial, sans-serif;
    font-size: var(--fontSize);
  }
  div#form {
    margin-top: 2rem;
    padding: 0.5rem;
    border: 2px solid var(--darkPurple);
  }
  form {
    display: flex;
    flex-direction: column;
  }
  label,
  button {
    color: var(--darkPurple);
    font-weight: bold;
  }
  label {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 0.5rem;
  }
  input {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 0.3rem;
    border: 1px solid var(--darkPurple);
    font-size: var(--fontSize);
  }
  button {
    margin-top: 1rem;
    padding: 0.5rem;
    border: 0px;
    background-color: var(--darkPurple);
    color: white;
    font-size: var(--fontSize);
  }
</style>
