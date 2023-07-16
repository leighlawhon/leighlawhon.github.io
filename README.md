## Jekyll Theme
* [Jekyll theme documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
* [ekyll theme repo](https://github.com/mmistakes/minimal-mistakes)

## Chapter 1.1 Purpose of a Portfolio
* [Interview questions for developers](https://business.linkedin.com/talent-solutions/resources/how-to-hire-guides/web-developer/interview-questions)
* [Behavioral interview questions](https://business.linkedin.com/talent-solutions/resources/interviewing-talent/behavioral-interview-questions-important-soft-skills)

## Chapter 1.2 Installing Jekyll
* [Jekyll tutorial](https://www.linkedin.com/learning/learning-static-site-building-with-Jekyll)
* [Jekyll documentation](https://jekyllrb.com/docs/)

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

## Chapter 1.3 Going Live On GitHub
No notes.

## Chapter 1.4 Components of Jekyll

### Links
* [Learn more about YAML](https://www.linkedin.com/learning/cisco-devnet-associate-200-901-cert-prep-1-software-development-and-design/learn-about-yaml-and-its-usage)
* [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/)
* [Liquid cheat sheet](https://www.shopify.com/partners/shopify-cheat-sheet)

## Chapter 2.1 Writing a Bio
No notes.

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
* [Adobe Color](https://color.adobe.com/trends)
* [Colour Lovers](https://www.colourlovers.com/web/trends/websites)

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

## Chapter 3.1 Building Layouts
No notes.

## Chapter 3.2 Adding Categories and Tags

### Layout changes
```html
  <ul class="taxonomy__index">
    {% assign sorted_tags = site.tags | sort %}
    {% for tag in sorted_tags %}
    {% assign cat_tags = tag[1] | where: "categories", "article" | sort %}
    {% if cat_tags != empty %}
    <li>
        <a href="#{{ tag[0] | slugify }}">
            <strong>{{ tag[0] }}</strong> <span class="taxonomy__count">{{ i }}</span>
        </a>
    </li>
    {% endif %}
    {% endfor %}
</ul>

{% assign entries_layout = page.entries_layout | default: 'grid' %}
{% for tag in sorted_tags %}
{% assign cat_tags = tag[1] | where: "categories", "article" | sort %}
{% if cat_tags != empty %}
<section id="{{ tag[0] | slugify | downcase }}" class="taxonomy__section">
    <h2 class="archive__subtitle">{{ tag[0] }}</h2>
    <div class="entries-{{ entries_layout }}">
        {% for post in tag.last %}
        {% include archive-single.html type=entries_layout %}
        {% endfor %}
    </div>
    <a href="#page-title" class="back-to-top">{{ site.data.ui-text[site.locale].back_to_top | default: 'Back to Top' }}
        &uarr;</a>
</section>
{% endif %}
{% endfor %}
```

## Chapter 3.3 Adding images

### Adding Images to the Home Page
```markdown
![my avatar](assets/images/bioshot.jpeg){: .avatar} 
# Hi! I'm Leigh Stewardson. 
I am a self-taught programmer, instructor, product manager, game developer, painter and writer. Check out some of my favorite articles and projects below or go to [**My Work**](/mywork) or [**My Writing**](/mywriting) to see a categorized list.
```

### Adding images to an Article
```markdown
header:
  overlay_image: https://images.unsplash.com/photo-1502691876148-a84978e59af8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80
  teaser: https://images.unsplash.com/photo-1502691876148-a84978e59af8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80
  
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
```

## Chapter 3.4 Project Writeups and Articles
Read articles provided

## Chapter 4.1 Working in Codespaces: Shuffling Cards
Create repo from zipped project `Shuffling_Cards` in the `zipped_file` folder.

### Additional Tutorials
* [GitHub Codespaces for Students](https://www.linkedin.com/learning/github-codespaces-for-students/)
* [>earnoing GitHub Codespaces for Enterprise](https://www.linkedin.com/learning/learning-github-codespaces-for-enterprise)

## Chapter 4.2 Working in Codespaces: Piece of Cake
Create repo from zipped project `Piece_of_Cake` in the `zipped_file` folder.

## Conclusion
Here are a list of projects you might want to consider for your portfolio:
* [Getting Started with DevOps](https://www.linkedin.com/learning/paths/getting-started-with-devop)
* [Become a JavaScript Developer](https://www.linkedin.com/learning/paths/become-a-javascript-developer)
* [Getting Started with Software Testing](https://www.linkedin.com/learning/paths/getting-started-with-software-testing)
* [Advance your Node.js Skills](https://www.linkedin.com/learning/paths/advance-your-node-js-skills)
* [Become a Full-stack Web Developer](https://www.linkedin.com/learning/paths/become-a-full-stack-web-developer)
