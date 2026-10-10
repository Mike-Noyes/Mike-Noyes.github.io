
# Home Page for the Teaching Website of Mike Noyes

I began this website as a place to gather all of the various materials that I have accumulated over the years teaching undergraduate math courses at CU Boulder.  My intention is that it will provide a unified place for students to find material related to courses that they are taking.  It is **NOT** designed to teach the material from scratch.  That's what the actual courses are for!  It is meant to supplement these courses, and to hopefully help students make their way through some fascinating but sometimes difficult mathematical ideas.  This is a work in progress.

<!--
---
I plan to do the following on this page:
1. Have a blog.
2. Put in links to various other GitHub projects
3. Create a Calc 3 project that my students can use to help them this semester.

---
-->

## About Me

I received my PhD from CU Boulder in the Spring of 2011.  I worked with Brian Rider (now at Temple University) in Random Matrix Theory.  After spending one year at the University of Waterloo doing Post Doc work with Andu Nica in Free Probability Theory, I taught at Bard High School Early College in Manhattan for 8 years.  I returned to CU Boulder in the Fall of 2020 and have been here ever since.  I am currently a Lecturer in the Mathematics Department.  I teach undergraduate courses, mainly in the Calculus sequence.

I can reached by email at <noyesmb@colorado.edu>.

## Teaching Links

* [Go to the Calc 1 Page](calc1.html)
* [Go to the Calc 2 Page](calc2.html)
* [Go to the Calc 3 Page](calc3.html)
* [Go to the Linear Algebra Page](linalg.html)
* [Go to the Ordinary Differential Equations Page](ode.html)

## Other Links

* [Math Projects](projects/projects.html)
* [Math Links and Resources]()
* [Misc]()

## My Blog

### Recent Posts
Below you will find my latest posts.   

<!-- If using Jekyll, this liquid loop automatically lists your posts from the _posts folder -->
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> — <i>{{ post.date | date: "%B %d, %Y" }}</i>
    </li>
  {% endfor %}
</ul>

---

This site is licensed under the [MIT License](LICENSE).
