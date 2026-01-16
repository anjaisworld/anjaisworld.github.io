---
layout: default
title: Blog
---

<section class="blog-section">
    <div class="container">
        <h1 class="section-title">Anjai's Adventures Blog</h1>
        <p style="text-align: center; margin-bottom: 3rem; color: var(--cream);">
            Explore my latest adventures, discoveries, and stories from the mystical world of Zelda and Minecraft.
        </p>
        
        <div class="blog-posts-grid">
            {% for post in site.posts %}
            <div class="blog-card">
                <h2 class="blog-card-title">
                    <a href="{{ post.url | relative_url }}" style="color: inherit; text-decoration: none;">
                        {{ post.title }}
                    </a>
                </h2>
                <p class="blog-card-excerpt">{{ post.excerpt }}</p>
                <div class="blog-card-date">
                    📅 {{ post.date | date: "%B %d, %Y" }}
                </div>
            </div>
            {% endfor %}
        </div>

        {% if site.posts.size == 0 %}
        <div style="text-align: center; padding: 3rem; color: var(--cream);">
            <p>No blog posts yet. Check back soon for exciting adventures!</p>
        </div>
        {% endif %}
    </div>
</section>

<style>
.blog-section {
    padding: 5rem 2rem;
    background: rgba(45, 80, 22, 0.3);
}

.blog-card a {
    transition: color 0.3s ease;
}

.blog-card a:hover {
    color: var(--lime-green) !important;
}
</style>
