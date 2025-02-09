## ANÁLISE DE ALGORITMOS: Projeto Final
# Projeto de rota de ônibus em Boa Vista com Caixeiro Viajante multi-objetivo 
- Giovanna Mendes Garbácio (2021000712)

- Vitor Jordão Carneiro Briglia (2021013007)

## INSTRUÇÕES

O objetivo o trabalho Final é implementar um algoritmo aproximado para o caixeiro viajante multi-objetivo. Modelar e apresentar uma rota para os ônibus de Boa Vista-RR, considerando dois objetivos:
  - maximização do número de passageiros e minimização do tempo de rota.
  - Apresentar uma análise sobre os resultados encontrados com os algoritimos.

## RESUMO

O Relatório final em formato de artigo está disponível no arquivo [**Relatório Final.pdf**](https://github.com/vitor1616/VitorJordao_GiovannaGarbacio_FinalProject_AA_RR_2024/blob/main/Relat%C3%B3rio%20Final.pdf)

O Problema do Caixeiro Viajante busca encontrar a rota mais curta para visitar um conjunto de cidades e retornar ao ponto de partida, visitando cada cidade apenas uma vez. Esse problema NP-completo torna-se cada vez mais difícil à medida que o número de cidades cresce, levando a uma quantidade exponencial de possibilidades de rotas. Métodos heurísticos, como o Simulated Annealing, são frequentemente usados para encontrar soluções próximas do ótimo. Este trabalho implementa um algoritmo aproximado para o TSP multi-objetivo, modelando uma rota de ônibus em Boa Vista, Roraima. O objetivo é maximizar o número de passageiros e minimizar o tempo de viagem, utilizando a distância e a frequência de paradas de ônibus como parâmetros principais. Embora o Simulated Annealing forneça soluções eficientes, os desafios incluem o grande tamanho do grafo e a aproximação do fluxo de passageiros. Apesar dessas dificuldades, o método se mostrou flexível e eficaz na otimização de rotas de ônibus.

## ARQUIVOS
Todos os arquivo estão disponíveis também no [Drive](https://drive.google.com/file/d/1GmV2061WRlb2x7nmpLR9fZVYjcnMV-x7/view).

```
Códigos
├── ApenasParadas
│   ├── gerar_imagem.py
│   └── gerar_paradas.py
├── BuscaSimulatedAnneling
│   ├── gerar_rotaV7.py
│   └── imagem_comb.py
├── Grafo_inicial
│   └── gerar_grafo.py
├── GrafoParadas_V3
│   ├── gerar_grafo_com_paradas.py
│   └── gerar_imagem.grafo.py
├── ParadasOnibus
│   └── gerar_coordebadas_paradas_.py
├── file_in_root.ext
└── README.md
```

### Descrição do conteúdo das pastas na ordem de execução
* **ParadasOnibus** - O arquivo *gerar_coordenadas_paradas.py* gera o arquivo coordenadas_parada.txt com a latitude, longitude e endereço de todas as paradas contidas na pasta rotas.
* **Grafo_inicial** - O arquivo *gerar_grafo.py* cria o grafo que representa Boa Vista e recorta algumas partes do mapa que não são necessárias. O grafo é salvo em grafo_inicial_ARESTAS.json e grafo_inicial_NOS.json. O arquivo *gerar_imagem_grafo.py* plota uma imagem *grafo_inicial.png* do grafo gerado para vizualização.
* **GrafoParadasV3** - O arquivo *gerar_grafo_com_paradas.py* Associa as paradas de ônibus criadas em *ParadasOnibus* com o grafo da cidade criado por *Grafo_inicial* e atribui o peso aos vértices relativo a quantidade de associação a cada vértice. O arquivo *gerar_imagem_grafo.py* plota uma imagem *grafo_paradas.png* do grafo gerado com peso para vizualização.
* **ApenasParadas** - O arquivo *grafo_paradas.py* cria um gráfo só com as paradas que é armazenado em *grafo_paradas_somente_paradas_ARESTAS.csv* e *grafo_paradas_somente_PARADAS.csv*. O arquivo *gerar_imagem.py* plota uma imagem *grafo_paradas.png* do grafo gerado apenas com as paradas para vizualização.
* **BuscaSimulatedAnneling** - O arquivo *gerar_rotaV7.py* cria uma rota que é armazenada em *rota_simulated_annealing* (os testes feitos estão na pasta **Rotas Criadas**). O arquivo *gerar_comp.py* plota uma imagem *grafo_rota_simulated_annealing.png* da rota gerada para vizualização.

## RESULTADOS

Obtivemos diversas rotas (que estão salvas em Rotas Criada), dentre elas destacamos a [Rota3](https://github.com/vitor1616/VitorJordao_GiovannaGarbacio_FinalProject_AA_RR_2024/blob/main/Rotas%20Criadas/Rota3/grafo_rota_simulated_annealing3.png), que é a mais curta em distância, a [Rota12](https://github.com/vitor1616/VitorJordao_GiovannaGarbacio_FinalProject_AA_RR_2024/blob/main/Rotas%20Criadas/Rota12/grafo_rota_simulated_annealing12.png) que ebusca o maior número de pessoas e a [Rota5](https://github.com/vitor1616/VitorJordao_GiovannaGarbacio_FinalProject_AA_RR_2024/blob/main/Rotas%20Criadas/Rota5/grafo_rota_simulated_annealing5.png), que julgamos ser a mais equilibrada em relação aos dois fatores.

