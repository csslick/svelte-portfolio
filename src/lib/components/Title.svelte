<script>
  import titleImg from '../../assets/title.png';
  export let title = '';
</script>

<section id="title">
  <div class='container'>
    <div class="detail row">
      <figure class="image col-md-6">
        <img src={titleImg} alt="title">
      </figure>
      <div class="text col-md-6">
        <h2>{@html title}</h2>
      </div>
    </div>
  </div>
</section>

<style lang="scss">
  #title  {
    background: #343434;
    color: #fff;
    height: 100dvh;
    .container {
      height: 100%;
      display: flex;
      align-items: center;
    }
    figure img {
      width: 100%;
    }
    .text {
      display: flex;
      justify-content: center;
      align-items: center;
      h2 {
        font-size: 3em;
      }
    }
  }
</style>