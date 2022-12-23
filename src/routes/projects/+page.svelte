<script>
  import Project from '$lib/components/Project.svelte';
  import armadaUrl from './armada.png';
  import wreckbinUrl from './wreckbin.png';
  import shoppingCartUrl from './shoppingCart.png';
  import airlinesUrl from './airlines.png';
</script>

<svelte:head>
  <title>Joey Guillaume | Projects</title>
</svelte:head>

<div class="space-y-8">
  <!-- Armada -->
  <Project
    title="Armada"
    img={armadaUrl}
    web="https://team-armada.github.io/index.html"
    github="https://github.com/team-armada/"
  >
    <p class="text-justify">
      Armada is an open-source container orchestration tool that allows
      administrators to automate the configuration and deployment of development
      environments in the cloud.
    </p>

    <br />

    <p class="text-justify">
      Built with AWS, Docker, React, TypeScript, Express, and PostgreSQL.
    </p>
  </Project>

  <!-- WreckBin -->
  <Project title="WreckBin" img={wreckbinUrl}>
    <p class="text-justify">
      Wreckbin enables you to view and analyze the output of your webhooks by
      exposing an API endpoint that will record all relevant data.
    </p>

    <br />

    <p class="text-justify">
      Built with React, Express, MongoDB, and PostgreSQL.
    </p>
  </Project>

  <!-- Shopping Cart -->
  <Project title="Shopping Cart" img={shoppingCartUrl}>
    <p class="text-justify">
      A small e-commerce shopping-cart application created in order to practice
      working with React and Docker.
    </p>

    <br />

    <p class="text-justify">Built with Docker, React, and TypeScript.</p>
  </Project>

  <!-- Airlines-->
  <Project title="Airlines" img={airlinesUrl}>
    <p class="text-justify">
      A React application that displays and filters airline routes with
      pagination.
    </p>

    <br />

    <p class="text-justify">Built with React & JavaScript.</p>
  </Project>
</div>
