# NHANES 2021-2023 CVD Dataset
## Autor: Bruno Ricardo Corrêa
## Fonte dos dados: [NHANES 2021-2023](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2021)

Dataset preparado para modelos de aprendizado de máquina para prever doenças cardiovasculares.

## Dicionário de dados

Os dados obtidos no estudo NHANES (2021-2023) estão separados em diferentes datasets, para que seja possível utilizar para o treinamento de modelos de Aprendizado de Máquina, é necessário fazer uma união dos mesmos.

---

### DEMO_L.xpt

Contém dados demográficos, status da entrevista, informações socioeconômicas e pesos amostrais.

* `SEQN`: Número de sequência do entrevistado (Identificador único para cruzar os dados).
* `SDDSRVYR`: Ciclo de liberação dos dados (ex: "12" para Agosto 2021-Agosto 2023).
* `RIDSTATR`: Status da entrevista/exame (se apenas entrevistado ou também examinado).
* `RIAGENDR`: Gênero do participante.
* `RIDAGEYR`: Idade em anos no momento da triagem (limitado a 80 para proteger a privacidade).
* `RIDAGEMN`: Idade em meses na triagem (apenas para participantes de 0 a 24 meses).
* `RIDRETH1`: Raça/Etnia reportada (agrupamento clássico).
* `RIDRETH3`: Raça/Etnia reportada incluindo a categoria de Asiáticos Não-Hispânicos.
* `RIDEXMON`: Período de 6 meses em que o exame foi realizado (Novembro-Abril ou Maio-Outubro).
* `RIDEXAGM`: Idade em meses no momento do exame (para menores de 19 anos).
* `DMQMILIZ`: Indicador de serviço militar ativo nas Forças Armadas dos EUA.
* `DMDBORN4`: País de nascimento (EUA ou outros).
* `DMDYRUSR`: Tempo (em anos) de residência nos EUA para nascidos no exterior.
* `DMDEDUC2`: Nível de escolaridade para adultos (20+ anos).
* `DMDMARTZ`: Estado civil para adultos (20+ anos).
* `RIDEXPRG`: Status de gravidez no momento do exame.
* `DMDHHSIZ`: Número total de pessoas morando na residência.
* `DMDHRGND`: Gênero da pessoa de referência da residência.
* `DMDHRAGZ`: Idade da pessoa de referência da residência.
* `DMDHREDZ`: Escolaridade da pessoa de referência.
* `DMDHRMAZ`: Estado civil da pessoa de referência.
* `DMDHSEDZ`: Escolaridade do cônjuge da pessoa de referência.
* `WTINT2YR`: Peso amostral para a entrevista completa de 2 anos.
* `WTMEC2YR`: Peso amostral para os exames no MEC (Mobile Examination Center) de 2 anos.
* `SDMVSTRA`: Pseudo-estrato de variância mascarada (necessário para cálculos estatísticos complexos).
* `SDMVPSU`: Pseudo-PSU (unidade primária de amostragem) de variância mascarada.
* `INDFMPIR`: Razão entre a renda familiar e o nível de pobreza (Poverty Income Ratio).

### BPXO_L.xpt

Contém dados de pressão arterial oscilométrica e frequência cardíaca (pulso).

* `BPAOARM`: Braço selecionado para a medição.
* `BPAOCSZ`: Tamanho da braçadeira codificado com base na circunferência do braço.
* `BPXOSY1`: Pressão sistólica - 1ª leitura.
* `BPXODI1`: Pressão diastólica - 1ª leitura.
* `BPXOSY2`: Pressão sistólica - 2ª leitura.
* `BPXODI2`: Pressão diastólica - 2ª leitura.
* `BPXOSY3`: Pressão sistólica - 3ª leitura.
* `BPXODI3`: Pressão diastólica - 3ª leitura.
* `BPXOPLS1`: Pulso (frequência cardíaca) - 1ª leitura.
* `BPXOPLS2`: Pulso - 2ª leitura.
* `BPXOPLS3`: Pulso - 3ª leitura.

### BMX_L.xpt

Contém dados de medidas corporais (antropometria).

