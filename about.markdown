---
layout: page
title: about
permalink: /about/
intro: I'm a fourth year computer science major at the University of Chicago, specializing in Human Computer Interaction. Here, you'll find some of what I've made & encountered these past few years.

courses:
  - Computer Vision
  - Emergent Interface Technologies
  - Mobile Computing
  - Intro to HCI
  - Virtual Reality Production
  - Discrete Math
  - Algorithms
  - Usable Security and Privacy
  - Computer Architecture
  - Networks and Distributed Systems
  - Abstract Linear Algebra

experience:
  - place: Human Computer Integration Lab
    position: Research Assistant
    period: January 2020 - present
    city: Chicago, IL
    description: Exploring EMS as a way to teach force.

  - place: Center for Data and Computing (CDAC)
    position: Research Intern
    period: June 2019 - August 2019
    city: Chicago, IL
    description: Assisted with an AWS Spot pricing project. Then implemented autoencoder neural networks to create my own Deepfakes.

  - place: University of Chicago
    position: MADD/CSIL technical staff
    period: May 2017 - January 2020
    city: Chicago, IL
    description: Performed hardware/software maintainance in support of the Computer Science department. Also staffed the Hack Arts Lab, assisted patrons with laser cutters, 3D printers, and other tech.

  - place: Toyota Insurance Management Solutions
    position: Data Engineer Intern
    period: June 2018 - August 2018
    city: Los Angeles, CA
    description: Built and automated ETL pipelines using AWS (primarily EC2, S3, Athena) and Google Analytics. Developed a chatbot proof of concept to improve customer service and data collection, using Dialogflow and Google Cloud Platform, Facebook Messenger, and Line Messenger.

  - place: Blake Software Design 2016
    position: UX designer / Team member
    period: February 2016 - May 2016
    city: Minneapolis, MN
    description: Designed an interactive quiz app for the Bakken Museum's "Mary and Her Monster" exhibit in Minneapolis. Led regular consultations with client. Drafted and revised UX wireframes.

leadership:
  - place: Outside the Lines
    position: President
    period: January 2017 - present
    city: Chicago, IL
    description: Organize figure drawing events weekly at the Logan Center for the Arts. Promote greater community engagement with visual arts and the tradition of figure drawing.

  - place: Asynchronous Anonymous
    position: Graphic Design & Social Media
    period: January 2018 - present
    city: Chicago, IL
    description: Organize student-led talks about technology and passion projects, to foster peer-to-peer learning and opportunities for collaboration in the student body. Design branding and manage events.

education:
  - place: University of Chicago
    course: BS in Computer Science with specialization in HCI, expected June 2020
  - place: University of Minnesota
    course: University of Minnesota Talented Youth Mathematics Program (UMTYMP)

skills:
  - Prototyping and wireframing
  - Graphic design

tools:
  - GCP (Firebase, Dialogflow, Stackdriver)
  - AWS (Athena, S3, EC2, Lambda, Sagemaker, CodeCommit)
  - Subversion, GitHub
  - Mac OS X, Linux/Unix shell
  - Oracle Virtualbox
  - Arduino
  - Jekyll
  - 3D printing
  - Lasercutting (basic)


languages:
  - Python (pandas, boto3, numpy)
  - C
  - HTML, CSS, JS
  - English
  - Mandarin
  - German (beginner)

---
<div class="about-wrapper">
  <div class="about">
    <div class="about-intro">
      <div class="about-intro-description">
        {{ page.intro | markdownify }}
      </div>
    </div>
    <div class="about-attributes">

      <div class="triptych">
        <div class="courses">
            <h3 class="triptych-title">Courses</h3>
            {% for courses-item in page.courses %}
                <div class="item">{{ courses-item }}</div>
            {% endfor %}
        </div>
        <div class="tools">
            <h3 class="triptych-title">Tools</h3>
            {% for item in page.tools %}
                <div class="item">{{ item }}</div>
            {% endfor %}
        </div>
        <div class="languages">
            <h3 class="triptych-title">Languages</h3>
            {% for item in page.languages %}
                <div class="item">{{ item }}</div>
            {% endfor %}
        </div>
      </div>


        <div class="about-experience">
            <h3 class="about-section-title">Experience</h3>
            <div class="about-section">
                {% for experience-item in page.experience %}
                    <div class="about-section--head">
                        <div class="list_left">
                            <dd class="list_title">{{ experience-item.place }}</dd>
                            <dd class="list_content list_content--position">{{ experience-item.position }}</dd>
                        </div>
                        <div class="list_right">
                            <dd class="list_content list_content--period">{{ experience-item.period }}</dd>
                            <dd class="list_content list_content--city">{{ experience-item.city }}</dd>
                        </div>
                    </div>
                    <div class="list_below">
                        <dd class="list_content list_content--about">{{ experience-item.description }}</dd>
                    </div>
                {% endfor %}
            </div>
        </div>
        <div class="about-leadership">
            <h3 class="about-section-title">Leadership</h3>
            <div class="about-section">
                {% for item in page.leadership %}
                <div class="about-section--head">
                    <div class="list_left">
                        <dd class="list_title">{{ item.place }}</dd>
                        <dd class="list_content list_content--position">{{ item.position }}</dd>
                    </div>
                    <div class="list_right">
                      <dd class="list_content list_content--period">{{ item.period }}</dd>
                      <dd class="list_content list_content--city">{{ item.city }}</dd>
                    </div>
                </div>
                    <div class="list_below">
                        <dd class="list_content list_content--about">{{ item.description }}</dd>
                    </div>
                {% endfor %}
            </div>
        </div>




<!-- 
      <div class="about-education">
        <div class="about-section">
          <h3 class="about-section-title">Education</h3>
          <dl class="relational-list">
            {% for education-item in page.education %}
              <dt class="relational-list__title">{{ education-item.course | markdownify}}</dt>
              <dd class="relational-list__description">{{ education-item.place | markdownify}}</dd>
            {% endfor %}
          </dl>
        </div>
      </div>

      <div class="about-tools">
        <div class="about-section">
          <h3 class="about-section-title">Tools &amp; Technologies</h3>
          <ul class="list--dashed list--small">
            {% for tool in page.tools %}
              <li>{{ tool | markdownify }}</li>
            {% endfor %}
          </ul>
        </div>
      </div>

      <div class="about-skills">
        <div class="about-section">
          <h3 class="about-section-title">Skills</h3>
          <ul class="list--dashed list--small">
            {% for skill in page.skills %}
              <li>{{ skill }}</li>
            {% endfor %}
          </ul>
        </div>
      </div>
    </div>

    <div class="about-site">
      <div class="about-section about-site-description">
        <h3 class="about-section-title">Colophon: about this site</h3>
        <div class="paragraph-small">{{ page.about_site | markdownify }}</div>
      </div>
    </div>
 -->
</div>

