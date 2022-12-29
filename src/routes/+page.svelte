<script>
  import ArrowRightIcon from '$lib/components/ArrowRightIcon.svelte';
  import Project from '$lib/components/Project.svelte';
  // import PostsList from '$lib/components/PostsList.svelte';
  import SocialLinks from '$lib/components/SocialLinks.svelte';
  import { avatar, bio, name } from '$lib/info.js';
  import armadaUrl from './projects/armada.png';

  /** @type {import('./$types').PageData} */
  export let data;
</script>

<svelte:head>
  <title>{name}</title>
  <meta name="description" content={bio} />
</svelte:head>

<div class="flex flex-col flex-grow gap-8 pb-16">
  <!-- bio -->
  <section class="flex flex-col items-center gap-16 pt-8 pb-16">
    <div class="flex flex-col items-center w-full gap-6 rounded-lg">
      <img
        src={avatar}
        alt={name}
        class="mx-auto rounded-full w-36 h-36 ring-2 ring-zinc-200 dark:ring-zinc-700"
      />
      <div class="flex gap-6">
        <SocialLinks />
      </div>
      <div>
        <a href={'/resume.pdf'} target="_blank" rel="noreferrer"
          ><button
            class="bg-teal-500 hover:bg-teal-700 text-white font-bold py-2 px-4 rounded "
          >
            View Resume
          </button>
        </a>
      </div>
      <p class="text-base text-zinc-600 dark:text-zinc-400 text-justify">
        {bio}
      </p>
      <p
        class="text-base text-zinc-600 dark:text-zinc-400"
        style="text-align: justify;"
      >
        I recently co-created
        <a
          class="font-medium text-teal-500"
          href="https://team-armada.github.io/index.html">Armada</a
        >, an open-source container orchestration tool that allows
        administrators to automate the configuration and deployment of
        development environments in the cloud.

        <br />
        <br />

        Check out some of my latest
        <a class="font-medium text-teal-500" href="/projects ">projects</a> and see
        how I've brought my ideas to life.
      </p>
    </div>
  </section>
  <section class="w-full">
    <div class="flex items-center justify-between gap-4 mb-8">
      <h2
        class="text-sm font-medium sm:text-base text-zinc-500 dark:text-zinc-400"
      >
        Project Spotlight
      </h2>
      <a
        href="/projects"
        class="flex items-center gap-1 text-sm font-medium text-teal-500"
        >View All Projects<ArrowRightIcon class="w-4 h-4" /></a
      >
    </div>
    <!-- Armada -->
    <Project
      title="Armada"
      img={armadaUrl}
      web="https://team-armada.github.io/index.html"
      github="https://github.com/team-armada/"
    >
      <p class="text-justify">
        Armada is an open-source container orchestration tool that allows
        administrators to automate the configuration and deployment of
        development environments in the cloud.
      </p>

      <br />

      <p class="text-justify">
        Built with AWS, Docker, React, TypeScript, Express, and PostgreSQL.
      </p>

      <br />

      <a
        href="https://team-armada.github.io/case-study.html"
        target="_blank"
        rel="noreferrer"
        ><button
          class="bg-teal-500 hover:bg-teal-700 text-white font-bold py-2 px-4 rounded "
        >
          Read the Case Study
        </button>
      </a>
    </Project>
  </section>
</div>

<style>
  a {
    text-decoration: underline;
  }
</style>
