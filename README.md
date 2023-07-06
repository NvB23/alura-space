Sendo Assim vamos enviar o projeto para o GitHub

Primeiro crie um novo repositório no +;
Vá ao projeto e crie o arquivo .gitignore;
Vá ao site gitignore.io, pesquise por Django, copie tudo e cole no arquivo;

No terminal: 
git init (Inicia o repositório)
git add. (Copia e Seleciona tudo que vai mandar)
git commit -m "nome do projeto"
git remote add origin link do github
git push origin master
==============================================================
*************************************************************

Para criar um APP digite no terminal: python manage.py startapp nome_do_app, e coloque seu app no arquivo settings em "INSTALLEDS_APPS"
com " 'nome _do_app', ";

No arquivo views.py no seu APP import "from django.http import HttpResponse" e escreva a sua função;
Depois vá ao arquivo urls.py em setup importe a função e a adicione ao urlpatterns;

Para isolar as URLs crie um arquivo chamado urls.py no APP, nele importe o path do urls do setup e também a função, depois crie uma
lista chamda urlpatterns com um path nele assim como o urlpatterns do urls do setup. Em urls do setup adicione a biblioteca include ao
import de path e use ele no lugar do nome da função passando como parâmetro a localização da urls do APP;
