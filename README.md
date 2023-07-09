## Jekyll Theme
* **Jekyll theme documentation:** https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
* **Jekyll theme repo:** https://github.com/mmistakes/minimal-mistakes

## Chapter 1.1
* **Interview questions for developers:** https://business.linkedin.com/talent-solutions/resources/how-to-hire-guides/web-developer/interview-questions
* **Behavioral interview questions:** https://business.linkedin.com/talent-solutions/resources/interviewing-talent/behavioral-interview-questions-important-soft-skills

## Chapter 1.2 Installing Jekyll
* **Jekyll tutorial:** https://www.linkedin.com/learning/learning-static-site-building-with-Jekyll
* **Jekyll documentation**: https://jekyllrb.com/docs/

### Gemfile:
```yaml
gem "jekyll-remote-theme"
group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-algolia"
end
```

### _config.yml
```yaml
# Build settings
remote_theme: "mmistakes/minimal-mistakes@4.24.0"
plugins:
  - jekyll-remote-theme
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache
```

## Capter 1.3 Components of Jekyll
* **YAML:** https://www.linkedin.com/learning/cisco-devnet-associate-200-901-cert-prep-1-software-development-and-design/learn-about-yaml-and-its-usage
* **Markdown cheat sheet:** https://www.markdownguide.org/cheat-sheet/
* **Liquid cheat sheet:** https://www.shopify.com/partners/shopify-cheat-sheet

https://www.colourlovers.com/web/trends/websites

## Chapter 2.2 Adding Skills
Examples of skills you can list:

### Programming languages, Frameworks & libraries
* **Frameworks, libraries, and Programming languages –** JavaScript, TypeScript, HTML5, CSS, PHP, etc.
* **Technologies –** SQL Server, JAMStack, Gatsby, Netlify, GitHub, etc.
* **Website builders –** WordPress, Wix, Webflow, Jekyll, etc.
* **Specialty Skills–** Accessibility, Optimization, Dev ops
* **Software and tools–** Jira, Figma, Sketch, VSCode, GitHub, Terminal

### Soft Skills
* Communication, 
* Mentorship/leadership skills
* Collaboration
* Time Management
* Problem-Solving / Critical Thinking

### Basic table
```markdown
| Skill | Level |
| ---- | ---- |
| skill | level |
```

### YAML
```yaml
technical:
 - title: CSS and SCSS
   level: Intermediate
 - title: HTML5
   level: Intermediate
 - title: JavaScrpt
   level: Advanced
 - title: ReactJS
   level: Advanced

soft:
 - title: Writing
   level: Intermediate
 - title: Leadership
   level: Intermediate
```

## Chapter 2.3 Site Design
### Links
* https://color.adobe.com/trends

## Chapter 2.4 Customizing your site
### Custom.html
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link
    href="https://fonts.googleapis.com/css2?family=Rubik:wght@700&family=Waiting+for+the+Sunrise&family=Work+Sans:ital,wght@0,300;0,600;1,300&display=swap"
    rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/3.2.1/anime.min.js"></script>
```
### Custom.scss
```scss
--- 
#to make sure Jekyll reads this 
--- 

@import "default";
@import "author";
@import "footer";
@import "grid_layout";
@import "home";
@import "nav";
@import "post";
@import "taxonomy";
```

### _config
```yml
header_scripts:
 - assets/css/custom
footer_scripts:
  - /assets/js/animation.js
```

### anime.js
```javascript
anime({
    targets: ".grid__item",
    scale: [
        { value: 1, duration: 800 },
        { value: 1.1, duration: 200 },
        { value: 1, duration: 800 },
    ],
    easing: "easeInOutSine",
    delay: function (el, i, l) {
        return i * 200;
    },
    loop: false,
});
```

## 3.2 Adding Categories Pages

### Layout changes
```html
  {% assign sorted_tags = site.tags | sort %}
  {% for tag in sorted_tags %}
  {% assign cat_tags = tag[1] | where: "categories", "work" | sort %}
  {% if cat_tags != empty %}
```

## 3.3 Adding images

```markdown
# Hi! I'm Leigh Stewardson. 
I am a self-taught programmer, instructor, product manager, game developer, painter and writer. Check out some of my favorite articles and projects below or go to [**My Work**](/mywork) or [**My Writing**](/mywriting) to see a categorized list.
```
