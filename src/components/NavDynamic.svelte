<script>
  import { isActive, url, context } from "@sveltech/routify";

  $: ({ component } = $context);

  $: list = component.parent.children
    .filter(child => child.isIndexable => !child.isNonIndexable)
    .map(child => (child.index ? child.index : child))

</script>

<ul>
  {#each list as {shortPath, prettyName}}
    <li class:c-navigation__item--selected={$isActive(shortPath)}>
        <a href={$url(shortPath)}>{prettyName}</a>
    </li>
  {/each}
</ul>