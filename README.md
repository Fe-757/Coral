# Coral
Coral is a programming language developed exclusively for creating backends in a simple way.

# About
Coral is in a very early stage, version 0.1.0, expect bugs and a lack of features as it is an initial version.

# How to run
Download the Coral.exe compiler > Add the compiler to your system's Path > Open a directory and create a text file, write the server code, and save it as .coral > Open PowerShell in the file's directory and run: coral filename.coral

# Exemples:

A simple server:

create.http <rec, ret> = [
  ret "Resposta do servidor"
    ret.end]
port {3000}

Hosting an HTML page:

require = files

create.https <rec, ret> = [
  index = "home.html"
    ret.index] 
port {3001}

download page:

require = files

create.https <rec, ret> = [
  index = "myapp.html"
    ret.index] 

$ download (
rec {/download.html}
ret 'my-app.apk'
ret.end)

port {3002}

# Contact
If you would like to suggest ideas or give feedback, please send an email to: Ferfernando345256@gmail.com
