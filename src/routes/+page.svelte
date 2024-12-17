<script>
  import Semesters from "$lib/organisms/Semesters.svelte";
  import Program from "$lib/organisms/Program.svelte";
  import Snowfall from "$lib/atoms/snowfall.svelte";
  let { data } = $props();
  const { title, subtitle, content, semesters } = data;
</script>
<Snowfall />
<Program {title} {content} />
<Semesters {semesters} {subtitle} />