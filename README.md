[index (1).html](https://github.com/user-attachments/files/23393295/index.1.html)
<!doctype html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Abrir arquivo</title>
  <meta name="viewport" content="width=device-width,initial-scale=1" />
</head>
<body>
  <p>Carregando... se não redirecionar, <a id="manual" href="#">clique aqui</a>.</p>

  <script>
    const links = {
      ios_app: "https://drive.google.com/drive/folders/1r4UzjTY1gAsI3yr7zOOJWvPFgqDmr2Ao?usp=drive_link",
      android_app: "https://drive.google.com/drive/folders/1r4UzjTY1gAsI3yr7zOOJWvPFgqDmr2Ao?usp=drive_link",
      onedrive: "https://arvsystemscombr-my.sharepoint.com/:f:/g/personal/ruan_jesus_arvsystems_com_br/EmBbj03vdcVAkh7PRweu6ZYBwF-9hHt3lIUhUZSPhP89ZA?e=MrUNza",
      desktop_browser: "https://drive.google.com/drive/folders/1r4UzjTY1gAsI3yr7zOOJWvPFgqDmr2Ao?usp=drive_link"
    };

    const ua = navigator.userAgent || navigator.vendor || window.opera;
    const manualA = document.getElementById('manual');

    function isIos() { return /iPhone|iPad|iPod/i.test(ua); }
    function isAndroid() { return /Android/i.test(ua); }
    function isWindows() { return /Windows NT/i.test(ua); }
    function isMac() { return /Macintosh/i.test(ua); }

    let dest = links.desktop_browser;

    if (isIos()) dest = links.ios_app;
    else if (isAndroid()) dest = links.android_app;
    else if (isWindows()) dest = links.onedrive;
    else if (isMac()) dest = links.desktop_browser;

    manualA.href = dest;
    setTimeout(() => { window.location.replace(dest); }, 400);
  </script>
</body>
</html>
