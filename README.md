# Python-Automation-with-ChatGPT

https://www.youtube.com/watch?v=w-X_EQ2Xva4

https://raw.githubusercontent.com/RodrigoMvs123/Python-Automation-with-ChatGPT/main/README.md

Python 
Program 
Extract headers from webpage 
Translate to Spanish 
Save into html file 
Write Program 
Go through downloads folder
Find files older than 30 days  
Move into “to delete” folder 
Python / ChatGPT / Python, Python 

Python Program 
Accept user input for automation task 
Connect to API to request Python code 
Save into Python file 

Why Python for Automation?
Large ecosystem - Many useful libraries for Automation 
Simple, flexible and easy to learn 
Library 
Server operating system 
Cloud Platforms  / Ansible 
     - You will find a great library for your specific automation use case

Python 
Automation and DevOps 
Data Analysis 
Machine Learning 

JavaScript 
Web Development 

Java 
Enterprise Software 

Demo Part:
Connect to OpenAI API 
Python OpenAI API Python 
Building app with OpenAI´s API 
ChatGPT uses OpenAI´s powerful models, but has been further fine-tuned 

OpenAI provides API to access their pre-trained AI models
Using this API, developers can connect and easily integrate AI capabilities into their own apps and scripts 


Application Interface 
OpenAI API - https://platform.openai.com/docs/api-reference/introduction

Users   

How to connect to the API ? 
1 Create an account on OpenAI platform 
2 Create an API Key
Unique Key for your user account used for authentication   
                        Python / API Key / OpenAi API

Create account and API Key 
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
https://platform.openai.com/docs/introduction

Pre-Requisites for Demo
                       1- Learn Python Syntax and Programming Basics
                       2- Need to have Python3 installed

[\W]$ mkdir python-chatgpt
[\W]$ cd python-chatgpt
[\W]$ ls
[\W]$ code.
[\W]$ python3
>>> exit()
[\W]$ pip3


1- Python and PIP installation 
2- Know Python syntax and programming basics

Write Python script to connect to OpenAI

[\W]$ mkdir python-chatgpt
[\W]$ cd python-chatgpt
[\W]$ ls
[\W]$ code.
Visual Studio Code 

>PYTHON-CHATGPT
python-chatgpt.py


Interaction with API using HTTP requests
Library
HTTP Client / HTTP Request OpenAI´s HTTP Server
HTTP Response / HTTP Client 

>PYTHON-CHATGPT
python-chatgpt.py
import requests
1 - Generic HTTP library
2 - OpenAI specific library 
Hides underlying complexity 
            3 - Syntax specific to that specific technology it was built for 

In this demo, we will use the generic requests library 


 >PYTHON-CHATGPT
python-chatgpt.py
import requests
( module ) requests
Requests HTTP Library 
Request in an HTTP library,written in python, for human beings.Basic GET usage:
>>> import requests 
>>> r =request.get (‘https://www..python.org’)
>>> r status_code
200
> b ‘python is a programming language’ in r.content
True

Which API endpoint ( = specific location or URL to access a particular function or service)?
Our input 
Python 
HTTP Request 
api.openai.com 
Different Endpoints 
/ Completions 
/ Images / Generations 
…
 

 >PYTHON-CHATGPT
python-chatgpt.py
import requests

api_endpoint = ‘https://api.openai.com/v1/completions’ // endpoint 
api_key = “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”

Which URL to connect 
Key for automation 
HTTP library to actually send the request 

HTTP Request Methods 

Indicate the desired action to be performed 
GET = to retrieve data 
POST = To send data and optionally get data back 
Other Methods: PATCH, PUT, DELETE, … 



 >PYTHON-CHATGPT
python-chatgpt.py
import requests

api_endpoint = ‘https://api.openai.com/v1/completions’ // endpoint 
api_key = “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”

request.post(api_endpoint)


We need the following in the POST request:
URL = The API endpoint, we want to send this request to 
HEADER = Metadata of the request 
BODY = Json data to send in the body of the request 
 
Metadata of a HTTP request 
Authorization 
To provide credentials / token when sending a request
to a protected resource / endpoint

https://platform.openai.com/docs/api-reference/completions/create
Completions 
> Create Completion 

curl


 >PYTHON-CHATGPT
            hello-world.py

python-chatgpt.py
import requests
import argparse 
import os

parser = argparse.ArgumentParser()
parser.add_argument(“prompt”, help=”The prompt to send to the OpenAI API”)
parser.add_argument(“file_name”, help=”Name of the file to save Python script”)
args = parser.parse_args() 

api_endpoint = ‘https://api.openai.com/v1/completions’ 
// “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”
api_key = os.getenv(“OPENAI_API_KEY”)


            request_headers = {
           “Content-Type”: “application/json”
           “Authorization”:  “Bearer” + api_key

}

request_data ={
            "model": "text-davinci-003",
            "prompt": f"Write python script to{args.prompt}.Provide only code, no text",
            "max_tokens": 500,
            "temperature": 0.5


}

response = request.post(api_endpoint, headers=request_headers, json=request_data)

if response.status_code == 200:
       response_text = response.json()[“choises”] [0] [“text”])
