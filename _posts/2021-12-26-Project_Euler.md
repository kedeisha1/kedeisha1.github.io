---
layout: post
title: Project Euler Webscraping 
image: "/posts/project_euler.png"
tags: [Scripting, Python]
---
I created a script that shows the most recent coding challenge from projecteuler.net (Not including images)

```ruby
import urllib.request
import re
import requests
from bs4 import BeautifulSoup

htmlfile = urllib.request.urlopen("https://projecteuler.net/recent")

htmltext = htmlfile.read()

regex = re.findall((r'problem=\d\d\d'), str(htmltext))
response = requests.get("https://projecteuler.net/" + regex[0])
soup = BeautifulSoup(response.text, "html.parser")

problem_page = response.text

         

euler_problem = open('eulerproblem.html', 'w')
euler_problem.write(problem_page)
euler_problem.close()

with open("eulerproblem.html", 'r') as html_file:
    content = html_file.read()
    soup = BeautifulSoup(content,"html.parser")
    problem_print = soup.get_text().replace('$', '').replace('\times', 'x')
    problem = soup.find_all('div', class_ = 'problem_content')
    print(problem_print)
    
 ```
