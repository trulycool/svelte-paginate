<script>
  import PaginationNav from './PaginationNav.svelte'
</script>

<div class="dark-pagination-nav">
  <PaginationNav
    {...$$props}
    on:setPage
  />
</div>

<!-- ### REF -->
<!-- background: hsl(200, 80%, 5%); -->

<style>
.dark-pagination-nav :global(.pagination-nav) {
  display: flex;
  justify-content: center;
  background: rgba(13, 99, 146, 0.445);
  border-radius: 3px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
}
.dark-pagination-nav :global(.option) {
  padding: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: 0.2s all ease-out;
  user-select: none;
  color: hsl(200, 90%, 90%);
}
.dark-pagination-nav :global(.option svg path) {
  fill: hsl(200, 90%, 90%);
}
.dark-pagination-nav :global(.option:first-child) {
  border-radius: 3px 0 0 3px;
}
.dark-pagination-nav :global(.option:last-child) {
  border-radius: 0 3px 3px 0;
}
.dark-pagination-nav :global(.option.number),
.dark-pagination-nav :global(.option.ellipsis) {
  padding: 10px 15px;
}
.dark-pagination-nav :global(.option:hover) {
  background: rgb(129, 10, 133);
  cursor: pointer;
}
.dark-pagination-nav :global(.option.active) {
  color: hsl(200, 100%, 50%);
}
</style>