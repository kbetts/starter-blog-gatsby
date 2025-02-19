<p align="center">
  <a style="padding-right: 16px;" href="https://forestry.io">
    <img src="https://app.forestry.io/assets/forestry-logotype-pos-c71a6bd237d9199d0457ba2811553997ff5bab0d2cd0e740686ab26c00d9c240.svg" width="112" height="28">
  </a>
  <a href="https://www.gatsbyjs.org/">
    <img src="/static/gatsby_logo.svg" width="112" height="28">
  </a>
</p>
<h1 align="center">
  Brevifolia
</h1>

## About

Brevifolia is minimalist blog starter to get you going using [Forestry](https://forestry.io/) with [Gatsby](https://www.gatsbyjs.org/). 

This blog is statically generated by Gatsby, a rendered combination of react components and markdown files. It is preconfigured to work with Forestry as a way to manage your content. Forestry makes changes by editing markdown or data files, uploading media to the correct directory and committing these updates to your repo directly.

The styles were coded & designed by yours truly, using [scss](https://sass-lang.com/) with [css modules](https://github.com/css-modules/css-modules) (which are [inherently support by gatsby](https://www.gatsbyjs.org/docs/css-modules/)) and the [bem](http://getbem.com/) naming convetion. The font used is [Work Sans](https://fonts.google.com/specimen/Work+Sans). 

##  Quick Setup

#### *Import to Forestry Button*
TBD...
#### *Gatsby new - after submit to gatsby starter*
TBD...
#### *Set-up Locally*
In your terminal, navigate to where you would like this blog to live, then run 
```bash
#clone the repo
git clone git@github.com:kendallstrautman/starter-blog-gatsby.git

#navigate to the directory
cd starter-blog-gatsby

#install dependencies & run dev server with yarn 
yarn install
yarn dev

#or with npm 
npm install
npm run dev
```
A new browser window should open with the dev server running or you can navigate to localhost:8000 

### Plugins

With Gatsby offering a plugin-rich ecosystem, there are a few key plugins that make this project possible. 

- [Gatsby-image](https://using-gatsby-image.gatsbyjs.org/) optimizes image loading and provides the correct file paths for output. 
- [Gatsby-transformer-remark](https://www.gatsbyjs.org/packages/gatsby-transformer-remark/?=gatsby-tranf) gives us access to and transforms the markdown files, using also [gatsby-remark-images](https://www.gatsbyjs.org/packages/gatsby-remark-images/?=gatsby-remark), [gatsby-remark-normalize-paths](https://www.gatsbyjs.org/packages/gatsby-remark-normalize-paths/?=gatsby-remark-no), & [gatsby-remark-relative-images](https://www.gatsbyjs.org/packages/gatsby-remark-relative-images/?=gatsby-remark-re) to make sure the content in the markdown works properly. 
- [Gatsby-transformer-yaml allows](https://www.gatsbyjs.org/packages/gatsby-transformer-yaml/?=gatsby-tranfor) us to use the data in .yaml files, feel free to add [gatsby-transformer-json](https://www.gatsbyjs.org/packages/gatsby-transformer-json/?=gatsby-tranfor) if you prefer that format for data files. 
- [Gatsby-plugin-sass](https://www.gatsbyjs.org/packages/gatsby-plugin-sass/?=gatsby-plugin-sass) lets us write styles using scss or sass. 
- [Gatsby-plugin-react-helmet](https://www.gatsbyjs.org/packages/gatsby-plugin-react-helmet/?=gatsby-plugin-react) extends the well-known react-helmet, allowing you to adjust content in the ‘head’ of your components. 

## Project Structure 

- Site-level configuration is stored in `config.json` so it can be exposed to Forestry. This file is loaded in the `gatsby-config.js` to configure Gatsby and all it to be accessible via siteMetaData in your graphql queries.
- Access any of Gatsby's [browser api's](https://www.gatsbyjs.org/docs/browser-apis/) via the `gatsby-browser.js`, or load global styles etc.
- Add and access plugin options or siteMetaData via `gatsby-config.js`
- Access Gatsby's [node api's](https://www.gatsbyjs.org/docs/node-apis/) via `gatsby-node.js`. This is where the creation of new blog pages or nodes is handled. 
- Edit styles via `src/styles/...`
- `content/`contains all your markdown blog posts, images & data files (e.g. authors list, info page data). 
- `src/pages` is a very important and required directory for Gatsby. This is where all your pages for the site live. 
- Blog posts are built from a template that can be accessed at `src/templates`. 
- The pages & template are comprised of components from `src/components`.

## Using Forestry as your CMS

The `.forestry` directory contains all the settings information and frontmatter configuration to allow Forestry to setup the sidebar structure and editing capacity for this blog. After importing this blog into forestry, you can [access and edit](https://forestry.io/docs/editing/) all of the content via the sidebar. 

You can add new blog posts, [data files](https://forestry.io/docs/editing/data-files/), or entire pages and sections to fit your needs. You can also [customize how media](https://forestry.io/docs/media/) is handled, by configurating gitLFS, Cloudinary, S3, or Netlify Large Media.

You can set up a [remote admin](https://forestry.io/docs/editing/remote-admin/) for content editors to log in directly to yoururl.com/admin to make content updates.

### Instant Previews

The [instant preview](https://forestry.io/docs/previews/instant-previews/) method spins up the Gatsby development server for a long-lived preview that can quickly respond to content updates. When using instant previews, your preview command should be the develop command. The development server spawned by this command should be available over port 8000, and bind to 0.0.0.0. The forestry:preview command in this project's package.json will spin up a Gatsby dev server compatible with Forestry's instant previews.

## Deploy Options

[Netlify](https://www.netlify.com/blog/2016/09/29/a-step-by-step-guide-deploying-on-netlify/) is a great way to easily deploy sites. There's no special setup you need to do with Forestry to deploy with Netlify. When Forestry makes commits to your repo, Netlify will auto-trigger a rebuild / deploy when new commits are made.
