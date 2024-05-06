---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "University of Arizona"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the workshop
latitude: "0"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "0"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "June 3-4, 2024"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 am - 12:00 pm"    # human-readable times for the workshop e.g., "9:00 am - 4:30 pm CEST (7:00 am - 2:30 pm UTC)"
startdate: 20240603      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 20240604        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Michele Cosi", "Uwe Hilgert"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["KEYS Crew", "KEYS Staff"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["hilgert@arizona.edu", "keys@bio5.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<h2 id="general">INTRODUCTION TO SCIENCE COMPUTATION</h2>

<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE
Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION
This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://www.latlong.net/ to find the lat/long of an
address.
{% endcomment %}

<p id="where">
  <strong>Where:</strong>This training will take place in person as well as online. The organizers will provide you with the information you will need to connect to this meeting.
</p>

{% comment %}
DATE
This block displays the date and links to Google Calendar.
{% endcomment %}

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
SPECIAL REQUIREMENTS
Modify the block below if there are any special requirements.
{% endcomment %}

<p id="requirements">
  <strong>Requirements:</strong>
  {% if online == "false" %}
    Participants must bring a laptop with a
    Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on.
  {% else %}
    Participants must have access to a computer with a
    Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on.
  {% endif %}
  They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>

{% comment %}
ACCESSIBILITY
Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}

<p id="accessibility">
  <strong>Accessibility:</strong>
{% if online == "false" %}
  We are committed to making this workshop
  accessible to everybody.  For workshops at a physical location, the workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Material will be provided in advance of the workshop.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>
{% else %}
  We are dedicated to providing a positive and accessible learning environment for all. Please
  notify the instructors in advance of the workshop if you require any accommodations or if there is
  anything we can do to make this workshop more accessible to you
</p>
{% endif %}

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact:</strong>
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<p id="roles">
  <strong>Roles:</strong>
  To learn more about the roles at the workshop (who will be doing what),
  refer to <a href="https://carpentries.org/workshop_faq/#what-are-the-roles-of-everyone-participating-in-a-workshop">our Workshop FAQ</a>.
</p>

<hr/>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<h2 id="code-of-conduct">Code of Conduct</h2>

<p>
Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>

<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Report a Code of Conduct Incident</button>
  </a>
</p>
<hr/>


{% comment %}
Collaborative Notes
If you want to use an Etherpad, go to
https://pad.carpentries.org/YYYY-MM-DD-site
where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}

{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}


<p>
  This Google Doc at <a href="https://docs.google.com/document/d/1A2lRqSD169z466qz53Dw4CtCZUXe40gZzZs2tGukyPA/edit?usp=sharing">https://docs.google.com/document/d/1A2lRqSD169z466qz53Dw4CtCZUXe40gZzZs2tGukyPA/edit?usp=sharing</a> holds additional IMPORTANT information on the workshop and how to prepare for it. 
<p>

<!--
{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}

<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
{% if site.carpentry == "incubator" %}
<p><a href="{{ site.incubator_pre_survey }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.incubator_post_survey }}">Post-workshop Survey</a></p>
{% elsif site.incubator_pre_survey or site.incubator_post_survey %}
<div class="alert alert-danger">
WARNING: you have defined custom pre- and/or post-survey links for
a workshop not configured for The Carpentries Incubator
(the value of `curriculum` is not set to `incubator` in `_config.yml`).
Please comment out the `incubator_pre_survey` and `incubator_post_survey` fields
in `_config.yml` or, if this workshop is teaching a lesson in the Incubator,
change the value of `carpentry` to `incubator`.
</div>
{% else %}
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>
{% endif %}
-->

<hr/>

<h3 id="syllabus"><u>Syllabus</u></h3>

