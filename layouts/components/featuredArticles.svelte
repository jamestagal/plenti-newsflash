<script>
  import { readable } from "svelte/store";
  export let allContent,
    title,
    headline01,
    headline02,
    headline03,
    headline04,
    headline05;
  let blogs = allContent.filter((content) => content.type === "blog");
</script>

<!-- Featured articles -->
<section class="featured-articles section section-header-offset">
  <div class="featured-articles-container container d-grid">
    <div class="featured-content d-grid">
      <div class="headline-banner">
        <h3 class="headline fancy-border">
          <span class="place-items-center">{title}</span>
        </h3>
          <div class="news">
            <span class="news-single active headline-description"
              >{headline01}</span
            >
            <span class="news-single headline-description">{headline02}</span
            >
            <span class="news-single headline-description">{headline03}</span
            >
            <span class="news-single headline-description">{headline04}</span
            >
            <span class="news-single headline-description">{headline05}</span
            >
          </div>
      </div>
      {#each blogs as blog, i}
        {#if blog.fields.featured.main === true}
          <a
            href={blog.path}
            class="article featured-article featured-article-{i + 1}"
          >
            <img
              src={blog.fields.postImage.url}
              alt={blog.fields.postImage.alt}
              class="article-image"
            />
            <span class="article-category">{blog.fields.category.name}</span>

            <div class="article-data-container">
              <div class="article-data">
                <span>{blog.fields.publish.date}</span>
                <span class="article-data-spacer"></span>
                <span>{blog.fields.readTime}</span>
              </div>

              <h3 class="title article-title">{blog.fields.title}</h3>
            </div>
          </a>

          <!-- <a href="blog/post-2" class="article featured-article featured-article-2">
        <img
          src="media/images/featured/featured-2.jpg"
          alt=""
          class="article-image"
        />
        <span class="article-category">Food</span>

        <div class="article-data-container">
          <div class="article-data">
            <span>Dec 6th 2021</span>
            <span class="article-data-spacer"></span>
            <span>4 Min read</span>
          </div>

          <h3 class="title article-title">Fine dining 101</h3>
        </div>
      </a>

      <a href="blog/post-3" class="article featured-article featured-article-3">
        <img
          src="media/images/featured/featured-3.jpg"
          alt=""
          class="article-image"
        />
        <span class="article-category">Health</span>

        <div class="article-data-container">
          <div class="article-data">
            <span>Dec 5th 2021</span>
            <span class="article-data-spacer"></span>
            <span>5 Min read</span>
          </div>

          <h3 class="title article-title">Natural fat burner</h3>
        </div>
      </a> -->
        {/if}
      {/each}
    </div>

    <div class="sidebar d-grid">
      <h3 class="title featured-content-title">Trending news</h3>

      <a href="." class="trending-news-box">
        <div class="trending-news-img-box">
          <span class="trending-number place-items-center">01</span>
          <img
            src="media/images/trending/trending_1.jpg"
            alt=""
            class="article-image"
          />
        </div>

        <div class="trending-news-data">
          <div class="article-data">
            <span>23 Dec 2021</span>
            <span class="article-data-spacer"></span>
            <span>3 Min read</span>
          </div>

          <h3 class="title article-title">Sample article title</h3>
        </div>
      </a>

      <a href="." class="trending-news-box">
        <div class="trending-news-img-box">
          <span class="trending-number place-items-center">02</span>
          <img
            src="media/images/trending/trending_2.jpg"
            alt=""
            class="article-image"
          />
        </div>

        <div class="trending-news-data">
          <div class="article-data">
            <span>23 Dec 2021</span>
            <span class="article-data-spacer"></span>
            <span>3 Min read</span>
          </div>

          <h3 class="title article-title">Sample article title</h3>
        </div>
      </a>

      <a href="." class="trending-news-box">
        <div class="trending-news-img-box">
          <span class="trending-number place-items-center">03</span>
          <img
            src="media/images/trending/trending_3.jpg"
            alt=""
            class="article-image"
          />
        </div>

        <div class="trending-news-data">
          <div class="article-data">
            <span>23 Dec 2021</span>
            <span class="article-data-spacer"></span>
            <span>3 Min read</span>
          </div>

          <h3 class="title article-title">Sample article title</h3>
        </div>
      </a>

      <a href="." class="trending-news-box">
        <div class="trending-news-img-box">
          <span class="trending-number place-items-center">04</span>
          <img
            src="media/images/trending/trending_4.jpg"
            alt=""
            class="article-image"
          />
        </div>

        <div class="trending-news-data">
          <div class="article-data">
            <span>23 Dec 2021</span>
            <span class="article-data-spacer"></span>
            <span>3 Min read</span>
          </div>

          <h3 class="title article-title">Sample article title</h3>
        </div>
      </a>

      <a href="." class="trending-news-box">
        <div class="trending-news-img-box">
          <span class="trending-number place-items-center">05</span>
          <img
            src="media/images/trending/trending_5.jpg"
            alt=""
            class="article-image"
          />
        </div>

        <div class="trending-news-data">
          <div class="article-data">
            <span>23 Dec 2021</span>
            <span class="article-data-spacer"></span>
            <span>3 Min read</span>
          </div>

          <h3 class="title article-title">Sample article title</h3>
        </div>
      </a>
    </div>
  </div>
</section>

