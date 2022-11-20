# A Simple Email Signature Builder

Make with Svelte.

## Features

- Update name, title, and phone via form
- Button to copy signature for pasting into email client
- Name, title, and phone saved to URL query strings so can be bookmarked
- Very awful HTML should (hopefully) work on all clients.

## Screenshot

<img width="359" alt="image" src="https://user-images.githubusercontent.com/130651/202879276-c7558721-2f69-4a3c-8110-a515b6fc6729.png">

## Installation

- In `/public` make sure you have your logo and preferred social media icons (Instagram, YouTube, LinkedIn, and Facebook are included)
- In `Signature.svelte` edit `logoUrl` and `links`
- To deploy run `yarn build` and then copy all files in `/dist` to a webserver

Note, it currently assumes you are installing to a sub-directory called `sigmaker` (eg. http://example.com/sigmaker/).  
If you want it installed to the root domain or a different subdomain you need to update `--base=/sigmaker` in `packages.json`.
