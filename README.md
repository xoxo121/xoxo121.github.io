# xoxo121.github.io

Personal academic website of Rahul Vimalkanth — [https://xoxo121.github.io/](https://xoxo121.github.io/)

## Structure

```
index.html            page content (bio, news, research, experience)
stylesheet.css        base typography and link colors
css/home.css          layout, theming, badges, news, footer
images/headshots/     profile photo
images/research/      paper thumbnails
images/experience/    organization logos
images/favicon/       favicons
```

## Editing

- **Adding a paper:** copy one of the entry tables inside `<div id="research-list">` in `index.html`, then drop a thumbnail into `images/research/`. Venue badges are the `.badge-*` classes in `css/home.css`; add a new one there if your venue isn't covered. Papers without a public link or figure go in the "Work in Submission" section, which uses full-width `.cell-full` entries instead of a thumbnail column.
- **Adding news:** add a `<div class="news-item">` at the top of `.news-list`. The list scrolls after ~5 items.
- **Adding experience:** copy an entry table from the Experience section. Logos live in `images/experience/` and sit inside a `.logo-frame`, which keeps a white plate behind them so dark marks stay visible in dark mode.
- **Theses and Patents:** commented-out scaffolding for both sections sits at the end of the main content in `index.html`. Uncomment to enable.

## Credits

Template adapted from [Chris Agia](https://github.com/agiachris/agiachris.github.io), which builds on [Jon Barron](https://github.com/jonbarron/jonbarron_website).
