### **Criação de uma Máquina Virtual no Azure**
#### **Escolha do Tipo de Trabalho**
Ao criar uma nova VM, o Azure pergunta se o ambiente será:
- **Ambiente de desenvolvimento/teste:** otimizado para custos mais baixos e menor redundância.
- **Ambiente de produção:** recomendado para cargas de trabalho críticas, com mais opções de escalabilidade, segurança e disponibilidade.

#### **Tabela de Recursos Criados por Ambiente**
- O Azure apresenta uma tabela com os serviços que serão criados automaticamente dependendo do ambiente escolhido.
- Existe uma **opção para criar a VM com vários serviços já instanciados**, como:
  - Banco de Dados SQL
  - Armazenamento de arquivos
  - Serviços de backup e segurança
  - Monitoramento com Azure Monitor e Log Analytics

---

### **Fases de Criação da Máquina Virtual**
1️⃣ **Informações e Parâmetros Básicos**
   - Escolha da **assinatura** e do **grupo de recursos**.
   - Definição do **nome da VM**.
   - Seleção da **região** onde a VM será criada.
   - Escolha do **sistema operacional** (Windows, Linux).
   - Tipo de **imagem da VM** (Ubuntu, Windows Server, Red Hat, etc.).
   - Seleção do **tamanho da VM** (CPU, RAM) baseado nas necessidades da aplicação.
   - Opção de ativar **Habilitação de Autoescala** (para adaptar recursos automaticamente).

2️⃣ **Discos**
   - Escolha do **tipo de disco** para armazenamento:
     - SSD Premium (melhor desempenho)
     - SSD Standard (intermediário)
     - HDD Standard (mais barato)
   - Opção de criar **discos adicionais** para armazenamento de dados.

3️⃣ **Rede**
   - Configuração da **Rede Virtual (VNet)** e **sub-rede**.
   - Escolha de um **IP público** para acesso remoto.
   - Configuração do **NSG (Network Security Group)** para definir regras de acesso.
   - Habilitação de balanceamento de carga, caso necessário.

4️⃣ **Gerenciamento**
   - Definir regras para **ligar/desligar automaticamente** a VM.
   - Escolher se a **identidade gerenciada** será ativada para controle de permissões no Azure.
   - Configuração de backup e recuperação.

5️⃣ **Monitoramento**
   - Habilitação do **Azure Monitor**, que permite visualizar métricas como CPU, RAM e disco.
   - Opção de integrar com **Log Analytics** para registrar logs detalhados.

6️⃣ **Avançado (Extensões, Aplicativos da VM, Dados Personalizados)**
   - Possibilidade de instalar **extensões** como:
     - Agentes de segurança
     - Ferramentas de gerenciamento remoto
   - Configuração de **scripts personalizados** para executar comandos automaticamente após a criação da VM.

7️⃣ **Marcas (Tags)**
   - Permitem classificar recursos usando **pares chave/valor**.
   - Exemplo:
     - `Ambiente: Produção`
     - `Projeto: WebAppX`
     - `Departamento: TI`
   - Tags ajudam a organizar e filtrar os recursos dentro da assinatura do Azure.

### **Área de Trabalho Virtual do Azure**  
A **Área de Trabalho Virtual do Azure (Azure Virtual Desktop - AVD)** é um serviço que permite a implantação e o gerenciamento de **ambientes de trabalho remotos na nuvem**. Ele possibilita que usuários acessem **aplicações e desktops Windows** a partir de qualquer dispositivo, com segurança e escalabilidade.  

#### **Principais características:**
- **Multiusuário no Windows 10 e 11:** Permite que vários usuários compartilhem a mesma VM sem precisar de sistemas operacionais de servidor.  
- **Gerenciamento simplificado:** Administração centralizada para criar e configurar desktops virtuais rapidamente.  
- **Segurança e conformidade:** Proteção integrada com autenticação multifator (MFA) e integração com Microsoft Defender.  
- **Escalabilidade:** Permite ajuste automático de recursos conforme a demanda.  
- **Redução de custos:** Economia ao utilizar VMs otimizadas para diferentes cargas de trabalho.  

O AVD é ideal para empresas que precisam fornecer acesso remoto a desktops e aplicativos sem necessidade de infraestrutura local. 🚀
