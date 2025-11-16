# 2.1. Construção de Grafo RDF em Python
Exemplo de construção de uma ontologia a partir do banco de dados relacional disponível [neste link](https://www.w3.org/TR/r2rml/#example-input-database), incluindo:
- Como popular um grafo RDF
- Realizar serialização em Python usando `rdflib`
- Visualizar o grafo (NetworkX/Matplotlib, PyVis).

# 2.2. Exemplo de Consulta SPARQL usando a API do Wikidata
Exemplo de consulta SPARQL utilizando a API pública da plataforma Wikidata disponível [neste link](https://query.wikidata.org/), incluindo:
- Conversão para DataFrame (pandas)
- Visualização dos dados

## Visualização do mapa
![alt text](<2.2 - mapa_cidades_populacao.png>)

# 2.3. Ontologia + SPARQL
Exemplo de construção de uma ontologia simples, como popular um grafo RDF, serializar em Turtle e rodar consultas SPARQL em Python usando [`rdflib`]. Inclui opções de visualização (NetworkX/Matplotlib, PyVis) e inferência (owlrl).

> Conceitos-modelo: `Pessoa`, `Pesquisador` (subclasse de Pessoa), `Artigo`, `Instituicao`<br>
> Propriedades: `autorDe` (Pessoa→Artigo), `afiliadoA` (Pessoa→Instituicao)

## Modelo de Ontologia

**Classes**

- `ex:Pessoa`, `ex:Artigo`, `ex:Instituicao`

- `ex:Pesquisador rdfs:subClassOf ex:Pessoa`

**Propriedades de objeto**

- `ex:autorDe (domain: Pessoa, range: Artigo)`

- `ex:afiliadoA (domain: Pessoa, range: Instituicao)`

**Indivíduos (exemplos)**

- Pessoas: `ex:Bernardo`, `ex:Giovanna`, `ex:Claudio`, `ex:Carla`

- Artigos: `ex:ArtigoIA`, `ex:ArtigoBI`

- Instituições: `ex:UFRJ`, `ex:ITLAB`

## Representação do Grafo RDF

![alt text](<2.3 - grafo_estatico.png>)
