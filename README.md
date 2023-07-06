- Instalar Python;
- Instalar virtualenv;
- Criar pasta do projeto e lançar no VS Code;
- Abrir o terminal (Ctrl J);

- Digitar: 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
virtualenv venv
(Para criar o ambiente virtual com a pasta)

.\venv\Scripts\activate
(Para ativar o ambiente)
* Para desativa-lo basta digitar: deactivate;
* Caso a ativação der um erro de "[...] execução de scripts foi desabilitada neste sistema. [...]", vá ao PowerShell e digite: Set-ExecutionPolicy Unrestricted,
depois digite A.

pip install freeze
(Para saber as versões dos pacotes instalados)

pip freeze > requirements.txt
(Para criar um arquivo com as informações dos pacotes instalados)

django-admin help
(Para ver todos os comandos do django)

django-admin startproject setup .
(Para criar a pasta do projeto django)

python manage.py runserver
(Para executar o projeto)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Vá a settings.py para mudar configurações como idioma(pt-br) e hora(America/Sao_Paulo).

*************************************************************
PARA EVITAR QUE SUA CHAVE SECRETA VAZE:
pip install python-dotenv

Crie o arquivo .env e coloque a linha da secret_key sem aspas.

Depois importe o os na linha 13 e from dotenv import load_dotenv
load_dotenv()

E na secret_key coloque: str(os.getenv("SECRET_KEY"))


==============================================================
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
