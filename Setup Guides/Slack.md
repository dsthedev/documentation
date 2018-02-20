# Setting up Slack

* Set zoom to 80% `Ctrl + -` x 2

* Install Black Theme (Partially Broken as of v3.0.5)

  * Find your Slack's application directory.

    - Windows: `%homepath%\AppData\Local\slack\`
    - Mac: `/Applications/Slack.app/Contents/`
    - Linux: `/usr/lib/slack/` (Debian-based)

  * Open up the most recent version (e.g. `app-2.5.1`) then open
    `resources\app.asar.unpacked\src\static\index.js`

  * At the very bottom, add

    ```javascript
    // First make sure the wrapper app is loaded
    document.addEventListener("DOMContentLoaded", function() {

       // Then get its webviews
       let webviews = document.querySelectorAll(".TeamView webview");

       // Fetch our CSS in parallel ahead of time
       const cssPath = 'https://cdn.rawgit.com/widget-/slack-black-theme/master/custom.css';
       let cssPromise = fetch(cssPath).then(response => response.text());

       let customCustomCSS = `
       :root {
          /* Modify these to change your theme colors: */
          --primary: #09F;
          --text: #CCC;
          --background: #080808;
          --background-elevated: #222;
       }
       `

       // Insert a style tag into the wrapper view
       cssPromise.then(css => {
          let s = document.createElement('style');
          s.type = 'text/css';
          s.innerHTML = css + customCustomCSS;
          document.head.appendChild(s);
       });

       // Wait for each webview to load
       webviews.forEach(webview => {
          webview.addEventListener('ipc-message', message => {
             if (message.channel == 'didFinishLoading')
                // Finally add the CSS into the webview
                cssPromise.then(css => {
                   let script = `
                         let s = document.createElement('style');
                         s.type = 'text/css';
                         s.id = 'slack-custom-css';
                         s.innerHTML = \`${css + customCustomCSS}\`;
                         document.head.appendChild(s);
                         `
                   webview.executeJavaScript(script);
                })
          });
       });
    });
    ```

  * Restart Slack to see changes

* Preferences

  * Notifications
    * Only notify for direct messages, mentions & keywords
    * Change sound to Knock Brush
  * Windows App - Don't launch on login
  * Messages & Media - Just display names
  * Sidebar colors: `#171717,#404245,#424242,#ECF0F1,#4A4A4A,#FAFAFA,#2ECC71,#00A362`
  * Advanced
    * Change Download location to `E:\Downloads\Slack`

.