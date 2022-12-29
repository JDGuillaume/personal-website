<script>
  import tippy from 'tippy.js';
  import { onMount } from 'svelte';
  import { linkedin, instagram, twitter, github } from '$lib/info';

  onMount(async () => {
    tippy('#github', {
      content: 'GitHub',
      placement: 'bottom',
      theme: 'teal',
      delay: [500, 200],
    });

    tippy('#linkedin', {
      content: 'LinkedIn',
      placement: 'bottom',
      theme: 'teal',
      delay: [500, 200],
    });

    tippy('#email', {
      content: 'Email',
      placement: 'bottom',
      theme: 'teal',
      delay: [500, 200],
    });
  });
</script>

{#if github}
  <a
    href={`https://github.com/${github}`}
    class="group"
    aria-label="Follow on GitHub"
  >
    <svg
      id="github"
      viewBox="0 0 24 24"
      aria-hidden="true"
      class="w-6 h-6 transition fill-zinc-500 group-hover:fill-zinc-600 dark:fill-zinc-400 dark:group-hover:fill-zinc-300"
    >
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M12 2C6.475 2 2 6.588 2 12.253c0 4.537 2.862 8.369 6.838 9.727.5.09.687-.218.687-.487 0-.243-.013-1.05-.013-1.91C7 20.059 6.35 18.957 6.15 18.38c-.113-.295-.6-1.205-1.025-1.448-.35-.192-.85-.667-.013-.68.788-.012 1.35.744 1.538 1.051.9 1.551 2.338 1.116 2.912.846.088-.666.35-1.115.638-1.371-2.225-.256-4.55-1.14-4.55-5.062 0-1.115.387-2.038 1.025-2.756-.1-.256-.45-1.307.1-2.717 0 0 .837-.269 2.75 1.051.8-.23 1.65-.346 2.5-.346.85 0 1.7.115 2.5.346 1.912-1.333 2.75-1.05 2.75-1.05.55 1.409.2 2.46.1 2.716.637.718 1.025 1.628 1.025 2.756 0 3.934-2.337 4.806-4.562 5.062.362.32.675.936.675 1.897 0 1.371-.013 2.473-.013 2.82 0 .268.188.589.688.486a10.039 10.039 0 0 0 4.932-3.74A10.447 10.447 0 0 0 22 12.253C22 6.588 17.525 2 12 2Z"
      />
    </svg>
  </a>
{/if}

{#if linkedin}
  <a
    id="linkedin"
    href={`https://linkedin.com/${linkedin}`}
    class="group"
    aria-label="Follow on LinkedIn"
  >
    <svg
      viewBox="0 0 24 24"
      class="w-6 h-6 transition fill-zinc-500 group-hover:fill-zinc-600 dark:fill-zinc-400 dark:group-hover:fill-zinc-300"
    >
      <path
        d="M18.335 18.339H15.67v-4.177c0-.996-.02-2.278-1.39-2.278-1.389 0-1.601 1.084-1.601 2.205v4.25h-2.666V9.75h2.56v1.17h.035c.358-.674 1.228-1.387 2.528-1.387 2.7 0 3.2 1.778 3.2 4.091v4.715zM7.003 8.575a1.546 1.546 0 01-1.548-1.549 1.548 1.548 0 111.547 1.549zm1.336 9.764H5.666V9.75H8.34v8.589zM19.67 3H4.329C3.593 3 3 3.58 3 4.297v15.406C3 20.42 3.594 21 4.328 21h15.338C20.4 21 21 20.42 21 19.703V4.297C21 3.58 20.4 3 19.666 3h.003z"
      />
    </svg>
  </a>
{/if}

<a
  href={`mailto:josephdguillaume@gmail.com`}
  class="group"
  aria-label="Send Email"
>
  <svg
    id="email"
    xmlns="http://www.w3.org/2000/svg"
    x="0px"
    y="0px"
    width="24"
    height="24"
    viewBox="0 0 64 64"
    class="w-6 h-6 transition fill-zinc-500 group-hover:fill-zinc-600 dark:fill-zinc-400 dark:group-hover:fill-zinc-300"
  >
    <path
      d="M 15 14 C 11.691 14 9 16.691 9 20 L 9 44 C 9 47.309 11.691 50 15 50 L 49 50 C 52.309 50 55 47.309 55 44 L 55 20 C 55 16.691 52.309 14 49 14 L 15 14 z M 16.349609 18 L 47.652344 18 L 35.443359 29.597656 C 33.513359 31.432656 30.486641 31.432656 28.556641 29.597656 L 16.349609 18 z M 13 20.337891 L 25.800781 32.498047 C 27.538781 34.149047 29.77 34.974609 32 34.974609 C 34.23 34.974609 36.460219 34.148047 38.199219 32.498047 L 51 20.337891 L 51 44 C 51 45.103 50.103 46 49 46 L 15 46 C 13.897 46 13 45.103 13 44 L 13 20.337891 z"
    />
  </svg>
</a>
