## Welcome to Nala Page on GitHub

This is [Nala's Page on GitHub](https://nomagev.github.io) where I try, somehow, to create a very basic, Jekyll structure-based site.

### Markdown

Markdown is the basis of this site as markup language.

### Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
