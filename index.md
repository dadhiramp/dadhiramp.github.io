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
    
    <style>
          div {
                height: 20px;
                width: 200px;
                background-color: lightblue;
                padding: 5px;
                margin: 0 0 10px 10px;
                text-align: center;
                
          }
      </style>
      
<body>
    <article>
        <h1>List of repos in github</h1>
    </article>
</body>