// open()= Built-In function that opens a file and returns it 
       with open(“output.py”, “w”) as file: 
//  with open(“yyy”, “w”) as file: 
//  with open (args.file_name, “w”)


              file.write(response_text) 
else: 
       print(f“Request failed with status code: { str (response.status_code)}”)

#!/usr/bin/env python

#Print “Hello World”
[\W]$

// https://platform.openai.com/docs/models/gpt-3-5
// text-davinci-003

Instal Library 
python3 = Execute Python script
pip3 = Python package manager to install Python libraries
[\W]$ pip3 install request

Execute Python Script 
[\W]$ python3 python-chatgpt.py


Write Python script to connect to OpenAI
      "prompt": "Write python script for printing out today’s date. Provide code no text",

[\W]$ python3 python-chatgpt.py
import datetime
#Get today´s date
today = datetime.date.today()

#print out today´s date
print (f”Today´s date is {today}”)

[\W]$ 

Accept Prompt Input 

[\W]$ python3 python-chatgpt.py “print todays date”
import datetime
print (datetime.datetime.now().strftime(“%d/%m/&y‘))

[\W]$ python3 python-chatgpt.py “Hello World”
print (“Hello World”)

[\W]$ python3 python-chatgpt.py “calculate number of days from 1 million minutes”
days = 1000000 / (24 * 60)
print(days)



Save Python code and extract API Key 

Python script file 
Plain Python code…
OpenAI API 
[\W]$ python3 python-chatgpt.py “calculate number of days from 1 million minutes”
 >PYTHON-CHATGPT
python-chatgpt.py
            output.py 
days = 1000000 // 1140
print(days) 
[\W]$ python3 python-chatgpt.py “print hello world”
print(“Hello World”)

[\W]$ python3 python-chatgpt.py “print hello world” “hello-world.py”
 >PYTHON-CHATGPT
python-chatgpt.py
            output.py 
hello-world.py
[\W]$ export OPENAI_API_KEY=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


[\W]$ python3 python-chatgpt.py “print hello world” “hello-world.py”
 >PYTHON-CHATGPT
python-chatgpt.py
hello-world.py


Automation Script for Blog Post Use Case
Translate article headers to Spanish and save into HTML file 

Python
Extract headers from webpage
Translate to Spanish
Save into html file

[\W]$ python3 python-chatgpt.py “extract all html headers from a web page, translate to Spanish and save the result into an html file” “extract-translate-headers.py”

[\W]$
 >PYTHON-CHATGPT
            extract-translate-headers.py
            hello-world.py
python-chatgpt.py


 >PYTHON-CHATGPT
            extract-translate-headers.py
# Import libraries 
import requests
from bs4 import BeautifulSoup
from googletrans import translate 

 # Get the page
url = ‘https://requests.readthedocs.io/en/latest/api/’
// https://www.crummy.com/software/BeautifulSoup/bs4/doc/
page = request.get(url)

# Parse the page 
soup = BeautifulSoup(page.text, ‘html.parse’)

# Get all the headers elements 
headers = soup.find_all([ ‘h1’, ‘h2’,’h3’, ‘h4’, ‘h5’, ‘h6’])

# Translate each header to Spanish
translator = googletrans.translator()
spanish_headers = []
for header in headers:
     translate_result = {
           “text”: translator.translate(header.text, dest=’es’).text,
           “name”: header.name
     }     
     spanish_headers.append(translated_header)
 
# Create an HTML file with the Spanish headers
with open(‘spanish_headers.html’, ‘w’) as f:
       f.write (‘<html n\>’)
       for header in spanish_headers:
            f.write(f’<header[“name”]}>{header [“text”]}</header[”name”]>n\’)
       f.write (‘</html\n>’)

[\W]$ pip3 uninstall bs4 googletrans
Proceed (Y/n) Y 
[\W]$ pip3 install bs4
[\W]$ pip3 install googletrans===3.1.0a0
[\W]$ python3 extract-translate-headers.py
 >PYTHON-CHATGPT
            extract-translate-headers.py
            hello-world.py
python-chatgpt.py

