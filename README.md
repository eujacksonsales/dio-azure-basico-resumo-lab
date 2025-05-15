# Resumo Conceitos Azure

## O que é computação em Nuvem
Computação em nuvem é nada mais nada menos do que armazenamento e criação de recursos de tecnologia armazenados em data centers, onde antes tudo era feito dentro da própria organização com vários servidores e mainframes, hoje a nuvem domina, com várias tecnologias reunidas em um único lugar. E essa tecnologia em nuvem está amplamente difundida por todo mundo e as BigTechs são grandes resposáveis por manter essa nova tecnologia funcionando.

## Modelos de Nuvem
- Nuvem Privada: Aqui temos utilização de recursos da nuvem, porém utilizado apenas dentro da própria organização, ou seja, utiliza-se da tecnologia de nuvem de uma BigTech, porém é utilizada apenas internamente.
- Nuvem Pública: Aqui é possível utilizar esses recursos em qualquer lugar do mundo, pois existem vários data centers por todo o mundo, logo torna-se muito mais fácil fazer transferência de dados para outro lugar, caso seja necessário.
- Nuvem Híbrida: Utiliza-se do conceito das duas nuvens(Privada e Pública), para um melhor gerenciamento de dados. É o modelo mais utilizado hoje pelas organizações.
- Multi Nuvem: Junção de Nuvem de vários provedores, embora não seja tão recomendado, pois aumenta a complexidade de gerenciamento e manutenção, entretanto grandes organizações já estão utilizando-a.
  
## Custos com uso da Nuvem
- Capex: Custos físicos advindos das instalações necessárias na organização para surportar a computação em nuvem, geralmente esse custo não tem data de término. Utilizando-se da analogia de uma casa, o Capex é o custo para construir a casa, porém após ela construida, tem-se gastos com energia, água, e manutenção geral.
- Opex: Aqui são os custos que vem através da utilização dos recursos em nuvem e só são cobrados por consumo, ou seja, se você utilizar um serviço, no mês seguinte será cobrado por aquele uso. O valor sempre vai ser proporcional a quantidade de uso que você utiliza. Pode-se fazer uma analogia de compras dentro da casa, se você deseja comprar muita comida, vai pagar um valor mais alto, se comprar pouca, vai pagar um valor mais baixo.
 
# Módulo 1

## Conceitos Fundamentais

- **Elasticidade:** É utilizada quando precisa ser ter um aumento ou redução automática de recursos conforme a demanda.

- **Governança:** É o conjunto de boas práticas utilizada para fazer a gestão dos recursos que estão sendo utilizados na nuvem. Andam em conjunto com o conceito de segurança.

- **Segurança:** É o que o nome já diz, construir recursos e colocar segurança neles é essencial para a proteção de dados tanto dos usuários quanto dos colaboradores, além de trazer um maior controle de uso por cada colaborador.

- **Disponibilidade:** Conceito de que os seus recursos quase sempre estarão ativos, fazendo com que os sistemas não fiquem fora do ar.

- **Gerenciabilidade:** Você consegue gerir os recursos de diversas formas, não só pela plataforma. Trazendo uma maior tranquilidade e versatilidade no uso de colaboradores e sistemas.

- **Previsibilidade:** Por você já conseguir construir os recursos e sistemas de forma planejada e estruturada, tem-se muita previsibilidade de como será a entrega desses recursos e os valores cobrados também.

- **Confiabilidade:** O uso na nuvem é bastante confiável pois são grandes BigTechs que ficam responsáveis por montar toda essa estrutura e com certeza fazem de tudo para trazer a maior confiabilidade possível.

- **Escalabilidade:** Você consegue se conectar com o mundo inteiro, logo você tem uma escala mundial através das regiões e zonas de disponibilidades. Pode-se instalar vários servidores no globo. Além de ter um aumento ou diminuição de capacidade de computação conforme a demanda.

---

## Virtual Machine

### Modelos de Serviço

- **IaaS – Maior responsabilidade local**  
  Infraestrutura como Serviço: Onde a parte da infraestrutura principalmente física fica sob responsabilidade do provedor, e a organização por todos os outros recursos.

- **PaaS – Média responsabilidade local**  
  Plataforma como Serviço: Já com a plataforma, o provedor disponibiliza bem mais recursos para construção de sistemas, como servidores e armazenamento, trazendo uma maior velocidade na construção de aplicações.

- **SaaS – Menor responsabilidade local**  
  Software como Serviço: Diversos softwares criados para lidar com demandas específicas das organizações, e nela você consegue construir e gerenciar com muito mais facilidade do que outros níveis.

### Modelo de Responsabilidade Compartilhada

