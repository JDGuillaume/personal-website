<script>
  import Project from '$lib/components/Project.svelte';
  import armadaUrl from './armada.png';
</script>

<svelte:head>
  <title>Joey Guillaume | Projects</title>
</svelte:head>

<div class="space-y-8">
  <Project
    title="Armada"
    img={armadaUrl}
    web="https://team-armada.github.io/index.html"
    github="https://github.com/team-armada/"
  >
    Armada is an open-source container orchestration tool that allows
    administrators to automate the configuration and deployment of development
    environments in the cloud.
  </Project>
</div>
