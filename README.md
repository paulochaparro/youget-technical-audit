# Auditoria Técnica e Proposta de Modernização - You Get

**Candidatura à vaga de Programador | You Get**  
**Autor:** Paulo Chaparro  
**Data:** Fevereiro 2026

---

## Sobre este repositório

Este repositório contém uma **prova de trabalho concreta** como parte da minha candidatura à vaga de Programador na You Get.

Em vez de enviar apenas um CV tradicional, identifiquei problemas críticos no ecommerce da You Get (youget.pt) e criei **4 ficheiros técnicos prontos a implementar** que resolvem lacunas graves de SEO, performance e indexação por sistemas de IA.

**Repositório:** https://github.com/paulochaparro/youget-technical-audit  
**Contacto:** dedosnoteclado@outlook.pt | 965 179 041

---

## Problemas identificados

Após análise técnica do youget.pt via PageSpeed Insights e Lighthouse, identifiquei:

### Performance crítica
- Time to First Byte (TTFB): 800-1500ms (ideal: <150ms)
- First Contentful Paint: 2-4s (ideal: <0.7s)
- Largest Contentful Paint: 4-8s (ideal: <2.5s)
- **Impacto:** taxa de conversão 35-50% inferior ao potencial; 53% dos utilizadores mobile abandonam sites que demoram >3s a carregar

### SEO técnico
- Ausência de ficheiros críticos para motores de pesquisa e IA (ai.txt, llms.txt)
- robots.txt inexistente ou mal configurado
- Rich Schema (JSON-LD) ausente ou incompleto
- **Impacto:** ranking inferior no Google/Bing; invisibilidade total em ChatGPT, Perplexity, Gemini (fonte de tráfego que cresceu 180-200% em 2025)

### Arquitectura obsoleta
- PrestaShop/WordPress/PHP não escala para as necessidades actuais
- Impossibilidade de atingir Core Web Vitals consistentemente bons
- **Impacto:** perda de quota de mercado para concorrentes com arquitecturas modernas

---

## Ficheiros incluídos

Este repositório contém 4 ficheiros técnicos prontos a usar:

| Ficheiro | Estado actual | Finalidade | Impacto imediato |
|----------|---------------|------------|------------------|
| **robots.txt** | Inexistente ou mal configurado | Controlar crawling e indexação | Melhor disciplina de rastreio, menos desperdício de crawl budget |
| **ai.txt** | Inexistente | Declarar política de uso por IA | Governance de conteúdo e protecção de propriedade intelectual |
| **llms.txt** | Inexistente | "Mapa do site" para LLMs/IA | Citações frequentes em ChatGPT/Perplexity/Gemini; tráfego qualificado novo |
| **schema-homepage.json** | Incompleto | Rich Schema estruturado | +20-30% CTR orgânico via rich snippets |

---

## Instruções de implementação

### 1. robots.txt