* `BMDSTATS`: Código de status do componente de medidas corporais (ex: completo, parcial).
* `BMXWT`: Peso corporal (kg).
* `BMIWT`: Código de comentário sobre o peso (ex: uso de aparelho médico, roupas).
* `BMXRECUM`: Comprimento recumbente (cm) (para crianças pequenas).
* `BMIRECUM`: Comprimento recumbente - Código de comentário.
* `BMXHEAD`: Circunferência da cabeça (cm).
* `BMIHEAD`: Circunferência da cabeça - Código de comentário.
* `BMXHT`: Altura em pé (cm).
* `BMIHT`: Altura em pé - Código de comentário.
* `BMXBMI`: Índice de Massa Corporal (IMC) (kg/m²).
* `BMDBMIC`: Categoria de IMC para crianças e adolescentes (ex: peso normal, obeso).
* `BMXLEG`: Comprimento da perna superior (cm).
* `BMILEG`: Comprimento da perna superior - Código de comentário.
* `BMXARML`: Comprimento do braço superior (cm).
* `BMIARML`: Comprimento do braço superior - Código de comentário.
* `BMXARMC`: Circunferência do braço (cm).
* `BMIARMC`: Circunferência do braço - Código de comentário.
* `BMXWAIST`: Circunferência da cintura (cm).
* `BMIWAIST`: Circunferência da cintura - Código de comentário.
* `BMXHIP`: Circunferência do quadril (cm).
* `BMIHIP`: Circunferência do quadril - Código de comentário.

### ALB_CR_L.xpt

Contém dados de Albumina e Creatinina medidos na urina.

* `URXUMA`: Albumina na urina (ug/mL).
* `URXUMS`: Albumina na urina convertida para (mg/L).
* `URDUMALC`: Código de comentário para Albumina na urina (indica se o valor esteve abaixo do limite de detecção).
* `URXUCR`: Creatinina na urina (mg/dL).
* `URXCRS`: Creatinina na urina convertida para (umol/L).
* `URDUCRLC`: Código de comentário para Creatinina na urina.
* `URDACT`: Razão Albumina-Creatinina na urina (mg/g).

### TRIGLY_L.xpt

Contém dados laboratoriais do Colesterol LDL e Triglicerídeos no soro (necessário jejum).

* `WTSAF2YR`: Peso amostral para a subamostra que realizou jejum (importante para o modelo caso os dados de jejum sejam usados).
* `LBXTLG`: Triglicerídeos (mg/dL).
* `LBDTRSI`: Triglicerídeos em unidades do SI (mmol/L).
* `LBDLDL`: Colesterol LDL calculado pela equação de Friedewald (mg/dL).
* `LBDLDLSI`: Colesterol LDL (Friedewald) em unidades do SI (mmol/L).
* `LBDLDLM`: Colesterol LDL calculado pela equação de Martin-Hopkins (mg/dL).
* `LBDLDMSI`: Colesterol LDL (Martin-Hopkins) em unidades do SI (mmol/L).
* `LBDLDLN`: Colesterol LDL calculado pela equação NIH 2 (mg/dL).
* `LBDLDNSI`: Colesterol LDL (NIH 2) em unidades do SI (mmol/L).

### CBC_L.xpt

Contém os dados laboratoriais do Hemograma Completo (Hemograma com diferencial de 5 partes) e o peso amostral do componente de flebotomia.

* `WTPH2YR`: Peso amostral para o componente de Flebotomia (exame de sangue).
* `LBXWBCSI`: Contagem de Glóbulos Brancos / Leucócitos (1000 células/uL).
* `LBXLYPCT`: Porcentagem de Linfócitos (%).
* `LBXMOPCT`: Porcentagem de Monócitos (%).
* `LBXNEPCT`: Porcentagem de Neutrófilos segmentados (%).
* `LBXEOPCT`: Porcentagem de Eosinófilos (%).
* `LBXBAPCT`: Porcentagem de Basófilos (%).
* `LBDLYMNO`: Número absoluto de Linfócitos (1000 células/uL).
* `LBDMONO`: Número absoluto de Monócitos (1000 células/uL).
* `LBDNENO`: Número absoluto de Neutrófilos (1000 células/uL).
* `LBDEONO`: Número absoluto de Eosinófilos (1000 células/uL).
* `LBDBANO`: Número absoluto de Basófilos (1000 células/uL).
* `LBXRBCSI`: Contagem de Glóbulos Vermelhos / Hemácias (milhões de células/uL).
* `LBXHGB`: Hemoglobina (g/dL).
* `LBXHCT`: Hematócrito (%).
* `LBXMCVSI`: Volume Corpuscular Médio / VCM (fL).
* `LBXMC`: Concentração de Hemoglobina Corpuscular Média / CHCM (g/dL).
* `LBXMCHSI`: Hemoglobina Corpuscular Média / HCM (pg).
* `LBXRDW`: Amplitude de Distribuição dos Glóbulos Vermelhos / RDW (%).
* `LBXPLTSI`: Contagem de Plaquetas (1000 células/uL).
* `LBXMPSI`: Volume Plaquetário Médio (fL).
* `LBXNRBC`: Hemácias Nucleadas (por 100 Glóbulos Brancos).

