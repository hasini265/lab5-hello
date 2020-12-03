Django - hello world!

1. To get started with Django, you need to have Python installed and Virtual Environment setup.
2. Next install Django with the following command:
   "pip install django"

Creating a project:

1. From the command line, cd into a directory where you’d like to store your code, then run the following command:
   "django-admin startproject lab5_hello"

2. This will create a lab5_hello directory in your current directory.

3. change into lab5_hello directory and let's run the following command:
   python manage.py runserver

4. Then you will get something like this:

   Performing system checks...

   System check identified no issues (0 silenced).

   You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
   Run 'python manage.py migrate' to apply them.
   December 03, 2020 - 02:33:25
   Django version 3.1.4, using settings 'lab5_proj.settings'
   Starting development server at http://127.0.0.1:8000/
   Quit the server with CONTROL-C.

5. visit http://127.0.0.1:8000/ with your Web browser. You’ll see a “Congratulations!” page, with a rocket taking off. It worked.

6. Before proceeding further, Run 'python manage.py migrate'.

Creating the Polls app:

1. To create your app, make sure you’re in the same directory as manage.py and type this command:
   $ python manage.py startapp polls
2. Write your first view
   Let’s write the first view. Open the file polls/views.py and put the views.py Python code in it.
3. To call the view, we need to map it to a URL - and for this we need a URLconf.
   To create a URLconf in the polls directory, create a file called urls.py
   In the polls/urls.py file, add the urls.py code.
4. The next step is to point the root URLconf at the polls.urls module. In mysite/urls.py, add an import for django.urls.include and insert an include() 
   in the urlpatterns list.
   The include() function allows referencing other URLconfs. Whenever Django encounters include(), it chops off whatever part of the URL matched up to 
   that point and sends the remaining string to the included URLconf for further processing.
5. You have now wired an index view into the URLconf. Verify it’s working with the following command:
   $ python manage.py runserver
6. Go to http://localhost:8000/hello/ in your browser, and you should see the text “Message: Hello world!”, defined in the index view.

