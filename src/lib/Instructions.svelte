<script>
  export let instructions
</script>

<form>
  <button>Show Instructions for … </button>
  <div>
    <select bind:value={instructions} name="instructions">
      <option value="outlook_win">Outlook (Windows)</option>
      <option value="mail_macos">Mail App (macOS)</option>
      <option value="mail_ios">Mail App (iOS)</option>
      <option value="gmail_web">Gmail (web)</option>
      <option value="gmail_ios">Gmail App (iOS)</option>
      <option value="fastmail_web">FastMail (web)</option>
    </select>

    {#if instructions === 'outlook_win'}
      <ol>
        <li>In Outlook click the <u>New Email</u> button</li>
        <li>In the menubar of the new blank email, click <u>Insert</u></li>
        <li>
          Within the insert menubar click <u>Signature</u> and then
          <u>Signatures</u>
        </li>
        <li>In the <u>Signatures and Stationary</u> window click <u>New</u></li>
        <li>
          In the <u>New Signature</u> window give your new signature a name and
          click <u>OK</u>
        </li>
        <li>Copy your customised signature (from this page)</li>
        <li>
          Pase your signature into the "Edit signature" text box and click <u
            >OK</u>
        </li>
        <li>
          If you have more than one signature, you may set the default signature
          under <u>Choose default signature</u>
        </li>
        <li>Click <u>OK</u></li>
      </ol>
    {:else if instructions === 'mail_ios'}
      <ol>
        <li>Open <u>Settings</u> on your iPhone or iPad</li>
        <li>Scroll down to and select <u>Mail</u></li>
        <li>Now scroll down to and select <u>Signature</u></li>
        <li>Delete anything already in the text box</li>
        <li>Copy your customised signature (from this page)</li>
        <li>Paste into the text box</li>
        <li>You'll notice that the formatting looks a bit wonky</li>
        <li>Shake the iOS device and select <u>Undo</u> when it pops up</li>
        <li>The formatting should now look correct</li>
        <li>
          Save the signature by selecting <u><b>&lt;</b> Mail</u> in the top left
          corner
        </li>
      </ol>
    {:else if instructions === 'gmail_web'}
      <ol>
        <li>Log into the <a href="https://gmail.com/">Gmail</a> webpage</li>
        <li>
          Go to <a href="https://mail.google.com/mail/u/0/#settings/general"
            >Settings - See all settings - General</a>
        </li>
        <li>Scroll to the <u>Signature</u> section (near the bottom)</li>
        <li>Click <u>+ Create New</u></li>
        <li>Delete anything already in the Gmail signature box</li>
        <li>Copy your customised signature (from this page)</li>
        <li>Paste into the signature box</li>
        <li>
          Under <u>Signature Defaults</u> set the new signature as the default for
          both new emails and replies
        </li>
        <li>Click <u>Save</u> at the bottom of the page</li>
      </ol>
    {:else if instructions === 'gmail_ios'}
      <ul>
        <li>
          Gmail on iOS will automatically use the default Gmail web signature
        </li>
      </ul>
      <i>Note: The signature doesn't display when you compose an email.</i>
    {:else if instructions === 'mail_macos'}
      <ol>
        <li>
          In Mail.app go to <u>Preferences - Signatures - All Signatures</u>
        </li>
        <li>Click <u>+</u> to create a new signature</li>
        <li>
          Untick <u>Always match my default message font</u>
        </li>
        <li>Copy your customised signature (from this page)</li>
        <li>Paste into the signature box (the images will not show up)</li>
      </ol>
      <i
        >Note: This only partially works. It will look correct but none of the
        links will work. If you'd like the proper version please contact <a
          href="mailto:support@ink.fish">support@ink.fish</a
        >.</i>
    {:else if instructions === 'fastmail_web'}
      <ol>
        <li>
          Log into the <a href="https://app.fastmail.com/login/">FastMail</a> webpage
        </li>
        <li>
          Go to <a href="https://www.fastmail.com/settings/identities"
            >Settings - Sending identities</a>
        </li>
        <li>Find the identity you want to add an signature for</li>
        <li>Click the <u>Edit</u> button to the right of the identity</li>
        <li>Delete anything already in the Fastmail <u>Signature</u> box</li>
        <li>Copy your customised signature (from this page)</li>
        <li>Paste into the <u>Signature</u> box</li>
        <li>Click the <u>Save</u> button</li>
      </ol>
    {/if}
  </div>
</form>

<style>
  form {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    /* border: 2px solid var(--darkPurple);
    padding: 0.5rem; */
  }
  button {
    padding: 0.5rem;
    border: 2px solid var(--darkPurple);
    background-color: white;
    /* background-color: var(--darkPurple);
    color: white;*/
    font-size: var(--fontSize);
    font-weight: bold;
  }
  select {
    width: 100%;
    padding: 0.5rem;
    border: 1px solid var(--darkPurple);
    color: white;
    background-color: var(--darkPurple);
    font-size: var(--fontSize);
    font-weight: bold;
    text-align: center;
  }
  a,
  a:link,
  a:visited,
  a:active {
    color: var(--logoBlue);
    font-weight: bolder;
  }
  a:hover {
    color: blue;
  }
  u {
    color: var(--darkPurple);
    font-weight: bolder;
  }
  i {
    display: block;
    line-height: 1.3;
    text-align: justify;
  }
  ol,
  ul {
    margin: 0;
    line-height: 1.5;
  }
</style>
