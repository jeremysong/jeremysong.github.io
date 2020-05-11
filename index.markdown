---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
<html>
    <head>
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
        <link rel="stylesheet" href="css/timeline.css">
        <link rel="stylesheet" href="css/style.css">
    </head>
    <body>
        <div class="container py-5">
            <div class="row">
                <ul class="timeline">
                {% for paper in site.data.papers %}
                     <li class="timeline-item bg-white rounded ml-3 p-4 shadow">
                        <div class="timeline-arrow"></div>
                        <h2 class="h5 mb-0">{{ paper.title }}</h2><span class="small text-gray"><i class="fa fa-clock-o mr-1"></i>{{ paper.date }}
                        {% if paper.url %}
                        &nbsp;<a href="{{ paper.url }}">(link)</a>
                        {% endif %}
                        </span>
                        {% if paper.comment %}
                        <p class="text-small mt-2 font-weight-light">{{ paper.comment }}</p>
                        {% endif %}
                    </li>
                {% endfor %}
                </ul>
            </div>
        </div>    
    </body>
</html>