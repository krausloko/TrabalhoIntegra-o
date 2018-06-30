# Integração entre Webservice e Banco de Dados

Trabalho Final da disciplina BLU3024 - Integração de Sistemas para Automação, UFSC - Campus Blumenau

## Function:
O algoritmo desenvolvido é segmentado em três módulos:uma requisição do cliente e de acordo com o tipo de soliticação realizada enviará informações acerca do clima e do tempo de deslocamento de uma das localidades disponíveis.

## Quick start:
<p>1- Fazer download completo do repositório.<p>
<p>2- Executar o arquivo 'Avaliacao_1_homografia.m'.<p>
<p>3- Inserir o caminho para a pasta com conjunto de imagens (dataset) 'Avaliacao_1_homografia.m'.<p>
<p>4- Optar por uma das referências possíveis: 0 para imagem do canto ou 1 para imagem central.<p>
<p>5- Abrir as janelas para ver o panorama.<p>

## How it works:
**Módulo 1: Obter Informações**  
Responsável por acessar o webservice Open Weather Map a cada um minuto para obter informações do clima do Porto de Itajaí:
- Temperatura atual em graus Celsius;
- Umidade relativa do ar atual;
- Velocidade e direção do vento atuais.
Além das informações do clima, também é responsável por acessar o webservice do Google Maps para obter o tempo de deslocamento deste local até as quatros localidades disponíveis:
- UFSC Blumenau (coordenadas: -26.920729, -49.098526);
- Vila Germânica (coordenadas: -26.914024, -49.085023); 
- Prefeitura de Blumenau (coordenadas:  
- Aeroporto de Navegantes (coordenadas: -26.877582, -48.649516).  
**Módulo 2: Salvar Informações.**  
Responsável por persistir as leituras do clima e dos tempos de deslocamento em um banco de dados NoSQL, o Cassandra.  
**Módulo 3: Disponibilizar Informações**  
Responsável por atender as requisições dos clientes, o webservice deve disponibilizar informações de acordo com o tipo de requisição enviado pelo cliente as seguintes informações:
- Nome do local a que os dados armazenados pelo webservice se referem (neste caso Porto de Itajaí)
- Data da última leitura de dados;
- Hora da última leitura de dados;
- Temperatura atual; 
- Umidade relativa do ar atual;
- Velocidade e direção do vento;
- Tempo de deslocamento, tanto de carro, quanto de ônibus, do Porto de Itajaí até o local solicitado pelo cliente (um dos quatro locais disponíveis citados acima). 

Para ver o embasamento teórico e explicação detalhada do código basta ler o arquivo 'Relatório A1 - Visão Computacional.pdf'

## Results:
**Dataset**  
 ![building1](https://user-images.githubusercontent.com/35512686/39162585-9d2aba6e-474c-11e8-9dc5-d646d0621f64.JPG)
 ![building2](https://user-images.githubusercontent.com/35512686/39162586-9d55aef4-474c-11e8-88b3-ab9239e4d800.JPG)
 ![building3](https://user-images.githubusercontent.com/35512686/39162587-9d812ade-474c-11e8-8250-b14df9318203.JPG)
 ![building4](https://user-images.githubusercontent.com/35512686/39162589-9dac12ee-474c-11e8-9067-80fa51a4cea4.JPG)
 ![building5](https://user-images.githubusercontent.com/35512686/39162591-9defa7b6-474c-11e8-8059-2e46194290de.JPG)  
**Resultado**  
![resultado](https://user-images.githubusercontent.com/35512686/39167838-94c8c65c-4767-11e8-9f0b-8600ba6cc797.jpg)
## Requirements:
- Matlab R2016 ou mais recente
- Machine Vision Toolbox - Peter Corke
## License:
This toolbox is under the MIT License: http://opensource.org/licenses/MIT.
