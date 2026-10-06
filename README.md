# NHANES 2021-2023 CVD Dataset
## Autor: Bruno Ricardo Corrêa
## Fonte dos dados: [CDC NHANES](https://wwwn.cdc.gov/nchs/nhanes/Default.aspx)

Dataset prepared for machine learning models to predict cardiovascular diseases. (Dataset preparado para modelos de Aprendizado de Máquina para a predição de Doenças Cardiovasculares).

## Dicionário de dados

Os dados obtidos no estudo NHANES (2021-2023) estão separados originalmente em diferentes datasets, para que seja possível utilizar para o treinamento de modelos de Aprendizado de Máquina, é necessário fazer uma união dos mesmos. Após a união, foi aplicado um processo de Engenharia de Atributos (*Feature Engineering*). 

Durante o pré-processamento, as variáveis irrelevantes ou redundantes foram removidas e **novas variáveis e indicadores de risco** foram derivados (ex: razões aterogênicas `ratio_chol_hdl`, cálculo da função renal `eGFR_2021`, categorias agrupadas de tabagismo, álcool, tempo de atividade física, variáveis de comorbidades consolidadas de tireoide e fígado, além das flags de proveniência de dados).

O dataset analítico final estruturado neste repositório possui **227 atributos**.

### Lista de Atributos (227 Colunas)

