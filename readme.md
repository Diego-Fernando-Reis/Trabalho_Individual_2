## Tabela Empresas Parceiras:

| ID_Empresa | Nome                 | Localizacao        | Outras_Informacoes                                    |
|------------|----------------------|--------------------|--------------------------------------------------------|
| 1          | Tech Solutions Inc. | Silicon Valley, CA | Líder no desenvolvimento de soluções de software.     |
| 2          | DataTech Analytics  | New York, NY       | Especializada em análise de dados e Business Intelligence |
| 3          | WebDev Co.           | Los Angeles, CA    | Focada no desenvolvimento web e mobile.               |

## Tabela Tecnologias:

| ID_Tecnologia | Nome         | Area                   |
|---------------|--------------|------------------------|
| 1             | Python       | Desenvolvimento de Software |
| 2             | SQL Server   | Banco de Dados         |
| 3             | TensorFlow   | Machine Learning       |
| 4             | JavaScript  | Desenvolvimento Web     |
| 5             | React        | Desenvolvimento Web     |
| 6             | HTML/CSS     | Desenvolvimento Web     |

## Tabela Colaboradores:

| ID_Colaborador | Nome           | Cargo                  | Email                             | ID_Empresa |
|----------------|----------------|------------------------|-----------------------------------|------------|
| 1              | João Silva     | Desenvolvedor Full Stack | joao.silva@techsolutions.com    | 1          |
| 2              | Maria Santos   | Analista de Dados       | maria.santos@datatech.com       | 2          |
| 3              | Pedro Oliveira | Desenvolvedor Frontend  | pedro.oliveira@webdev.com       | 3          |

## Tabela Relacionamento Empresa-Tecnologia:

| ID_Relacionamento | ID_Empresa | ID_Tecnologia |
|-------------------|------------|---------------|
| 1                 | 1          | 1             |
| 2                 | 2          | 2             |
| 3                 | 2          | 3             |
| 4                 | 3          | 4             |
| 5                 | 3          | 5             |
| 6                 | 3          | 6             |

## Cardinalidade

### Empresas Parceiras - Tecnologias (Muitos-para-Muitos):
    - **Relação:** Muitos-para-Muitos (N:N)
   - **Descrição:** Neste caso, uma empresa parceira pode utilizar várias tecnologias, e uma mesma tecnologia pode ser utilizada por várias empresas parceiras. Por exemplo, várias empresas podem utilizar a tecnologia Python, enquanto uma única empresa pode utilizar várias tecnologias diferentes, como Python, SQL Server e TensorFlow. Isso é representado pela relação de muitos-para-muitos entre as tabelas de Empresas Parceiras e Tecnologias, exigindo uma tabela de relacionamento intermediária para registrar essa associação.

### Colaboradores - Empresas Parceiras (Um-para-Muitos):
    - **Relação:** Um-para-Muitos (1:N)
   - **Descrição:** Nesta relação, um colaborador está associado a apenas uma empresa parceira, enquanto uma empresa pode ter vários colaboradores. Por exemplo, um colaborador João Silva está associado à empresa Tech Solutions Inc., mas essa empresa pode ter vários outros colaboradores. Isso é representado pela relação de um-para-muitos entre as tabelas de Colaboradores e Empresas Parceiras.

### Colaboradores - Tecnologias (Muitos-para-Muitos):
    - **Relação:** Muitos-para-Muitos (N:N)
   - **Descrição:** Nesta relação, um colaborador pode ter habilidades em várias tecnologias, e uma mesma tecnologia pode ser dominada por vários colaboradores. Por exemplo, um colaborador pode ser especialista tanto em Python quanto em JavaScript, enquanto várias outras pessoas também podem ser especialistas nessas mesmas tecnologias. Isso é representado pela relação de muitos-para-muitos entre as tabelas de Colaboradores e Tecnologias, também exigindo uma tabela de relacionamento intermediária para registrar essa associação.

   Essas são as cardinalidades no modelo de banco de dados fornecido, indicando como as entidades estão relacionadas entre si.

   ## Entidades Necessárias

### Empresas Parceiras:
- **ID da Empresa:** Chave Primária, Inteiro
- **Nome da Empresa:** Texto
- **Localização:** Texto
- **Outras informações relevantes:** Texto

### Tecnologias:
- **ID da Tecnologia:** Chave Primária, Inteiro
- **Nome da Tecnologia:** Texto
- **Área da Tecnologia:** Texto

### Colaboradores:
- **ID do Colaborador:** Chave Primária, Inteiro
- **Nome do Colaborador:** Texto
- **Cargo:** Texto
- **E-mail:** Texto
- **ID da Empresa em que trabalha:** Chave Estrangeira referenciando Empresas Parceiras, Inteiro

## Relacionamentos

- Uma Empresa Parceira pode utilizar várias Tecnologias (relação muitos-para-muitos).
- Um Colaborador está associado a uma única Empresa Parceira (relação um-para-muitos).

## Simulação de Registros

### Empresas Parceiras:
1. **ID:** 1, **Nome:** "Tech Solutions Inc.", **Localização:** "Silicon Valley, CA", **Outras informações:** "Líder no desenvolvimento de soluções de software".
2. **ID:** 2, **Nome:** "DataTech Analytics", **Localização:** "New York, NY", **Outras informações:** "Especializada em análise de dados e Business Intelligence".

### Tecnologias:
1. **ID:** 1, **Nome:** "Python", **Área:** "Desenvolvimento de Software"
2. **ID:** 2, **Nome:** "SQL Server", **Área:** "Banco de Dados"

### Colaboradores:
1. **ID:** 1, **Nome:** "João Silva", **Cargo:** "Desenvolvedor Full Stack", **E-mail:** "joao.silva@techsolutions.com", **ID da Empresa:** 1
2. **ID:** 2, **Nome:** "Maria Santos", **Cargo:** "Analista de Dados", **E-mail:** "maria.santos@datatech.com", **ID da Empresa:** 2
