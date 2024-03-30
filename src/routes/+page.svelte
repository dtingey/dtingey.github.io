<script>
  import GithubIcon from '$lib/GithubIcon.svelte';
  import LinkedinIcon from '$lib/LinkedinIcon.svelte';
  
  let skills = ['ML Engineering', 'Deep Learning', 'Web Development', 'Software Engineering', 'Data Science'];
  let experiences = [
    { year: '2023-Present', role: 'Junior Data Scientist', company: 'ZONTAL Inc.' },
    { year: '2022-2023', role: 'Machine Learning TA', company: 'The Coding School' },
    { year: '2021-2023', role: 'Undergraduate Researcher - Computational Biology', company: 'BYU Department of Physics' },
    { year: '2019-2021', role: 'Missionary - Volunteer', company: 'The Church of Jesus Christ of Latter-day Saints' }
  ];
  let publications = [
    { 
        title: 'TrIP─Transformer Interatomic Potential Predicts Realistic Energy Surface Using Physical Bias',
        authors: 'BE Hedelius, D Tingey, D Della Corte',
        journal: 'Journal of Chemical Theory and Computation', 
        link: 'https://pubs.acs.org/doi/abs/10.1021/acs.jctc.3c00936' }
  ];
  let projects = [
    {
        title: 'INSyT',
        long_title: 'Onnovative Network Security Technologies',
        description: 'A network security detection system that monitors network and system logs, identifies attacks, and offers suggestions for how to respond.',
        link: 'https://github.com/Isaacwilliam4/INSyT',
        code_link: 'https://github.com/Isaacwilliam4/INSyT'
    },
    {
        title: 'OBi-WAN',
        long_title: 'Open Biology Workflow Automation Network',
        description: 'A computational biology assistant that performs experimentation, data analysis, and visualization tasks.',
        link: 'https://github.com/dtingey/obi-wan',
        code_link: 'https://github.com/dtingey/obi-wan'
    },
    { 
        title: 'TrIP',
        description: 'A transformer-based interatomic potential for molecular dynamics simulations.',
        link: 'https://github.com/dellacortelab/trip',
        code_link: 'https://github.com/dellacortelab/trip'
    },
    {
        title: 'RetNet Validation',
        description: 'Validating the RetNet model architecture and comparing it to other SoTA model architectures.',
        link: 'https://github.com/DRAGNLabs/301r_retnet',
        code_link: 'https://github.com/DRAGNLabs/301r_retnet'
    },
    {
        title: 'Scripture RAG',
        description: 'A RAGatoullie based chatbot that answers questions using the scriptures.',
        link: 'https://github.com/dtingey',
        code_link: 'https://github.com/dtingey'
    },
  ]
</script>

<div class="container mx-auto px-4">
  <section class="text-center py-12">
    <h2 class="text-4xl font-bold">Hello, I'm <span class="text-blue-500">Damon Tingey</span></h2>
    <p class="text-xl mt-4">I am a Full Stack Engineer who specializes in ML applications and products.</p>
  </section>

  <section class="py-8">
    <h3 class="text-3xl font-semibold mb-6">Skills</h3>
    <div class="flex justify-center gap-4 flex-wrap">
      {#each skills as skill}
        <span class="inline-block bg-blue-100 text-blue-800 px-4 py-2 rounded-full">{skill}</span>
      {/each}
    </div>
  </section>

  <section class="py-8">
    <h3 class="text-3xl font-semibold mb-6">Work Experience</h3>
    <div class="space-y-3">
      {#each experiences as experience}
        <div class="bg-gray-100 p-4 rounded-lg">
          <p class="font-bold">{experience.year}</p>
          <p>{experience.role} at {experience.company}</p>
        </div>
      {/each}
    </div>
  </section>

  <section class="py-8">
    <h3 class="text-3xl font-semibold mb-6">Publications</h3>
    <div class="space-y-3">
      {#each publications as publication}
        <a href={publication.link} class="block bg-gray-100 p-4 rounded-lg mb-4 transform transition-transform duration-200 ease-in-out hover:-translate-y-1">
          <p class="font-bold">{publication.title}</p>
          <p>{publication.authors}</p>
          <p>{publication.journal}</p>
        </a>
      {/each}
    </div>
  </section>

  <section class="py-8">
    <h3 class="text-3xl font-semibold mb-6">Projects</h3>
    <div class="grid grid-cols-3 gap-4">
      {#each projects as project}
        <div class="bg-gray-100 p-4 rounded-lg transform transition-transform duration-200 ease-in-out hover:-translate-y-1 flex-col justify-between">
          <a href={project.link} class="block mb-4">
            <p class="font-bold">{project.title}</p>
            <p>{project.description}</p>
          </a>
          <a href={project.code_link} class="inline-flex items-center justify-center px-4 py-2 bg-gray-500 text-white rounded hover:bg-gray-700 transition ease-in-out duration-150">
            <GithubIcon props={{class: "h-6 w-6"}} />
          </a>
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


