Blogging Website

Overview:
----------
This project walks you through the creation of a dynamic Blog Website using Flask. You'll learn how to handle user authentication, manage session-based access to protected routes, and build a full-featured blogging platform with a comment system.

Pages and Features:
--------------------
1. Home Page:
   - Displays summaries of all blog posts, ordered from newest to oldest.

2. Post Detail Page:
   - Accessed via: /post/<post_id>
   - Shows full content of a blog post along with all comments.
   - Logged-in users can submit new comments.

3. New Post Page:
   - Only accessible to logged-in users.
   - Allows creation of new blog posts using a form.

4. Registration Page:
   - Enables new users to register for an account.

5. Login Page:
   - Allows registered users to log in and manage their session.

6. Logout:
   - Ends the user session and redirects to the homepage.

Key Concepts and Tools Used:
-----------------------------
✔ Flask App structure with blueprints and routes  
✔ Static file serving for CSS styling  
✔ Base HTML layout with dynamic navigation using Jinja2  
✔ Template inheritance and loops for rendering post lists  
✔ Flask-SQLAlchemy for database modeling and interaction  
✔ Models for User, Post, and Comment  
✔ Flask-WTF for form rendering and validation  
✔ Flask-Login for user authentication and login protection  
✔ Real-time updates using Flask-SocketIO
✔ File upload handling with secure filenames

Deployment Instructions:
-----------------------
1. Create a new web service on Render.com
2. Connect your GitHub repository
3. Use the following settings:
   - Environment: Python
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn --worker-class gevent main:app`
4. Add environment variables:
   - `SECRET_KEY`: Generate a secure random key
   - `DATABASE_URL`: Your database connection string
5. Deploy the application
✔ Password hashing for secure credentials  
✔ Dynamic routing for individual post detail pages  
✔ Flash messaging for feedback (e.g., login success/failure, form errors)  
✔ Basic 404 error handling