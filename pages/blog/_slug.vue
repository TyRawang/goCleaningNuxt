<template>
  <section>
    <TheBlogDetailBanner />
    <div class="clearfix"></div>
    <TheBlogDetailBody2
      :posts="posts"
      :article="article"
      :categories="categories"
    />
    <!--    <nuxt-content :document="article" />-->
    <div class="clearfix"></div>
  </section>
</template>

<script>
import TheBlogDetailBanner from "@/components/blog/TheBlogDetailBanner";
import TheBlogDetailBody2 from "@/components/blog/TheBlogDetailBody2";
export default {
  head() {
    return {
      title: this.article.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.article.seo.metaDescription,
        },
        {
          hid: "og:title",
          property: "og:title",
          content: this.article.seo.metaTitle,
        },
        {
          hid: "og:description",
          property: "og:description",
          content: this.article.seo.metaDescription,
        },
        {
          hid: "twitter:title",
          name: "twitter:title",
          content: this.article.seo.metaTitle,
        },
        {
          hid: "twitter:description",
          name: "twitter:description",
          content: this.article.seo.metaDescription,
        },
      ],
    };
  },

  components: {
    TheBlogDetailBanner,
    TheBlogDetailBody2,
  },

  async asyncData({ $strapi, params, error }) {
    let article = {};
    let posts = [];
    let categories = [];
    // console.log(params)
    posts = await $strapi.find("articles");
    categories = await $strapi.find("categories");
    const articleData = await $strapi.find("articles", { slug: params.slug });
    console.log("articleData", articleData);
    if (articleData.length > 0) {
      article = articleData[0];
    }

    return { posts, categories, article };
  },
};
</script>

<style>
.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
</style>
