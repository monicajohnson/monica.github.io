---
layout: page
title: Posts
permalink: /posts/
---

<div class="row">
    <div class="col-sm-4 col-sm-push-8">
        <img src="/assets/portrait_square.jpg" alt="portrait" class="img-circle img-responsive"/>
    </div>
    <div class="col-sm-8 col-sm-pull-4">
        {% for post in site.posts limit:5 %}
        <div class="row">
            <div class="col-sm-12">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h1 class="panel-title">{{ post.title }}</h1>
                    </div>
                    <div class="panel-body">
                        {% if post.excerpt %}
                            <p>{{ post.excerpt }}</p>
                            <div class="pull-right">
                                <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">Read more<span class="caret"></span></a>
                            </div>
                        {% else %}
                            <p>{{ post.content }}</p>
                        {% endif %}
                    </div>
                    <div class="panel-footer text-right">
                        <p><small>{{ post.date | date: "%b %-d, %Y" }}</small></p>
                    </div>
                </div>
            </div>
        </div>
        {% endfor %}
        
        <div class="row">
            <div class="col-sm-12">
                <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS <i class="fa fa-rss" aria-hidden="true"></i></a></p>
            </div>
        </div>              
    </div>
</div>