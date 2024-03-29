<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<script>
  let projects = [
    { name: "Project 1", description: "This is a description of project 1.", link: "#" },
    { name: "Project 2", description: "This is a description of project 2.", link: "#" },
    { name: "Project 3", description: "This is a description of project 3.", link: "#" }
  ];
</script>

<style>
  .container {
    max-width: 800px;
    margin: auto;
    padding: 20px;
  }
  .project {
    margin-bottom: 20px;
  }
  .project h2 {
    margin: 0;
  }
  .project p {
    margin: 5px 0;
  }
  .project a {
    color: #007BFF;
    text-decoration: none;
  }
</style>

<div class="container">
  <h2>About Me</h2>
  <p>Hello! I'm a software developer with a passion for building web applications. I specialize in Svelte and have experience with other modern JavaScript frameworks.</p>
  
  <h2>Projects</h2>
  {#each projects as {name, description, link}}
    <div class="project">
      <h3>{name}</h3>
      <p>{description}</p>
      <a href="{link}">View Project</a>
    </div>
  {/each}
</div>

