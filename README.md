# Projetos-Bootcamp

## Projeto Final | Bootcamp Data Science 2021 - Alura

### CONTEXTUALIZAÇÃO

O surto de síndrome respiratória aguda grave coronavírus 2 (SARS-CoV-2) ou doença coronavírus 2019 (COVID-19) originada na China, se espalhou para o resto do mundo, levando a Organização Mundial de Saúde (OMS) a classificá-la como uma pandemia global [1].

A COVID-19 foi relatada pela primeira vez no Brasil em fevereiro de 2020 e o país rapidamente se tornou um dos mais afetados globalmente. No início de abril, o vírus começou a se espalhar pelas favelas de São Paulo e Rio de Janeiro, e o perfil do paciente mudou. Pessoas com menos de 50 anos foram hospitalizadas e morreram em taxas mais elevadas do que na Europa, China e EUA, sugerindo que a extrema desigualdade e a pobreza aumentam a vulnerabilidade à doença. Em países com poucos recursos, pessoas que poderiam ter sobrevivido em outros lugares estão morrendo de COVID-19 [2].

COVID-19 se espalha principalmente pelo trato respiratório. Estudos já confirmaram a transmissão de pessoa para pessoa como a principal via de disseminação. Pacientes com COVID-19 com histórico de doenças como doenças do sistema respiratório, deficiência imunológica, diabetes, doenças cardiovasculares e câncer são propensos a eventos adversos (admissão em unidade de terapia intensiva com necessidade de ventilação invasiva ou até morte)[1].

O foco atual tem sido o desenvolvimento de novos métodos terapêuticos, incluindo antivirais, anticorpos monoclonais e vacinas [1]. No entanto, embora haja sem dúvida uma necessidade urgente de identificar opções de tratamento eficazes contra a infecção com COVID-19, é igualmente importante a obtenção de dados precisos para melhor prever e preparar os sistemas de saúde e evitar colapsos, definido pela necessidade de leitos de UTI acima da capacidade (assumindo que recursos humanos, EPIs e profissionais estejam disponíveis) [3].

[1] Kooshkaki, O., Derakhshani, A. et al. Disease 2019: A Brief Review of the Clinical Manifestations and Pathogenesis to the Novel Management Approaches and Treatments, Front. Oncol., 10, 2020. https://www.frontiersin.org/article/10.3389/fonc.2020.572329 Acesso em: 23 Abr 2021.

[2] Ponce, D. The impact of coronavirus in Brazil: politics and the pandemic. Nat Rev Nephrol, 16, 483, 2020. https://www.nature.com/articles/s41581-020-0327-0#citeas Acesso em: 23 Abr 2021.

[3] COVID-19 - Clinical Data to assess diagnosis. https://www.kaggle.com/S%C3%ADrio-Libanes/covid19 Acesso em: 08 Fev 2021.

### OBJETIVO

O projeto desenvolvido teve como objetivo prever quais pacientes precisarão ser admitidos na unidade de terapia intensiva e, assim, definir qual a necessidade de leitos de UTI do hospital, a partir dos dados clínicos individuais disponíveis. Para tal, foram construidos modelos com as técnicas de Machine Learning.

Os dados utilizados foram disponibilizados no kaggle pelo time de ciência de dados do Hospital Sírio Libanês e podem ser acessados por este link (https://www.kaggle.com/S%C3%ADrio-Libanes/covid19).

### ESTRUTURA DO PROJETO

O projeto foi desenvolvido seguindo as recomendações do time do hospital Sírio-Libanês:

  * Cuidado para não usar os dados quando a variável de destino estiver presente, pois a ordem do evento é desconhecida (talvez o evento de destino tenha acontecido antes de os resultados serem obtidos). Eles foram mantidos lá para que possamos aumentar este conjunto de dados em outros resultados posteriormente.
  
![alt text](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F1591620%2Fb1bc424df771a4d2d3b3088606d083e6%2FTimeline%20Example%20Best.png?generation=1594740856017996&alt=media)

  * A identificação precoce dos pacientes que desenvolverão um curso adverso da doença (e precisam de cuidados intensivos) é a chave para um tratamento adequado (salvar vidas) e para gerenciar leitos e recursos. Portanto, um bom modelo preditivo usando apenas a primeira janela de tempo (0-2) provavelmente será mais clinicamente relevante.

  * Atenção às medidas repetidas em indivíduos, uma vez que esses valores são (positivamente) correlacionados.

O banco de dados é composto por 54 variáveis, contendo informações demográficas, doenças pré-existentes, resultados de exames de sangue e sinais vitais.
