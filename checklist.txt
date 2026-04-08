# Checklist AV1 - Projeto Big Data

## Status das Etapas do Pipeline (AV1)

### 1) Ingestão
- [x] Em progresso
- [ ] Finalizado
- [ ] Pendente

**Evidências:**
- Coleta via API SPPO no notebook `codigo/ingestao_av1_big_data.ipynb`
- Uso de `requests.get(...)`
- Geração de dados brutos e amostra em `dados/amostra_gps_sppo_bruto.csv`

---

### 2) Armazenamento
- [x] Em progresso
- [ ] Finalizado
- [ ] Pendente

**Evidências:**
- Persistência de dados brutos em CSV
- Persistência da camada tratada (silver) em CSV/Parquet
- Amostra tratada em `dados/sppo_amostra.csv`

---

### 3) Transformação
- [x] Em progresso
- [ ] Finalizado
- [ ] Pendente

**Evidências:**
- Conversão de timestamps para datetime
- Criação de colunas derivadas (data, hora, minuto, dia_semana, latências)
- Limpeza: nulos críticos, coordenadas inválidas, velocidade negativa

---

## Observações para próxima entrega
- [ ] Ajustar caminhos `/content/...` para estrutura local do projeto
- [ ] Criar documento de arquitetura em PDF/DOCX
- [ ] Completar pasta `documentacao` com diagrama e materiais da apresentação


O que está feito

Pipeline básico implementado no notebook codigo/ingestao_av1_big_data.ipynb
Fonte de dados definida e consumida via API (requests.get)
Ingestão de dados brutos funcionando
Transformação aplicada (conversão de timestamps, colunas derivadas, limpeza)



Validações de qualidade básicas (dropna, filtros de coordenada, velocidade)
Saída silver gerada em CSV/Parquet (no caminho /content/silver)
Pasta dados com amostras:
dados/amostra_gps_sppo_bruto.csv
dados/sppo_amostra.csv
README existente (README.txt) com visão geral e instruções


Parcial 
Estrutura do repositório para AV1/AV2 está parcial
existe dados/ e codigo/
não vi documentacao/, notebooks/ e src/ separadas
Carregamento/destino existem, mas com caminho acoplado ao Colab (/content/...)
*Não sei se isso faz alguma diferença mas diverge do que laura pediu no documento dela* 

Não feito
Dashboards/visualizações finais e storytelling de resultados (AV2)
Estrutura completa pedida para AV2 (/documentacao, /notebooks, etc.)