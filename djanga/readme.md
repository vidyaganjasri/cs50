# 🐍 Django Project – Quick Start Guide

---

## 💡 What is Django?

**Django** is a high-level **Python web framework** used to build the **backend** of websites and web applications.

It helps you:
- ✅ Handle **HTTP requests** and responses
- ✅ Connect to **databases**
- ✅ Serve **HTML pages or JSON data**
- ✅ Build secure, scalable apps with **user authentication**, **form handling**, and **URL routing**

http status code :
✅ 200	OK (Success)
❌ 404	Not Found
⛔ 403	Forbidden
🔥 500	Server Error

---

## ⚙️ Installation
cmd: pip install django 

## Creation of django project 
cmd: django-admin startproject demo(#this is project name)

## To list the flie
cmd: dir

## To open in VS CODE
cmd: code .

## structures:

demo/

├── demo/

│   ├── __init__.py     → Tells Python this folder is special (a "package")

│   ├── settings.py     → Where all the important settings (like the database) are stored

│   ├── urls.py         → Decides which web pages users can visit

│   ├── asgi.py         → Used for advanced server setups (not often needed)

│   └── wsgi.py         → Used when you want to put your project online (on a server)

├── manage.py           → The main tool to run your project and perform tasks


