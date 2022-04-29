# Academic CV Template

An Easy-to-use Nuxt template to build your Academic CV Website.

Demo: https://eason.best
# How to use?

Look at the [nuxt 3 documentation](https://v3.nuxtjs.org) to learn more.

## Setup

Make sure to install the dependencies:

```bash
# yarn
yarn install

# npm
npm install

# pnpm
pnpm install --shamefully-hoist
```

## Development Server

Start the development server on http://localhost:3000

```bash
npm run dev
```

## Production


Build the application for production:

```bash
npm run build
```

Checkout the [deployment documentation](https://v3.nuxtjs.org/docs/deployment) for more information.


## GitHub Action CI/CD Settings

> This part need to be refined and revised

> The script is at [`.github/workflows/node.js.yml`](./.github/workflows/node.js.yml)
### 1. Add CI/CD Access Token

Add your personal access token to the `Settings>Secrets>Actions` with Key `GH_TOKEN`. 
<br>[(Click me to know how to create personal access token.)](https://www.google.com/search?q=how+to+get+personal+access+token+github)

![](https://i.imgur.com/xfpPUF3.png)

### 2. Specify domain name

Change the domain of script `npm run cname` at [package.json](./package.json) to the domain name you want to use.
<br>If none, ~~buy one~~ remove the url but keep the script.

![](https://i.imgur.com/aEzOjID.png)

### 3. Done

You did it! When you push onto GitHub at branch main, the GitHub Actions will deploy a new GitHub Page for you.
