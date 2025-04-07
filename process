# 📘 Streamlit App – Relatório Gráfico Provimento nº 31/2024 - TJMA
# Autor: MAPEIA PROCESSOS 2

import streamlit as st
from graphviz import Digraph
from PIL import Image

# 📌 CONFIG
st.set_page_config(page_title="Relatório TJMA - COGEX", layout="wide")

# 🎨 CABEÇALHO INSTITUCIONAL
col1, col2 = st.columns([3, 1])
with col1:
    st.markdown("## <span style='color:#000;'>Relatório Gráfico de Fluxo Processual –</span> <span style='color:#800000;'>COGEX</span>", unsafe_allow_html=True)
with col2:
    st.image("https://upload.wikimedia.org/wikipedia/commons/3/38/Logo_TJMA_MA.png", width=120)

st.markdown("---")

# 📄 DADOS DO PROCESSO
st.subheader("🔹 Provimento nº 31/2024 – TJMA")
st.markdown("""
- **Data:** 28 de junho de 2024  
- **Resumo:** Revogação do art. 4º do Prov. nº 07/2021 da CGJ-MA  
- **Fase:** Revisão e Anulação Normativa  
""")

# 📋 ETAPAS DO FLUXO
etapas = [
    "Análise crítica do art. 4º do Prov. 07/2021",
    "Identificação de incompatibilidade normativa",
    "Manifestação da Corregedoria",
    "Redação da proposta de revogação",
    "Consulta ao setor jurídico institucional",
    "Referência cruzada com normas atuais",
    "Revogação formal via Prov. nº 31/2024",
    "Atualização do Código de Normas",
    "Divulgação oficial às serventias"
]

# 📊 GERAR DIAGRAMA COM GRAPHVIZ
dot = Digraph(comment='Fluxo - Provimento nº 31/2024')
dot.attr(rankdir='TB', size='10')

dot.node('INICIO', 'Início', shape='oval', style='filled', fillcolor='lightgreen')
dot.node('FIM', 'Fim', shape='oval', style='filled', fillcolor='lightcoral')

for i, etapa in enumerate(etapas):
    dot.node(f"E{i}", etapa, shape='box', style='filled', fillcolor='lightblue')

dot.edge('INICIO', 'E0')
for i in range(len(etapas) - 1):
    dot.edge(f"E{i}", f"E{i+1}")
dot.edge(f"E{len(etapas) - 1}", 'FIM')

# 📈 VISUALIZAÇÃO
st.subheader("📌 Fluxograma do Processo Normativo")
st.graphviz_chart(dot)

# 🎨 LEGENDA E DESIGN
st.markdown("""
---
### 🎨 Identidade Visual & Diretrizes
- **Cores Oficiais:**  
  - 🟡 Amarelo (RGB: 255, 204, 0)  
  - ⚫ Preto (RGB: 0, 0, 0)  
  - 🍷 Vinho (RGB: 128, 0, 32)
- **Logotipo:** Exibido no topo direito  
- **Fonte:** Segoe UI ou equivalente

---

### 📌 Estrutura Descritiva do Relatório

O relatório apresenta a estrutura gráfica e descritiva do fluxo processual da COGEX, utilizando dados oficiais extraídos do sistema de gestão integrado.

**Blocos:**
1. **Origem dos Dados:** Coleta automatizada via Google Workspace.
2. **Explicação do Fluxo Processual:** Gargalos, tempos médios e performance.
3. **Aplicação Prática:** KPIs, metas, melhorias recomendadas.

""")

# RODAPÉ
st.markdown("---")
st.markdown("© 2024 COGEX - Corregedoria Geral da Justiça do Maranhão", unsafe_allow_html=True)
