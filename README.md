<!doctype html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>CMS</title>
    <script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
  </head>
  <body>
    <h1>Painel CMS - Neuropp Filomena</h1>
    <button onclick="netlifyIdentity.open()">Entrar no painel</button>

    <script>
      if (window.netlifyIdentity) {
        netlifyIdentity.on("init", (user) => {
          if (!user) {
            netlifyIdentity.on("login", () => {
              document.location.href = "/admin/";
            });
          }
        });
        netlifyIdentity.init();
      }
    </script>

    <script src="https://unpkg.com/netlify-cms@^2.0.0/dist/netlify-cms.js"></script>
  </body>
</html>
