# Modelo_de_Otimizacao_para_Gerar_Prontuario_de_Florais_de_Bach_Atraves_do_Solver

#### Aluna: [Fernanda Viviani de Paula](https://github.com/fernandaviviani/BIMaster_Trabalho_Final)
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC) 

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

---

### Resumo

De acordo com a medicina natural, nossos medos, preocupações e ansiedades são uma porta de entrada não apenas para males emocionais como para patologias físicas. 
Esta vertente milenar da medicina também acredita que podemos curar nosso corpo físico e emocional através das ervas medicinais.

O médico inglês Edward Bach desenvolveu um sistema de cura capaz de curar todo tipo de enfermidade e sofrimento emocional prestando atenção à natureza da doença.

De acordo com o Instituto Hahnemanniano Do Brasil, foram denominados “Florais de Bach”, a série de 38 infusões naturais extraídas de flores silvestres da 
região de Gales, Grã Bretanha, cujas propriedades curativas foram descobertas pelo médico gaulês entre os anos 1926 e 1934.

Os algoritmos genéticos foram desenvolvidos por John Henry Holland e são inspirados na Teoria da Evolução das Espécies de Darwin a partir da sobrevivência 
do mais forte, onde as novas populações são criadas a partir da combinação e mutação dos indivíduos das gerações anteriores.  A teoria de Darwin foi traduzida 
para o modelo computacional através do método de busca pela solução ótima ou a solução de uma determinada função objetivo.

No campo da medicina, são utilizados para resolver problemas complexos em diversas áreas como cardiologia, oncologia e reabilitação. Os algoritmos genéticos 
podem ser utilizados para a detecção de doenças, diagnósticos, e gerenciamento de cuidados de saúde, permitindo que os médicos visualizem possíveis aplicações 
desse método metaheurístico na aplicação prática da sua profissão

O presente trabalho tem como objetivo criar um modelo de algoritmo genético utilizando a ferramenta Solver do Excel para gerar o melhor prontuário possível 
de prescrição dos Florais de Bach. O prontuário é criado a partir das 38 flores existentes dentro deste sistema de cura onde são selecionadas apenas as cinco 
melhores para resolver o problema emocional do paciente. Foram classificados apenas sete tipos distintos de características emocionais: medo, angústia, indecisão, 
tristeza, falta de confiança, solidão e desespero. 


### Abstract <!-- Opcional! Caso não aplicável, remover esta seção -->

According to natural medicine, our fears, worries and anxieties are a gateway not only for emotional men but also for physical pathologies. 
This millennial branch of medicine also believes that we can heal our physical and emotional bodies through medicinal herbs.

English physician Edward Bach developed a healing system capable of curing all kinds of illness and emotional distress by paying attention to 
the nature of the illness.

According to the Instituto Hahnemanniano Do Brasil, “Florais de Bach”, a series of 38 natural infusions extracted from wild flowers in the region 
of Wales, Great Britain, whose healing properties were discovered by the Gallic doctor between 1926 and 1934 .

The genetic algorithms were combined by John Henry Holland and are inspired by Darwin's Theory of Evolution of Species from the survival of the fittest, 
where new ones were created from the combination and mutation of individuals from previous generations. Darwin's theory was translated into the computational 
model through the method of searching for the optimal solution or the solution of a given objective function.

In the field of medicine, they are used to solve complex problems in areas such as cardiology, oncology and rehabilitation. Genetic algorithms can be used for 
disease detection, diagnosis, and health care management, allowing physicians to envision possible applications of this metaheuristic method in the practical 
application of their profession.

The present work aims to create a genetic algorithm model using the Excel Solver tool to generate the best possible Bach Flower Remedies prescription record. 
The medical record is created from the 38 existing flowers within this healing system where only the five best are selected to solve the patient's emotional problem. 
Only seven distinct types of emotional characteristics were classified: fear, anguish, indecision, sadness, lack of confidence, loneliness and despair.


### 1. Introdução

Os dados coletados estão salvos em uma pasta de trabalho do Excel onde também foi realizada a modelagem do problema no Solver em uma planilha separada.
Os dados foram armazenados da seguinte forma:
Na coluna B conta a ID dos 38 florais, categorizadas entre 1 e 38.
Na linha 2 consta a ID das sete características emocionais, categorizadas entre 1 e 38.
Na linha referente a cada floral consta a nota de classificação do mesmo para a resolução de cada problema, categorizada entre 1 e 5.


### 2. Modelagem

A extração da base de dados e modelagem do Solver foram realizadas em formato de Pasta de Trabalho do Excel e apresenta os campos listados abaixo:
 
Planilha Tabela de Florais:
 
Planilha com as 38 flores e as sete características emocionais, onde cada floral é mensurado a partir da sua capacidade de resolver cada um dos problemas 
apresentados em uma escala entre 1 e 5:

<img src="https://github.com/fernandaviviani/BIMaster_Trabalho_Final/blob/main/Tabela%20Florais%20img.PNG"/>

 
Planilha Solver:
 
