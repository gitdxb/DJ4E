# DJ4E
Django for everybody by Dr Charles

Course link: https://www.dj4e.com/

## How to setup Django on PythonAnywhere (credit to DJ4E)
1. Setup a PYAW account
2. Start a `bash` shell, setup virtual env:
<pre><code>
mkvirtualenv django3 --python=/usr/bin/python3.6
pip install django ## this may take a couple of minutes
</pre></code>
3. When exit and come back, type this:
<pre><code>
workon django3
</pre></code>
4. Lets make sure that your django was installed successfully with the following command:
<pre><code>
python -m django --version
# This should show something like 3.0.2
</pre></code>
5. Lets also get a copy of the sample code for DJ4E checked out so you can look at sample code as the course progresses and install some important additional Django software libraries using pip.
<pre><code>
cd ~
git clone https://github.com/csev/dj4e-samples
cd dj4e-samples
pip install -r requirements.txt
python3 manage.py check
</pre></code>
6. After checking error
<pre><code>
python3 manage.py makemigrations
python3 manage.py migrate
</pre></code>
7. Building app
<pre><code>
cd ~
mkdir django_projects
cd django_projects
django-admin startproject mysite
</pre></code>
8. You need to edit the file ~/django_projects/mysite/mysite/settings.py and change the allowed hosts line (around line 28) to be:
<pre><code>
 ALLOWED_HOSTS = [ '*' ]
</pre></code>

For more, visit: https://www.dj4e.com/assn/dj4e_install.md