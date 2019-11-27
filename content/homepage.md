<section id="main-desc">
  <div class="container">

    <div class="col-12">
      {{.Params.headerText | default .Site.Params.headerText | safeHTML}}
      {{.Params.headerParagraph | default .Site.Params.headerParagraph | safeHTML}}
      <hr>
    </div>

  </div>
</section>



<section id="product-slider">
  <div class="container">

    <div id="carouselExampleFade" class="col-12 carousel slide carousel-fade" data-ride="carousel">
      <div class="carousel-inner">
    {{ range  .Site.Params.product}}
        <div class="carousel-item active">
          <div class="row">
            <div class="col-md-8">
              <h3>Roblox</h3>
              <p>Roblox is the ultimate virtual universe that lets you play, create, and be anything you can imagine. Join millions of players and discover an infinite variety of immersive worlds created by a global community!</p>
              <p>In the mood for an epic role-playing adventure? Want to compete against rivals worldwide? Or do you just want to hang out and chat with your friends online? A growing library of worlds created by the community means there’s always
                something new and exciting for you to play every day.</p>
            </div>
            <img src="roblox-thumb.jpg" class="img-fluid col-md-4" alt="Roblox">
          </div>
        </div>
{{ end }}

      </div>
      <a class="carousel-control-prev" href="#carouselExampleFade" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleFade" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

  </div>
</section>

<section id="toplist">
  <div class="container">
    <div class="row m-0">

      <div class="col-12 m-0 mb-4">
        <hr>
      </div>

      <div class="col-12">
        <h2>Top 3 Products</h2>
      </div>
      {{ range .Site.Params.product}}
      <div class="col-lg-4">

        <img src="https://via.placeholder.com/300x200" class="w-100" title="product 1">
        <h3>{{ .slideHeadline | safeHTML }}</h3>
        <p>{{ .slideText| safeHTML}}</p>
        <a href="https://test.com" class="btn btn-primary" target="_blank">Buy here »</a>

      </div>


      {{ end }}



    </div>
  </div>
</section>
