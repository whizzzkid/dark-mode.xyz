## Enable Dark Mode for Any Website!

This is the simplest way to convert your website to have a dark mode. This is a Cloudflare app that
converts your website into a dark-mode compatible website. If you're serving your website through
Cloudflare CDN then just enable this free app so that your website can render in dark on every browser.

###  Installation Steps

**Step 1:** Make sure your traffic is being routed through Cloudflare.

**Step 2:** Enable this app.

**Step 3:** Your website should now render in dark mode based on user's device theme.

***Note:** Some HTML components can behave weird but the app tries it's best to convert the page to a
dark themed one.*

### How does it work

The app installs a script on the page, that basically inverts the color of every element on the page, making it render in dark-mode and make it easier on the eyes.

### Performance

Most of the changes are applied via CSS, using:

```css
@media (prefers-color-scheme: dark) {

    :root,
    img {
        filter: invert(1) hue-rotate(180deg);
    }
}
```

A few more changes are applied by a JS snippet that finds elements for images loaded by other means
and filters those out. This happens in liner time, based on the number of nodes in your DOM.

### Benefits

It's a one-click fix to add dark mode to any website served over Cloudflare and should work on every
device. This website uses this app!
