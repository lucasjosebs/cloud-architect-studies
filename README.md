> 🚧 Documentação em andamento — atualizada continuamente.
# Cloud Fundamentals, Administration and Solution Architect

## Índice
- [Virtualização](#virtualização)
- [Cloud Computing](#cloud-computing)
- [Arquiteturas](#arquiteturas-e-aplicações-cloud)
- [AWS](#amazon-web-services-aws)
- [Azure](#azure)
- [GCP](#google-cloud-platform-gcp)
- [Docker](#docker)
- [Kubernetes](#kubernetes)
- [DevOps](#devops)

## Virtualização

### Introdução

O sistema operacional é como um grande "orquestrador", decidindo como otimizar e utilizar os recursos de hardware da melhor forma possível. Porém, em ambientes modernos de nuvem, temos de prontidão a possibilidade de, em um "passe de mágica", aumentar ou diminuir nossos recursos de *CPU*, *RAM* e *ARMAZENAMENTO*.

Nesse tópico, vamos abordar o mecanismo que torna possível essa manipulação e escalabilidade, a partir da técnica conhecida como **Virtualização**

### Como funciona?

A virtualização surgiu como uma forma de separar melhor o hardware do software. No modelo tradicional, os softwares são instalados em uma infraestrutura física (hardware). Porém sempre que essa infraestrutura não suportasse mais a demanda de usuários ou serviços, o hardware precisava ser substituído, o chamado *upgrade vertical*. Por outro lado criou-se também os clusters de computadores, múltiplas máquinas ligadas entre si e dividindo as tarefas, e aumentando as máquinas de acordo com a demanda de processamento necessários, chamado então de *upgrade horizontal*. Ainda neste modelo, cada um dos computadores mantinham sua própria estrutura de SO e seus próprios processos.  

![Fig.1 - Cluster de computadores](img/cluster_de_computadores.png)
*Fig.1 - Cluster de computadores.*

A virtualização revolucionou esse cenário ao abstrair o hardware físico, inserindo uma camada lógica que permite uma separação eficiente entre os recursos físicos e os sistemas operacionais. Como exemplo a virtualização permite, a instalação de vários sistemas operacionais em uma mesma máquina.

![Fig.2 - Tradicional vs Virtualização](img/estrutura_tradicional_x_virtualizacao.png)
*Fig.2 - Tradicional vs Virtualização.*

Logo depois surgiu o inverso, um único ambiente virtualizado, gerenciado por um *hypervisor* que abstrai os recursos físicos do *cluster*, apresentando-os como um único *pool* de recursos para as máquinas virtuais consumirem. A máquina virtual compreende todo o *hardware* do *cluster* como um único supercomputador, com vários núcleos, memória e armazenamento, permitindo a flexibilidade no aumento destes recursos para a máquina virtual, sempre que houver a necessidade e a disponibilidade da infraestrutura física. Se o *cluster* físico atingir o limite, basta adicionar mais um servidor físico ao *cluster* (escalonamento horizontal) sem que a máquina virtual precise ser desligada ou reconfigurada, garantindo elasticidade e continuidade ao negócio.

### Benefícios

* **Redução de Custos:** A virtualização pode reduzir investimentos em hardware, energia e espaço físico, reaproveitando recursos ociosos.

* **Redução do tamanho do parque de equipamentos (*datacenter*):** Com o melhor aproveitamento dos recursos atuais, a necessidade de  aquisição de novos equipamentos diminui, reduzindo gastos com instalações, espaço físico, manutenção e assim por diante.

* **Gerenciamento centralizado:** Facilidade de monitorar serviços/processos em execução dependendo da estratégia de virtualização adotada.

* **Manutenção de sistemas legados:** Em casos de sistemas legados onde o *hardware* pode possuir mais de vinte anos e rodando em um SO obsoleto, apenas por requisitos de um serviço ou aplicação. A virtualização permite simular aquele *hardware* antigo e emular o SO necessário para dar continuidade ao sistema.

* **Ambientes de testes:** A virtualização permite criar ambientes isolados que simulam diferentes sistemas operacionais ou arquiteturas, sem a necessidade de adquirir equipamentos físicos dedicados para cada cenário de teste.

* **Confiabilidade e Segurança:** Com a VMs funcionando de maneira independente, se um problema surgir em uma delas, este não afetará as demais.

![Fig.3 - Serviços Virtualizados](img/servicos_virtualizados.png)
*Fig.3 - Serviços Virtualizados.*

### Infraestrutura

A Virtualização nos permite fornecer uma versão virtual de muitas tecnologias essenciais em computação, como principais podemos citar **Hardware**, **Armazenamento** e **Redes**, que serão detalhados a seguir. É importante entender que a virtualização é uma tecnologia de *software* que abstrai componentes físicos em camadas lógicas e consolida recursos em pools, permitindo executar várias VMs em uma única máquina física, cada uma com seu próprio SO e compartilhando os recursos dessa mesma máquina. O componente responsável por criar e gerenciar essas VMs é chamado de *Hypervisor*.

* **Hardware:** Chamado de HV - *Hardware Virtualization*. Esse é um dos principais itens sobre a virtualização, um sistema operacional pode ser instalado sobre outro tipo de sistema, com seus recursos de *hardware* sendo representados via *software* pelo *Hypervisor*.

* **Armazenamento:** Chamado também de SDS - *Software Defined Storage* (Armazenamento Definido por Software). É uma camada de *software* criada sobre discos físicos, onde os dispositivos acessam esses discos, de modo a tornar o acesso mais flexível, gerenciável e personalizável.

* **Redes:** Chamado de SDN - *Software Defined Networking* (Rede Definida por Software). É possível criar um tipo de infraestrutura lógica de redes sobre uma determinada rede física, permite a configuração e o detalhamento de acordo com as necessidades do ambiente.

Ao utilizar essas técnicas de virtualização, todos os dispositivos podem ser representados em forma de *softwares*: Servidores e estações de trabalho se tornam VMs, a rede e o armazenamento são virtualizados e se tornam **SDN e SDS**. E assim construímos o **SDDC - *Software Defined Data Center* (Data Center Definido por Software).**

## Cloud computing 
## Arquiteturas e aplicações cloud
## Amazon Web Services (AWS)
## Azure
## Google Cloud Platform (GCP)
## Docker
## Kubernetes 
## DevOps
