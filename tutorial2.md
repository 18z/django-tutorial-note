Python Django tutorial 2

* 設定database、時區與語系、installed_apps

		vim settings.py

* 建立app

		python manage.py startapp article

		cd article
		ls -l

		models.py
		test.py
		view.py

* 定義欄位

		vim models.py

* create db

		python manage.py syncdb


* show create schema

		python manage.py sql article


* remove table and data from inside the db

		python manage.py reset article 


python manage.py shell
		
		>> from article.models import Article (press enter)
		>> article.object.all()
		[]
		>> from django.utils import timezone (pe)
		>> a = Article(title="test 1", body="blah", pub_date=timezone.now(), likes=0) (pe)
		>> a.save() (pe)
		>> a.id
		>> a = Article(title="test 2", body="blah",	pub_date=timezone.now(), likes=0) (pe)
		>> a.save() (pe)
		>> a.id
		>> a = Article(title="test 3", body="blah", pub_date=timezone.now(), likes=0) (pe)
		>> a.save() (pe)
		>> article.object.all()
		>> 

vim models.py
	def __unicode__
