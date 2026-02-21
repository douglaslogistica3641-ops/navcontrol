# NavControl — Gestão de Abastecimento Naval

![NavControl](https://img.shields.io/badge/versão-17.1.1-blue)
![Licença](https://img.shields.io/badge/licença-MIT-green)

Sistema web para controle de abastecimento de óleo diesel e água potável em embarcações. Desenvolvido como uma aplicação de página única (SPA) com HTML, CSS e JavaScript puro, utilizando `localStorage` para persistência local dos dados.


---

## Funcionalidades

- ✅ Cadastro de embarcações (com capacidades de tanques)
- ✅ Cadastro de empresas fornecedoras
- ✅ Registro de abastecimentos (compra e transferência entre embarcações)
- ✅ Controle de estoque em tempo real (posição atual de óleo e água)
- ✅ Lançamento de consumo operacional (dedução automática do estoque)
- ✅ Dashboard com gráficos e KPIs
- ✅ Relatórios em PDF (formato naval com identificador único)
- ✅ Sistema de autenticação com perfis (admin e operador)
- ✅ Controle de acesso por embarcação (operadores só visualizam embarcações autorizadas)
- ✅ Solicitações de correção (operadores podem pedir correções aos administradores)
- ✅ Auto‑save automático a cada 45 minutos (gera planilha Excel)
- ✅ Importação/exportação de dados (CSV/Excel)
- ✅ Backup completo em JSON
- ✅ Tema claro/escuro

---

## Tecnologias utilizadas

- HTML5, CSS3, JavaScript (ES6+)
- [Chart.js](https://www.chartjs.org/) – gráficos
- [jsPDF](https://github.com/parallax/jsPDF) + [autoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) – PDF
- [xlsx](https://sheetjs.com/) – planilhas Excel
- [PapaParse](https://www.papaparse.com/) – CSV
- [Font Awesome](https://fontawesome.com/) – ícones
- [Google Fonts (Inter, JetBrains Mono)](https://fonts.google.com/)

---

## Como usar

### Acesso inicial

Ao abrir o sistema pela primeira vez, utilize as credenciais padrão:

| Usuário | Senha   | Perfil        |
|---------|---------|---------------|
| admin   | 123456  | Administrador |

### Navegação

- **Dashboard**: visão geral com gráficos e últimos abastecimentos.
- **Registros**: tabela completa de abastecimentos, com filtros e ordenação.
- **Posição de Estoque**: estoque atual de cada embarcação, com alertas visuais.
- **Empresas / Embarcações**: cadastros (apenas admin).
- **Consumo Operacional**: lançamento de consumo diário (óleo/água/horas).
- **Relatórios**: geração de PDF naval detalhado por embarcação/período.
- **Solicitações**: operadores pedem correções; administradores resolvem.
- **Configurações**: ajustes de densidade, thresholds de alerta, auto‑save, etc.

### Dados persistentes

Todos os dados são armazenados no **`localStorage` do navegador**. Não há servidor backend – você pode usar o sistema offline, mas os dados ficam restritos ao dispositivo e navegador utilizados. Para compartilhar dados entre usuários, utilize as funções de **exportar/importar backup** ou planilhas.