### HDL_L.xpt

Contém dados laboratoriais de colesterol HDL no soro sanguíneo.

* `LBDHDD`: Colesterol HDL (mg/dL).
* `LBDHDDSI`: Colesterol HDL em unidades do SI (mmol/L).

### TCHOL_L.xpt

Contém dados laboratoriais de colesterol total no soro sanguíneo (método de referência).

* `LBXTC`: Colesterol Total (mg/dL).
* `LBDTCSI`: Colesterol Total em unidades do SI (mmol/L).

### BIOPRO_L.xpt

Contém os dados de Perfil Bioquímico Padrão do soro.

* `LBXSATSI`: Alanina Aminotransferase (ALT) (IU/L).
* `LBDSATLC`: Código de comentário para ALT (indica se abaixo da detecção).
* `LBXSAL`: Albumina sérica refrigerada (g/dL).
* `LBDSALSI`: Albumina sérica refrigerada (g/L).
* `LBXSAPSI`: Fosfatase Alcalina (ALP) (IU/L).
* `LBXSASSI`: Aspartato Aminotransferase (AST) (IU/L).
* `LBXSC3SI`: Bicarbonato (mmol/L).
* `LBXSBU`: Nitrogênio da Ureia no Sangue / BUN (mg/dL).
* `LBDSBUSI`: Nitrogênio da Ureia no Sangue (mmol/L).
* `LBXSCLSI`: Cloreto (mmol/L).
* `LBXSCK`: Creatina Fosfoquinase / CPK (U/L).
* `LBXSCR`: Creatinina sérica refrigerada (mg/dL).
* `LBDSCRSI`: Creatinina sérica refrigerada (umol/L).
* `LBXSGB`: Globulina (g/dL).
* `LBDSGBSI`: Globulina (g/L).
* `LBXSGL`: Glicose sérica refrigerada (mg/dL) *(Nota: a recomendação analítica do NHANES é usar preferencialmente LBXGLU para glicose).*
* `LBDSGLSI`: Glicose sérica refrigerada (mmol/L).
* `LBXSGTSI`: Gama-glutamil Transferase / GGT (IU/L).
* `LBDSGTLC`: Código de comentário para GGT.
* `LBXSIR`: Ferro sérico refrigerado (ug/dL).
* `LBDSIRSI`: Ferro sérico refrigerado (umol/L).
* `LBXSLDSI`: Desidrogenase Láctica / LDH (U/L).
* `LBXMAGN`: Magnésio (mg/dL).
* `LBXSOSSI`: Osmolalidade (mmol/Kg).
* `LBXSPH`: Fósforo (mg/dL).
* `LBDSPHSI`: Fósforo (mmol/L).
* `LBXSKSI`: Potássio (mmol/L).
* `LBXSNASI`: Sódio (mmol/L).
* `LBXSTB`: Bilirrubina Total (mg/dL).
* `LBDSTBSI`: Bilirrubina Total (umol/L).
* `LBDSTBLC`: Código de comentário para Bilirrubina Total.
* `LBXSCA`: Cálcio Total (mg/dL).
* `LBDSCASI`: Cálcio Total (mmol/L).
* `LBXSCH`: Colesterol Total sérico refrigerado (mg/dL) *(Nota: a recomendação analítica do NHANES é usar preferencialmente LBXTC, do arquivo TCHOL_L).*
* `LBDSCHSI`: Colesterol Total sérico refrigerado (mmol/L) *(mesma nota acima).*
* `LBXSTP`: Proteína Total (g/dL).
* `LBDSTPSI`: Proteína Total (g/L).
* `LBXSTR`: Triglicerídeos séricos refrigerados (mg/dL) *(Nota: a recomendação analítica do NHANES é usar preferencialmente LBXTLG, do arquivo TRIGLY_L).*
* `LBDSTRSI`: Triglicerídeos séricos refrigerados (mmol/L) *(mesma nota acima).*
* `LBXSUA`: Ácido Úrico (mg/dL).
* `LBDSUASI`: Ácido Úrico (umol/L).

