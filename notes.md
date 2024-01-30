### This note is about what I did to make the website run.

I did the start-up process of al-folio. 
However, instead of using the deployment procedure that the al-folio README.md suggested, I directly use github's actions for jekyll. See this link: https://jekyllrb.com/docs/continuous-integration/github-actions/

However, deployment would fail because there is no jupyter. So I added the following in the jekyll.yml that is created. This made the deployment work.

```
      - name: Install Jupyter # to allow jekyll-jupyter plugin to embed jupyter notebooks
        run: pip install jupyter 
```

* To remove or add pages to the navigation bar, just change the "nav=true" to "nav=false" in the corresponding page. The "about" page cannot be changed.

* To add a customized field for bibliography, e.g. highlight, we add it in _includes/bib.liquid.

```
{% if entry.highlight %}
  <a href="{{ entry.highlight }}" class="btn btn-sm z-depth-0" role="button">highlight</a>
{% endif %}
```

