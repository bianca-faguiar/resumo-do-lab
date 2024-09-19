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