### INS_L.xpt

Contém dados laboratoriais de insulina sérica.

* `LBXIN`: Insulina (uU/mL).
* `LBDINSI`: Insulina (pmol/L).
* `LBDINLC`: Código de comentário da Insulina.

### HSCRP_L.xpt

Contém dados laboratoriais de proteína C-Reativa de alta sensibilidade (marcador de inflamação).

* `LBXHSCRP`: Proteína C-Reativa de Alta Sensibilidade / hs-CRP (mg/L) (Indicador de inflamação).
* `LBDHRPLC`: Código de comentário da hs-CRP.

### GHB_L.xpt

Contém dados laboratoriais de glico-hemoglobina (HbA1c).

* `LBXGH`: Glico-hemoglobina (HbA1c) em (%).

### GLU_L.xpt

Contém dados laboratoriais de glicose plasmática em jejum (método de referência).

* `LBXGLU`: Glicose plasmática em jejum (mg/dL).
* `LBDGLUSI`: Glicose plasmática em jejum (mmol/L).

### DIQ_L.xpt

Contém dados do questionário sobre Diabetes e seu tratamento.

* `DIQ010`: Algum médico já disse que o paciente tem diabetes?
* `DID040`: Idade em que o paciente foi informado de que tinha diabetes.
* `DIQ160`: Algum médico já disse que o paciente tem pré-diabetes?
* `DIQ180`: Fez teste de sangue nos últimos 3 anos para avaliar diabetes/açúcar alto?
* `DIQ050`: O paciente toma insulina atualmente?
* `DID060`: Há quanto tempo o paciente toma insulina?
* `DIQ060U`: Unidade de tempo para a pergunta anterior (meses ou anos).
* `DIQ070`: Toma comprimidos para baixar o açúcar no sangue (hipoglicemiantes orais)?

### ALQ_L.xpt

Contém dados do questionário sobre uso de Álcool.

* `ALQ111`: Já bebeu qualquer tipo de bebida alcoólica na vida?
* `ALQ121`: Com que frequência tomou bebidas alcoólicas nos últimos 12 meses?
* `ALQ130`: Média de bebidas por dia nos dias em que bebeu (últimos 12 meses).
* `ALQ142`: Quantos dias tomou 4/5 (mulheres/homens) bebidas nos últimos 12 meses?
* `ALQ270`: Quantas vezes tomou 4/5 bebidas em 2 horas ou menos nos últimos 12 meses?
* `ALQ280`: Quantas vezes tomou 8 ou mais bebidas em um dia nos últimos 12 meses?
* `ALQ151`: Alguma vez na vida tomou 4/5 bebidas todos os dias?
* `ALQ170`: Quantas vezes tomou 4/5 bebidas em uma única ocasião nos últimos 30 dias?

### SMQ_L.xpt

Contém dados do questionário sobre uso de Cigarros / Fumo.

* `SMQ020`: Já fumou pelo menos 100 cigarros na vida inteira?
* `SMQ040`: Atualmente, o paciente fuma cigarro?
* `SMD641`: Número de dias que fumou cigarro nos últimos 30 dias.
* `SMD650`: Média de cigarros por dia nos últimos 30 dias.
* `SMD100MN`: Costuma fumar cigarros mentolados ou não-mentolados?
* `SMQ621`: Quantos cigarros fumou na vida inteira? (Específico para jovens).
* `SMD630`: Idade em que fumou o primeiro cigarro inteiro (Específico para jovens).
* `SMAQUEX2`: Indicador do modo de aplicação do questionário (ex: Entrevista no domicílio ou ACASI no MEC).

### MCQ_L.xpt

Contém dados do questionário sobre Condições Médicas diagnosticadas.