Foi citado um pouco acima todos os modelos de computação em nuvem e a tamanha responsabilidade de cada uma, e é exatamente isso, os níveis de responsabilidade entre a organização e o provedor da nuvem. Observa-se que a responsabilidade compartilhada não fica toda para o provedor e além disso formas errôneas de gerenciar os recursos também não são responsabilidade do provedor. A responsabilidade deles está em garantir todos os benefícios do que é ser computação em nuvem, como foi falado no módulo 1.

---

### Níveis de SLA e Tempo Máximo de Indisponibilidade

| SLA (%)   | Por Semana      | Por Mês         | Por Ano          |
|-----------|------------------|------------------|------------------|
| 99,00%    | 1,68 horas        | 7,20 horas        | 3,65 dias         |
| 99,90%    | 10,1 minutos      | 43,2 minutos      | 8,76 horas        |
| 99,95%    | 5,04 minutos      | 21,6 minutos      | 4,38 horas        |
| 99,99%    | 1,01 minuto       | 4,32 minutos      | 52,56 minutos     |
| 99,999%   | 6,05 segundos     | 25,9 segundos     | 5,26 minutos      |

Segue-se exemplos dos modelos de disponibilidade, e em contrapartida quanto tempo de indisponibilidade cada um desses níveis atrai. Vale ressaltar que quanto maior a disponibilidade, maior o custo, porém menor o tempo fora do ar.

---

# Módulo 2

## Arquitetura Azure

### Regiões e Zonas de Disponibilidade

- **Replicação de Dados** em vários data centers para manter funcionando o sistema.
- **Zona de Disponibilidade = Data Center**  
  Fornece proteção contra tempo de inatividade.
- **Região >= 3 Zonas de Disponibilidade**
- **Pares de Regiões** usados em situação de disaster recovery  
  No Brasil ainda não há par de região local, sendo conectado com a região dos EUA.
- **Regiões Soberanas do Azure:**
  - **Estados Unidos:** Fins militares e governamentais
  - **China:** Provedor operado pela 21Vianet com uso restrito

---

## Assinaturas e Grupo de Recursos

- **Grupo de Recursos:** Para agregar e gerenciar recursos em uma única unidade, pode-se ter recursos de qualquer tipo e/ou região.

- **Assinaturas de dev, teste e produção:**
  - 1 Conta .. N Assinaturas
  - 1 Assinatura .. 1 Conta

### Exemplo Real

> Recentemente passei por uma situação de utilização de grupos de recursos e assinaturas, onde precisava criar uma conexão entre a Azure e o Make, nisso foi preciso não só criar como gerenciar todo o processo, afim de garantir uma excelente conexão, seguindo os princípios da nuvem.

---

## Computação e Rede

### Máquinas Virtuais do Azure (VMs) e Dimensionamento

- **VM (Virtual Machine):** Criada para facilitar o uso de computadores pelas organizações sem precisar de máquinas físicas.

- **Rack:** Onde ficam os componentes das VMs para melhor administração física e virtual.

- **Domínio de Falha:** Conjunto de vários racks. Caso um falhe, os outros não são afetados diretamente.

- **Área de Trabalho Virtual do Azure:** Ambiente com recursos da Azure, alguns pré-instalados.

- **Serviços de Contêineres do Azure:** Usados para construir aplicações específicas com recursos mínimos. Exemplo: Docker.

- **Azure Functions:** Funções em diversas linguagens que executam ações específicas. Exemplo: .Net no Windows, Python no Linux.

---

## Serviços de Aplicativo

Criar, implantar e dimensionar aplicativos Web e APIs.

---

## Redes Virtuais (VNet)

- **VNet:** Redes Virtuais que conectam recursos como VMs de forma segura.

- **Gateway de VPN:** Comunicação de diferentes locais em uma mesma rede virtual.

- **ExpressRoute:** Conexões privadas entre redes locais e a nuvem Microsoft.

- **Cloud DNS:** Serviço DNS gerenciado na nuvem para endereçamento IP, totalmente escalável e de alta disponibilidade, voltado para domínios públicos e privados.

---

## Identidade, Acesso e Segurança

### Microsoft Entra ID

Sistema de autenticação para usuários do Microsoft Azure.

### Autenticação vs Autorização

- **Autenticação:** Confirma sua identidade (ex: MFA com e-mail e SMS).
- **Autorização:** Define o que você pode fazer após estar autenticado.

### Acesso Condicional

Define acesso com base em condições específicas, como usuário, dispositivo, tipo de app, etc.

### Controle de Acesso Baseado em Função (RBAC)

Atribui permissões com base em funções (ex: CEO, CTO, vendedor).

### Confiança Zero (Zero Trust)

Modelo de segurança que nunca confia e sempre verifica antes de liberar acessos.

### Microsoft Defender para Nuvem

Plataforma de proteção de aplicativos para ambientes híbridos e multinuvem.
