import os
import requests
from pprint import pprint

from dotenv import load_dotenv
load_dotenv()

api_key = os.environ.get("api_key")


def busca_por_id(film_id):
    url = f"http://www.omdbapi.com/?apikey={api_key}&i={film_id}"
    pedido = requests.get(url)
    dicionario_do_pedido = pedido.json()
    return dicionario_do_pedido


# print(busca_por_id("tt3228774"))


def busca_por_texto(texto_buscar):
    url = f"http://www.omdbapi.com/?apikey={api_key}&s={texto_buscar}"
    pedido = requests.get(url)  # conectar na URL
    # transformo a string que eu recebi num dicionário de python
    dicionario_do_pedido = pedido.json()
    return dicionario_do_pedido


# print(busca_por_texto('cruella'))


'''
Agora, faça uma função busca_qtd_total que retorna quantos
itens (pode ser filme, jogo, série ou o que for) batem com
uma determinada busca.
'''


def busca_qtd_total(texto_buscar):
    url = f"http://www.omdbapi.com/?apikey={api_key}&s={texto_buscar}"
    pedido = requests.get(url)  # conectar na URL
    # transformo a string que eu recebi num dicionário de python
    dicionario_do_pedido = pedido.json()
    return dicionario_do_pedido['totalResults']


res = busca_qtd_total("cruella")
# print(res)

'''
Faça uma função busca_qtd_filmes que retorna quantos
filmes batem com uma determinada busca.
'''


def busca_qtd_filmes(texto_buscar):
    url = f"http://www.omdbapi.com/?apikey={api_key}&s={texto_buscar}&type=Movie"
    pedido = requests.get(url)  # conectar na URL
    # transformo a string que eu recebi num dicionário de python
    dicionario_do_pedido = pedido.json()
    return dicionario_do_pedido['totalResults']


# print(busca_qtd_filmes("star wars"))


'''
Faça uma função busca_qtd_jogos que retorna quantos
jogos batem com uma determinada busca.
'''


def busca_qtd_jogos(texto_buscar):
    url = f"http://www.omdbapi.com/?apikey={api_key}&s={texto_buscar}&type=Game"
    pedido = requests.get(url)  # conectar na URL
    # transformo a string que eu recebi num dicionário de python
    dicionario_do_pedido = pedido.json()
    return dicionario_do_pedido['totalResults']


# print(busca_qtd_jogos("star wars"))

'''
Faça uma função nome_do_filme_por_id que recebe a id de
um filme e retorna o seu nome.
'''


def nome_do_filme_por_id(id_filme):
    url = f"http://www.omdbapi.com/?apikey={api_key}&i={id_filme}&type=Movie"
    req = requests.get(url)
    result = req.json()
    return result["Title"]


# print(nome_do_filme_por_id("tt3228774"))

'''
Faça uma função ano_do_filme_por_id que recebe a id de
um filme e retorna o seu ano de lançamento.
'''


def ano_do_filme_por_id(id_filme):
    url = f"http://www.omdbapi.com/?apikey={api_key}&i={id_filme}&type=Movie"
    req = requests.get(url)
    result = req.json()
    return result["Released"]


'''
Peguemos vários dados de um filme de uma vez.

A ideia é receber uma id e retornar 
um dicionário com diversos dados do filme.

O dicionário deve ter as seguintes chaves:
 * ano
 * nome
 * diretor
 * genero

E os dados devem ser preenchidos baseado nos dados do site.
'''


def dicionario_do_filme_por_id(id_filme):
    url = f"http://www.omdbapi.com/?apikey={api_key}&i={id_filme}&type=Movie"
    req = requests.get(url)
    result = req.json()
    resultDict = {
        "name": result["Title"],
        "ano": result["Released"],
        "diretor":  result["Director"],
        "genre":  result["Genre"]
    }
    return resultDict or []


# print(dicionario_do_filme_por_id("tt3228774"))
'''

Faça uma função busca_filmes que, dada uma busca, retorna
os dez primeiros items (filmes, series, jogos ou o que for)
que batem com a busca.

A sua resposta deve ser uma lista, cada filme representado por 
um dicionário. cada dicionario deve conter os campos
'nome' (valor Title da resposta) e 'ano' (valor Year da resposta).
'''


def busca_filmes(texto_buscar):
    pass  # implemente!


'''
Faça uma função busca_filmes_grande que, dada uma busca, retorna
os VINTE primeiros filmes que batem com a busca.
'''


def busca_filmes_grande(texto_buscar):
    pass  # implemente!
