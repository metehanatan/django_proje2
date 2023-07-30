## Django ORM Query;
''' shell
python manage.py shell
'''

'''python
# todo modelini import etmek:
from todo.models import todo

# Tum objeler:
todo.objects.all()

# Tum objeleri say:
todo.objects.all().count()

# Yeni todo olusturmak:
todo.objects.create(title="Shell uzerinden olusturulan todo")
todo.objects.create(title="Shell uzerinden yeni olusturulan todo", is_active=True)

# is_active olanlari göster:
todo.objects.filter(is_active=True)

# is_active olanlarin sayisini goster:
todo.objects.filter(is_active=True).count()

# UPDATE
# Yapilan sorguya uyan objelerin istenilen alanlari degistirilebilir.
todo.objects.filter(is_active=False).update(is_active=True)


# title icinde Django geçmeyenleri bul ve Django ekle
todos = todo.objects.exclude(title__icontains="django")          
for item in todos:
    item.title = f"{item.title} - Django"
    item.save()

'''