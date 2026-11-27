# Octane

App para guardar e analisar dados de treino e saúde vindos de relógios Garmin e Amazfit (atividades, sono, frequência cardíaca, HRV), com insights gerados por LLM numa etapa futura. Projeto de Lucas e Miguel, para uso deles e de poucos amigos no início.

## Regras para o Claude

- Responder e escrever em português.
- Não alterar nada (código, arquivos, banco, configuração) sem antes combinar com o Lucas ou o Miguel. Propor primeiro, executar depois do ok.
- Nunca fazer commit nem push. Os commits são feitos por eles.
- Seguir as etapas na ordem combinada e sugerir melhorias que caibam no escopo atual.
- Nunca colocar segredos (chaves do Supabase, da Garmin, da Anthropic) no código ou no Git. Usar `.env` local; o repositório só tem `.env.example`.
- Dados de saúde são sensíveis: cada usuário só acessa os próprios dados.

## Fluxo de trabalho

- Cada tarefa vira uma issue e um branch (`feat/<numero>-<descricao>`), integrado à `main` por pull request revisado pelo outro.
- Commits no padrão Conventional Commits (`feat:`, `fix:`, `docs:`).

## Arquitetura

As decisões ainda estão em discussão. Proposta atual: site em Python com Streamlit, Supabase (Postgres, Storage, Auth), dados da Garmin Personal API e de arquivos FIT, LLM via API do Claude. Não tratar a proposta como decidida até que conste aqui como aceita.

Documento completo da proposta: https://claude.ai/artifact/FBdxWsNEU7JziFFkjUdTeU
