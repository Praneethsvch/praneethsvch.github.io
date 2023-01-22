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
                background-color: black;
                width: 500px;
                height: 750px;
                margin: 5px;
                text-align: justify;
                line-height: 25px;
                font-size: 15px;
                margin-top: 30px;
            }

            .flex-container .text-container {
                width: 200%;
            }

            
            div.project-container {
              width: 400px;
              height: 500px;
              margin: 25px;
              float: center;
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
                        Flooding is one of the most dangerous and costly natural hazards, and has a large impact on infrastructure, mobility, public health, and safety. Following Hurricane Henri, on the night of Wednesday, September 1, 2021, Hurricane Ida reached New York City. For the first time in history, the National Weather Service (NWS) declared a flash flood emergency in New York City. It flooded streets, subways, and homes. Most tragically, Ida took the lives of 13 New Yorkers.
                        <br/>
                        <br/>
                        Former Mayor, Bill de Blasio on September 27, 2021 released <a href="https://www1.nyc.gov/assets/orr/pdf/publications/WeatherReport.pdf">"The New Normal: Combatting Storm-Related Extreme Weather in New York City"</a>, a landmark report that provides New York City with a new blueprint to prepare for and respond to extreme weather. As an immediate enhancements to storm analysis & data initiatives, <a href="https://www.floodnet.nyc/">FloodNet</a>, a network of state-of-the-art flood sensors, has prospered into a partnership with the MOCR, Office of the CTO, DEP, NYCEM, DOT, and NWS, aiming to expand the City’s nascent flood sensor network to provide real-time depth data in high-risk locations.
                        <br/>
                        <br/>
                        This sensing platform can be integrated into an early warning system throughout the city, alert communities on emergency preparedness and response, including real-time mitigation measures, identify areas that most urgently need post-storm assistance, validate existing flood models, and inform long-term stormwater resiliency planning. 
                        <br/>
                        <br/>
                        <i><u> <a href="https://praneethsvch.github.io/projects/floodnet">more about my work at FloodNet</a> </u></i>
                    </p>
                    
              </div>
            <div>
                <div class="project-container">
                    {% for project in site.data.settings.projects %}
                    <br/>
                    <br/>
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

