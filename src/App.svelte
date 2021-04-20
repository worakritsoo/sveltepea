<script>
  import { onMount } from 'svelte';
  let data;
  import Card from './Card.svelte';
  import Header from './Header.svelte';
  import Search from './Search.svelte';
  import Link from './routes/components/linkCard.svelte';

  onMount(async () => {
    data = await fetch(
      'https://dmsxupload.pea.co.th/tests3/api/exec/get_data?procedure=list_asset_owner&parameter=L301023000;0;0'
    ).then((x) => x.json());
  });
  const options = [
    { route: 'ลิ้ง', component: Link },
    { route: 'ค้นหา', component: Search },
  ];

  let selected = options[0];
</script>

<main>
  <Header />
  <section>
    <Search />
  </section>
</main>
