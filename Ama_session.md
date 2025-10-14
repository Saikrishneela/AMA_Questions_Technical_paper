1. Explain Django’s MTV (Model-Template-View) architecture. How does it differ conceptually from MVC?

Answer:
Django follows the MTV (Model–Template–View) architecture, which is a variation of the MVC (Model–View–Controller) pattern.

Model: Defines the structure of the database (data fields, relationships, and behaviors). It handles all data-related logic.

Template: Manages the presentation layer (HTML, CSS, JS) and defines how data is displayed to the user.

View: Contains the business logic; it processes requests, interacts with the model, and returns responses using templates.

Difference from MVC:
In Django:

View (MTV) = Controller (MVC)

Template (MTV) = View (MVC)
The main conceptual difference is in naming — Django’s “view” handles the logic, not the actual display.

2. What are Django signals? Give a practical use case for using signals in a Django application.

Answer:
Django signals allow certain senders (like models) to notify a set of receivers (functions) when specific actions occur in the application.

Common signals:

pre_save, post_save

pre_delete, post_delete

request_started, request_finished

Use case example:
Automatically create a user profile whenever a new User object is created:

3. Describe the role of middleware in Django. How would you implement a custom middleware to log user requests?

Answer:
Middleware is a lightweight, low-level plugin system in Django that processes requests and responses globally before they reach the view or after they leave it.

Roles of middleware:

Request/response modification

Authentication, sessions, and CSRF handling

Logging, caching, compression, etc.

Then, add it to MIDDLEWARE in settings.py:

4. What is the difference between ForeignKey, OneToOneField, and ManyToManyField in Django models?

Answer:

Relationship Type	Description	Example
ForeignKey	Defines a one-to-many relationship. A model instance can relate to many others.	One Author → Many Books
OneToOneField	Defines a one-to-one relationship. Each instance of a model is linked to exactly one instance of another model.	One User → One Profile
ManyToManyField	Defines a many-to-many relationship. Each instance can relate to multiple others.	A Student → Many Courses, and vice versa


5. Explain how Django handles database migrations.

Answer:
Migrations in Django are used to synchronize database schema with model changes.

python manage.py makemigrations
python manage.py migrate
Django compares the current models with the previous migration state and generates SQL commands automatically to apply changes (like creating tables, adding fields, etc.).

6. What is the purpose of the Django ORM (Object Relational Mapper)?

Answer:
The Django ORM allows developers to interact with the database using Python code instead of raw SQL.

Benefits:

Simplifies CRUD operations.

Provides database abstraction (supports SQLite, PostgreSQL, MySQL, etc.).

Protects against SQL injection.

Makes code more maintainable and portable.

# Without ORM (SQL)
SELECT * FROM Book WHERE author='John';

# With ORM
Book.objects.filter(author='John')


7. How does Django manage static files and media files?

Answer:
Django separates static files (CSS, JS, images) from media files (user-uploaded files).

Static files:

Defined in STATIC_URL and STATICFILES_DIRS.

Collected into one folder using:
python manage.py collectstatic

Media files:

Defined in MEDIA_URL and MEDIA_ROOT.

Used for user uploads like profile pictures.




