<script>
  export let title;
  export let img = undefined;
  export let web = undefined;
  export let github = undefined;

  let links = [
    web && {
      url: web,
      label: 'Website',
    },
    github && {
      url: github,
      label: 'GitHub',
    },
  ].filter(Boolean);
</script>

<div
  class="flex flex-col md:flex-row items-start space-x-0 md:space-x-8 pb-8 border-b border-slate-300 dark:border-slate-700"
>
  <div class="order-2 md:order-1 !mx-auto w-auto md:md-0 md:w-1/3">
    {#if img}
      <img
        alt={`${title} Screenshot`}
        src={img}
        class="!mb-0 !mt-0 max-h-80 "
      />
    {/if}
  </div>
  <div class="order-1 md:order-2 w-auto md:w-2/3">
    <h2 id={title} class="text-3xl sm:text-4xl !mt-0 !mb-0 md:block">
      <a href={`#${title}`}>{title}</a>
    </h2>
    <div class="flex justify-start !mt-2 !mb-2 gap-2">
      {#each links as link}
        <a
          href={link.url}
          class="inline-flex items-center tracking-wide font-medium text-teal-500"
          style="text-decoration: underline;"
        >
          {link.label}
        </a>
      {/each}
    </div>
    <p>
      <slot />
    </p>
  </div>
</div>
