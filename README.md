[Show generated on hosted project page by GitHub](https://twissi.github.io/pages-tryout/)


How to customize a GitHub Pages theme
================================

All steps can also be found in [GitHub help](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/)

1.Create GitHub Page
------------
Create a new GitHub repo, enable [GitHub Pages](https://pages.github.com) and select minimal theme (or any other [supported theme](https://pages.github.com/themes/))

2.Install Jekyll to run GitHub page locally
------------

To preview your changes run GitHub page locally. Find help to setup Jekyll [here](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)

Note: You need a internet connection to fetch GitHub metadata

3.Customize CSS
------------

Create file `/assets/css/style.scss` in your site repository. Add the following content:

    ---
    ---

    @import "{{ site.theme }}";

    /* Add your CSS here */


[Learn more about customizing](https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/#customizing-your-jekyll-themes-css).

4.Customize page layout
------------

Create file `/_layouts/default.html` in your site repository
Copy the content of your Theme default.html in your new file `https://github.com/pages-themes/THEME_NAME/blob/master/_layouts/default.html`

For example add your github avatar to the page (see available [GitHub metadata](#github-metadata))
<pre>
  {% raw %}
  {% if site.github.contributors %}
    <img src="{{ site.github.contributors[0].avatar_url }}" width="50" height="50">
  {% endif %}
  {% endraw %}
</pre>

[Learn more about html layout](https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/#customizing-your-jekyll-themes-html-layout)

<br/>
<br/>

This might also help you
================================

How to configure Jekyll
------------

Use `_config.yml` to configure Jekyll.

For example: To show download buttons on your project page you can add the following to the config file

    show_downloads: true


More help with Jekyll configuration can be found [here](https://help.github.com/articles/configuring-jekyll).


Sample markdown
-------------
To get started with GitHub Flavored Markdown you can find some sample content [here](https://github.github.com/github-flavored-markdown/sample_content.html).


GitHub metadata
------------

You can use the following GitHub specific metadata in you template.

<pre>
{
  "api_url": "https://api.github.com",
  "baseurl": "/pages/Twissi/pages-tryout",
  "build_revision": "8754c2bf2482929123d12f4eecb60b97617af0e3",
  "clone_url": "http://github.com/Twissi/pages-tryout.git",
  "contributors": [
    {
      "login": "Twissi",
      "id": 261567,
      "avatar_url": "https://avatars0.githubusercontent.com/u/261567?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/Twissi",
      "html_url": "https://github.com/Twissi",
      "followers_url": "https://api.github.com/users/Twissi/followers",
      "following_url": "https://api.github.com/users/Twissi/following{/other_user}",
      "gists_url": "https://api.github.com/users/Twissi/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/Twissi/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/Twissi/subscriptions",
      "organizations_url": "https://api.github.com/users/Twissi/orgs",
      "repos_url": "https://api.github.com/users/Twissi/repos",
      "events_url": "https://api.github.com/users/Twissi/events{/privacy}",
      "received_events_url": "https://api.github.com/users/Twissi/received_events",
      "type": "User",
      "site_admin": false,
      "contributions": 4
    }
  ],
  "environment": "development",
  "help_url": "https://help.github.com",
  "hostname": "github.com",
  "is_project_page": true,
  "is_user_page": false,
  "issues_url": "http://github.com/Twissi/pages-tryout/issues",
  "language": null,
  "latest_release": false,
  "license": null,
  "organization_members": null,
  "owner_gravatar_url": "http://github.com/Twissi.png",
  "owner_name": "Twissi",
  "owner_url": "http://github.com/Twissi",
  "pages_env": "development",
  "pages_hostname": "localhost:4000",
  "private": false,
  "project_tagline": "Trying out github pages",
  "project_title": "pages-tryout",
  "public_repositories": [...],
  "releases": [],
  "releases_url": "http://github.com/Twissi/pages-tryout/releases",
  "repository_name": "pages-tryout",
  "repository_nwo": "Twissi/pages-tryout",
  "repository_url": "http://github.com/Twissi/pages-tryout",
  "show_downloads": true,
  "source": {
    "branch": "gh-pages",
    "path": "/"
  },
  "tar_url": "http://github.com/Twissi/pages-tryout/tarball/gh-pages",
  "url": "http://github.com/pages/Twissi/pages-tryout",
  "wiki_url": "http://github.com/Twissi/pages-tryout/wiki",
  "zip_url": "http://github.com/Twissi/pages-tryout/zipball/gh-pages"
}

</pre>