O modelo de algoritmo genético desenvolvido a partir do Solver gera o ID dos problemas emocionais, o grau de intensidade apresentado pelo paciente para cada 
característica apresentada (1-10) e as cinco melhores flores para solucionar o quadro apresentado no diagnóstico clínico, com o grau de eficácia de cada uma (1-5) 
e seus respectivos ID.
Há também a função maximizar, que mostra a média e eficácia da fórmula apresentada pelo Solver para resolver o quadro do paciente.
Além disso, foi acrescentada uma função que determina que cada fórmula deve conter apenas flores distintas.
É importante ressaltar que cada prontuário deve conter cinco flores para garantir a eficácia do mesmo. 

<img src="https://github.com/fernandaviviani/BIMaster_Trabalho_Final/blob/main/SOLVER%20img.PNG"/>

 
As questões são: 
1 – Como esta flor resolve cada uma das sete características emocionais? (Escala de 5 = Muito Eficiente a 1 = Muito Ineficiente)
5 4 3 2 1
2 – Quais são as cinco melhores flores distintas para solucionar o problema emocional apresentado pelo paciente? 
O solver nos fornece as cinco melhores opções dentro do conjunto das 38 flores
Maximização
a combinação dos florais deve ter a melhor média possível a partir da soma da pontuação individual de cada um deles para a resolução do problema

Identificar as restrições
cada fórmula deve ter cinco flores distintas entre si
a média da combinação dos florais de cada fórmula deve ser maior ou igual a 6 e não pode ultrapassar o valor 10.
a nota de cada floral que mede a sua eficácia para resolver o problema emocional (y) deve ser um valor inteiro entre 1 e 10.
cada flor é representada por um número inteiro entre 1 e 38
cada problema emocional é representado por um número inteiro entre 1 e 7

Variáveis de Decisão

Xij - fórmula com os melhores florais (i) para resolver o problema emocional (j)

Função Objetivo

MAX (Xij) =  Y1 + Y2 + Y3 + Y4 + Y5 / 5

onde Y é o valor da nota atribuída para cada flor (i) na resolução do problema emocional (j)

Restrições

Y1 + Y2 + Y3 + Y4 + Y5 / 5  ≥ 6
Y1 + Y2 + Y3 + Y4 + Y5 / 5  ≤ 10
Xij ⊃ 5i
i  ≥ 6 
i ≤ 38
j ≥ 1
j ≤ 7
i ∊ ℤ
j ∊ ℤ
 


### 3. Resultados

A análise dos resultados obtidos revela uma alta acurácia do modelo para resolver os problemas emocionais apresentados pelos pacientes. Principalmente quando 
comparadas as flores escolhidas pelo Solver para o prontuário com a eficácia das mesmas de acordo com a literatura especializada em florais de Bach. 
Inclusive quando os resultados são comparados com a análise técnica  da obra do próprio Edward Bach “ Os outros curadores e outros remédios” que evidencia quais 
os problemas em que cada flor atua com mais eficácia.

A análise das flores escolhidas pelo Solver mostra que cada uma apresenta uma nota de eficiência entre 4 e 5 para solucionar cada característica emocional, o que 
representa aproximadamente 80% e 100% de valia.

O valor máximo que a função maximizar pode fornecer para cada prontuário é 50, visto que o modelo é construído a partir de cinco variáveis distintas que podem ter 
uma eficácia de grau máximo 5.

Nos teste realizados, a função maximizar apresenta resultados entre 35,45 e 45. O que evidencia uma eficácia entre 70,9% e 90%.
Apesar de uma restrição na quantidade de flores, o modelo pode trabalhar com diferentes tipos de problemas emocionais. Porém, os resultados mostram que testes 
realizados com menos problemáticas a serem resolvidos, apresentaram uma eficiência com maior acurácia que foi evidenciada pela função maximizar.


### 4. Conclusões

A análise evidenciou que o modelo apresenta alta acurácia nos resultados dos prontuários para tratar as setes características emocionais elucidadas na Tabela 
de Florais.

Ficou evidente a importância de ter como restrição a necessidade de que as cinco flores selecionadas sejam distintas umas das outras, de modo que o modelo não 
inclua na fórmula a mesma flor mais de uma vez. 
Convém salientar que prontuários que apresentam muitas características emocionais para serem tratadas apresentam uma acurácia menor daqueles com menos problemáticas 
envolvidas.

Como o foco do presente estudo está nos Florais de Bach, convém que dados relativos à Solução sejam analisados em conjunto com a literatura sobre esta temática e a 
prática clínica do terapeuta.
Como sugestão para trabalhos futuros podemos incluir a adaptação do mesmo modelo para o prontuário de pacientes que apresentam problemas emocionais a partir do 
tratamento de fitoterapia (com ervas medicinais).

### 5. Sugestão para Trabalhos Futuros

Existe uma etapa antes de prescrever as flores onde através de algumas perguntas modelo SIM/NÃO o terapeuta consegue fazer uma anamnese com o diagnóstico do paciente. Pode-se fazer um modelo de algorítimo genético no Solver similar ao proposto neste presente trabalho, porém com os sintomas e a pontuação que o paciente teve no questionário. O objetivo será descobrir o problema emocional que o paciente tem, para então ir para a etapa seguinte de prescrição das flores (que é o modeloque já temos pronto com este trabalho).


Matrícula: 202.100.338

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
