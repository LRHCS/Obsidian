The Jinja library lets you to use python in a HTML file
{%python_expression%}
- {##}
	- comment
- {%block title%}Home{%endblock%}
	- title is the name of this block, we can personalize the title tag in our python script
	- we need to enter in the render_template("base.html", **title="login"**)
		- this will change the title to login, if we dont enter anything, it will be Home
- {% extends layout %}
	- it will display the layout
	-  It tells the template engine that this template “extends” another template. When the template system evaluates this template, it first locates the parent. The extends tag should be the first tag in the template. Everything before it is printed out normally and may cause confusion.
- if 
- ```python
{% if kenny.sick %}
	Kenny is sick.
{% elif kenny.dead %}
	You killed Kenny!  You bastard!!!
{% else %}
	Kenny looks okay --- so far
{% endif %}```
- for
- ```python
<h1>Members</h1>
<ul>
{% for user in users %}
  <li>{{ user.username|e }}</li>
{% endfor %}
</ul>```
- variable
- ```python
{% set navigation = [('index.html', 'Index'), ('about.html', 'About')] %}
{% set key, value = call_something() %}```
- import
- ```python
{% import 'forms.html' as forms %}
<dl>
    <dt>Username</dt>
    <dd>{{ forms.input('username') }}</dd>
    <dt>Password</dt>
    <dd>{{ forms.input('password', type='password') }}</dd>
</dl>
<p>{{ forms.textarea('comment') }}</p>

```