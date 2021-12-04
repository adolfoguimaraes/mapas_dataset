# Mapas Dataset

Arquivos em formato GEOJSON de Mapas do Brasil. Os arquivos originais são extraídos do site do IBGE (https://www.ibge.gov.br/geociencias/organizacao-do-territorio/malhas-territoriais/15774-malhas.html?=&t=downloads) e convertidos no formato GEOJSON no site https://mapshaper.org/. 

## Uso no ObservableHQ

**Esses mapas foram utilizados para montar o seguintes mapas no ObservableHQ:**

* https://observablehq.com/@adolfoguimaraes/br-se-queridodiario-mapa
* https://observablehq.com/@adolfoguimaraes/br-queridodiario-mapa

Neste caso, foi preciso utilizar o parâmetro `gj2008` na exportação do arquivo JSON. Segundo a documentação: 

`gj2008`: (GeoJSON) Generate output that is consistent with the pre-RFC 7946 GeoJSON spec (dating to 2008). Polygon rings are CW and holes are CCW, which is the opposite of the default RFC 7946-compatible output. Mapshaper's default GeoJSON output is now compatible with the current specification (RFC 7946).

Documentação completa disponível em: https://github.com/mbloch/mapshaper/wiki

## Problema no tamanho dos mapas

**Alguns mapas precisaram se reduzidos de tamanho (identificados pelo sufixo `_small` nos arquivos)**.

Uma explicação do que foi feito, está neste link: https://blog.exploratory.io/how-to-reduce-your-geojson-file-size-smaller-for-better-performance-8fb77759870c

**Obs:** Após a coversão precisei carregar e exportar novamente no MapShaper para gerar o formato de 2008. Não vi como incluir isso no comando de redução. 