| Coluna | Descrição |
| :--- | :--- |
| `age` | Idade em anos no momento da triagem (limitado a 80). |
| `age_mo` | Idade em meses na triagem (apenas para participantes de 0 a 24 meses). |
| `alb_gdl` | Albumina sérica refrigerada (g/dL). |
| `alb_gl` | Albumina sérica refrigerada (g/L). |
| `alc_4_5_12m` | Quantas vezes tomou 4/5 bebidas em 2 horas ou menos nos últimos 12 meses? |
| `alc_5_daily` | Alguma vez na vida tomou 4/5 bebidas todos os dias? |
| `alc_8_10_12m` | Quantas vezes tomou 8 ou mais bebidas em um dia nos últimos 12 meses? |
| `alc_avg_day` | Média de bebidas por dia nos dias em que bebeu (últimos 12 meses). |
| `alc_binge_12m` | Quantos dias tomou 4/5 bebidas nos últimos 12 meses? |
| `alc_cat` | Categoria de consumo de álcool derivada pelo pipeline (0=Abstainer, 1=Occasional, 2=Moderate, 3=Heavy). |
| `alc_ever` | Já bebeu qualquer tipo de bebida alcoólica na vida? |
| `alc_freq_12m` | Com que frequência tomou bebidas alcoólicas nos últimos 12 meses? |
| `alc_lifetime` | Quantas vezes tomou 4/5 bebidas em uma única ocasião nos últimos 30 dias? |
| `alp` | Fosfatase Alcalina (ALP) (IU/L). |
| `alt` | Alanina Aminotransferase (ALT) (IU/L). |
| `alt_cmt` | Código de comentário para ALT. |
| `anemia_treatment_3m` | Tratamento para anemia nos últimos 3 meses? |
| `angina_diag` | Médico já disse que tem angina? |
| `arm_circ_cm` | Circunferência do braço (cm). |
| `arm_circ_cmt` | Circunferência do braço - código de comentário. |
| `arm_len_cm` | Comprimento do braço superior (cm). |
| `arm_len_cmt` | Comprimento do braço superior - código de comentário. |
| `arthritis_diag` | Médico já disse que tem artrite? |
| `arthritis_type` | Qual tipo de artrite (ex: reumatoide, osteoartrite)? |
| `ast` | Aspartato Aminotransferase (AST) (IU/L). |
| `asthma_atk_12m` | Teve ataque de asma no último ano? |
| `asthma_diag` | Já foi informado(a) que tem asma? |
| `asthma_er_12m` | Visita ao pronto-socorro devido à asma no último ano? |
| `asthma_status` | Ainda tem asma? |
| `bas_ct` | Número absoluto de basófilos (1000 células/uL). |
| `bas_pct` | Porcentagem de basófilos (%). |
| `bicarb_mmol` | Bicarbonato (mmol/L). |
| `birth_country` | País de nascimento (EUA ou outros). |
| `bm_status` | Código de status do componente de medidas corporais. |
| `bmi` | Índice de Massa Corporal (IMC) (kg/m²). |
| `bmi_cat_child` | Categoria de IMC para crianças e adolescentes. |
| `border_diab_diag` | Fez teste de sangue nos últimos 3 anos para avaliar diabetes/açúcar alto? |
| `bp_arm` | Braço selecionado para a medição. |
| `bp_cuff` | Tamanho da braçadeira codificado com base na circunferência do braço. |
| `bun_mgdl` | Nitrogênio da Ureia no Sangue / BUN (mg/dL). |
| `bun_mmol` | Nitrogênio da Ureia no Sangue (mmol/L). |
| `cancer_diag` | Médico já disse que tem câncer ou tumor maligno? |
| `cancer_t1` | Tipo de câncer: 1º diagnosticado. |
| `cancer_t2` | Tipo de câncer: 2º diagnosticado. |
| `cancer_t3` | Tipo de câncer: 3º diagnosticado. |
| `cancer_t4` | Tipo de câncer: mais de 3 tipos diagnosticados. |
| `chd_diag` | Médico já disse que tem doença arterial coronariana? |
| `chf_diag` | Médico já disse que tem insuficiência cardíaca congestiva? |
| `chlor_mmol` | Cloreto (mmol/L). |
| `copd_diag` | Médico já disse que tem DPOC, enfisema ou bronquite crônica? |
| `cpk` | Creatina Fosfoquinase / CPK (U/L). |
| `crp_cmt` | Código de comentário da hs-CRP. |
| `crp_mgl` | Proteína C-Reativa de Alta Sensibilidade / hs-CRP (mg/L). |
| `cycle` | Ciclo de liberação dos dados. |
| `dia_bp1` | Pressão diastólica - 1ª leitura. |
| `dia_bp2` | Pressão diastólica - 2ª leitura. |
| `dia_bp3` | Pressão diastólica - 3ª leitura. |
| `diab_age` | Idade em que o paciente foi informado de que tinha diabetes. |
| `diab_diag` | Algum médico já disse que o paciente tem diabetes? |
| `diab_ins_dur` | Há quanto tempo o paciente toma insulina? |
| `diab_ins_unit` | Unidade de tempo para a pergunta anterior (meses ou anos). |
| `diab_insulin` | O paciente toma insulina atualmente? |
| `diab_pills` | Toma comprimidos para baixar o açúcar no sangue? |
| `eGFR_2021` | Taxa de Filtração Glomerular Estimada (fórmula CKD-EPI 2021) calculada pelo pipeline. |
| `ecig_ever` | Quantos cigarros fumou na vida inteira? (específico para jovens). |
| `education` | Nível de escolaridade para adultos (20+ anos). |
| `eos_ct` | Número absoluto de eosinófilos (1000 células/uL). |
| `eos_pct` | Porcentagem de eosinófilos (%). |
| `exam_age_mo` | Idade em meses no momento do exame (para menores de 19 anos). |
| `exam_mo` | Período de 6 meses em que o exame foi realizado. |
| `exam_status` | Status da entrevista/exame (se apenas entrevistado ou também examinado). |
| `f_gluc_mgdl` | Glicose plasmática em jejum (mg/dL) - método de referência. |
| `f_gluc_mmol` | Glicose plasmática em jejum (mmol/L). |
| `gall_surg` | Já fez cirurgia de vesícula biliar? |
| `gallstone_diag` | Médico já disse que tem pedra na vesícula (cálculo biliar)? |
| `gender` | Gênero do participante. |
| `ggt` | Gama-glutamil Transferase / GGT (IU/L). |
| `ggt_cmt` | Código de comentário para GGT. |
| `glob_gdl` | Globulina (g/dL). |
| `glob_gl` | Globulina (g/L). |
| `hay_fever_atk_12m` | Teve episódio de febre do feno no último ano? |
| `hba1c` | Glico-hemoglobina (HbA1c) em %. |
| `hct` | Hematócrito (%). |
| `hdl_mgdl` | Colesterol HDL (mg/dL). |
| `hdl_mmol` | Colesterol HDL em unidades do SI (mmol/L). |
| `head_circ_cm` | Circunferência da cabeça (cm). |
| `head_circ_cmt` | Circunferência da cabeça - código de comentário. |
| `height_cm` | Altura em pé (cm). |
| `height_cmt` | Altura em pé - código de comentário. |
| `hgb` | Hemoglobina (g/dL). |
| `hh_ref_age` | Idade da pessoa de referência da residência. |
| `hh_ref_edu` | Escolaridade da pessoa de referência. |
| `hh_ref_gender` | Gênero da pessoa de referência da residência. |
| `hh_ref_marital` | Estado civil da pessoa de referência. |
| `hh_size` | Número total de pessoas morando na residência. |
| `hh_spouse_edu` | Escolaridade do cônjuge da pessoa de referência. |
| `high_bp_diag` | Já foi informado(a) que tem pressão alta? |
| `high_bp_meds` | Toma remédio para pressão alta? |
| `high_chol_diag` | Já foi informado(a) que tem colesterol alto? |
| `high_chol_meds` | Toma remédio para baixar o colesterol? |
| `hip_circ_cm` | Circunferência do quadril (cm). |
| `hip_circ_cmt` | Circunferência do quadril - código de comentário. |
| `id` | Número de sequência do entrevistado (identificador único). |
| `insulin_cmt` | Código de comentário da insulina. |
| `insulin_pmol` | Insulina (pmol/L). |
| `insulin_uiu` | Insulina (uU/mL). |
| `iron_ugdl` | Ferro sérico refrigerado (ug/dL). |
| `iron_umol` | Ferro sérico refrigerado (umol/L). |
| `ldh` | Desidrogenase Láctica / LDH (U/L). |
| `ldl_f_mgdl` | Colesterol LDL calculado pela equação de Friedewald (mg/dL). |
| `ldl_f_mmol` | Colesterol LDL (Friedewald) em mmol/L. |
| `ldl_mh_mgdl` | Colesterol LDL calculado pela equação de Martin-Hopkins (mg/dL). |
| `ldl_mh_mmol` | Colesterol LDL (Martin-Hopkins) em mmol/L. |
| `ldl_nih_mgdl` | Colesterol LDL calculado pela equação NIH 2 (mg/dL). |
| `ldl_nih_mmol` | Colesterol LDL (NIH 2) em mmol/L. |
| `leg_len_cm` | Comprimento da perna superior (cm). |
| `leg_len_cmt` | Comprimento da perna superior - código de comentário. |
| `liver_autoimm` | Tipo de condição do fígado: autoimune. |
| `liver_cat` | Categoria consolidada de problemas de fígado (derivada de liver_diag e liver_curr). |
| `liver_cirrhosis` | Tipo de condição do fígado: cirrose. |
| `liver_curr` | Ainda tem problema no fígado? |
| `liver_diag` | Médico já disse que tem algum problema no fígado? |
| `liver_ever` | Alguma vez foi dito que tem doença hepática? (jovens). |
| `liver_fatty` | Tipo de condição do fígado: fígado gordo/esteatose. |
| `liver_fibrosis` | Tipo de condição do fígado: fibrose. |
| `liver_other` | Tipo de condição do fígado: outra. |
| `liver_viral` | Tipo de condição do fígado: hepatite viral. |
| `lym_ct` | Número absoluto de linfócitos (1000 células/uL). |
| `lym_pct` | Porcentagem de linfócitos (%). |
| `mag_mgdl` | Magnésio (mg/dL). |
| `marital` | Estado civil para adultos (20+ anos). |
| `mch` | Concentração de hemoglobina corpuscular média / CHCM (g/dL). |
| `mchc` | Hemoglobina corpuscular média / HCM (pg). |
| `mcv` | Volume corpuscular médio / VCM (fL). |
| `menstruation_started` | Já iniciou ciclo menstrual? |
| `metal_objects` | Tem objetos de metal dentro do corpo? |
| `mi_diag` | Médico já disse que teve ataque cardíaco (infarto)? |
| `military` | Indicador de serviço militar ativo nas Forças Armadas dos EUA. |
| `mon_ct` | Número absoluto de monócitos (1000 células/uL). |
| `mon_pct` | Porcentagem de monócitos (%). |
| `mpv` | Volume plaquetário médio (fL). |
| `neu_ct` | Número absoluto de neutrófilos (1000 células/uL). |
| `neu_pct` | Porcentagem de neutrófilos segmentados (%). |
| `nrbc` | Hemácias nucleadas (por 100 glóbulos brancos). |
| `osmol_mmol` | Osmolalidade (mmol/Kg). |
| `pa_mod_dur` | Minutos gastos em atividade física moderada (por ocasião). |
| `pa_mod_freq` | Frequência da atividade física moderada no tempo livre (vezes). |
| `pa_mod_min_wk` | Minutos de atividade física moderada por semana (derivado). |
| `pa_mod_unit` | Unidade de tempo para atividade física moderada. |
| `pa_vig_dur` | Minutos gastos em atividade física vigorosa (por ocasião). |
| `pa_vig_freq` | Frequência de atividade física vigorosa no tempo livre. |
| `pa_vig_min_wk` | Minutos de atividade física vigorosa por semana (derivado). |
| `pa_vig_unit` | Unidade de tempo para atividade física vigorosa. |
| `phos_mgdl` | Fósforo (mg/dL). |
| `phos_mmol` | Fósforo (mmol/L). |
| `pls1` | Pulso (frequência cardíaca) - 1ª leitura. |
| `pls2` | Pulso - 2ª leitura. |
| `pls3` | Pulso - 3ª leitura. |
| `plt` | Contagem de plaquetas (1000 células/uL). |
| `potas_mmol` | Potássio (mmol/L). |
| `poverty_ratio` | Razão entre a renda familiar e o nível de pobreza (poverty income ratio). |
| `prediab_diag` | Algum médico já disse que o paciente tem pré-diabetes? |
| `pregnancy` | Status de gravidez no momento do exame. |
| `psu` | Pseudo-PSU (unidade primária de amostragem) de variância mascarada. |
| `q_mode` | Indicador do modo de aplicação do questionário. |
| `race` | Raça/etnia reportada (agrupamento clássico). |
| `race_det` | Raça/etnia reportada incluindo a categoria de asiáticos não-hispânicos. |
| `ratio_chol_hdl` | Razão Colesterol Total / HDL (criada pelo pipeline). |
| `ratio_trig_hdl` | Razão Triglicerídeos / HDL (criada pelo pipeline). |
| `rbc` | Contagem de glóbulos vermelhos / hemácias (milhões de células/uL). |
| `rdw` | Amplitude de distribuição dos glóbulos vermelhos / RDW (%). |
| `recum_len_cm` | Comprimento recumbente (cm). |
| `recum_len_cmt` | Comprimento recumbente - código de comentário. |
| `s_creat_mgdl` | Creatinina sérica refrigerada (mg/dL). |
| `s_creat_umol` | Creatinina sérica refrigerada (umol/L). |
| `s_gluc_mgdl` | Glicose sérica refrigerada (mg/dL). |
| `s_gluc_mmol` | Glicose sérica refrigerada (mmol/L). |
| `sed_min_day` | Tempo sedentário: quantos minutos gasta sentado por dia típico? |
| `smk_100` | Já fumou pelo menos 100 cigarros na vida inteira? |
| `smk_avg_day` | Média de cigarros por dia nos últimos 30 dias. |
| `smk_cat` | Categoria de tabagismo derivada pelo pipeline (0=Never, 1=Current Daily, 2=Current Occasional, 3=Former). |
| `smk_menthol` | Costuma fumar cigarros mentolados ou não-mentolados? |
| `smk_quit_days` | Número de dias que fumou cigarro nos últimos 30 dias. |
| `smk_start_age` | Idade em que fumou o primeiro cigarro inteiro. |
| `smk_status` | Atualmente, o paciente fuma cigarro? |
| `sod_mmol` | Sódio (mmol/L). |
| `stratum` | Pseudo-estrato de variância mascarada. |
| `stroke_diag` | Médico já disse que teve acidente vascular cerebral (AVC)? |
| `sys_bp1` | Pressão sistólica - 1ª leitura. |
| `sys_bp2` | Pressão sistólica - 2ª leitura. |
| `sys_bp3` | Pressão sistólica - 3ª leitura. |
| `t_bili_cmt` | Código de comentário para bilirrubina total. |
| `t_bili_mgdl` | Bilirrubina Total (mg/dL). |
| `t_bili_umol` | Bilirrubina Total (umol/L). |
| `t_calc_mgdl` | Cálcio Total (mg/dL). |
| `t_calc_mmol` | Cálcio Total (mmol/L). |
| `t_prot_gdl` | Proteína Total (g/dL). |
| `t_prot_gl` | Proteína Total (g/L). |
| `target` | Variável alvo: Presença de Doença Cardiovascular (1=Sim, 0=Não). |
| `tc_bch_mmol` | Colesterol Total sérico refrigerado (painel bioquímico padrão) em mmol/L. |
| `tc_mgdl` | Colesterol Total (mg/dL) - método de referência. |
| `tc_mgdl_source` | Flag indicando a origem da medição de colesterol total (método referência ou fallback). |
| `tc_mmol` | Colesterol Total em unidades do SI (mmol/L) - método de referência. |
| `tg_bch_mmol` | Triglicerídeos séricos refrigerados (painel bioquímico padrão) em mmol/L. |
| `tg_mgdl` | Triglicerídeos (mg/dL). |
| `tg_mgdl_source` | Flag indicando a origem da medição de triglicerídeos (método referência ou fallback). |
| `tg_mmol` | Triglicerídeos em unidades do SI (mmol/L). |
| `thyroid_cat` | Categoria consolidada de problemas de tireoide (derivada de thyroid_diag e thyroid_curr). |
| `u_acr` | Razão albumina-creatinina na urina (mg/g). |
| `u_alb_cmt` | Código de comentário para albumina na urina. |
| `u_alb_mgdl` | Albumina na urina (mg/dL). |
| `u_alb_ugml` | Albumina na urina (ug/mL). |
| `u_creat_cmt` | Código de comentário para creatinina na urina. |
| `u_creat_mgdl` | Creatinina na urina (mg/dL). |
| `u_creat_umol` | Creatinina na urina convertida para umol/L. |
| `uric_mgdl` | Ácido Úrico (mg/dL). |
| `uric_umol` | Ácido Úrico (umol/L). |
| `waist_circ_cm` | Circunferência da cintura (cm). |
| `waist_circ_cmt` | Circunferência da cintura - código de comentário. |
| `wbc` | Contagem de glóbulos brancos / leucócitos (1000 células/uL). |
| `weight_cmt` | Código de comentário sobre o peso. |
| `weight_kg` | Peso corporal (kg). |
| `wt_fast_2yr` | Peso amostral para a subamostra que realizou jejum. |
| `wt_int_2yr` | Peso amostral para a entrevista completa de 2 anos. |
| `wt_mec_2yr` | Peso amostral para os exames no MEC (Mobile Examination Center) de 2 anos. |
| `wt_mec_lab` | Peso amostral para o componente de flebotomia. |
| `yrs_us` | Tempo (em anos) de residência nos EUA para nascidos no exterior. |
