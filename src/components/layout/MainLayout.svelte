<script lang="ts">
  import * as Sidebar from "$lib/components/ui/sidebar/index.js";
  import AppSidebar from "$lib/components/app-sidebar.svelte";

  let { children } = $props();
</script>

<div class="flex h-screen">
  <Sidebar.Provider>
    <AppSidebar />
    <main class="flex-1">
      <Sidebar.Trigger />
      {@render children?.()}
    </main>
  </Sidebar.Provider>
</div>
