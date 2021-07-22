# Wowchemy Shortcode Starter Template

**Looking to build and publish a [Wowchemy](https://wowchemy.com) shortcode that doesn’t exist yet?**

Unsure if there's already a relevant shortcode? [Explore](https://wowchemy.com/docs/writing-markdown-latex/) the existing shortcodes.

_[**Wowchemy**](https://wowchemy.com) makes it easy to create a beautiful website for free. Edit your site in Markdown, Jupyter, or RStudio, generate it with Hugo, and deploy with GitHub or Netlify. Customize anything on your site with widgets, themes, and language packs._

## 👉 Core Concepts

- Each Wowchemy shortcode consists of an HTML file
- You may use [Go Templating](https://gohugo.io/templates/introduction/), [shortcode parameters](https://gohugo.io/content-management/shortcodes/), and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts to design the shortcode

## 🧑‍🎨 Create a Shortcode

1. Click the [_Use This Template_](https://github.com/wowchemy/wowchemy-shortcode-starter/generate) button on GitHub
   1. Name your repository `wowchemy-shortcode-<SHORTCODE-NAME>` where `<SHORTCODE-NAME>` is an appropriate name for your shortcode
1. Browse your new GitHub project, click the  `go.mod` file, and then the ✏️ pencil button to edit it
   1. Replace the placeholder URL in `go.mod` with your new GitHub URL in the form `module github.com/<USERNAME>/wowchemy-shortcode-<SHORTCODE-NAME>` where `<USERNAME>` is your GitHub username and `<SHORTCODE-NAME>` is the name of the shortcode
   1. Scroll to the bottom and click _Commit Changes_ to save
1. Browse to the `layouts/shortcodes/` folder, click `my-shortcode.html`, and click the ✏️ pencil button to edit it
   1. Rename `my-shortcode.html` in the text box to a unique ID in the form `github_<USERNAME>_<SHORTCODE-NAME>.html`, again replacing `<USERNAME>` with your GitHub username and `<SHORTCODE-NAME>` with your shortcode name
   1. Scroll to the bottom and click _Commit Changes_ to save
1. Edit the HTML for your new shortcode
   - You may use [Go Templating](https://gohugo.io/templates/introduction/) and [Bootstrap](https://getbootstrap.com/docs/4.5/layout/grid/) layouts
   - View the Hugo docs on [Shortcodes](https://gohugo.io/content-management/shortcodes/)
   - You can access the shortcode content using `{{.Inner}}`
   - Check out the [built-in shortcodes](https://github.com/wowchemy/wowchemy-hugo-modules/tree/master/wowchemy/layouts/shortcodes) for inspiration

### Example

Say your GitHub username is `pikachu` and you wish to create a shortcode named `pokemon`:

1. We click _Use This Template_ and enter `wowchemy-shortcode-pokemon` as the project name
1. We replace the first line of `go.mod` with `module github.com/pikachu/wowchemy-shortcode-pokemon`
1. We browse to the `layouts/shortcodes/` folder, and rename `my-shortcode.html` to `github_pikachu_pokemon.html`
1. We customize the HTML in `github_pikachu_pokemon.html`
1. We add the shortcode to our site and share the shortcode with the community following the guide below

## 🌈 Add the Shortcode to your Site

1. Install your shortcode in your site by referencing it at the bottom of your `config/_defaults/config.toml`:
   ```toml
   # At the bottom of your `config.toml` is a Module section:
   [module]

     # Your existing modules will appear here.

     # Add your shortcode's GitHub URL below.
     # Replace <USERNAME> and <SHORTCODE-NAME> with your GitHub username and shortcode name, respectively.
     [[module.imports]]
       path = "github.com/<USERNAME>/wowchemy-shortcode-<SHORTCODE-NAME>"
   ```
1. Use your shortcode in page content. For example let's create `content/post/test-my-shortcode.md`:
   ```markdown
   ---
   title: My shortcode
   date: '2020-11-27'
   ---

   Check out my shortcode:

   {{% github_pikachu_pokemon %}}Content to *process*.{{% /github_pikachu_pokemon %}}
   ```

## 📢 Share your Shortcode

Share your shortcode with the community on [Discord](https://discord.gg/z8wNYzb) and [Twitter](https://twitter.com/intent/tweet?text=I%27m%20creating%20a%20beautiful%20website%20shortcode%20using%20the%20free%20%E2%9D%A4%EF%B8%8F%2C%20open%20source%20%40wowchemy%20Website%20Builder%20for%20%40GoHugoIO%20by%20%40GeorgeCushen%20%E2%9C%A8%20Have%20some%20feedback%3F%20Please%20comment%20%F0%9F%A4%97&hashtags=MadeWithWowchemy&url=https://wowchemy.com/).
