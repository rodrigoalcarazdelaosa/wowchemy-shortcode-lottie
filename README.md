Wowchemy Shortcode for adding [Lottie animations](https://lottiefiles.com) and [animated stickers from Telegram](https://telegram.org/blog/animated-stickers) to your [Wowchemy](https://wowchemy.com) Site.

## 🌈 Add the Shortcode to your Site

1. Install your shortcode in your site by referencing it at the bottom of your `config/_defaults/config.toml`:
   ```toml
   # At the bottom of your `config.toml` is a Module section:
   [module]

     # Your existing modules will appear here.

     # Add your shortcode's GitHub URL below.
     [[module.imports]]
       path = "github.com/rodrigoalcarazdelaosa/wowchemy-shortcode-lottie"
   ```
2. Use your shortcode in page content. For example let's create `content/post/test-my-shortcode.md`:
   ```markdown
   ---
   title: My shortcode
   date: '2020-11-27'
   ---

   Check out my shortcode:

   {{% github_rodrigoalcarazdelaosa_lottie src="https://assets5.lottiefiles.com/packages/lf20_q4nxakl0.json" width="100%" %}}
   ```
