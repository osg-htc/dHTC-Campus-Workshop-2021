---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "cp"    # what kind of Carpentry (must be either "lc" or "dc" or "swc").
venue: "Using and Facilitating the Use of dHTC and the OSG"        # brief name of host site without address (e.g., "Euphoric State University")
address: "online"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latlng: "35.198132,-97.445449"       # decimal latitude and longitude of workshop venue (e.g., "41.7901128,-87.6007318" - use https://www.latlong.net/)
humandate: "February 8, 2021"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "1:00 pm - 4:00 pm CDT"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2021-02-08      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2021-02-08       # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Christina Koch", "Carrie Brown", "Emelie Fuchs", "Lauren Michael", "Mats Rynge", "Jess Vera"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
# helper: [""]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["support@opensciencegrid.org"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes: https://docs.google.com/document/d/1GkeHB5FfrhjkdcFEZXw6a4bkGNFo2WseeQQetwEXO5w/edit
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---
<h2 id="general">General Information</h2>

<p>In this installment of dHTC Campus Workshops offered by the <a href="https://path-cc.io/">Partnership to Advance Throughput Computing (PATh)</a>, we'll offer a half-day training on "Using and Facilitating the Use of dHTC and OSG", followed by a half-day of Virtual Office Hours on all things dHTC for campus cyberinfrastructure (CI) staff. Registration is required for participants to receive virtual meeting room details via email.</p>

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
Remote via Zoom - attendee links will be sent via email to all workshop registrants
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
<p>This 3-hour training will include hands-on and discussion-based exercises on the following topics:</p>
<ul>
  <li>Introduction to distributed high throughput computing (dHTC) approaches and systems</li>
  <li>How to execute computational work on the <a href="https://opensciencegrid.org/">Open Science Grid</a> (and via the <a href="https://www.osgconnect.net">OSG Connect service</a>)</li>
  <li>OSG support for 'big data'</li>
  <li>Identifying computational research that would be accelerated by dHTC approaches</li>
  <li>Facilitating researchers to advance their work through dHTC approaches and services</li>
  <li>Services for building dHTC Facilitation capacity in campus teams</li>
</ul>

<center><form>
<button name="button" style="background-color: D71920; padding: 15px 32px" formaction="https://indico.fnal.gov/event/46925/">Register to Attend</button>
</form></center>

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<!-- <p id="requirements">
  <strong>Requirements:</strong> A computer with an ssh client. We will have training/test accounts for participants to test-drive job submission in the Open Science Grid.
</p> -->


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

 <div class="row">
  <div class="col-md-8">
    <h2>Detailed Schedule and Materials</h2>

    <table class="table table-striped">
      <tr>
        <td>1:00-1:30 CDT</td>
        <td>Introduction to dHTC and OSG</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>1:30-1:40 CDT</td>
        <td>Break</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>1:40-2:00 CDT</td>
        <td>Running dHTC Jobs via HTCondor</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>2:00-2:15 CDT</td>
        <td>Software and Data Support in OSG</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>2:15-2:45 CDT</td>
        <td>Break</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>2:45-3:00 CDT</td>
        <td>Account Setup</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>3:00-3:20 CDT</td>
        <td>dHTC Facilitation for Researchers on Your Campus</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td>3:20-4:00 CDT</td>
        <td>Hands On Exercises: Running dHTC Jobs on OSG with HTCondor</td>
        <td></td>
        <td></td>
      </tr>
    </table>
  </div>
</div>
<!--
<h3>Open Office Hours: All Things dHTC!</h3>

<p>Join us on February 9th from 1:00-4:00 CDT for Open Office Hours. Members of the PATh will be available to answer any questions relevant to distributed high throughput computing (dHTC) and services for campuses (including everything discussed in our <a href="https://indico.fnal.gov/event/45998/timetable/#20201022">October workshop</a>), with breakout rooms for:</p>
<ul>
  <li>services for building local dHTC capacity, including the HTCondor Software Suite (HTCSS)</li>
  <li>how to execute work on dHTC/HTCSS systems, including the OSG</li>
  <li>dHTC Facilitation and services for building Facilitation capacity</li>
  <li>local integration with the OSG (e.g. local "access points" and "data origins")</li>
  <li>sharing local cluster capacity via the OSG tools and services</li>
  <li>related services for cross-institution collaborations and science gateways</li>
</ul>
-->

<p>For more information, or to register, visit the <a href="https://indico.fnal.gov/event/46925/">dHTC Campus Workshop page on Indico</a>.
