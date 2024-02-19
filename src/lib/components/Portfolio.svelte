<script>
  // import data from '../../assets/portfolio';
  export let data = [];
</script>

<section id="portfolio" class='container py-5'>
  <h1>Portfolio</h1>
  <ul class="list row">
    {#each data as item}
      <li class="col-md-4">
        <img 
          src={item.imgUrl}
          alt={item.title}
        />
        <h4 class='mt-2'>{item.title}</h4>
        <p>{item.desc}</p>
        <a href="/detail/{item.id}" class="btn btn-primary mt-4">상세보기</a>
      </li>
    {/each}
  </ul>
</section>

<style lang='scss'>
  #portfolio {
    .list {
      li { margin-bottom: 100px;}
      img { 
        width: 100%;
        aspect-ratio: 4/3;
        object-fit: cover;
      }
    }
  }
</style>