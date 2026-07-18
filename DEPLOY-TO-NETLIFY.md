# Put PhotoPost AI on Netlify

This version is already converted for Netlify. It does not need Wix, a custom domain, or a separate server.

## What you will get

Netlify will give the app a secure address similar to:

`https://your-chosen-name.netlify.app`

HTTPS is automatic.

## Deploy the app

1. Download and unzip `PhotoPost-AI-Netlify.zip`.
2. Sign in to your Netlify account.
3. Choose **Add new project** and then **Deploy manually**.
4. Drag the entire unzipped `PhotoPost-AI-Netlify` folder into Netlify—not only the `public` folder.
5. Wait for the deploy to finish and open the generated `netlify.app` address.

The entire folder is required because it contains the website, `netlify.toml`, and the secure Netlify Functions.

## Add the OpenAI key

The app works in fallback mode before the key is added.

1. Open the new Netlify project.
2. Go to **Project configuration**.
3. Open **Environment variables**.
4. Add:
   - Key: `OPENAI_API_KEY`
   - Value: your OpenAI API key
5. Optional:
   - Key: `OPENAI_MODEL`
   - Value: `gpt-5-mini`
6. Make sure the variable is available to **Functions** if Netlify shows a scope choice.
7. Trigger a new deploy from the **Deploys** page.

Do not put the key in `public/app.js`, `netlify.toml`, or a screenshot.

## Confirm it works

Open the app address. Near the top it should say:

`AI photo analysis connected`

Then add a photo and press **Create my post**.

If it still says fallback mode:

- Confirm the key is spelled exactly `OPENAI_API_KEY`.
- Confirm it has Functions scope.
- Redeploy after adding the key.
- Check **Logs > Functions > generate** for an error.

## Choose a better Netlify address

In the Netlify project, open **Domain management** and change the project/site name to an available name. The address will remain a secure `netlify.app` address.

## Install it on your phone

Open the Netlify address in Chrome on Android. Use the app's **Install app** button when it appears, or open Chrome's menu and choose **Add to Home screen**.

## Updating later

Unzip the updated package and drag the complete updated project folder into the manual deploy area on the existing project's **Deploys** page.
