# **Resumo da Aula sobre SLA e Disponibilidade na Azure**

## 📌 **O que é SLA (Service Level Agreement)?**  
O **SLA** (Acordo de Nível de Serviço) é um compromisso entre o provedor de serviços e o cliente, garantindo um nível mínimo de disponibilidade e desempenho para os serviços contratados. Ele define métricas como **tempo de atividade (uptime)** e possíveis compensações caso o serviço não atinja o percentual prometido.

### **Tabela de SLA - Níveis de Disponibilidade (Até 5 Noves)**
| SLA (%) | Tempo de inatividade permitido por mês |
|---------|-------------------------------------|
| **99,9% (três noves)** | Até **43,8 minutos** |
| **99,95% (três noves e meio)** | Até **21,9 minutos** |
| **99,99% (quatro noves)** | Até **4,38 minutos** |
| **99,999% (cinco noves)** | Até **26 segundos** |

Quanto mais “noves” no SLA, maior a disponibilidade e menor o tempo permitido de inatividade.

---

## 🌍 **Opções de Disponibilidade ao Criar uma Máquina Virtual na Azure**
A Azure oferece diferentes níveis de **alta disponibilidade**, impactando diretamente o SLA:

1. **Single VM (Máquina Única)** – Menor SLA, sem redundância.  
2. **Availability Sets (Conjuntos de Disponibilidade)** – Distribui VMs em múltiplos racks dentro de um mesmo datacenter, protegendo contra falhas de hardware.  
3. **Availability Zones (Zonas de Disponibilidade)** – Distribui VMs entre diferentes datacenters na mesma região, garantindo maior resiliência a falhas.  

---

## 🏢 **Zonas de Disponibilidade (Availability Zones)**
As **Availability Zones** são datacenters fisicamente separados dentro de uma mesma região da Azure. Cada zona tem infraestrutura independente de energia, refrigeração e rede. Isso aumenta a resiliência contra falhas regionais.

- Exemplo: Se uma zona sofrer uma falha elétrica, suas máquinas podem continuar operando em outra zona disponível.

---

## 🔄 **Estratégias de Replicação e Redundância na Azure**
A replicação de dados é fundamental para garantir a integridade e disponibilidade dos serviços. A Azure oferece diferentes estratégias:

| Tipo de Redundância | Descrição |
|----------------|----------------------------------------------------------|
| **LRS (Locally Redundant Storage)** | Mantém **3 cópias** dos dados dentro de um único datacenter. Mais barato, mas menos resiliente. |
| **ZRS (Zone-Redundant Storage)** | Replica dados entre **múltiplas Zonas de Disponibilidade** na mesma região. Proteção contra falhas regionais. |
| **GRS (Geo-Redundant Storage)** | Replica dados em **duas regiões diferentes**, garantindo recuperação de desastres. |
| **RA-GRS (Read-Access Geo-Redundant Storage)** | Igual ao GRS, mas permite leitura na réplica secundária. |

---

## 🎯 **Impacto dos Parâmetros no SLA**
- O **nível de disponibilidade escolhido** (máquina única vs. Availability Zones) afeta diretamente o SLA.  
- O **tipo de redundância do armazenamento** (LRS, GRS, etc.) influencia a segurança dos dados e a recuperação de falhas.  
- Empresas que precisam de **99,99% ou mais de SLA** geralmente combinam **Availability Zones** e **GRS** para máxima resiliência.  

Esses fatores são críticos para aplicações empresariais que exigem **alta disponibilidade e continuidade de negócios**. 🚀
