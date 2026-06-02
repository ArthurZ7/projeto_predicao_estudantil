# Recomendação educacional e predição de desempenho acadêmico
 Agrupamento de Dados e Inteligência Computacional

>**PROBLEMA:** Instituições de ensino desejam identificar perfis de estudantes, prever risco acadêmico e recomendar ações pedagógicas personalizadas. <br><br>**PERGUNTA CENTRAL:** Como agrupar estudantes por perfil acadêmico/comportamental e usar esses grupos para prever desempenho ou recomendar intervenções?

## 📊 Base de Dados

Usamos uma base de dados de **desempenho escolar de estudantes** com informações socioeconômicas e comportamentais. Existem **dois cursos distintos**:
- **student-mat.csv**: Dados de alunos do curso de **Matemática**
- **student-por.csv**: Dados de alunos do curso de **Português**

Há 382 estudantes que aparecem em ambos os cursos.

---

## 🏗️ Estrutura dos Dados (33 atributos)

### **1. Dados Demográficos** 
| Atributo | Tipo | Descrição |
|----------|------|-----------|
| `school` | Categórico | GP (Gabriel Pereira) ou MS (Mousinho da Silveira) |
| `sex` | Binário | F (Feminino) ou M (Masculino) |
| `age` | Numérico | Idade entre 15-22 anos |
| `address` | Binário | U (Urbano) ou R (Rural) |

### **2. Dados Familiares**
| Atributo | Tipo | Descrição |
|----------|------|-----------|
| `famsize` | Binário | LE3 (≤3 pessoas) ou GT3 (>3 pessoas) |
| `Pstatus` | Binário | T (Pais vivem juntos) ou A (Separados) |
| `Medu` | Numérico | Educação mãe: 0-4 (nenhuma até superior) |
| `Fedu` | Numérico | Educação pai: 0-4 (nenhuma até superior) |
| `Mjob` | Categórico | Profissão mãe (professor, saúde, serviços, casa, outra) |
| `Fjob` | Categórico | Profissão pai (idem) |

### **3. Dados Escolares**
| Atributo | Tipo | Descrição |
|----------|------|-----------|
| `traveltime` | Ordinal | 1-4 (tempo de viagem: <15min até >1h) |
| `studytime` | Ordinal | 1-4 (horas de estudo/semana) |
| `failures` | Numérico | Número de reprovações anteriores |
| `schoolsup` | Binário | Apoio educacional extra (sim/não) |
| `famsup` | Binário | Apoio familiar (sim/não) |
| `paid` | Binário | Aulas pagas extras (sim/não) |
| `activities` | Binário | Atividades extracurriculares (sim/não) |
| `nursery` | Binário | Frequentou pré-escola (sim/não) |
| `higher` | Binário | Deseja educação superior (sim/não) |
| `internet` | Binário | Acesso à internet em casa (sim/não) |

### **4. Dados Comportamentais**
| Atributo | Tipo | Descrição |
|----------|------|-----------|
| `reason` | Categórico | Motivo escolha escola (perto de casa, reputação, curso, outro) |
| `guardian` | Categórico | Responsável principal (mãe, pai, outro) |
| `romantic` | Binário | Tem relacionamento romântico (sim/não) |
| `famrel` | Ordinal | Qualidade relação familiar (1-5: péssima até excelente) |
| `freetime` | Ordinal | Tempo livre após escola (1-5: muito baixo até muito alto) |
| `goout` | Ordinal | Sai com amigos (1-5: muito baixo até muito alto) |
| `Dalc` | Ordinal | Consumo álcool dias úteis (1-5: muito baixo até muito alto) |
| `Walc` | Ordinal | Consumo álcool fins de semana (1-5: muito baixo até muito alto) |
| `health` | Ordinal | Estado de saúde atual (1-5: péssimo até excelente) |
| `absences` | Numérico | Número de faltas (0-93) |

### **5. Variáveis de Desempenho (ALVO)**
| Atributo | Tipo | Descrição |
|----------|------|-----------|
| `G1` | Numérico | Nota 1º período (0-20) |
| `G2` | Numérico | Nota 2º período (0-20) |
| `G3` | Numérico | **Nota final (0-20)** - VARIÁVEL ALVO |

---