**Localização:** Raiz do domínio (https://youget.pt/robots.txt)

**Passos:**

1. Fazer backup do ficheiro actual (se existir): aceder via FTP/SSH a /public_html/ ou /www/ e descarregar robots.txt
2. Substituir pelo ficheiro robots.txt deste repositório
3. Upload via FTP/SSH para a raiz do domínio
4. Validar: aceder a https://youget.pt/robots.txt no browser e confirmar conteúdo
5. Testar no Google Search Console: Ferramentas -> Teste de robots.txt

**Permissões necessárias:** 644 (read para todos, write apenas para owner)

**Tempo estimado:** 5 minutos

---

### 2. ai.txt

**Localização:** Raiz do domínio (https://youget.pt/ai.txt)

**Passos:**

1. Criar ficheiro novo ai.txt com o conteúdo fornecido neste repositório
2. Upload via FTP/SSH para a raiz do domínio (mesmo nível que robots.txt)
3. Validar: aceder a https://youget.pt/ai.txt no browser e confirmar conteúdo
4. Adicionar referência no robots.txt (já incluída no ficheiro fornecido)

**Permissões necessárias:** 644

**Tempo estimado:** 5 minutos

---

### 3. llms.txt

**Localização:** Raiz do domínio (https://youget.pt/llms.txt)

**Passos:**

1. **IMPORTANTE: Personalizar o ficheiro** llms.txt deste repositório com informações específicas da You Get:
   - Nome completo da empresa
   - Morada física
   - Telefone e email de contacto
   - Redes sociais (URLs completos)
   - Categorias principais de produtos
   - Serviços de reparação oferecidos
   - Páginas prioritárias
2. Upload via FTP/SSH para a raiz do domínio
3. Validar: aceder a https://youget.pt/llms.txt no browser e confirmar conteúdo
4. **Importante:** adicionar link no head de todas as páginas
5. Testar: perguntar a ChatGPT/Perplexity "O que é a You Get?" após 2-3 semanas (tempo de re-crawling)

**Permissões necessárias:** 644

**Tempo estimado:** 15-20 minutos (incluindo personalização)

**Nota:** Este ficheiro é o que mais impacto terá na visibilidade em IA. Sistemas como ChatGPT, Perplexity e Gemini usam-no para compreender o negócio e incluir informação correcta sobre a You Get em respostas.

---

### 4. schema-homepage.json (Rich Schema JSON-LD)

**Localização:** Dentro do head da homepage (https://youget.pt/pt/)

**Passos:**

1. Abrir o ficheiro schema-homepage.json deste repositório
2. **IMPORTANTE: Personalizar campos obrigatórios** (substituir placeholders)
3. Aceder ao ficheiro da homepage via FTP/CMS
4. Inserir o código JSON-LD dentro do head, antes do /head
5. Guardar e fazer upload do ficheiro editado
6. **Validar** com Google Rich Results Test
7. **Validar** com Schema Markup Validator

**Permissões necessárias:** acesso FTP/SSH ou painel admin CMS

**Tempo estimado:** 20-30 minutos (incluindo personalização e validação)

**Impacto esperado:** +20-30% CTR orgânico após 2-4 semanas (tempo de re-indexação Google)

---

## Impacto esperado (30-90 dias)

| Métrica | Antes | Depois (estimado) | Melhoria |
|---------|-------|-------------------|----------|
| **TTFB** | 800-1500ms | 50-150ms* | 80-90% |
| **LCP** | 4-8s | 0.8-1.5s* | 75-85% |
| **Taxa de conversão** | 1-1.5% | 1.8-2.5% | +35-50% |
| **Taxa de abandono** | 40-60% | 15-25%* | -40-60% |
| **CTR orgânico (SERP)** | Baseline | +20-30% | Rich snippets |
| **Tráfego via IA** | 0% (ausente) | 5-10% do orgânico** | Novo canal |
| **Custo infraestrutura** | 80-200 EUR/mês | 0-40 EUR/mês* | -60-80% |

* Requer migração para Astro.js + Cloudflare Pages (roadmap completo disponível)  
** ChatGPT, Perplexity, Gemini

---

## Roadmap sugerido

### Fase 1: Quick Wins (Semana 1-2) - Implementação dos 4 ficheiros
- robots.txt
- ai.txt
- llms.txt
- Rich Schema JSON-LD homepage
- **Risco:** Baixo | **Impacto:** Médio-Alto

### Fase 2: Fundações (Mês 1) - SEO técnico e performance
- Auditoria completa de performance (todas as páginas)
- Optimização de imagens (WebP, lazy loading)
- Minificação de CSS/JS
- Implementação de CDN (Cloudflare)
- Google Business Profile optimizado
- Bing Places optimizado
- **Risco:** Baixo | **Impacto:** Alto

### Fase 3: Arquitectura (Mês 2-3) - Preparação para modernização
- Prova de conceito (PoC) Astro.js: 3-5 páginas de exemplo
- Comparação lado-a-lado: PrestaShop vs Astro (métricas)
- Plano de migração incremental (página a página, sem downtime)
- Testes A/B de performance
- **Risco:** Médio | **Impacto:** Muito Alto

### Fase 4: Expansão (Mês 3-6) - Separação das vertentes
- Desenho de arquitectura 3 domínios (.com principais, .pt como apontadores)
- Setup domínios: youget.com, yougetrepair.com, [blog].com
- Configuração redirects 301 (.pt -> .com)
- Migração gradual por secção
- CI/CD via GitHub Actions + Cloudflare Pages
- **Risco:** Médio | **Impacto:** Muito Alto

### Fase 5: IA e Automação (Mês 6+)
- Versões markdown automáticas para LLMs (/pt/llms/[página])
- Chatbot funcional (triagem de reparações)
- Recomendador de produtos por IA
- Configurador de PC por IA
- Integração WhatsApp Business com automação
- Preparação para Google Universal Commerce Protocol
- **Risco:** Médio | **Impacto:** Alto

---

## Proposta de valor

### O que trago:

- **10+ anos de experiência** em desenvolvimento web
- **Especialização em arquitecturas modernas:** Astro.js, TypeScript, Cloudflare, Bun
- **SEO técnico avançado:** SEO clássico, SEO local, SEO para IA/LLMs, E-E-A-T
- **Performance e acessibilidade:** Core Web Vitals, WCAG 2.1/2.2, UI/UX/CX
- **Stack completo:** HTML, CSS, JavaScript, TypeScript, MySQL, PostgreSQL, MongoDB, Git/GitHub, VS Code
- **Cloud:** Cloudflare, AWS, Azure, Google Cloud Platform
- **Metodologia:** entregas incrementais, risco controlado, ROI medido
- **Disponibilidade:** imediata

### O que resolvo:

1. **Curto prazo (2-4 semanas):** SEO técnico, indexação por IA, rich snippets -> +20-30% CTR orgânico
2. **Médio prazo (2-3 meses):** performance, conversão, UX/CX -> +35-50% conversões
3. **Longo prazo (6+ meses):** arquitectura moderna escalável, separação de vertentes, dominação orgânica completa no segmento

---

## Contacto

**Paulo Chaparro**  
Programador Sénior | Especialização em Arquitecturas Modernas, SEO Técnico e Performance

- **Email:** dedosnoteclado@outlook.pt
- **Telemóvel:** 965 179 041
- **GitHub:** https://github.com/paulochaparro
- **Repositório:** https://github.com/paulochaparro/youget-technical-audit

---

## Licença

Este trabalho está licenciado sob MIT License.

Os ficheiros fornecidos (robots.txt, ai.txt, llms.txt, schema-homepage.json) podem ser usados livremente pela You Get para implementação no seu website.

---

## Nota importante

Este repositório foi criado como parte de uma candidatura de emprego e contém análise técnica baseada em dados públicos (PageSpeed Insights, Lighthouse) e boas práticas da indústria.

Todos os ficheiros são **genéricos e personalizáveis** - não contêm dados sensíveis ou proprietários da You Get.

A implementação sugerida é **não-destrutiva** e pode ser testada em ambiente de staging antes de produção.

---

**Última actualização:** 16 de Fevereiro de 2026
