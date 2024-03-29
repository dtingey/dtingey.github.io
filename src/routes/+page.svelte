<script>
  let skills = ['ML Engineering', 'Deep Learning', 'Web Development', 'Software Engineering', 'Data Science'];
  let experiences = [
    { year: '2023-Present', role: 'Junior Data Scientist', company: 'ZONTAL Inc.' },
    { year: '2021-2023', role: 'Undergraduate Researcher', company: 'BYU Department of Physics' },
    { year: '2022-2023', role: 'Machine Learning TA', company: 'The Coding School' }
  ];
</script>

<div class="container mx-auto px-4">
  <section class="text-center py-12">
    <h2 class="text-4xl font-bold">Hello, I'm <span class="text-blue-500">Damon Tingey</span></h2>
    <p class="text-xl mt-4">I am a ML Engineer who specializes in web applications integration and development.</p>
  </section>

  <section class="py-12">
    <h3 class="text-3xl font-semibold mb-6">Skills</h3>
    <div class="flex justify-center gap-4 flex-wrap">
      {#each skills as skill}
        <span class="inline-block bg-blue-100 text-blue-800 px-4 py-2 rounded-full">{skill}</span>
      {/each}
    </div>
  </section>

  <section class="py-12">
    <h3 class="text-3xl font-semibold mb-6">Experience</h3>
    <div class="space-y-4">
      {#each experiences as experience}
        <div class="bg-gray-100 p-4 rounded-lg">
          <p class="font-bold">{experience.year}</p>
          <p>{experience.role} at {experience.company}</p>
        </div>
      {/each}
    </div>
  </section>

  <section class="text-center py-12">
    <h3 class="text-3xl font-semibold">Let's Connect</h3>
    <p class="mt-4">Feel free to reach out through any of the platforms below.</p>
    <div class="flex justify-center gap-4 mt-4">
      <a href="https://linkedin.com/in/damon-tingey" class="text-blue-600">LinkedIn</a>
      <a href="https://github.com/dtingey" class="text-gray-900">GitHub</a>
      <a href="mailto:damon.tingey@gmail.com" class="text-red-500">Email</a>
    </div>
  </section>
</div>


