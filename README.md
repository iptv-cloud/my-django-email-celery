# django-vue-graphql-celery
This is a  project demostrating the use of Django, Vuejs, Graphql, Celery, Redis to asychronously process huge job of loading file into the database.

Steps: 

1. Clone the repo: https://github.com/iptv-cloud/my-django-email-celery.git
2. cd productimporter
3. pip install pipenv && pipenv shell : this will install pipenv 
4. create a virtual environment.
5. pipenv install : this will install all the dependency packages
6. python manage.py makemigrations && python manage.py migrate && python manage.py runserver
7. open the localhost:8000 on your browser
8. Look for the urls

9. Sample graphql queries which may be used via http://127.0.0.1:8000/graphql/:
    for filtering->
    """
    query{
    products(find:"{'name':'Bryce Jones'}")
    {
        name
        sku
        description
    }
    }
    """
    for searching->
    """
    query{
        products(search:"Bry"){
            name
            sku
        }
        }
    """
