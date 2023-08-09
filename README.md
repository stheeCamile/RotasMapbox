# RotasMapbox

#  Projeto de Roteirização com Mapbox e OSMnx
Este projeto tem como objetivo demonstrar a criação de rotas em um bairro utilizando a biblioteca OSMnx para obtenção dos dados de ruas e a API do Mapbox para cálculo e visualização das rotas. O código está escrito em Python e utiliza as bibliotecas Folium, OSMnx, NetworkX, Plotly e Requests.

#  Descrição do Projeto
O projeto consiste em criar um mapa interativo que identifica um bairro, mostra marcadores nas ruas desse bairro e cria rotas que passam por essas ruas. O aplicativo também tem a capacidade de gerar uma rota que percorre todas as ruas do bairro.

#  Pré-requisitos
Python 3.x instalado
Pacotes necessários: osmnx, networkx, plotly, requests, folium

# Como Usar
Certifique-se de que você possui um token de acesso do Mapbox e substitua 'your_mapbox_token' pela sua chave no código.
Defina o nome do bairro e cidade na variável bairro e cidade.
O código obtém os dados das ruas do bairro usando o OSMnx e cria um grafo de ruas.
As coordenadas das ruas são obtidas a partir do grafo criado.
As coordenadas são agrupadas em grupos de no máximo 25 coordenadas para serem passadas à API do Mapbox Directions.
A função get_directions é usada para chamar a API do Mapbox Directions e obter as instruções de direção para cada grupo de coordenadas.
O mapa é plotado usando a biblioteca Folium com os marcadores das instruções de direção.
O mapa interativo é salvo em um arquivo HTML chamado route_map_with_directions.html.

# Executando o Projeto
1.Instale as bibliotecas necessárias executando o seguinte comando no terminal:
Copy code
pip install osmnx networkx plotly requests folium

2.Copie e cole o código em um arquivo .py.
3.Execute o arquivo .py.
4.Um arquivo HTML chamado route_map_with_directions.html será criado no diretório de execução. Abra esse arquivo em um navegador para ver o mapa interativo.

#  Notas
Certifique-se de substituir 'your_mapbox_token' pelo seu token de acesso do Mapbox.
As coordenadas são agrupadas em grupos de 25 para respeitar o limite de requisições da API do Mapbox Directions. Dependendo do tamanho do bairro, você pode ajustar esse valor.
Este projeto é um exemplo de como criar rotas em um bairro específico. Você pode expandir e personalizar o código para atender às suas necessidades específicas.
Lembre-se de considerar limitações de uso da API do Mapbox e outras políticas de uso ao implementar o projeto em um ambiente de produção
