# Svelte Resume

Flexible, customizable template for creating a printed pdf resume.

Built with [Svelte](https://svelte.dev). Design inspired by [enhancv](https://enhancv.com/).

Created with a Svelte [project template](https://github.com/sveltejs/template).


```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Clone to your local computer using

```bash
git clone https://github.com/theresamorelli/svelte-resume.git
```


Install the dependencies...

```bash
cd svelte-resume
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see the app running! Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

## Using Svelte Resume

Get started by replacing the dummy data with your info! Name and summary go in Header.svelte, and everything else goes in Body.svelte (both located in src/components/structural).

Adjust the appearance and fit your unique content by changing global css variables for color, spacing, and other appearance items. These are located in the :root selector at the top of global.css (example: --link-color). This particular configuration is designed to adapt to different content and maintain alignment.

Just a note: the particular settings optimize for my current version of Google Chrome (80.0.3987.132) with 8.5 x 11"-size PDF and Print Settings margins set to 'none'. Might look funky with other browsers or settings.

Preview how your resume will look in the browser with Print Preview. Create a PDF using your computer's [print to PDF](https://acrobat.adobe.com/us/en/acrobat/how-to/print-to-pdf.html) functionality.

Change styles and add your own components based on your resume's specific needs!

# Production Mode

Should you need to host on the web:

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```


## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within your project folder:

```bash
cd public
now deploy --name my-project
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
