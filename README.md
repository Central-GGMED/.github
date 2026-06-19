# 🏛️ GGMED - Gerência-Geral de Medicamentos | Anvisa

Bem-vindo ao workspace central de desenvolvimento e automação da GGMED. Este espaço é dedicado à construção de soluções tecnológicas para otimizar a análise regulatória, garantir a segurança da informação e acelerar o processamento de dados e fluxos internos da agência.

Nossa arquitetura e ecossistema são construídos com foco rigoroso na **privacidade de dados**, confiabilidade e no processamento seguro de informações institucionais.

---

## 🚀 Ecossistema de Projetos

*   **[Crivo](#)**: Motor avançado de automação e *parsing*. Projetado para a extração estruturada de documentos, utilizando processamento inteligente e expressões regulares para triagem e filtro rápido de informações complexas.
*   **[Automação de Parecer](#)**: Sistema dedicado à geração, estruturação e padronização de pareceres técnicos, reduzindo o tempo de resposta e garantindo a consistência do fluxo de análise.
*   **[Reação de Formulação](#)**: Módulo de acompanhamento, cruzamento e análise de dados técnicos referentes a formulações e componentes.
*   **[GQMED](#)**: Plataforma principal e repositório centralizado de suporte às ferramentas e rotinas operacionais da Gerência.
*   **[GESEF](#)**: Módulo de integração e suporte tecnológico voltado para as demandas específicas da Gerência de Eficácia e Segurança.

---

## 💻 Arquitetura e Stack Tecnológica

O ecossistema de desenvolvimento foi desenhado para operar com máxima segurança, rodando em ambientes locais e isolados sempre que possível:

*   **Banco de Dados:** Stack Full Oracle para a gestão robusta e escalável dos dados transacionais.
*   **Inteligência Artificial e Processamento Offline:** Implementação de LLMs locais via Docker e Open WebUI (Ollama) para análise e extração de dados sem o envio de informações sigilosas para a nuvem.
*   **Infraestrutura e Deploy:** Utilização de contêineres Docker para garantir que todos os desenvolvedores executem instâncias idênticas em suas máquinas, facilitando a manutenção de dependências.
*   **Desenvolvimento:** Padrão de versionamento rigoroso com Git, utilizando VS Code como ambiente padronizado.

---

## 🛡️ Diretrizes de Engenharia e Segurança

A natureza dos dados tratados exige conformidade absoluta e atenção máxima à segurança da informação:

1.  **Isolamento de Dados Sensíveis:** Nenhuma informação real de processo, dados confidenciais ou credenciais (*tokens/senhas*) devem ser expostos em *commits*. Utilize exclusivamente arquivos `.env` locais para variáveis de ambiente.
2.  **Fluxo de Versionamento:** Bloqueio de *commits* diretos na branch `main`. Todo novo desenvolvimento deve ser feito em *branches* isoladas (ex: `feature/novo-parser-crivo`) e integrado via *Pull Request*.
3.  **Ambiente Local:** Antes de iniciar os trabalhos do dia, certifique-se de realizar o *pull* das imagens Docker mais recentes para garantir a compatibilidade do sistema.
4.  **Suporte Técnico:** Em caso de bloqueios de ambiente, falhas de sincronização de containers ou dúvidas sobre arquitetura, abra um *ticket* de suporte interno ou comunique diretamente a equipe de desenvolvimento (Leonardo/Engenharia).
