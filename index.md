---
title: Jobs
layout: none
---


<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  {% assign mycss = "/assets/css/main.css" %}
  <link rel="stylesheet" href= "{{ mycss | relative-url }}">
</head>


 <div id = "Homepage">


   <section class="sec0">
      <div class="banner1" >     
            <section class="sec1">
              <div class = "logo-container">
                <div class = "company-logo" ></div>
                <span id = "innovate">Innovation happens when you are free to experiment.</span>
                <span id = "leap">The leap toward innovation can seem giant, but with daily practice it will eventually happen.</span>
              </div>
            </section>
      </div>
  </section>



  <section class="sec2">
    <div id="job-list">
      <h1 id = "job-lst-txt" >Available jobs</h1>
      <div  class="uk-margin uk-card uk-card-default uk-card-body">
        {% for job in site.jobs %}
          <h2 class ="job-block">
            <div class="bullet-jobs">&nbsp;</div>
              <a  href="{{ job.url | relative-url }}" >
                  {{ job.title }}
              </a>
          </h2>
          <p>{{ job.description | markdownify }}</p>
          <div id="job-info-row">
            <p><b>Keywords: </b>{{ job.Keywords  }}</p>
            <p><b>Location: </b>{{ job.location  }}</p>
            <p><b>Seniority:</b> {{  job.Seniority  }}</p>
          </div>
          {% if forloop.last == false %}
            <div id="job-lst-line"> </div>
          {% endif %}
       {% endfor %}
      </div>
    </div>
  </section>
  
<section class="sec3">
    <div id="subscribe">
      <span id="sub-text">Subscribe to get alerts</span>
      <p>No job listed above for you? You can create a job alert and we will send you an e-mail when a position you are interested becomes available.</p>
            <div class="notified-block-container">
                      <div class="notified-block">
                            <button id="get-notified" class= "notified-block" onclick="window.location.href='https://forms.office.com/r/QSCWNvEukh'">Get notified</button>
                      </div>        
                      <div class= "share-link-home">
                          <a href="#" style="float: right">
                            Share This Page
                            <img src="./assets/images/image1.png" style="float: right;margin-left: 10px;margin-right:10 px;" />
                          </a>
                      </div>
            </div>
    </div>
  </section>
    <div class="footer-baground">
      &nbsp; 
    </div>
</div>
