<style>
  .news-list {
    max-width: 920px;
  }

  .news-list .news-item {
    padding: 28px 0;
    border-bottom: 1px solid var(--line);
  }

  .news-list .news-item:first-child {
    padding-top: 8px;
  }

  .news-list .news-item.has-image {
    display: grid;
    grid-template-columns: 280px minmax(0, 1fr);
    gap: 28px;
    align-items: center;
  }

  .news-list .news-item-image-link {
    display: block;
    border: 1px solid var(--line);
    border-radius: 8px;
    overflow: hidden;
    background: #f5f5f2;
    aspect-ratio: 3 / 2;
    transition: border-color 0.2s ease, transform 0.2s ease;
  }

  .news-list .news-item-image-link:hover {
    border-color: var(--accent-dark);
    transform: translateY(-2px);
  }

  .news-list .news-item-image {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .news-item-body .eyebrow {
    margin-bottom: 6px;
  }

  .news-list .news-item h2 {
    font-size: 1.45rem;
    line-height: 1.25;
    margin: 0 0 8px;
  }

  .news-list .news-item h2 a {
    color: var(--ink);
    text-decoration: none;
  }

  .news-list .news-item h2 a:hover {
    color: var(--accent-dark);
  }

  .news-item-body p:not(.eyebrow) {
    color: #56646c;
    font-size: 0.96rem;
    line-height: 1.6;
    margin: 0 0 12px;
  }

  @media (max-width: 700px) {
    .news-list .news-item.has-image {
      grid-template-columns: 1fr;
      gap: 16px;
    }
  }
</style>
