# Otimização em Smart Cities
Essa implementação corresponde a um projeto de Iniciação Científica (e, por conseguinte, de TCC) sobre Otimização em Smart Cities, no que tange ao processamento em tempo online de requisições IoT em Fog Computing.

## Definição do problema

[A ser escrita]

## Arquivos do repositório
- Dijkstra.ipynb: implementação inicial de uma solução para o problema utilizando algoritmo de Dijkstra para calcular o menor caminho na rede para definir, a partir de um sensor, o Fog em que será alocada a requisição. Um problema encontrado nessa implementação foi a necessidade de colocar um Nó Cloud como destino do caminho mais curto, a fim de se investigar a possibilidade de quaisquer nós fog intermediários no caminho como passíveis de alocarem e processarem a requisição
- Floyd-Warshall.ipynb: utilização do algoritmo de Floyd-Warshall como pré-processamento do grafo para calcular todos os possíveis caminhos entre todos os nós. A vantagem é a utilização uma única vez do cálculo do caminho mais curto. Nessa implementação, também se considera processar mais de um caminho para encontrar um válido para processar a requisição. Essa implementação trouxe resultados satisfatórios
- Gerador de Instâncias.ipynb: programa externo para geração de arquivos de instância.
- X.txt: arquivo de instância de número X
- log_X.txt: arquivo de log da instância X, no qual cada linha apresenta "Requisicao <id-da-requisicao> | Sensor <objeto-Sensor-origem-da-requisicao> | <numero-de-caminhos-testados> caminhos testados | Selecionado: <caminho-selecionado>"
- mapa_calor_X.html: mapa de calor da instância X

## Discussões/Hipóteses pendentes do problema

- E se mudássemos o critério de "peso das arestas" no cálculo do caminho mais curto do "tempo" para "custo"? Validar uma requisição com base no tempo de vida em processar_caminho();
