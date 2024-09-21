# resumo-do-lab
Repositório com resumos das aulas do bootcamp em Cloud da dio.


## 🏷️ Lab 1 - Localizando serviços por categoria

- Personalização da interface (alterando idioma, tema e etc)
- Categorias:

Exploramos superficialmente todas as categorias do Azure, entendendo quais os serviços oferecidos para cada categoria.

- Tópicos explicado em aula:
  
Jump Server - é um computador em uma rede tipicamente usada para gerenciar dispositivos em uma zona de segurança separada.

Firewall - é um sistema de segurança que monitora e controla o tráfego de uma rede de computadores, permitindo ou bloqueando o acesso a ela de acordo com regras de segurança.

SLA (service level agreement) - é um compromisso assumido por um prestador de serviços (como uma garantia).


## ⚠️ Lab 2 - Criando máquinas virtuais e entendendo a indisponibilidade

Nesta aula foi explicado os conceitos envolvendo o SLA e o impacto que cada uma das porcentagens gera com relação à indisponibilidade. Além disso, quanto mais replicarmos as informações menos indisponibilidade gera para a nuvem.

Sobre as porcentagens:

99% = 1,68h de indisponibilidade
99,9% = 10,1 min de indisponibilidade
99,95% = 5min de indisponibilidade

## 🔢 Lab 3 - Configurando uma instância de Banco de Dados na Azure

Nesta aula foi mostrado que a criação de máquinas virtual na Azure é um processo que exige bastante atenção pela quantidade de opções de configurações possíveis. 

Além disso, foi apresentado uma calculadora na hora da criação do servidor e do banco de dados SQL, que dá uma noção do quanto gastaríamos pelo uso com base nas configurações escolhidas. 

## 🌍 Lab 4 - Componentes de Arquitetura do Azure

Começamos o Lab explorando a infraestrutura global do Azure, na página com o mapa de data centers pelo mundo [em seu site oficial](https://datacenters.microsoft.com/globe/explore).

Replicação de dados por regiões, pares de região e o impacto da LGPD, pois existem dados que não podem sair do país e nossa região par é nos EUA.

Tour virtual pelo datacenter da Microsoft.

Criação de um grupo de recursos no Azure. É possível gerenciar permissionamento nos grupos de recursos.

## 💾 Lab 5 - Configurando recursos e dimensionamentos em VM's no Azure

Configuração completa de uma máquina virtual explorando conceitos como Spot (que é um espaço mais barato que pode ser descontinuado, mas é bom pra teste), backup, discos órfãos, exclusão de VM e etc.

Configuração de uma área de trabalho virtual.

## 🧳 Lab 6 - Dominando o armazenamento no Azure 

Storage account (contas de armazenamento) - deve ter um nome global e exclusivo (de 3 a 24 caracteres).

Redundânccia de armazenamento - Configurações de redundância: 
- LRS (armazenamento com redundância local) - 3 cópias em um datacenter (se o datacenter cair, se perde os dados). Não é indicado para ambientes produtivos.
- ZRS (armazenamento com redundância de zona) - 3 cópias separadas por zonas de disponibilidade (a região precisa cair para perder os arquivos).
- GRS (armazenamento com redundância geográfica) - Datacenter único na primária e região secundária (par)
- GZRS  (armazenamento com redundância zona geográfica) - 3 zonas de disponibilidade na região primária e um único datacenter na região secundária.

Serviços de armazenamento: Blobs, file, Arquivos, tabelas.

Pontos de extremidade pública: https://<storage_account_name>.qual o servico.core.windows.net (basta mudar para o serviço, exemplo blobs, arquivos e etc)

Camadas de acesso de armazenamento: Frequente, esporádica, frio, arquivo morto. Quanto menos frequente, mais pagamos pelo acesso/consulta e menos pelo repositório.

Opções de gerenciamento de arquivo: 
- Azcopy (ajuda a copiar os dados do blobs e pastas de arquivo)
- gerenciador de armazenamento
- sincronização de arquivos

## 🔐 Lab 7 - Segurança e Identidade no Azure

Microsoft Entra ID é o responsável por represar todos os usuários (gerenciamento de identidades)

Autenticação - identifica a pessoa ou serviço, buscando acesso a um recurso
Autorização - Determina o nível de acesso de uma pessoa ou serviço autenticado.

Autenticação multifator - Fornece segurança adicional para as identidades, exigindo 2 ou mais elementos para autenticação completa (algo que você sabe, algo que você possui, algo que você é)

Acesso Condicional

Confiança Zero - Pressupõe sempre o pior cenário. Trabalha com os menores privilégios possível.

Proteção completa - Uma abordagem em camadas para proteger sistemas de computadores. Ataques em uma camada são isolados das camadas subsequentes.

Microsoft Defender para nuvem - É um serviço de monitoramento que fornece proteção contra ameaças nos datacenters do Azure e locais (incluindo o ambiente AWS e GCP)

## 💰 Lab 8 - Otimizando custos no Azure

Fatores que afetam os custos: Tipo de recurso, consumo, manutenção, área geográfica, tráfego de rede e assinatura.

Calculadora Azure, para utilizar as infos necessárias são: Região, camadas, opções de cobrança, opçoes de suporte, programas e ofertas e preço de desenvolvimento / testes no Azure.

TCO (Calculadora de custos totais de propriedade) - estima o custo total de uma migração para o Azure

Marcas (tags) - IMPORTANTE: Não são obrigatórias e herdáveis! Tratam-se de metadados que organizam recursos de maneira lógica. Consistem em um par nome-valor. Úteis para organizar infos de cobrança.

Lab - Testes com a calculadora.

## ⚖️ Lab 9 - Gerenciando políticas em acessos Azure

Azure Policy - Ajuda a impor padrões organizacionais e a avaliar a conformidade em escala. Fornece governança e consistência de recursos com conformidade regulatória, segurança, custo e gerenciamento. Avalia e identifica recursos que não atendem as suas políticas. E, por fim, fornece definições políticas e iniciativas integradas, em categorias como armazenamento, rede, computação, central de segurança e monitoramento.

Bloqueio de recursos - Protege de exclusão ou modificações acidentais.

Microsoft Purview - Soluções de governança, risco e conformidade de dados que ajuda você a obter uma única exibição unificada de seus dados. Reúne insights sobre seus dados locais, multinuvem e de software como serviço.

