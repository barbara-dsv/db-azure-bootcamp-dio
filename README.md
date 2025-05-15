# 📟 Desafio Azure: Instância de Banco de Dados (SQL Managed Instance)

Este repositório contém um resumo prático da experiência de criação e configuração de uma instância gerenciada de banco de dados SQL na plataforma Microsoft Azure. Faz parte do desafio proposto no curso da DIO.

## 📚 Conteúdo Abordado

### Tipos de Serviço em Nuvem

* **IaaS (Infrastructure as a Service):**

  * Nível mais básico da nuvem.
  * O cliente gerencia a maior parte dos recursos: rede, SO, segurança, backup.
  * Exemplo: VM no Azure com SQL Server instalado.

* **PaaS (Platform as a Service):**

  * Inclui tudo do IaaS, mais sistema operacional, ferramentas de desenvolvimento e serviços gerenciados.
  * O cliente foca mais na aplicação do que na infraestrutura.
  * Exemplo: Azure SQL Managed Instance.

* **SaaS (Software as a Service):**

  * Tudo é gerenciado pelo provedor (Microsoft).
  * O cliente usa diretamente o software sem se preocupar com infra.
  * Exemplo: Office 365, Outlook Web.

### Modelo de Responsabilidade Compartilhada

Cada tipo de serviço possui responsabilidades diferentes divididas entre o cliente e a Microsoft:

| Tipo | Cliente Responsável         | Compartilhado               | Microsoft Responsável        |
| ---- | --------------------------- | --------------------------- | ---------------------------- |
| IaaS | Dados, identidade, SO, apps | Rede, segurança             | Físico, armazenamento        |
| PaaS | Dados, identidade, apps     | Segurança, controle de rede | Infraestrutura, SO, backup   |
| SaaS | Dados e identidade          | -                           | Toda a infraestrutura e apps |

### Comparação dos Serviços

| Tipo | Controle | Gerenciamento | Complexidade | Custo            |
| ---- | -------- | ------------- | ------------ | ---------------- |
| IaaS | Alto     | Alto          | Alto         | Variável         |
| PaaS | Médio    | Médio         | Médio        | Otimizado        |
| SaaS | Baixo    | Baixo         | Baixo        | Normalmente fixo |

---


## 💡 Dicas para Uso da Azure na Criação de Instância Gerenciada de SQL

### ✅ Planejamento é tudo

* **Grupo de recursos:** use nomes claros e específicos para facilitar o gerenciamento.
* **Região:** escolha a mais próxima do usuário final para reduzir latência.

### 🧱 Escolha o tipo certo de banco

* **SQL Database (Single):** ideal para apps pequenos.
* **SQL Managed Instance:** ideal para migrações e apps maiores com dependência de features específicas.
* **SQL Server em VM:** mais liberdade, mas mais responsabilidade (IaaS).

### 🔐 Segurança

* Use **firewalls e redes virtuais** para restringir acesso.
* Configure **autenticação forte**.
* Ative **backups automáticos** e revise a política de retenção.

### 📶 Performance e escalabilidade

* Escolha entre **DTU** (fácil, projetos pequenos) e **vCore** (mais controle).
* Use **pools elásticos** quando tiver múltiplos bancos com uso variável.

### 💸 Custo

* Utilize a **calculadora do Azure** para estimar.
* Configure **alertas e limites de orçamento**.

### 🔪 Teste o acesso

* Use o **SSMS**, **Azure Data Studio** ou o **Query Editor** no portal.
* Libere a **porta TCP 1433** no firewall.

---

📌 **Repositório criado para o Desafio Prático da DIO sobre SQL no Azure**

> Desenvolvido por Babi 🌟
