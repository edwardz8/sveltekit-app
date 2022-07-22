<script lang="ts">
    export let name: IconType;
    export let width: string;
    export let height: string;

    type IconType = keyof typeof icons;

    const icons = {
        home: {
            box: 24,
            svg: `
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
        />
      `,
        },
        profile: {
            box: 24,
            svg: `
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
        />
      `,
        },
        about: {
            box: 24,
            svg: `
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M8 12h.01M12 12h.01M16 12h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
        />
      `,
        },
        like: {
            box: 24,
            svg: `
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="1"
          d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
        />
      `,
        },
        permalink: {
            box: 24,
            svg: `
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="1"
            d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
          />
        `,
        },
        remove: {
            box: 24,
            svg: `
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="1"
            d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
          />
        `,
        },
    };

    const icon = icons[name];
</script>

<svg
    class={$$props.class}
    {width}
    {height}
    viewBox="0 0 {icon.box} {icon.box}"
    fill="none"
    stroke="currentColor"
>
    {@html icon.svg}
</svg>
