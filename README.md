
### About Section

The about section contains a quick about blurb that can be edited by changing the text within the paragraph tags.

### Experience Section

The experience section creates a vertical timeline with all your relevant experience. The code for the timeline creation can be found within `js/scripts.js` and is an adaptation of [RyanFitzgerald/vertical-timeline](https://github.com/RyanFitzgerald/vertical-timeline).

The default format is as follows:

```HTML
<div id="experience-timeline">
    <div data-date="September 2015 – September 2016">
        <h3>Employer Name</h3>
        <h4>Job Title</h4>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex.
        </p>
    </div>
</div>
```

The data attribute `data-date` is what is used to add a date to the associated timeline point. All that is really required is a wrapping div (i.e. `#experience-timeline`) and nested divs to build the timeline. The h3, h4, and p tags are optional and the contents of the div can be styled however you wish.

To add an additional section, simply add additional nested divs under the main wrapping div.

### Education Section

The Education is just a series of `.education-block` classes with some details associated with them. By default, it shows school name, date, degree, and some additional details. For example:

```HTML
<div class="education-block">
    <h3>University of Ottawa</h3>
    <span class="education-date">Sept 2016 - Sept 2017</span>
    <h4>Bachelor of Science in Computer Science</h4>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex.
    </p>
</div>
```

To add additional section, simply add additional `.education-block` elements.

### Projects Section

The Project section contains a number of `.project` elements that represent each of your projects. By default, it contains a 300x300 image under `.project-image` and relevant project information under `.project-info`. An example is as follows:

```HTML
<div class="project">
    <div class="project-image">
        <img src="images/project.jpg" />
    </div>
    <!-- End .project-image -->

    <div class="project-info">
        <h3>Project Name Here</h3>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex.
        </p>
        <a href="#">View Project</a>
    </div>
    <!-- End .project-info -->
</div>
```

If you want to hide some projects by default, you can throw them in an additional row and add the markup for the "Show More" button. This would be done as follows:

```HTML
<!-- Projects Above -->

<a id="view-more-projects" href="#">View More Projects</a>
<div id="more-projects" class="row">
    <div class="project shadow-large">
        <div class="project-image">
            <img src="images/project.jpg" />
        </div>
        <!-- End .project-image -->
        <div class="project-info">
            <h3>Project Name Here</h3>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex. Etiam volutpat laoreet urna. Morbi ut tortor nec nulla commodo malesuada sit amet vel lacus. Fusce eget efficitur libero. Morbi dapibus porta quam laoreet placerat.
            </p>
            <a href="#">View Project</a>
        </div>
        <!-- End .project-info -->
    </div>
    <!-- End .project -->
</div>
```

This will add a link that says "View More Projects" under the current projects and when clicked, all projects in the "More-projects" div will be shown. This is optional functionality and isn't provided by default. It is important that you keep the wrapping div ID intact ("#more-projects") as well as the anchor ID ("#view-more-projects"), however the contents of the div and the anchor text itself can be edited however you like.

#### Projects without images

If you do not wish to have a project image associated with a project, you can simply add `no-image` as an additional class to the project. It would look like the following:

```HTML
<div class="project no-image">
    <div class="project-info">
        <h3>Project Name Here</h3>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex.
        </p>
        <a href="#">View Project</a>
    </div>
    <!-- End .project-info -->
</div>
```

### Skills Section

The Skills section is simply an unordered list that spits out a "Skill Cloud" with all the skills listed. To add / remove skills, simply edit or add list elements, like so:

```HTML
<ul>
    <li>JavaScript</li>
    <li>Python</li>
    <li>Ruby</li>
    <li>Go</li>
    <li>Node.js</li>
</ul>
```

### Contact Section

Since the page is static, I opted to use the awesome Formspree to allow for a contact form without the need for anything else. To use it, you must have the page hosted on a server (loading a basic HTML page won't work) where a referrer header is generated. Also, simply add the email to the action. An example is as follows:

```HTML
<form method="POST" action="https://formspree.io/email@email.com">
    <input type="hidden" name="_subject" value="Contact request from personal website" />
    <input type="email" name="_replyto" placeholder="Your email" required>
    <textarea name="message" placeholder="Your message" required></textarea>
    <button type="submit">Send</button>
</form>
```
For more information on configuration of the contact form or dealing with errors, check out [Formspree](https://formspree.io/).

For a quick tutorial about formspree, check out this [tutsplus tutorial](https://webdesign.tutsplus.com/tutorials/quick-tip-add-a-formspree-form-to-your-static-sites--cms-23870) that covers different aspects and features of the form tool.

### Footer Section

The Footer contains an optional copyright where you can place your name as well as an unordered list of all of your social or coding related profiles. By default it contains Github, Stack Overflow, Facebook, Twitter, and Google Plus. You can add or remove them easily and simply use the Font Awesome icon associated with the social profile you wish to use. For a list of all icons, [click here](http://fontawesome.io/icons/).

### Optional Sections

The template comes with an optional section that can be added to the page markup to list things like Certifications, Hobbies, and more (Note: these are not included by default). The markup for the additional optional section is as follows:

```HTML
<div class="optional-section background-alt">
    <h2 class="heading">Section Name</h2>

    <div class="optional-section-block">
        <h3>Some content title</h3>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur in iaculis ex. Etiam volutpat laoreet urna. Morbi ut tortor nec nulla commodo malesuada sit amet vel lacus. Fusce eget efficitur libero. Morbi dapibus porta quam laoreet placerat.
        </p>
        <ul>
            <li>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            </li>
            <li>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            </li>
            <li>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            </li>
        </ul>
    </div>
    <!-- End .optional-section-block -->

</div>
<!-- End .optional-section -->
```

You can copy .optional-section-block for each new item you wish you have in the optional section. Also, the background-alt class may need to be removed depending on where the optional section is placed in your layout as this adds the grey background. If you play it at the bottom after "Skills", it can be used as is. Also, by default the border is applied at the top, but this can also be adjusted as needed.

The optional section blocks have styling for h3 (the block title), h4, p, and ul tags by default.
chor if you want to link to external site
* Changed contact form input / textarea colours to be based off `$base-color`
* Changed main background to 100vh so it doesn't overflow if viewport height < 700px



Completely free (MIT)! See [LICENSE.md](LICENSE.md) for more.
