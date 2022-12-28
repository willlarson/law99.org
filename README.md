# nip05-github
a base for setting up nip 05 with github

Follow these steps to get NIP-05 verification on nostr with GitHub Pages

# Prerequisites
- A GitHub account

# Fork github repo
- Go to https://github.com/metasikander/nip05-github and create a fork of it with the "fork"-button in the top right corner
- Select a name and press the green "create fork" button.
- Setup github pages from repo.
  - Go into Settings -> Pages
  - Select branch ("main") and root folder (/root)
  - Save
  - Reload page, and press the "Visit site"-button
  - You will gett a 404-page
  - In the address-field, add ".well-known/nostr.json" to the end and press enter.
  - This should show a basic json-file.

# Edit nostr.json
- Back at the GitHub repo page, go into the .well-known folder, and edit the `nostr.json`-file. This can be done on the github website through the edit button.
- change the values with the name you want to use, and the pubkey you want to associate with it. This example is with multiple accounts, but if you only need one you can just remove the extra line and the ",".
```json
{
  "names": {
    "<your-nostr-nym>": "<your-nostr-pubkey>",
    "<your-nostr-nym>": "<your-nostr-pubkey>"
  }
}
```
- Push the changes to your website. If you're doing it on the github website, press the "Commit changes" button on the bottom.
- Verify that the nostr.json file is accessible by navigating to the page that we created earlier.

# Setup NIP05
- Go to your profile on http://anigma.io or http://astral.ninja and edit the NIP-05 field with <your-nostr-nym>@<your-github-username>.github.io.
- Congratulations, you are now part of the #nostr verified elite!

# Sources
https://twitter.com/0xsommerfeld/status/1604795583755161602  
https://github.com/vforvalerio87/registry.dude.rund
