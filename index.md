<body>
    <article>
        <h1>List of repos in github</h1>
          <script>
      fetch('https://api.github.com/users/dadhiramp/repos')
        .then(res => res.json())
        .then(res => {
            res.forEach(repo => {
                const repoInfo = document.createElement('div');
                repoInfo.innerHTML += `${repo.name}`;
                document.body.append(repoInfo);
            })
        });
    </script>
    </article>
</body>


