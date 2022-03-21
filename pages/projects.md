---
layout: default 
title: Projects
permalink: /projects
---

<html>
    <head>
        <style>
            .flex-container {
                display: flex;
                justify-content: space-between;
            }
            
            .flex-container > div {
                background-color: white;
                width: 1000px;
                height: 600px;
                margin: 5px;
                text-align: justify;
                line-height: 25px;
                font-size: 15px;
                margin-top: 30px;
            }

            .flex-container .text-container {
                width: 140%;
            }

            
            div.project-container {
              width: 365px;
              height: 560px;
              /*margin: 5px;*/
              float: right;
            }

            div.text-container{
                width: 800px;
            }
        </style>
    </head>
    <body>
        <div class="flex-container">
            <div class="text-container">
                    <h2>FloodNet</h2>
                    <p>
                        In New York City, sea level rise and increase in the occurrence of high intensity rain storms have led to a dramatic increase in flood risk, particularly in low-lying and coastal neighborhoods. Access to real-time information on flooding can aid infrastructure and resiliency planning, emergency response, transportation, and flood management decisions.
                        <br/>
                        <br/>
                        However, very little data exist on the frequency and extent of urban surface flooding, and there is an unmet need for hyperlocal information on the presence and depth of street-level floodwater.
                        <br/>
                        <br/>
                        <a href="https://www.floodnet.nyc/">FloodNet</a> is a cooperative of communities, researchers, and New York City government agencies developing a platform to provide real-time, street-level flood information - including the presence, frequency, and severity of local surface flood events - to a range of stakeholders, including policy makers, government agencies, citizens, emergency response teams, community advocacy groups, and researchers.
                        <br/>
                        <br/>
                        <i><u> <a href="https://praneethsvch.github.io/projects/floodnet">more about my work at FloodNet</a> </u></i>
                    </p>
                    
              </div>
            <div>
                <div class="project-container">
                    {% for project in site.data.settings.projects %}
                    <a href="{{ site.github.url }}/projects/{{ project.url }}">
                        <div class="project-unit" data-folder="{{ site.github.url }}/projects/{{ project.url }}" style="background-image: url({{ site.github.url }}/assets/img/projects/{{ project.url }}/thumbnail.jpeg)">
                            <div class="project-overlay">
                                <strong>{{ project.name }} <i class="fa fa-arrow-right" aria-hidden="true"></i></strong>
                            </div>
                        </div>
                    </a>
                    {% endfor %}
                </div>
            </div>
        </div>
    </body>
</html>

