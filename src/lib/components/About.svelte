<script>
  import profile from '../../assets/profile.jpg';
  const skills = [
    { name: 'HTML', point: '90%' },
    { name: 'CSS', point: '80%' },
    { name: 'JAVASCRIPT', point: '50%' },
    { name: 'VUE', point: '75%' },
  ]
</script>

<section id="about" class="container py-5">
    <h1>About</h1>
    <div class="row gx-5">
      <figure class="col-md-6">
        <img src={profile} alt="profile">
        <figcaption>About Michael Kwon</figcaption>
      </figure>
      <p class="col-md-6">Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam animi amet repellat officia dignissimos voluptates. Quae cupiditate culpa adipisci quaerat facilis eos obcaecati quas, nemo nobis sapiente ipsa expedita tempore.</p>
    </div>

    <article class="row py-5">
      <h2>Skills</h2>
      <dl>
        {#each skills as item}
        <div>
          <dt class="lead">{item.name}</dt>
          <dd>
            <div class="progress" role="progressbar">
              <div 
                class="progress-bar text-end pe-3" 
                style="width: {item.point}"
              >{item.point}</div>
            </div> 
          </dd> 
        </div>
        {/each}
      </dl>
    </article>
</section>

<style lang="scss">
  figure img {
    width: 100%;
  }
  </style>