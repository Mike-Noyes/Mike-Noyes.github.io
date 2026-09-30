
# Mike-Noyes.github.io

This is my **first** attempt at making a website!  This is a work in progress.

<!--
---
I plan to do the following on this page:
1. Have a blog.
2. Put in links to various other GitHub projects
3. Create a Calc 3 project that my students can use to help them this semester.

---
-->
I am a Lecturer at CU Boulder.  I teach undergraduate courses, mainly in the Calculus sequence.  As you can see from the list above, I hope to set up some material on this website to use for the Calc 3 class I am teaching this semester.

I can reached by email at <noyesmb@colorado.edu>.

## Teaching

* [Go to the Calc 3 Page](calc3.html)

## My Blog

Welcome to my personal blog. I am glad you are here. 

### Recent Posts
Below you will find my latest thoughts and tutorials. 

<!-- If using Jekyll, this liquid loop automatically lists your posts from the _posts folder -->
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> — <i>{{ post.date | date: "%B %d, %Y" }}</i>
    </li>
  {% endfor %}
</ul>

