<frontmatter>
    title: Resume - Tan Zhen Yong
</frontmatter>
{% set forWeb = false %}
{% set dot = '<svg height="5" width="5"><circle cx="2.5" cy="4" r="1" fill="black" /></svg>' %}

---
<div class="container">
    <div class="row no-gutters">
    <div class="col text-right">
      <h1 class="display-4">Tan Zhen Yong</h1>
    </div>
    <div class="col">

{{ fas_envelope }} tzy<small style="margin-left:1px; margin-right: 1px">{{ fas_at }}</small>beyondthesprawl{{ dot }}com<br>
{{ fab_github }} {% if forWeb %}[Xenonym](https://github.com/Xenonym){% else %}https://github.com/Xenonym{% endif %}<br>
{{ fab_linkedin }} {% if forWeb %}[Tan Zhen Yong](https://www.linkedin.com/in/tan-zhen-yong/){% else %}https://www.linkedin.com/in/tan-zhen-yong/{% endif %}</div>
</div>
</div>

---
<h1 class="font-weight-light text-center">{{ fas_university }} Education</h1>

---
#### National University of Singapore
_Aug 2016 - present_

- Bachelor of Computing (Honours) in Computer Science
- University Scholars Programme (USP) {% if forWeb %}<tooltip content="Click for more info."><trigger for="modal:usp" trigger="click">{{ fas_external_link_square_alt }}</trigger></tooltip>{% endif %}
- NUS Overseas Colleges Israel {% if forWeb %}<tooltip content="Click for more info."><trigger for="modal:noc" trigger="click">{{ fas_external_link_square_alt }}</trigger></tooltip>{% endif %}
<br><span class="text-muted">Batch 14, Jan 2018 - Jun 2018</span>

{% if forWeb %}
<modal title="{{ fas_graduation_cap }} University Scholars Programme (USP)" id="modal:usp" large>

_Aug 2016 - present_

The [University Scholars Programme (USP)](http://usp.nus.edu.sg/) is an undergraduate academic programme that aims to shape independent, adaptable thinkers and doers who will make an impact in the world. USP provides students with an innovative curriculum, diverse global opportunities and a transformative learning environment. Each year, around 200 incoming NUS students are admitted to USP. 
</modal>

<modal title="{{ fas_globe_asia }} NUS Overseas Colleges (NOC) Programme" id="modal:noc" large>

_Batch 14, Jan 2018 - Jun 2018_

The [NUS Overseas Colleges (NOC) Programme](https://enterprise.nus.edu.sg/educate/nus-overseas-colleges) is an internship programme with strong emphasis on technology entrepreneurship. Selected candidates will spend either 6 or 12 months with a high-tech start-up and take entrepreneurship courses at a designated partner university.
</modal>
{% endif %}

#### Tel Aviv University
_Jan 2018 - Jun 2018_

Foundations of Entrepreneurship course, as part of NUS Overseas Colleges Israel{% if forWeb %} <tooltip content="Click for more info."><trigger for="modal:noc" trigger="click">{{ fas_external_link_square_alt }}</trigger></tooltip>{% endif %}.

#### Temasek Polytechnic
_Apr 2011 - Apr 2014_

- Diploma in Digital Forensics with Merit
- Certificate in Innovation and Entreprenurship

###### Awards
- Fujistu Asia Silver Course Medal
- ISACA Singapore Chapter Prize

---
<h1 class="font-weight-light text-center">{{ fas_briefcase }} Work Experience</h1>

---
<h4>R&D Intern <small class="text-muted">CyberInt</small></h4>

_Jan 2018 - Jun 2018_

- Summer internship with [CyberInt](https://www.cyberint.com/), a leading cybersecurity managed services provider in Petah Tikva, Isarel. 
- Led a team of three interns in implementing new source acquisition methods for the Argos threat intelligence platform, used by threat analysts in both CyberInt and [SingTel](https://www.singtel.com/business/enterprise-solutions/cyber-security/enterprise-security/managed-security-services) as part of their managed security services offering. 
- Assisted the intelligence team with intelligence gathering and analysis as part of a service evaluation with Citibank APAC.

<h4>R&D Intern <small class="text-muted">National Institute of Technology, Matsue College</small></h4>

_Oct 2013 - Nov 2013_

- Winter internship with the National Institute of Technology, Matsue College, a engineering-focused institute in Matsue, Japan. 
- Created a motion-based interface to allow users to control humanoid robots with a Kinect sensor for research into bipedal robots.

---
<h1 class="font-weight-light text-center">{{ fas_tasks }} Competencies</h1>

---
#### Python
- Implemented new source acquisition methods for the [**Argos threat intelligence platform**](https://www.cyberint.com/product/argos-digital-risk-protection-platform/) while on internship at CyberInt.

#### JavaScript
- Contributed features and bug fixes to the open source static site generator [**MarkBind**](https://markbind.github.io/markbind/), including new syntax.
- Conceptualised and implemented part of the core fingerprinting library for the passwordless authentication system [**Autoauth**](https://github.com/cs3235-autoauth), built as the module project for [CS3235 Computer Security](https://www.comp.nus.edu.sg/~hugh/presentations/cs3235/).

#### PHP
- Led the development of a forensic web crawler **WebAnatomy**, as part of my final year project in Temasek Polytechnic, subsequently deployed at the [Civil Aviation Authority of Singapore (CAAS)](https://www.caas.gov.sg/) for monitoring web vandalism (~1.5 KLoC).

<!--#### Java
- In charge of storage and code quality for a relationship tracker and intelligence tool [**Intelli**](https://github.com/CS2103AUG2017-F10-B1/main) (~1 KLoC), built as the module project for [CS2103 Software Engineering](https://nus-cs2103-ay1718s1.github.io/website/).

#### Swift
- Built a social task manager app for iOS devices **DOgether** as part of [CP2106 Orbital Programme](https://orbital.comp.nus.edu.sg/) (~2 KLoC).-->