spanish_headers.html 
[\W]$ python3 extract-translate-headers.py

<html>
<h1>Una guía sobre cómo comenzar en TI en 2023 - Principales trayectorias profesionales de TI</h1>
<h2>La entrada a la tecnología puede ser abrumadora 🤯</h2>
<h2>Mi fondo 👩🏻‍💻</h2>
<h2>Carreras de TI más populares 💎</h2>
<h2>Enfoque general de aprendizaje 🧠</h2>
<h2>1 - Conviértete en ingeniero de software 👨🏼‍💻</h2>
<h2>Diferentes subcampos de la ingeniería de software.</h2>
<h2>Generalista o Especialista</h2>
<h2>Hoja de ruta para convertirse en ingeniero de software ☡</h2>
<h4>1 - Aprende los conceptos básicos de desarrollo y programación de software</h4>
<h4>2 - Desarrollar proyectos de ejemplo simples</h4>
<h2>¿Cómo elegir un lenguaje de programación?</h2>
<h2>Conceptos sobre características y sintaxis 💡</h2>
<h2>No se desperdicia conocimiento, siempre puedes cambiar</h2>
<h2>Consejos sobre cómo aprender 🧑🏼‍🏫</h2>
<h2>2 - Conviértase en un ingeniero DevOps ♾</h2>
<h2>Transición a DevOps</h2>
<h2>3 - Conviértete en ingeniero de la nube ☁️</h2>
<h2>Hoja de ruta para convertirse en un ingeniero de la nube ☡</h2>
<h2>Nube frente a DevOps</h2>
<h2>4 - Conviértete en Ingeniero de Seguridad TI - Ciberseguridad 🔐</h2>
<h2>Tareas y responsabilidades de un ingeniero de seguridad</h2>
<h2>Gran Demanda 👀</h2>
<h2>Hoja de ruta para convertirse en ingeniero de seguridad de TI ☡</h2>
<h2>5 - Conviértete en analista de datos, ingeniero de datos, científico de datos - Big Data 📊</h2>
<h4>Datos generados por humanos 👥</h4>
<h4>Datos generados por el dispositivo ⚙️</h4>
<h4>Datos sin procesar vs procesados</h4>
<h2>Analista de datos</h2>
<h4>Habilidades principales</h4>
<h2>Ingenieros de datos</h2>
<h2></h2>
<h2>Científico de datos</h2>
<h2>6 - Conviértete en un ingeniero de aprendizaje automático 🤖</h2>
<h2>Campo de ciencia de datos vs aprendizaje automático</h2>
<h2>¿Qué es el aprendizaje automático? 🤔</h2>
<h2></h2>
<h2></h2>
<h2>Habilidades que necesitas tener</h2>
<h2>Python - Lenguaje de Propósito General 🐍</h2>
<h2>Bibliotecas Python Core vs Python para un campo específico</h2>
<h2>¿Dónde y cómo aprender: grado en informática, cursos, bootcamps, autoaprendizaje? 📚</h2>
<h2>Encuentre una hoja de ruta clara</h2>
<h2>Comienza tu viaje hacia TI 👩🏻‍💻</h2>
</html>


Automation Script for Cleaning Download Folder

[\W]$ python3 python-chatgpt.py “go through files in Downloads folders, check their dates and if they are old than 30 days, move them to folder called to_delete” “clean-dowloads.py”

Use Case 1:
Move files older than 30 days into own folder

Python 
Go through downloads folder
Find files older than 30 days
Move into “to_delete” folder
 >PYTHON-CHATGPT
            clean-download.py
            extract-translate-headers.py
            hello-world.py
python-chatgpt.py
            spanish_headers.html
clean-downloads.py
import os
import shutil
from datetime import datetime, timedelta

# set the path of the folder to check
folder_path = os.path.join(os.path.expanduser('~'), 'Downloads')

# set the path of the folder to move files to
to_delete_folder_path = os.path.join(os.path.expanduser('~'), 'to_delete')

# create the folder if it doesn't exist
if not os.path.exists(to_delete_folder_path):
    os.makedirs(to_delete_folder_path)

# get the list of files in the folder
files = os.listdir(folder_path)

# get the current date
now = datetime.now()

# loop through the files
for file in files:
    # get the file path
    file_path = os.path.join(folder_path, file)

    # get the file's modification date
    modified_date = datetime.fromtimestamp(os.path.getmtime(file_path))

    # calculate the time difference
    time_difference = now - modified_date

    # if the file is older than 30 days, move it
    if time_difference > timedelta(days=30):
        shutil.move(file_path, to_delete_folder_path)

[\W]$ python3 clean-downloads.py

