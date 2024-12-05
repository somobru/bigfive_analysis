# Análise Big Five 
Esse código em python tem cmomo objetivo analisar perfis de personalidade com base no modelo Big Five.

Descrição da solução, em 2 níveis de abstração

Módulos:

Para esse projeto nós dividimos a solução em 5 grandes Módulos:
1. Módulo de Leitura de Dados
Função Relacionada: iniciar_menu
Descrição: A função iniciar_menu exibe um menu para o usuário com opções para iniciar o processamento ou sair. Se o usuário optar por iniciar, a função chama outras funções para calcular e exibir detalhes sobre o grupo ideal, como o número de líderes, mediadores e criativos, além do número de grupos possíveis.

2. Módulo de Análise dos Traços
Funções Relacionadas:

2.1. calcular_escores
Descrição: A função calcular_escores tem como objetivo calcular a média das pontuações (escores) para diferentes traços de personalidade com base no questionário. Ela leva em conta tanto o traço associado a cada resposta quanto a forma como o traço é avaliado (polo positivo ou negativo).

2.2. classificar_tracos
Descrição: A função classificar_tracos tem como objetivo classificar traços de personalidade com base nas médias das pontuações obtidas no teste de personalidade Big Five, categorizando-os em três grupos: mais acentuados, polo oposto e medianos.

2.3. calcula_tracos_faixa3
Descrição: Cria uma lista vazia chamada pontuacao_pessoas para armazenar as pontuações de várias pessoas. A função solicita que o usuário insira respostas separadas por vírgula (que representam as pontuações de uma pessoa para diferentes traços de personalidade). Avalia quais traços estão na faixa acentuada, no polo oposto e na faixa mediana, e os coloca em uma nova lista, sendo, respectivamente, alto, médio e baixo. Ao final, retorna as três listas preenchidas com os traços de cada pessoa classificados como altos, médios ou baixos.

3. Módulo de Formação de Grupos

Funções Relacionadas:

3.1. calcula_grupo
Descrição: Utiliza a função calcula_tracos_faixa3() para obter três listas: alto, médio e baixo. Para cada sublista em alto, médio e baixo, a função itera e verifica qual traço de personalidade está presente. Dependendo do traço de personalidade encontrado, a função adiciona um rótulo específico a uma lista chamada "pessoa".

3.2. calcula_planejador
Descrição: Calcula o número de pessoas planejdoras na sala, baseando-se em traços associados ao perfil planejador.

3.5. calcula_analista
Descrição: Calcula o número de pessoas analistas na sala, baseando-se em traços associados ao perfil analaista.

3.3. calcula_mediador
Descrição: Calcula o número de pessoas mediadoras na sala, baseando-se em traços associados ao perfil mediador.

3.4. calcula_lider
Descrição: Calcula o número de pessoas líderes na sala, baseando-se em traços associados ao perfil de liderança.

4. Módulo de Cálculo de Possíveis Grupos
Função Relacionada:

4.1. calcular_numero_grupos_possiveis
Descrição: Calcula a quantidade total de grupos possíveis com base na personalidade que tem o menor número de pessoas, já que visamos que todos os grupos tenham pelo menos uma pessoa associada a cada personalidade.

5. Módulo de Relatórios e Resultados

Função Relacionada:

5.1. main
Descrição: A função main serve para iniciar a execução do programa chamando a função iniciar_menu, que apresenta o menu para o usuário e gerencia o processamento principal do grupo ideal.

Resumo das Relações

Leitura de Dados: iniciar_menu- Exibe um menu e, com base na escolha do usuário, inicia o processamento do grupo ideal e exibe resultados relacionados.

Análise dos Traços:
calcular_escores- Calcula a média das pontuações para diferentes traços de personalidade, considerando o traço e seu polo.
classificar_tracos- Classifica os traços de personalidade em três grupos (acentuados, polo oposto e medianos) com base nas médias das pontuações.
calcula_tracos_faixa3- Solicita respostas dos usuários e as classifica em traços altos, médios ou baixos.

Formação de Grupos:
calcula_grupo- Usa as listas de traços classificados (alto, médio, baixo) para formar grupos com rótulos específicos para cada traço.
calcula_planejador, calcula_analista, calcula_mediador e calcula_lider- Calculam o número de pessoas planejadoras, analistas,  mediadoras e líderes com base em traços específicos.

Cálculo de Possíveis Grupos: calcular_numero_grupos_possiveis- Calcula o número total de grupos possíveis, garantindo que todos os grupos tenham pelo menos uma pessoa de cada personalidade.

Relatórios e Resultados: main- Chama a função iniciar_menu, que exibe um menu para o usuário e gerencia o processamento do grupo ideal com base na escolha do usuário.
