# AIOmetadata Release Visibility

Repositório de especificação, auditoria e evidências do projeto **Release Visibility / region-aware Hide Unreleased Movies** do AIOmetadata.

## Fonte normativa

A especificação normativa vigente deste projeto é o arquivo [PLAN.md](./PLAN.md), atualmente na **V30 NORMATIVE**.

O plano cobre a implementação relacionada à issue upstream **cedya77/aiometadata#742**, incluindo Release Visibility por região, rastreabilidade normativa, migrações e persistência, runtime/settings bootstrap, delivery control plane, multi-arch, lifecycle fatal, evidências e matriz de testes.

## Relação entre repositórios

- **SPEC / governança:** `procopio1000/aiometadata-release-visibility`
- **IMPLEMENTATION / código:** `procopio1000/aiometadata`
- **UPSTREAM:** `cedya77/aiometadata`
- **Issue principal:** `cedya77/aiometadata#742`

O repositório de implementação deve tratar uma revisão/commit específico deste repositório como autoridade normativa. Mudanças no plano devem ser versionadas aqui antes de serem consumidas pela implementação.

## Estrutura

- `PLAN.md` — Plano Mestre V30 NORMATIVE completo.
- `docs/architecture/` — arquitetura e contratos técnicos derivados do plano.
- `docs/decisions/` — ADRs e decisões explícitas.
- `docs/audits/` — auditorias e revisões do plano.
- `evidence/` — EvidenceBundles e provas produzidas pela implementação.
- `test-matrix/` — materialização e rastreabilidade da matriz de testes.

## Regra de autoridade

Quando houver divergência entre notas auxiliares e o `PLAN.md`, prevalece a versão normativa mais recente explicitamente adotada pelo projeto, preservando a rastreabilidade por commit SHA.

Este repositório não substitui o código do AIOmetadata. Ele governa a implementação, revisão, validação e evidência do trabalho realizado no fork de implementação.

## Auditoria vigente

- [Auditoria V29 → V30](./docs/audits/V29-to-V30.md) — revisão que originou a V30 NORMATIVE.
