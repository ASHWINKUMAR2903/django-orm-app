# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Screenshot 2023-04-03 111843](https://user-images.githubusercontent.com/119407186/229422143-988ac598-a54b-49ab-b54c-7b7a1d9fae88.png)

## DESIGN STEPS

### STEP 1:
An Django application is created inside dataproject folder.

### STEP 2:
A python program is written to create a table to store and retrieve data.

### STEP 3:
The table is created with 6 fields in which the username field is made as PrimaryKey.

### STEP 4:
Then the project files migrated. A superuser is also created.

### STEP 5:
Now the server side program is executed .

### STEP 6:
The admin page of our website is accessed using username and password.

### STEP 7:
Records are added and saved in the table inside the database.
## PROGRAM :
```python
from django.db import models
from django.contrib import admin

class GitDatabase(models.Model):
    username_primary_key = models.CharField(max_length=30, help_text="User name must be unique", primary_key=True,unique=True)
    password = models.CharField(max_length=30)
    firstname = models.CharField(max_length=20)
    lastname = models.CharField(max_length=20)
    profile_photo = models.ImageField()
    email = models.EmailField(max_length=50,unique=True)

class GitAdmin(admin.ModelAdmin):
    list_display = ('username_primary_key', 'password', 'firstname', 'lastname','profile_photo','email')
```

## OUTPUT :
![Screenshot 2023-04-03 093413](https://user-images.githubusercontent.com/119407186/229409652-65284a28-14cb-4859-82e6-f77dc082b942.png)
![Screenshot 2023-04-03 093818](https://user-images.githubusercontent.com/119407186/229409668-6a0f2f68-fab0-4585-b2e5-fd2187b1bfde.png)
## RESULT :
Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).
