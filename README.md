# Azure---VM---Guia

Este arquivo contém um resumo detalhado das questões e respostas relacionadas às **Máquinas Virtuais no Azure**, abordando segurança, escalabilidade, disponibilidade e boas práticas de configuração.

---

## 📌 Segurança e Autenticação

- **Acesso remoto seguro**: Utilize **Azure Bastion** para conectar-se sem expor portas RDP ou SSH.
- **Autenticação recomendada**: Prefira **chaves SSH com senha** para maior segurança.
- **Gerenciamento de permissões**: Controle o acesso às VMs utilizando **RBAC** e regras de segurança no **NSG**.

---

## 🔧 Gerenciamento e Disponibilidade

- **Backup e recuperação**: O **backup das VMs deve ser configurado e gerenciado pelo usuário** via **Azure Backup**.
- **Manutenção planejada**: A Microsoft pode exigir a **realocação das máquinas** para evitar downtime durante atualizações.
- **Alta disponibilidade**: Utilize **Conjuntos de Disponibilidade** para distribuir as VMs entre múltiplos **racks físicos**.
- **Domínios de falha**: Distribuem VMs para garantir **redundância contra falhas físicas**.

---

## 🚀 Escalabilidade e Desempenho

- **Escalonamento automático**: Configure **Virtual Machine Scale Sets** para **aumentar ou reduzir instâncias de VMs** com base no uso de CPU e memória.
- **Escalonamento vertical vs horizontal**:
  - **Vertical**: Aumenta os recursos de uma única VM (CPU, memória).
  - **Horizontal**: Adiciona novas VMs para distribuir carga.
- **Balanceamento de carga**: Implante um **Load Balancer** para distribuir solicitações entre várias instâncias.

---

## 📦 Configuração e Boas Práticas

- **Gerenciamento de sistema operacional**: O usuário deve garantir atualizações, segurança e monitoramento das VMs.
- **Tipos de armazenamento**:
  - **Premium Storage** oferece alta performance, mas **não suporta replicação geográfica (GRS)**.
- **Escolha do tipo de VM**:
  - **Máquinas Spot** são econômicas, mas podem ser desalocadas a qualquer momento.
  - **VMs de Produção exigem alta disponibilidade e backup**.
  - **VMs de Teste não precisam de configurações avançadas**.

---

## 🔄 Automação e Configuração

- **Azure DSC (Desired State Configuration)** permite gerenciar e padronizar configurações de VMs Windows e Linux.
- **Update Domains** ajudam a organizar atualizações sem impacto simultâneo em todas as VMs.

---