<div class="row">
  <div class="col-md-6">
    <h3 id="syllabus-shell">The Command Shell</h3>
    The command shell (a.k.a. UNIX Shell, Bash Shell, Shell) is a power tool that allows computer users to do complex things with just a few keystrokes. Contrary to graphical user interfaces (GUI) it allows users to direct the computer from a more foundational level, using written commands. Even what happens when you click on items in GUIs is directed by written commands. Working in the 'Shell' helps users combine existing programs in new ways and automate repetitive tasks so they aren’t typing the same things over and over again. Shell proficiency is fundamental to using a wide range of other powerful tools and computing resources, including “high-performance computing” supercomputers.<br>
    <br>
    Using the Bash Shell the workshop will introduce these concepts and procedures:<br>
    <br>
    <ul>
      <li>Files and Directories</li>
      <li>History and Tab Completion</li>
      <li>Pipes and Redirection</li>
      <li>Looping Over Files</li>
      <li>Creating and Running Shell Scripts</li>
    </ul> 
    <u>Additional Resources:</u>
      <ul>
		  <li><a href="{{site.swc_pages}}/shell-novice/reference">Shell Quick Reference</a></li>
		  <li><a href="{{site.swc_pages}}/shell-novice">Shell Lessons</a></li>
      <li><a href="http://explainshell.com/" target="_blank"><em>Explain Shell</em> (Parses shell commands and shows docs about the command)</a></li>
		  <li><a href="http://www.shellcheck.net/" target="_blank"><em>ShellCheck</em> (Identifies bugs in shell scripts)</a></li>
		  <li><a href="http://man.he.net/" target="_blank"><em>Linux Man Pages Online</em> (Same content as command line man/help pages)</a></li>
	  </ul>
  </div>
  <div class="col-md-6">
    <h3 id="syllabus-git">Version Control with Git</h3>
    Version control is the lab notebook of the digital world: it’s what professionals use to keep track of what they’ve done and to collaborate with other people. Every large software development project relies on it, and most programmers use it for their small jobs as well. And it isn’t just for software: books, papers, small data sets, and anything that changes over time or might need to be shared can and should be stored in a version control system.<br>
    <br>
  Using git (on your local computer) and GitHub (in the cloud), the workshop will introduce these version control concepts and procedures:<br>
    <br>
    <ul>
      <li>Creating and initializing a Repository: <code>init</code></li>
      <li>Recording Changes to Files: <code>add</code>, <code>commit</code>, ...</li>
      <li>Viewing Changes: <code>status</code>, ...</li>
      <li>Working on the Web: <code>clone</code>, <code>pull</code>, <code>push</code>, ...</li>
    </ul>
    <u>Additional Resources:</u>
	  <ul>
		  <li><a href="{{site.swc_pages}}/git-novice/reference">Git Quick Reference</a></li>
		  <li><a href="{{site.swc_pages}}/git-novice">Git Lessons</a></li>
      <li><a href="https://git-scm.com/book/en/v2/Git-in-Other-Environments-Git-in-Bash" target="_blank"><i>Mac/Linux:</i> Integrating Git into your shell prompt</a></li>
		  <li><a href="https://github.com/magicmonty/bash-git-prompt" target="_blank">An informative and fancy bash prompt for Git users</a></li>
		  <li><a href="https://education.github.com/pack" target="_blank">Unlimited <em>private</em> repositories for free on Github, <i>while you are a student</i></a></li>
		  <li><a href="https://git-annex.branchable.com/" target="_blank">Git for Archiving Data</a></li>
	  </ul>
  </div>
</div>

<hr/>


{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in a
  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  workshop,
  you will need access to software as described below.
  In addition, you will need an up-to-date web browser.
</p>
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

{% comment %}
For online workshops, the section below provides:
- installation instructions for the Zoom client
- recommendations for setting up Learners' workspace so they can follow along
  the instructions and the videoconferencing

If you do not use Zoom for your online workshop, edit the file
`_includes/install_instructions/videoconferencing.html`
to include the relevant installation instructions.
{% endcomment %}
{% if online != "false" %}
{% include install_instructions/videoconferencing.html %}
{% endif %}

{% comment %}
These are the installation instructions for the tools used
during the workshop.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/setup.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/setup.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/setup.html %}
{% elsif site.carpentry == "incubator" %}
Please check the "Setup" page of
[the lesson site]({{ site.incubator_lesson_site }}) for instructions to follow
to obtain the software and data you will need to follow the lesson.
{% endif %}
