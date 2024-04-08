<script>
  export let postImage,
    title,
    publish,
    readTime,
    description,
    quote,
    author,
    socials;
</script>

<section class="blog-post section-header-offset">
  <div class="blog-post-container container">
    <div class="blog-post-data">
      <h3 class="title blog-post-title">{title}</h3>
      <div class="article-data">
        <span>{publish.date}</span>
        <span class="article-data-spacer"></span>
        <span>{readTime}</span>
      </div>
      <img src={postImage.url} alt={postImage.alt} />
    </div>

    <div class="container">
      <p>
        {#each description as d}
          <p>{@html d.paragraph}</p>
        {/each}
      </p>

      <blockquote class="quote">
        <p>
          <span><i class="ri-double-quotes-l"></i></span>
          {quote}<span><i class="ri-double-quotes-r"></i></span>
        </p>
      </blockquote>

      <p>
        {#each description as d}
        <p>{@html d.paragraph}</p>
      {/each}
      </p>

      <div class="author d-grid">
        <div class="author-image-box">
          <img src="media/images/author.jpg" alt="" class="article-image" />
        </div>
        <div class="author-about">
          <h3 class="author-name">{author.name}e</h3>
          <p>{author.description}</p>
          <ul class="list social-media">
            <li class="list-item">
              <a href={socials.instagram} class="list-link"
                ><i class="ri-instagram-line"></i></a
              >
            </li>
            <li class="list-item">
              <a href={socials.facebook} class="list-link"
                ><i class="ri-facebook-circle-line"></i></a
              >
            </li>
            <li class="list-item">
              <a href={socials.x} class="list-link"
                ><i class="ri-twitter-line"></i></a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>
