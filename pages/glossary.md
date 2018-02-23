---
layout: page
title: Glossary
permalink: /glossary/
---

<div class="section">
    <h5>Glossary</h5> 
    <div class="row">
          <div class="col s12">
            <table class="highlight">
              <thead>
                <tr>
                    <th>Term</th>
                    <th>Description</th>
                </tr>
              </thead>
              <tbody>
                {% for term in site.data.glossary %}
                    <tr>
                        <td>{{term.name}}</td>
                        <td>{{term.description}}</td>
                    </tr>
                {% endfor %}
              </tbody>
            </table>
          </div>
    </div>
</div>