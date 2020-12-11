---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "cp"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").
venue: "Empowering Research Computing at Your Campus Through the Open Science Grid"        # brief name of host site without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "35.198132,-97.445449"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "Monday, February 8-9, 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "11:00 am - 3:00 pm CDT"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2021-02-08      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-02-09       # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Christina Koch", "Carrie Brown", "Emelie Fuchs", "Lauren Michael", "Mats Rynge", "Jess Vera"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
# helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["lmichael@wisc.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: https://docs.google.com/document/d/1GkeHB5FfrhjkdcFEZXw6a4bkGNFo2WseeQQetwEXO5w/edit
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %}
For a workshop please delete the following block
{% endcomment %}


<div class="alert alert-warning" style="font-size: 120%;">

In this installment of dHTC Campus Workshops offered by the Partnership to Advance Throughput Computing (PATh), we'll offer a half-day training on "Using and Facilitating the Use of dHTC and OSG", followed by a half-day of Virtual Office Hours on all things dHTC for campus cyberinfrastructure (CI) staff. Registration is required for participants to receive virtual meeting room details via email.
</div>

{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

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
  <strong>Requirements:</strong> A computer with an ssh client. We will have training/test accounts for participants to test-drive job submission in the Open Science Grid.
</p>

{% comment %}

ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.

<!-- <p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul> -->
{% endcomment %}

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
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

<h2>Topics</h2>
<div class="row">
  <div class="col-md-6">
    <h3>Day 1 Training</h3>
    <h6>Using and Facilitating the Use of dHTC and OSG</h6>
    <p>This 3-hour training (with 1-hour break) will include hands-on and discussion-based exercises on the following topics:</p>
    <ul>
      <li>Introduction to distributed high throughput computing (dHTC) approaches and systems</li>
      <li>How to execute computational work on the [Open Science Grid](https://opensciencegrid.org/) (and via the [OSG Connect service](https://www.osgconnect.net/))</li>
      <li>OSG support for 'big data'</li>
      <li>Identifying computational research that would be accelerated by dHTC approaches</li>
      <li>Facilitating researchers to advance their work through dHTC approaches and services</li>
      <li>Services for building dHTC Facilitation capacity in campus teams</li>
    </ul>
  </div>
  <div class="col-md-6">
    <h3>Day 2 Office Hours</h3>
    <h6>All Things dHTC!</h6>
    <p>Members of the PATh will be available to answer any questions relevant to distributed high throughput computing computing (dHTC) and services for campuses (including everything discussed in our [October workshop](https://indico.fnal.gov/event/45998/timetable/#20201022)), with breakout rooms for:</p>
    <ul>
      <li>services for building local dHTC capacity, including the [HTCondor Software Suite](https://research.cs.wisc.edu/htcondor/) (HTCSS)</li>
      <li>how to execute work on dHTC/HTCSS systems, including the OSG</li>
      <li>dHTC Facilitation and services for building Facilitation capacity</li>
      <li>local integration with the OSG (e.g. local "access points" and "data origins")</li>
      <li>sharing local cluster capacity via the OSG tools and services</li>
      <li>related services for cross-institution collaborations and science gateways</li>
    </ul>
  </div>
</div>  </div>
</div>

 <div class="row">
  <div class="col-md-8">
    <h2>Detailed Schedule and Materials</h2>
    <p>Coming soon!</p>
<!--    <p><b>Google Doc for Notes: <a href="https://docs.google.com/document/d/1GkeHB5FfrhjkdcFEZXw6a4bkGNFo2WseeQQetwEXO5w/edit">Document Link</a></b> </p>

    <table class="table table-striped">
      <tr><td>8:00-8:15 PDT</td> <td>User Account Requests</td> <td><a href="https://support.opensciencegrid.org/support/solutions/articles/5000632072-registration-and-login-for-osg-connect">Instructions</a> / <a href="https://www.osgconnect.net/signup">Sign up</a></td><td></td></tr>
      <tr><td>8:15-8:50 PDT</td><td>Brief Overview of the Open Science Grid + Job Submission</td><td><a href="https://docs.google.com/presentation/d/17efQMhWy_8SapVyiVJw-L8F9Q5-xVHtj0LsbJQqLWwA/edit?usp=sharing">Slides</a></td><td><a href="https://github.com/OSGConnect/tutorial-osg-locations">Hands-on</a></td></tr>
      <tr><td>8:50-9:45 PDT</td><td>High Throughput Computing and Facilitation</td><td><a href="https://docs.google.com/presentation/d/1EkMs2gtLVSTSeyjbrxs-dF3IpCOEARQi9qGgeS5VeMU/edit?usp=sharing">Slides</a></td><td><a href="https://github.com/OSGConnect/tutorial-AutoDockVina">Autodock</a>, <a href="https://github.com/OSGConnect/tutorial-blast-split">BLAST</a></td></tr>
      <tr><td>9:45-10:00 PDT</td><td>Break</td><td></td><td></td></tr>
      <tr><td>10:00-10:20 PDT</td><td>HTCondor Features</td><td><a href="https://docs.google.com/presentation/d/1LBMFaN7EoTkRDSbkkFRJzCgROsf5lKpH-Y5B6Tm3Bdc/edit?usp=sharing">Slides</a></td><td></td></tr>
      <tr><td>10:20-11:00 PDT</td><td>Supporting OSG on Your Campus</td><td><a href="https://docs.google.com/presentation/d/17BRyVrqrKfycrD1ApjotwzI1_4Z3tP7Vzk4oEq9X8lY/edit?usp=sharing">Slides</a></td><td></td></tr>
      <tr><td>11:00-11:15 PDT</td><td>Action Plan</td><td></td><td></td></tr>
      <tr><td>11:15-11:30 PDT</td><td>Feedback survey + open mic</td><td><a href="https://forms.gle/iF94uSymYtgDok5D9">Feedback Survey</a></td><td></td></tr>
    </table> -->
  </div>
</div>



