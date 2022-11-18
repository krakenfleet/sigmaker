<script>    
  import { copy } from 'svelte-copy';

  import Signature from './lib/Signature.svelte'
  const urlParams = new URLSearchParams(window.location.search);

  let name = urlParams.get('name') ?? "Randolf Carter";
  let title = urlParams.get('title') ?? "Legendary Dreamer"
  let phone = urlParams.get('phone') ?? "+1 234 567 8900"

  // function copySig() {
  //   only copies text/plain not text/html
  //   const output = document.getElementById("signature").innerHTML;
  //   const theClipboard = navigator.clipboard;
  //   theClipboard.writeText(output).then(() => console.log('Copied signature to clipboard: ', {name, title, phone}));  
  // }

  function copySig() {
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

    navigator.clipboard.write([clipboardItem]);
  }
</script>

<main>
  <div id="wrapper">
    <Signature {name} {title} {phone} />
    <button on:click={copySig}>Copy Signature</button>
    <div id="form">
      <form>
        <label for="name">Name</label>
        <input type="text" name="name" bind:value={name} />
        <label for="title">Title</label>
        <input type="text" name="title" bind:value={title} />
        <label for="phone">Phone</label>
        <input type="text" name="phone" bind:value={phone} />
        <button>Update URL</button>
      </form>
    </div>
  </div>
</main>

<style>
  div#wrapper {
    display: flex;
    flex-direction: column;
    width: 300px;
  }
  div#form {
    margin-top: 2rem;
    padding: .5rem;
    border: 2px solid #0c0732;
  }
  form {
    display: flex;
    flex-direction: column;
  }
  label, button {
    color: #0c0732;
    font-weight: bold;
  }
  label {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: .5rem;
  }
  input {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: .3rem;
    border: 1px solid #0c0732;
  }
  button {
    margin-top: 1rem;
    padding: .5rem;
    border: 0px;
    background-color: #0c0732;
    color: white;
  }
</style>

