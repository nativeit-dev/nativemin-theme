# Custom CSS For Virtualmin's Authentic Theme
---

![Screenshot of main Webmin dashboard](https://github.com/nativeit-dev/webmin-native-theme/blob/master/screenshots/dashboard.png?raw=true)

This repository contains the custom CSS that I created for use with the Webmin Authentic Theme via its *Theme Extensions* interface.

  - All of the changes were made using pure CSS without altering any theme files or Webmin source, so the relatively frequent update schedule for these projects should not affect my UI changes unless there are major breaking changes made to the UI elements or their class selectors.
  - All custom fonts and colors were declared as variables at the top of the file, and these variables were employed at every possible opportunity in order to make changes to the style and typography as straightforward and simple as possible.
  - The entirety of the customizations is contained within the single CSS file, the only other asset required for implementation as pictured is the background image.
  - The CSS has been sorted, organized, and commented *mostly*. Because this is entirely comprised of hacks and modifications of existing styles in the Authentic theme, it can be a little messy in places. (see below for known issues and TODOs)
  - Even with the caveats involved with heavily modifying existing styles, you should be able to implement this with your own branding, backgrounds, fonts, and colors, in an hour or two (assuming you're reasonably comfortable with CSS).
  - Even with no real experience with CSS, applying this as-pictured to an existing and up-to-date Virtualmin instance only takes a few minutes. 

## Installing
  1. Be sure your Virtualmin is **up-to-date** along with the Authentic theme.
  2. Set the **navigation bar color pallette** to the default **"Blue"** (from `Theme Configuration > Navigation menu`).
  3. Obtain a suitable background image and upload it somewhere that will allow you to link to it from the CSS.
  4. Go to `Theme Configuration > Theme Logos` and upload the logos you would like to appear on the login screen (unauthenticated logo) and at the bottom of the navigation bar (authenticated logo). A roughly square-ish PNG with a transparent background is the best option for this.
  5. **Copy the raw contents** of `styles.css` ([click here](https://raw.githubusercontent.com/nativeit-dev/webmin-native-theme/master/styles.css) for the raw version).
  6. Paste the entirety of it into the **Theme Extensions** panel under `Theme Configuration > Theme Extensions`.
  7. Under the first block of CSS Body declarations after the Variables, locate the following line: `background-image: radial-gradient(#e0e0e0, #333333), url('https://raw.githubusercontent.com/nativeit-dev/webmin-native-theme/master/img/background.jpg');` (this is line 44 in the current version, it's been clearly commented) and **replace the URL with the background image you uploaded in Step 3**.
  8. Save your changes.
  9. Tweak until your happy.

NOTE: *Background images in this repo are included for demo purposes. I have licensed these images for my own use through [Envato Elements](https://elements.envato.com/abstract-ink-backgrounds-DUEAQ4), but I *do not have the rights to distribute the images*, and you do not have the rights to use them. Please be considerate to both the author of the images and myself by not copying them without a license, or hotlinking to where they are hosted on my server. If you would like to obtain a license for them, you can find them [here](https://elements.envato.com/abstract-ink-backgrounds-DUEAQ4).*

### Open source assets employed:
  - [Oswald](github.com/googlefonts/OswaldFont) font by Vernon Adams
  - [Barlow](https://github.com/jpt/barlow) font by Jeremy Tribby
  - [Inconsolata](github.com/googlefonts/inconsolata) font by Raph Levien
  - Other misc. fonts from [Google Fonts](https://fonts.google.com/) have at times been imported and/or included in the variables as examples of other typefaces that happen to work well in this design. Alternative body fonts include other sans-serif typefaces such as Lato, Public Sans, and Roboto. If lowercase type isn't necessary for headings, Bebas Neue is a great alternative for Oswald (Bebas Neue Pro has recently added the benefit of full case and glyph options). I preferred smaller, more condensed monospace/code font options, and Source Code Pro or IBM Plex Mono are both great options.
  
  ---
  
  ### Virtualmin
[Virtualmin](https://github.com/virtualmin) is a *fantastic* full-featured open source web hosting control panel for Linux and \*BSD systems that has been developed over the course of now decades by a [dedicated and talented team of developers](https://github.com/virtualmin/virtualmin-gpl/graphs/contributors). If you aren't already aware of Virtualmin, it is an exceptional solution that balances the ease-of-use of most server control panels with an otherwise unique and in-depth suite of powerful features to help automate and streamline just about every routine server administration task, along with several other mission-specific use cases such as shared web hosting, application development, and enterprise infrastructure provisioning and maintenance.

In over two decades of website development and design that has morphed over the years into a more general career in I.T./networking engineering, I have never found anything even close to Virtualmin's abilities. It meets the need of experienced sysadmins while simultaneously rendering a toolset that are approachable and simple enough for a relative novice to use effectively. More importantly, it saves everyone involved no matter their skill level an immense amount of time with sensible defaults and pre-loaded automation. If that weren't already enough, their responsiveness to anyone looking for support in their forums and GH issues is remarkable, and they promptly offer expertise that can be trusted.

**My sincere thanks to everyone who has contributed to Webmin/Virtualmin.**
---

![Screenshot of Webmin login screen](https://github.com/nativeit-dev/webmin-native-theme/blob/master/screenshots/login-ui.png?raw=true)

![Screenshot of main Webmin navigation](https://github.com/nativeit-dev/webmin-native-theme/blob/master/screenshots/sidebar.png?raw=true)

![Screenshot of main Webmin theme extensions editor](https://github.com/nativeit-dev/webmin-native-theme/blob/master/screenshots/theme-extensions.png?raw=true)
