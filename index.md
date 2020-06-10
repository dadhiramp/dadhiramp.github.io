<body>
    <article>
        <h1>List of repos in github</h1>
          <script>
              const article = document.querySelector('article');
      fetch('https://api.github.com/users/dadhiramp/repos')
        .then(res => res.json())
        .then(res => {
            res.forEach(repo => {
                const repoInfo = document.createElement('div');
                repoInfo.innerHTML += `${repo.name}`;
                article.appendChild(repoInfo);
            })
        });
    </script>
    </article>
</body>


