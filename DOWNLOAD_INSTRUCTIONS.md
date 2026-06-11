# Downloadable HTML Artifact

The deployable artifact is the plain folder:

```text
loomra-chat-artifact/
├── index.html
└── README.txt
```

## What to upload to Netlify

Upload the **`loomra-chat-artifact` folder** to Netlify's manual deploy screen.

If Netlify asks for a site folder, choose `loomra-chat-artifact`. The file Netlify serves is:

```text
loomra-chat-artifact/index.html
```

## Why there is no zip file in the PR

Binary archives such as `.zip` files are not supported by this PR/review flow. To keep the PR valid, the artifact is committed as normal text files instead of a binary zip.

## If you want to make a zip yourself

From the repository root, run:

```bash
zip -r loomra-chat-artifact.zip loomra-chat-artifact
```

Then upload `loomra-chat-artifact.zip` or the unzipped `loomra-chat-artifact` folder to Netlify.