* `MCQ010`: Já foi informado(a) que tem asma?
* `MCQ035`: Ainda tem asma?
* `MCQ040`: Teve ataque de asma no último ano?
* `MCQ050`: Visita ao pronto-socorro devido à asma no último ano?
* `AGQ030`: Teve episódio de febre do feno (rinite alérgica sazonal) no último ano?
* `MCQ053`: Tratamento para anemia nos últimos 3 meses?
* `MCQ149`: Já iniciou ciclo menstrual? (para jovens).
* `MCQ160A`: Médico já disse que tem artrite?
* `MCQ195`: Qual tipo de artrite (ex: reumatoide, osteoartrite)?
* `MCQ160B`: Médico já disse que tem insuficiência cardíaca congestiva?
* `MCQ160C`: Médico já disse que tem doença arterial coronariana?
* `MCQ160D`: Médico já disse que tem angina?
* `MCQ160E`: Médico já disse que teve ataque cardíaco (infarto)?
* `MCQ160F`: Médico já disse que teve acidente vascular cerebral (AVC)?
* `MCQ160M`: Médico já disse que tem problema na tireoide?
* `MCQ170M`: Ainda tem problema na tireoide?
* `MCQ160P`: Médico já disse que tem DPOC (doença pulmonar obstrutiva crônica), enfisema ou bronquite crônica?
* `MCQ160L`: Médico já disse que tem algum problema no fígado?
* `MCQ170L`: Ainda tem problema no fígado?
* `MCQ500`: Alguma vez foi dito que tem doença hepática? (Jovens)
* `MCQ510A` a `MCQ510F`: Qual o tipo de condição do fígado? (A = fígado gordo/esteatose, B = fibrose, C = cirrose, D = hepatite viral, E = autoimune, F = outra).
* `MCQ550`: Médico já disse que tem pedra na vesícula (cálculo biliar)?
* `MCQ560`: Já fez cirurgia de vesícula biliar?
* `MCQ220`: Médico já disse que tem câncer ou tumor maligno?
* `MCQ230A` a `MCQ230D`: Qual o tipo de câncer? (A = 1º, B = 2º, C = 3º, D = Mais de 3 tipos).
* `OSQ230`: Tem objetos de metal (pinos, próteses articulares) dentro do corpo?

### PAQ_L.xpt

Contém dados do questionário sobre Atividade Física.

* `PAD790Q`: Frequência da atividade física moderada no tempo livre (vezes).
* `PAD790U`: Unidade de tempo para atividade física moderada (ex: por dia, semana, mês).
* `PAD800`: Minutos gastos em atividade física moderada (por ocasião).
* `PAD810Q`: Frequência de atividade física vigorosa no tempo livre.
* `PAD810U`: Unidade de tempo para atividade física vigorosa.
* `PAD820`: Minutos gastos em atividade física vigorosa (por ocasião).
* `PAD680`: Tempo sedentário: Quantos minutos gasta sentado por dia típico?

### BPQ_L.xpt

Contém dados do questionário sobre Pressão Arterial e Colesterol.

* `BPQ020`: Já foi informado(a) que tem pressão alta?
* `BPQ150`: Toma remédio para pressão alta?
* `BPQ080`: Já foi informado(a) que tem colesterol alto?
* `BPQ101D`: Toma remédio para baixar o colesterol?

### Variável do Modelo

Contém o alvo preditivo (variável dependente) criado no seu projeto.

* `target`: A variável alvo (rótulo/label) criada a partir da combinação de perguntas do questionário MCQ_L.xpt relacionadas a doenças cardiovasculares (MCQ160B, MCQ160C, MCQ160D, MCQ160E, MCQ160F) para indicar se o participante tem ou não uma condição cardiovascular diagnosticada.
### Atributos Customizados (Feature Engineering)

Este dataset (composto por 224 atributos) engloba os atributos originais listados acima e novas variu00e1veis criadas durante a etapa de Engenharia de Atributos:

* `smk_cat`: Categoria de tabagismo derivada.
* `alc_cat`: Categoria de consumo de u00e1lcool derivada.
* `pa_mod_min_wk`: Minutos de atividade fu00edsica moderada por semana.
* `pa_vig_min_wk`: Minutos de atividade fu00edsica vigorosa por semana.
* `pa_cat`: Categoria geral de atividade fu00edsica.
* `thyroid_cat`: Categoria agregada de problemas de tireoide.
* `liver_cat`: Categoria agregada de condiu00e7u00f5es hepu00e1ticas.
* `tc_mgdl_source` / `tg_mgdl_source`: Indicadores da fonte de dados de colesterol e trigliceru00eddeos.
