<script>
  import { onMount } from "svelte";

  export let id = ''; // 라우터에서 넘어온 id를 받아옴
  export let data = []; // 라우터에서 넘어온 data를 받아옴

  onMount(() => {
    console.log(id, data);
  });
 </script>

<section id="detail" class="container py-5">
  <h1>Detail</h1>
  <p>{id}</p>
  <h2>{data[id].title}</h2>
  <figure>
    <img src={data[id].imgUrl} alt={data[id].title} />
  </figure>
  <p>{data[id].desc}</p>
  <small class='text-secondary text-uppercase'>{data[id].skills}</small>
  <div class='my-4'>
    <a href={data[id].link} class='btn btn-primary' target='_blank'>홈페이지</a>
  </div>
</section>

<style lang="scss">
  figure {
    img { 
      width: 100%;
      aspect-ratio: 16/9;
      object-fit: cover;
    }
  }
</style>