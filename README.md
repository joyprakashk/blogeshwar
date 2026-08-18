<p align="center">
  <img src="blog/static/image/logo.png" alt="BLOGeshwar Logo" width="340"/>
</p>

# BLOGeshwar

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat-square&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-4.2-092E20?style=flat-square&logo=django&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

A web blogging platform built with Django. Users can register, log in, publish posts, and browse content from the community feed.

---

## Tech Stack

<p align="center">
  <img src="blog/static/image/tech-stack.png" alt="Tech Stack"/>
</p>
---

## Screenshots

**Register**
![Register](assets/blog-register.png)

**Login**
![Login](assets/blog-login.png)

**Write a Post**
![Write Post](assets/blog-post-write.png)

**Post Feed**
![Post Feed](assets/blog-posts.png)

---

## Getting Started

**Prerequisites:** Python 3.10+ installed on your system.

**1. Clone the repository**

```bash
git clone https://github.com/joyprakashk/blogeshwar.git
cd blogeshwar
```

**2. Create and activate a virtual environment**

```bash
# macOS / Linux
python3 -m venv venv
source venv/bin/activate

# Windows (PowerShell)
python -m venv venv
.\venv\Scripts\Activate.ps1

# Windows (cmd)
python -m venv venv
.\venv\Scripts\Activate.bat
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Apply database migrations**

```bash
python manage.py migrate
```

**5. Create an admin account** *(optional)*

```bash
python manage.py createsuperuser
```

**6. Start the development server**

```bash
python manage.py runserver
```

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

---

## Project Structure

```
Blog-Bridges/
├── assets/                
├── blog/                   
│   ├── migrations/
│   ├── static/image/       
│   ├── templates/blog/    
│   ├── models.py           
│   ├── views.py           
│   └── urls.py            
├── blog_app/               
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── manage.py
└── requirements.txt
```

---

## URL Routes

| Route | View | Description |
|---|---|---|
| `/` | signup | New user registration |
| `/login/` | loginn | User login |
| `/home/` | home | Community post feed |
| `/newpost/` | newPost | Create a new post |
| `/mypost/` | myPost | Current user's posts |
| `/signout/` | signout | Log out and redirect |
| `/admin/` | Django admin | Admin panel |

---

## Database

The repository ships with a committed `db.sqlite3` containing development data. To start with a clean database:

```bash
rm db.sqlite3                    
python manage.py migrate        
python manage.py createsuperuser 
```
