---
title: "Example Form Intake"
date: 2020-01-07T23:53:00+01:00
draft: true
hideLastModified: true
type: "project"
summaryImage: "formIntake.png"
summary: "Key articles and history that have shaped my understanding of the technology landscape"
tags: ["Example"]
weight: 50
---

# From FormSpree

<form name="contact" method="POST" action="https://formspree.io/f/xvodaalj">
  <div class="columns">
    <div class="column is-6">
      <label class="label" for="inputName">Name</label>
      <input type="text" name="name" class="input" id="inputName" placeholder="Name" required="">
    </div>
  </div>

  <div class="columns">
    <div class="column is-6">
      <label class="label" for="inputEmail">Email</label>
      <input type="email" name="email" class="input" id="inputEmail" placeholder="Email" required="">
    </div>
  </div>

  <div class="columns">
    <div class="column is-6">
      <label class="label" for="inputMessage">Message</label>
        <textarea name="message" class="textarea" id="inputMessage" rows="5" placeholder="Message" required=""></textarea>
    </div>
  </div>
        <button type="submit" class="button is-link">Send</button>
      </form>


<iframe id="scaled-frame" src="https://stackoverflow.com/a/67352660/5728693" style="border:3px solid lightgrey;" height=100%></iframe>



## Issue Collector (Jira to RBT labs)
{{<rawhtml >}}
<!-- This is the script for the issue collector feedback form -->

<script type="text/javascript" src="https://rbtlabs.atlassian.net/s/d41d8cd98f00b204e9800998ecf8427e-T/rzvw4p/b/23/a44af77267a987a660377e5c46e0fb64/_/download/batch/com.atlassian.jira.collector.plugin.jira-issue-collector-plugin:issuecollector/com.atlassian.jira.collector.plugin.jira-issue-collector-plugin:issuecollector.js?locale=en-US&collectorId=9351b067"></script>

<!-- This is the script for specifying the custom trigger. -->

<script type="text/javascript">
    window.ATL_JQ_PAGE_PROPS =  {
        "triggerFunction": function(showCollectorDialog) {
            //Requries that jQuery is available! 
            jQuery("#feedback-button").click(function(e) {
                e.preventDefault();
                showCollectorDialog();
            });
        }
    };
</script>

<a href="#" id="feedback-button" class='btn btn-primary btn-large'>Report feedback</a>



{{</rawhtml >}}

## Docker Run

```
docker run --rm -it \
  -v $(pwd):/src \
  -p 1313:1313 \
  klakegg/hugo:0.83.1-ext-alpine \
  server -D

```