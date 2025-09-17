<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>美奈の日常</title>
  <link rel="stylesheet" href="style.css">
  <style>
    body {
      margin: 0;
      font-family: sans-serif;
      background-color: #e0f7fa; /* 水色背景 */
    }

    header {
      background-color: #2196f3; /* 青 */
      color: white; /* 白文字 */
      text-align: center;
      padding: 1em 0;
    }

    main {
      padding: 2em;
    }

    h2 {
      color: #1976d2; /* 見出しの青系 */
    }

    a {
      color: #0d47a1; /* リンクの濃い青 */
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    #blackout {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: black;
      z-index: 9999;
    }

    footer {
      background-color: #2196f3;
      color: white;
      text-align: center;
      padding: 1em 0;
      margin-top: 2em;
    }
  </style>
</head>
<body>
  <header>
    <h1>美奈の日常</h1>
  </header>

  <main>
    <h2>Minaです。</h2>
    <p>
      Dairy1 : いろいろな気持ちを残すために書こうと思います<br>  
    </p>

    <h2>ブログ一覧</h2>
    <ul>
      <li><a href="https://hikari-hikaru.github.io/Mina_dairyblog2/">2025年5月14日（dairy2ページ）</a></li>
    </ul>

    <!-- クリックで隠しリンクが出るトリガー -->
    <p id="trigger">（なんでもない文章）</p>
  </main>

  <footer>
    <p>© 2025 Mina's Diary</p>
  </footer>

  <div id="blackout"></div>

  <!-- 隠しリンク出現スクリプト -->
  <script>
    document.getElementById("trigger").addEventListener("click", function() {
      if (!document.getElementById("secretLink")) {
        const link = document.createElement("span");
        link.id = "secretLink";
        link.textContent = "ここから先へ";
        link.style.display = "block";
        link.style.marginTop = "10px";
        link.style.color = "#0d47a1";
        link.style.cursor = "pointer";
        
        // 2段階目（クリックで実際に飛ぶ）
        link.addEventListener("click", function() {
          window.location.href = "https://hikari-hikaru.github.io/hidden_page/"; // 隠しページURL
        });

        this.appendChild(link);
      }
    });
  </script>
</body>
</html>
