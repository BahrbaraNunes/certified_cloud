# Introdução à lição

Nesta lição, discutiremos os desafios que um alto volume de dados representa. Também discutiremos o escopo dos tipos de origem de dados que você pode precisar para ingerir e armazenar. Terminaremos com uma discussão sobre as opções da AWS disponíveis para armazenar dados.

### Os tópicos desta lição são:

- Introdução ao Amazon Simple Storage Service (Amazon S3);
- Introdução a data lakes;
- Introdução aos métodos de armazenamento de dados.

# Volume

Nós acabamos de discutir os 5 Vs da Análise de Dados e os desafios que surgem com eles. O Volume de dados é o primeiro desafio. Há muitas empresas com dificuldades em lidar com quantidades massivas de dados.

É verdade! Geramos dados em grandes volumes, praticamente todos têm um tablet, um celular, um laptop. As pessoas geram toneladas de dados todos os dias. - Você tem um smartwatch?

- Sim! Eu tenho e adoro! Eu não trouxe ele hoje, mas quando está comigo, me diz quantos passos eu dei, como ficou a minha frequência cardíaca, ele até permite que eu verifique meus e-mails e atenda chamadas.

Nossa! A praticidade é incrível! Mas pense nisso num ponto de vista dos dados. Seu dispositivo coleta dados constantemente e envia aos servidores para processar cada passo e cada verificação de frequência cardíaca. Em seguida, eles retornam os resultados para o dispositivo para que você e, somente você, possa ver sempre que quiser.

Esse é apenas um exemplo de um conjunto inteiro de dispositivos classificado como: Internet das Coisas ou IoT. As empresas de IoT obtêm uma imensidão de informações de dispositivos como estes. E não param por aí. As mídias sociais mudaram a maneira como as empresas comercializam os produtos delas e para os clientes. Isso mudou a maneira como elas lidam com as reclamações e até mesmo com o atendimento ao cliente. Você pode imaginar a quantidade de dados gerados e carregados a cada minuto, apenas por meio das mídias sociais?

Eu tenho certeza que são quantidades muito, muito grandes!

Eu li recentemente que mais de 100 milhões de e-mails de spam são enviados a cada minuto e outra coisa, os usuários da Netflix consomem mais de 70 mil horas de vídeo a cada minuto.

E no YouTube? Os usuários assistem a mais de 4 milhões de vídeos a cada minuto.

A International Data Corporation, também chamada de IDC, prevê um crescimento massivo de dados entre agora e 2025. A corporação prevê que a Global DataSphere, que são os dados coletados de todos os lugares, crescerá de 33 zetabytes no ano passado para 175 zetabytes até 2025.

Zetabytes?! Isso dá… São 21 zeros!? Pelo que eu me lembro, apenas alguns anos atrás, as previsões ainda estavam na faixa dos hexabites. Quem imaginaria que chegaríamos a este ponto? Então, o que esse rápido aumento no volume de dados significa para os responsáveis pelas tomadas de decisões nos negócios?

Isso significa que eles precisam de soluções de análise de dados. Em primeiro lugar, as empresas gerenciam um volume passivo de dados e devem trabalhar com eficiência em sistemas distribuídos, mesmo naqueles que abrangem países ou continentes. E essas soluções devem ser facilmente escaláveis, para que elas possam acomodar enormes picos de volume e de tráfego.

Vou resumir isso. Uma solução para analisar dados tem que suportar enormes quantidades de dados. Portanto, precisa possuir um armazenamento que seja escalável e durável e precisa ser capaz de coletar esses dados de muitas fontes diferentes.

Este seria um bom ponto para discutirmos os diferentes tipos de dados que, talvez, precisem ser analisados.

Exatamente! Primeiro, vamos usar dados relacionais ou estruturados. Esses dados normalmente são armazenados em bancos de dados relacionais. Né? Daí o nome. Eles são estruturados por regras e constraints definidas no próprio banco de dados. Esse tipo de dados é espinha dorsal de aplicações transacionais.

Em segundo lugar, os dados semiestruturados. Esses dados, geralmente, são armazenados no banco de dados não relacional, ou também chamado de NoSQL, ou até mesmo em arquivos de JSON ou XML. Esses dados não têm uma estrutura rígida e muitas vezes, por sua própria natureza, são temporários. Os exemplos incluem movimentos que você faz em um videogame on-line, por exemplo, o cache do navegador da internet ou até mesmo aplicativos de redes sociais que excluem automaticamente suas publicações após um determinado período.

E, finalmente, aos dados não estruturados. Esses dados, geralmente, possuem a forma de arquivos ou objetos, não têm uma estrutura única e representam todo o resto que uma empresa coleta e gera. Esses dados geralmente são considerados intocáveis porque não atendem às normas convencionais. Eles exigem a criação de tags e precisam ser catalogados pra serem analisados, o que impede que muitas empresas utilizem suas soluções de Data Analytics. Eu sei que às vezes parece difícil entender o que significa dados não estruturados. Então, aqui vão alguns exemplos pra vocês. Poderiam ser: imagens, mensagens de e-mail, arquivos de texto, conteúdos de mídias sociais, mensagens de texto e vídeo.

Eu ouvi dizer que apenas 10% de todos os dados coletados ou gerados pelas empresas são estruturados. - É verdade?

- Sim! Vários artigos foram escritos em estudos realizados sobre esse mesmo problema. Esses dados, que são os mais simples de incorporar em soluções de análise de dados, representam apenas uma pequena porcentagem dos dados que realmente estão sendo coletados. Um pouco chocante perceber isso.

Nossa! Eu ouvi dizer que há outros 10% de todos os dados coletados ou gerados por empresas, são dados semiestruturados. E o restante? Os outros 80%, são dados não estruturados. Em outras palavras, a maior parte dos dados de sua empresa também é a mais difícil de analisar. Muitas vezes, as empresas enfrentam dificuldades para criar soluções de análise de dados que podem extrair com precisão e eficácia esses dados valiosos para produzirem insights significativos. Às vezes, parece que os dados estão congelados nos servidores de arquivos e muitos são difíceis de entender. Mas não precisa ser assim. Apresentaremos algumas soluções excelentes, mais adiante neste curso.

## Crescimento exponencial de dados de negócios

As empresas armazenam dados há décadas, isso não é novidade. O que mudou nos últimos anos foi a capacidade de analisar determinados tipos de dados.

Há três classificações amplas de tipos de origem dos dados:

Dados estruturados são organizados e armazenados na forma de valores que são agrupados em linhas e colunas de uma tabela.
Dados semiestruturados muitas vezes são armazenados em conjuntos de pares de chave-valor que são agrupados em elementos em um arquivo.
Dados não estruturados não são estruturados de forma consistente. Alguns dados podem ter uma estrutura semelhante a dados semiestruturados, mas outros podem conter apenas metadados.
Muitos artigos da internet falam muito da enorme quantidade de informações presente em dados não estruturados. Novos aplicativos são lançados que agora podem catalogar e fornecer informações incríveis sobre esse recurso inexplorado.

Mas o que são dados não estruturados? Eles estão em todos os arquivos que armazenamos, todas as fotos que tiramos e e‑mails que enviamos.