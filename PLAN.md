# Plano mestre V29 FINAL — auditoria extrema / Release Visibility + Full Process Resource, Dependency-I/O, Config-Generation, Persistent-Artifact, Runtime-Settings Bootstrap, Cross-Store Migration, Durability-Convergence, Deployment-Entrypoint, Delivery-Control-Plane, Multi-Arch & Fatal-Lifecycle Closure completo do AIOmetadata

**Issue principal:** #742 — Add region-specific support to “Hide Unreleased Movies”  
**Repositório:** `cedya77/aiometadata`  
**Base histórica do V3:** `dev@7ef886c6c4bb3a5d665411051637aa375edeba37`  
**Base do V6 originalmente auditada:** `dev@26523cf4e0be9a0b0fd513b4ec8530d346e87e18`  
**Base V8 reaprovada:** `dev@6b9cd26375faa0f0f1a75b54b6352ade36d56fb7`  
**HEAD re-auditada da V28:** `dev@d270a3a7f3b6e41304d9f91045b1d481311c3c96`
**Tree SHA da V28:** `b4db5931c47035862fac075ac01ec02fe1e621c0`
**Release publicada de base:** `v3.1.0` em `6e83e22ab9de5093f9918a1871157f401feebb03`; o HEAD V28 está `1 commit` à frente da release publicada
**Delta de código V8 → snapshot V28:** `5 commits`, `20 paths alterados` (`19 modificados`, `1 adicionado`, `0 removidos`)
**Delta desde a base do V6:** `8 commits`
**Árvore auditada na V28:** `584 entradas`
**Arquivos/blob:** `545`
**Diretórios:** `39`
**Issue #742:** aberta, sem comentários no snapshot revalidado em 2026-09-25
**Data desta reauditoria V28:** `2026-09-25`
**Regra de snapshot:** qualquer mudança de `dev` após `d270a3a7f3b6e41304d9f91045b1d481311c3c96` exige rerun integral do Rebase Gate + Delta File Gate + Occurrence Gate + Caller-Closure Gate + Evidence Ingress Gate + Retry Closure Gate + TMDB Direct-Network/Control-Plane Gate + Movie Identity/Mapping-Provenance Gate + Stability-Domain Gate + Fleet-Admission Gate + Setup-Orchestration Closure Gate + Template-Policy Closure Gate + Region-Domain Closure Gate + Edit-Save Idempotence Gate + Effective-TMDB-Discover-Source-Context Gate + Post-Signature-Mutation Gate + Hidden-Dependency Gate + Local-Membership-Projection Gate + TMDB-Discover-Preview-Parity Gate + Direct-Discover-Caller Gate + Template-Temporal-Semantics Gate + Request-Config-Snapshot Gate + In-Process-Route-Parity Gate + Abort-Propagation Gate + Jellyfin-Failure-State Gate + Response-Freshness Gate + Conditional-HTTP Gate + Operation-Context-Carrier Gate + Shared-Flight-Cancellation Gate + Abort-Error-Cache Gate + Detached-Work Gate + Shared-Admission-Accounting Gate + HTTP-Disconnect-Signal Gate + Runtime-Semantics Gate + Promise-Race-Loser-Lifecycle Gate + Shared-Flight-Rejoin Gate + Refresh-Lease-Ownership/Fencing Gate + Shutdown-Drain-Ordering Gate + Scheduler-Quiescence Gate + Cancellation-Commit-Authority Gate + Response-Finalization-Telemetry Gate + Async-Occurrence-Ledger Gate + Background-Work-Registry Gate + Shared-HTTP-Transport-Cancellation Gate + Startup-Loser-Ownership Gate + Detached-Startup-Maintenance Gate + Scheduler-Disposer-Closure Gate + Upgraded-Socket-Shutdown Gate + Deferred-Flush-Closure Gate + Config-Save-Background-Work Gate + Bespoke-Retry-Sleep-Closure Gate + Poster-Upstream-Disposal Gate + Snapshot-Occurrence-Manifest Gate + Resource-Occurrence-Manifest Gate + Direct-Network-Caller-Closure Gate + Outbound-Dispatcher-Lifecycle Gate + Signal-Composition Gate + Transport-Drain-Close Gate + Process-Resource Closure Gate + Persistent-Storage Resource Gate + Local-Stream/File-Handle Gate + Dependency-I/O Capability Gate + Lifecycle-Dependency-Fingerprint Gate + Config-Generation/Replica-Fencing Gate + Scanner-Reachability/Dynamic-Boundary Gate + Frontend-Effect Closure Gate + Persistent-Artifact Occurrence Gate + Durable-Artifact Atomicity/Recovery Gate + IMDb-Ratings Snapshot/Lifecycle Gate + Stream-Constructor/Readline Gate + Persistent-Artifact Multi-Process Gate + Runtime-Setting Occurrence Gate + Settings-Bootstrap Ordering Gate + Legacy-Ratings Cross-Store Migration Gate + Mixed-Version Ratings Fleet Gate + Ratings-Readiness Truthfulness Gate + Artifact-Residency/Filesystem-Capability Gate + Snapshot Pre-Read Allocation Gate + IMDb Dataset-Schema Gate + Scheduler-Numeric-Bounds Gate + Legacy-Ratings Coherent-Snapshot Gate + Ratings-Durability-Convergence Gate + HTTP-Validator/Fetch-Authority Gate + Runtime-Entrypoint/Emitted-Bootstrap-Parity Gate + Deployment-Readiness/Traffic-Admission Gate + Replica-Scope Observability/Control-Plane Gate + Normative-Authority/Traceability Gate; mudança de `express`/`fresh`/`etag` no dependency lock também exige rerun do Conditional-HTTP Gate; mudança de `undici`, `axios`, `fetch-socks`, `kitsu`, `@fanart-tv/api`, `name-to-imdb`, `ioredis`, `pg`, `better-sqlite3`, `Dockerfile`, `.nvmrc`, `engines.node`, `@types/node`, Node runtime patch/minor efetivo ou workflows que selecionam Node exige rerun do Lifecycle-Dependency-Fingerprint Gate e dos Runtime-Semantics/Abort/Transport/Process-Resource/Storage/Dependency-I-O gates afetados antes de implementação/merge.
**Objetivo:** cobrir todos os caminhos localizados que produzem, hidratam, armazenam, cacheiam, paginam, filtram ou apresentam `movie/series` em catálogos e buscas quando o comportamento depende de conteúdo ainda não lançado, preservando compatibilidade e impedindo que decisões específicas de usuário, região, relógio, conta ou estado dinâmico contaminem caches compartilhados.

**Escopo da afirmação de cobertura:** esta V28 fornece **cobertura estática rastreável do snapshot acima**, preserva toda a trilha V8→V27 e acrescenta a camada normativa V28 para fechar coerência do import legado Redis sob writer antigo, convergência memória→durável após persist failure, paridade source→build/entrypoint, liveness/readiness→traffic admission, escopo por réplica de observabilidade/control-plane e autoridade normativa/traceabilidade do próprio plano. A claim passa a exigir reconciliação de **sete universos** — async occurrences, process-resource occurrences, network-caller occurrences, frontend-effect occurrences, persistent-artifact occurrences, runtime-setting occurrences e runtime-entrypoint/deployment occurrences — além de todos os gates funcionais acumulados. Tudo que exige runtime/upstream/dependency/distribuição permanece transformado em gate executável; não há promessa de infalibilidade externa nem de testes futuros não executados.

> **Regra de precedência da V28:** as seções 1–584 preservam a arquitetura/trilha acumulada V8→V27; as seções 585+ são a camada normativa mais recente. Em conflito sobre coerência de import Redis durante mixed-version writer, memória-versus-durabilidade, ETag/validator versus persistência local, source→emitted bootstrap/entrypoint, liveness/readiness versus traffic admission, escopo por réplica de markers/control-plane ou autoridade normativa/traceabilidade do documento, **a redação V28 prevalece**. Nos domínios V27 de settings bootstrap, cross-store migration/readiness/storage/schema e nos domínios V26 de artifacts/lifecycle, a redação anterior continua normativa onde não for explicitamente refinada pela V28. O `NormativeAuthorityIndex` da seção 594 passa a ser a autoridade mecânica para resolver qualquer conflito remanescente entre camadas históricas.

---

> **Regra de precedência da V29:** as seções 1–601 preservam integralmente a arquitetura, evidência e decisões acumuladas V8→V28; as seções **602+** são a camada normativa mais recente para delivery control plane, merge/release admission, multi-architecture publication, byte-order do snapshot, readiness withdrawal, external termination grace, fatal process errors e bootstrap authority seed. Em conflito nesses domínios, **V29 prevalece**. O `BootstrapAuthoritySeedV29` da seção 613 inicializa o generator; depois de gerado e validado, o `NormativeAuthorityIndex` detalhado continua sendo a autoridade mecânica de resolução de precedência.

**Reauditoria V29:** 2026-09-25 — `dev` continua em `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree `b4db5931c47035862fac075ac01ec02fe1e621c0`; #742 continua aberta e sem comentários no snapshot revalidado. A V29 acrescenta um **oitavo universo**, `DeliveryControlPlaneOccurrenceManifest`, e eleva a matriz normativa para **850+ casos**.

**Regra adicional de snapshot V29:** mudança em `.github/workflows/**`, repository rulesets/branch protection efetivos, Actions/runner identities resolvidas, release/tag publication policy, OCI build platforms, Docker base digest, shutdown/readiness/fatal handlers ou binary snapshot format exige rerun dos gates V29 afetados. Mudança externa do control plane pode invalidar evidence mesmo sem novo Git commit.

---

# 1. Resultado final da auditoria

> **Atualização normativa V29:** a reauditoria manteve o mesmo HEAD/tree da V28 e não encontrou novo source drift, mas encontrou sete boundaries que a claim V28 ainda não congelava: **(1)** CI definido em YAML não prova que o status é required para merge; **(2)** merge/release control-plane pode mudar fora do Git tree; **(3)** a evidence exigida para o merge HEAD precisa de trigger/admission explícito para o SHA realmente mesclado e publicado; **(4)** Actions, `ubuntu-latest` e base images são dependências móveis; **(5)** o projeto publica amd64+arm64, enquanto o snapshot binário não declara byte order; **(6)** shutdown precisa retirar readiness/fleet eligibility antes de drenar e caber no termination grace externo; **(7)** `unhandledRejection` atualmente é log-and-continue, incompatível com fail-stop após erro assíncrono global. As seções 602+ criam o oitavo universo `DeliveryControlPlaneOccurrenceManifest`, fecham o bootstrap paradox do AuthorityIndex e acrescentam os casos 801–850.

> **Atualização normativa V28:** o snapshot foi revalidado novamente em 2026-09-25 e `dev` continua exatamente em `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree `b4db5931c47035862fac075ac01ec02fe1e621c0`; a #742 continua aberta e sem comentários. A V27 fechou corretamente hydration, cross-store migration, readiness e storage semantics, mas a reauditoria adversarial encontrou boundaries adicionais: **(1)** o writer v3.1.0 substitui `imdb:ratings` por `RENAME` e grava o ETag em operação separada, enquanto uma migração por múltiplos `HSCAN` não possui snapshot isolation sob writer legado vivo; **(2)** `memoryUpdated=true` + `persisted=false` pode deixar uma geração apenas em memória e um futuro ETag-match pode pular o download sem quitar a dívida de persistência; **(3)** a prova de bootstrap precisa alcançar o JavaScript CommonJS emitido e todos os entrypoints reais (`dist/server/server.js`, TS/dev e container), não só o grafo fonte; **(4)** `/health/live` e `/health/ready` possuem papéis distintos e o deployment precisa provar que traffic admission consome readiness, não apenas liveness; **(5)** snapshot instance-local e markers/control-plane compartilhados precisam de escopo por réplica; **(6)** HEAD é otimização de validator, não pode virar dependência de disponibilidade nem mascarar durability debt; e **(7)** um plano cumulativo deste tamanho precisa de authority index + requirement traceability gerados para impedir implementação de texto histórico superseded. As seções 585+ criam o sétimo universo `RuntimeEntrypointOccurrenceManifest` e acrescentam os casos 751–800.

> **Atualização normativa V27:** o snapshot da V26 foi revalidado e continua exatamente em `d270a3a7f3b6e41304d9f91045b1d481311c3c96`; portanto não há novo code drift. A reauditoria encontrou, porém, três classes que a claim V26 ainda não fechava: **(1)** migração cross-store/rolling fleet do storage IMDb antigo em Redis para o novo snapshot local, incluindo cache-clear e rollback; **(2)** bootstrap de settings DB-backed antes de consumidores que congelam `process.env` em module load; e **(3)** truthfulness de readiness quando não existe snapshot/legacy fallback e o primeiro download falha. A camada V27 ainda torna pre-read o `MAX_SNAPSHOT_BYTES`, valida o schema/header TSV, formaliza storage backing do `addon/data` e fecha parser/bounds dos scheduler delays. As seções 569+ criam `RuntimeSettingOccurrenceManifest`, elevam a reconciliação para **seis universos** e acrescentam os casos 701–750.

> **Atualização normativa V26:** `dev` avançou um commit após o snapshot V25, para `d270a3a7f3b6e41304d9f91045b1d481311c3c96` (`Feat/imdb ratings memory (#749)`). O delta modifica `addon/lib/dashboardApi.js`, `addon/lib/imdbRatingProjection.ts`, `addon/lib/imdbRatings.ts` e adiciona `addon/lib/imdbRatingsTable.ts`. A #742 continua aberta e sem comentários. O novo código move ratings de um hash Redis para uma tabela em memória com snapshot `addon/data/imdb-ratings.bin`, introduz `fs.readFile/writeFile/rename`, `retryTimer`, refresh de startup detached, `stream.pipeline`, `readline.createInterface` e limpeza Redis detached. A reauditoria também confirmou que a V25 classificava handles/streams, porém não reconciliava sistematicamente **artefatos persistentes gerados por operações one-shot**; esse blind spot já existia em cache migration flags, mapper caches, wiki caches, poster warm summary e heap diagnostics. As seções 548+ criam `PersistentArtifactOccurrenceManifest`, fecham o delta atual e elevam a matriz acumulada para **700+ casos**.
> **Atualização normativa V25:** a reauditoria integral da V24 foi executada contra o mesmo HEAD/tree e confirmou que a arquitetura funcional da #742 permanece válida. A prova V24, porém, ainda estreitava `ResourceOccurrence` a transports de rede: o snapshot possui Redis, Pools PostgreSQL (inclusive read replica opcional), SQLite operacional/cold-store, HTTP listener e streams/file handles locais; também há I/O encapsulado em `kitsu`, `@fanart-tv/api` e `name-to-imdb` que um scanner de `fetch`/Axios/undici não descobre sozinho. A auditoria encontrou ainda um race correctness-critical em configuração: `configCache.getOrLoad()` pode publicar um load antigo depois de um save novo, e `DATABASE_READ_URI` pode ampliar esse risco por replica lag; `configVersion = Date.now()` não é fencing token monotônico. As seções 531+ criam Process Resource + Dependency Capability + Frontend Effect manifests, lifecycle lockfile fingerprint e Config Revision/Replica-Fencing, elevando a matriz acumulada para **650+ casos**.

> **Atualização normativa V24:** a reauditoria do mesmo HEAD confirmou que `dev` continua em `6e83e22ab9de5093f9918a1871157f401feebb03`. A arquitetura funcional da #742 permanece válida, mas a prova V23 de lifecycle ainda tinha um blind spot: o scanner autoritativo inventariava trabalho assíncrono, não recursos process-lifetime nem todo caller de rede direto. O snapshot cria múltiplos `undici.Agent`/`ProxyAgent`, `fetch-socks` dispatchers e um global dispatcher fora do poster cache; Gemini/OpenRouter possuem `closeAgent()` sem caller; e o `httpClient` pode instalar `new ProxyAgent(...)` global sem reter o handle. As seções 514+ criam Resource/Network Occurrence Manifests, fecham todos esses transports, completam a reconciliação dos 17 arquivos backend com `.unref()` e elevam a matriz acumulada para **600+ casos**.
> **Atualização normativa V23:** a reauditoria do mesmo HEAD/tree confirmou que `dev` continua exatamente em `6e83e22ab9de5093f9918a1871157f401feebb03`, portanto não houve drift de snapshot. A arquitetura funcional da #742 permanece válida, mas a prova V22 de async closure ainda era incompleta: dos 46 arquivos backend com `setTimeout`, nove caminhos nem apareciam no documento; `addon/lib/metaColdStore/store.ts` possui flush diferido por `setImmediate`; `addon/lib/posterCache/store.ts` possui eviction diferida; `addon/lib/posterCache/upstream.ts` mantém agents e destroy timers; `addon/lib/jellyfin/ids.ts` possui write-behind de DB sem caller de shutdown; e há trabalhos detached em config save, recommendations, Jellyfin SWR/cache writes e startup maintenance. Além disso, retries/backoffs bespoke em AniList/TVDB/TVMaze/AniListTracker e o `sleep()` compartilhado continuam não canceláveis apesar do contrato abstrato V19/V22. As seções 499+ materializam esses paths, transformam o Async-Occurrence Ledger em manifest verificável e elevam a matriz acumulada para 560+ casos.

> **Atualização normativa V22:** a reauditoria do mesmo snapshot confirmou a arquitetura V21, mas encontrou um gap objetivo na própria prova de closure: o documento exigia classificação global de `Promise.race`/timers/schedulers sem materializar o ledger completo. O snapshot contém 14 arquivos backend com `Promise.race`, 19 com `setInterval` e 46 com `setTimeout`; parte relevante não estava no mapa V21. Também ficaram fora do mandatory map o transport compartilhado `addon/utils/httpClient.ts`/`addon/utils/retry.ts`, startup maintenance detached, schedulers de recommendations/playstate/cache-cleanup/MovieLens/mappers/ratings/wiki/poster e sockets Jellyfin atualizados. As seções 483+ fecham esses paths com Async-Occurrence Ledger, BackgroundWorkRegistry, transport/retry cancellation, startup-loser ownership, disposer contracts e upgraded-socket drain, elevando a matriz acumulada para 520+ casos.

> **Atualização normativa V21:** a nova reauditoria do mesmo snapshot confirmou que a V20 fechava corretamente conditional HTTP, context carrier e ownership básico de shared work, mas ainda deixava implícitos boundaries de término capazes de quebrar a implementação: a origem do `AbortSignal` HTTP não estava definida e `req.close` é semanticamente perigoso em Node moderno; o runtime permitido (`>=24.0.0 <25`) não congela a semântica de `IncomingMessage.signal`; `Promise.race()` ainda podia abandonar trabalho side-effecting; um shared flight cancelado pelo último waiter podia aceitar um waiter novo antes de assentar; `cacheRefreshAhead` usa deadline igual ao TTL do lock, sem owner token/fencing; o shutdown atual possui apenas fases `traffic/resource`, com timeout que não cancela o closer e warmers/schedulers sem quiescência comum; e `requestTracker.js` observa `res.statusCode` antes de `res.send()` poder converter a resposta em `304`. As seções 469+ fecham esses paths, elevando a matriz acumulada para 465+ casos e prevalecendo sobre V8→V20 nesses boundaries.

> **Atualização normativa V20:** a reauditoria do mesmo snapshot e do dependency lock confirmou que a V19 fechava os conceitos de response freshness e abort, mas ainda deixava implícitos quatro detalhes capazes de quebrar a implementação: Express 5.2.1 gera weak ETag automaticamente e executa `req.fresh`/304 dentro de `res.send()`, `Last-Modified` atual representa apenas `configVersion`, o lifecycle de um waiter abortado não é o mesmo lifecycle do shared `singleFlight`, e um `AbortError` pode cair no generic error-cache como falha compartilhável. As seções 456+ fecham conditional HTTP real, context carrier, shared-work cancellation, abort/error-cache poisoning, detached refresh e admission accounting, elevando a matriz acumulada para 420+ casos. Elas prevalecem sobre V8→V19 nesses boundaries.

> **Atualização normativa V19:** a reauditoria do mesmo snapshot confirmou que a V18 fechava o domínio TMDB/Discover, mas ainda não transformava em gates explícitos cinco boundaries de execução: snapshot único da configuração por operação, scratch state fora da config, paridade do caminho Jellyfin in-process que executa sem middleware/fila, cancelamento real do trabalho após timeout e validade temporal de negative/backoff/response state. As seções 443+ fecham esses paths e prevalecem sobre os veredictos históricos V8→V18.

> **Atualização normativa V18:** a reauditoria final do mesmo snapshot encontrou gaps concretos que a V17 ainda não nomeava: o TMDB Discover de séries remove `with_runtime.gte/lte` do request e reaplica a restrição localmente via `tvInfo()`, o endpoint `/api/tmdb/discover/preview` executa um pipeline diferente do catálogo real e o preview temporal pode usar o relógio/fuso do navegador enquanto o catálogo persistido usa tokens dinâmicos resolvidos no backend. A camada V18, nas seções 424+, fecha esses caminhos e prevalece sobre os veredictos históricos V8→V17.

O V8 já estava arquiteturalmente muito avançado, mas a reauditoria V9 encontrou **drift real**:
`dev` avançou 4 commits até `6e83e22ab9de5093f9918a1871157f401feebb03` (release 3.1.0).
O delta foi classificado integralmente e não implementa a #742, porém altera `watch_state`,
watchlist/dropped e persistência Jellyfin, exigindo refinamento da identidade dinâmica. Além
disso, a nova leitura do código encontrou gaps de assinatura, race de raw write e paginação
que não estavam explicitados com força suficiente no V8.

Os blockers cumulativos V8 + V9 são:

```text
A. search filtrada ainda podia devolver página curta/vazia sem caminhar páginas seguintes;
B. cursor validity considerava tempo, mas não toda a freshness que pode mudar membership;
C. cursor não versionava explicitamente o contrato de paginação/page size/CACHE_EPOCH;
D. sourceMembershipSignature ainda precisava ser a mesma identidade usada pelo page cache;
E. TMDB Collection hideUnreleased/sortDirection podiam mudar source output sem identidade
   canônica única no cache/paginação;
F. refresh-ahead/source page replacement podia mudar o snapshot antes do cursor expirar;
G. _releaseAvailability vive hoje em basic do meta hash, exigindo contrato explícito com
   metaHashStore.ts para TTL independente;
H. stale-negative revalidation precisava de primitive de bypass/refetch realmente atômico
   em relação a reads normais, não apenas uma intenção arquitetural;
I. EffectiveSearchSourceContext precisava virar a única autoridade para cache, execução,
   paginação, logs e métricas — incluindo Simkl disabled/V2 e Lumiere unavailable;
J. request clock precisava ser capturado uma única vez por request para evitar midnight races;
K. Worldwide evaluator precisava materializar também a transição automática de 365 dias;
L. filtros watched dinâmicos podiam mudar membership sem invalidar cursor;
M. occurrence gate encontrou arquivos auxiliares que precisavam de classificação A/B/C/D;
N. o repositório não possui test runner/script de testes, embora o DoD exija golden-master,
   integration, migration e concurrency tests;
O. cache autenticado Simkl detail precisa provar account-invariance ou ser scoped;
P. o endpoint de referência TMDB para países já existe e deve ser reutilizado, evitando
   infraestrutura duplicada;
Q. o snapshot V8 sofreu drift de 4 commits até `6e83e22`; o delta inclui watch_state,
   watchlist/dropped e Jellyfin auth e precisa ser classificado antes de qualquer alegação V9;
R. `discoverSig` usa MD5 truncado a 8 hex e `hashConfig()` usa MD5 truncado a 10 hex;
   nenhum deles pode ser a única identidade correctness-critical de source/filter/paging;
S. `fillFilteredPage()` distingue upstream exhaustion de maxPages apenas internamente, mas
   `fillOnce()` não persiste progresso quando zero metas sobrevivem; budget exhaustion pode
   produzir página vazia sem cursor de progresso;
T. dedupe precisa ocorrer antes do accounting de `served`/cursor e possuir contrato estável
   entre páginas; consumir duplicatas upstream e só removê-las depois desalinha skip/cursor;
U. refetch/plain-read usam flights distintos, porém o write final é `SET` incondicional;
   respostas concorrentes/out-of-order ou replicas diferentes podem sobrescrever facts mais novos;
V. `sourceFetchedAt` precisa ser campo factual obrigatório do raw envelope/evidence; `observedAt`
   ou tempo de normalização não podem servir como freshness authority;
W. o novo `watch_state` da v3.1.0 exige separar dynamic **source state** de dynamic **filter state**;
   watchlist/dropped de Jellyfin não devem ser indevidamente hasheados como watched-filter;
X. o plano precisa de rollout/rollback explícito para namespaces de cache/cursor/search, para
   impedir que rollback de aplicação interprete artefatos V9 com semântica V8;
Y. `CalendarDate`/`nextLocalMidnight` precisam de testes DST/offsets não inteiros; nunca somar
   24h para encontrar a próxima meia-noite local;
Z. correctness-critical signatures precisam de digest versionado com resistência prática a
   colisão (SHA-256, >=128 bits efetivos), mantendo hashes curtos atuais apenas como legado/UI/debug.
AA. checkpoint zero-visible em served=0 precisa ser consultado antes do fast-path skip===0;
AB. filtered cursor miss não pode cair em legacyPage guess;
AC. cross-page dedupe exige membership exata ou policy response-only explícita;
AD. cursor offset precisa de coordinate system inequívoco (raw vs transformed);
AE. cursor write precisa detectar conflito cross-replica, não last-write-wins silencioso;
AF. page-set stability deve substituir promessa de snapshot global não fornecida pelo upstream;
AG. raw envelope novo precisa de namespace versionado rollback-safe;
AH. raw retention TTL e consumer freshness SLA precisam ser separados;
AI. fetchGeneration storage-monotonic, não sourceFetchedAt, deve ordenar raw writes;
AJ. qualquer stale evidence que produziria HIDE precisa revalidation ou UNKNOWN/SHOW;
AK. account scope nunca usa hash simples de token/secret;
AL. rollout exige kill switch + homogeneous-fleet gate;
AM. rollback precisa provar forward compatibility de config V10 no baseline pre-V10 (`v3.1.0`);
AN. countries UI failure não pode apagar releaseRegion persistido;
AO. catalogSharing/export/import precisa provar preservation de provenance;
AP. cursor boundary é estritamente now < validUntil/stableUntil;
AQ. key TTL não substitui read-time cursor validation;
AR. skip arbitrário precisa ser alcançado exatamente, sem page guess;
AS. strong signature canonicalization precisa distinguir arrays order-sensitive de set-like.
AT. freshness compartilhada precisa de clock autoritativo do storage para não depender de clock skew entre replicas;
```

A V10 preserva todos os acertos anteriores e passa a exigir, cumulativamente:

```text
1.  separation formal entre release evidence e release policy;
2.  tri-state released / unreleased / unknown;
3.  release regional para filmes sem quebrar Worldwide;
4.  legacy instant semantics para Worldwide e calendar-day semantics para regional;
5.  provider independence para movie evidence;
6.  hardening de series evidence;
7.  CanonicalFilterContext único e imutável;
8.  RequestEvaluationClock único por request;
9.  catalog cache neutro em relação à release policy;
10. search cache neutro e explicitamente versionado;
11. meta/component cache com releaseEvidence opcional e freshness própria;
12. releaseEvidence nunca obrigatório para reconstruir um meta;
13. cold store sem congelar negative regional evidence;
14. canonical raw TMDB release_dates owner;
15. single writer/schema/TTL para tmdb:movie:release_dates;
16. sourceFetchedAt real e nunca rejuvenescido por re-normalização;
17. forced factual revalidation para stale-negative evidence;
18. standard filtered-pagination cursor;
19. custom/StremThru cursor;
20. merged-catalog cursor;
21. filtered search pagination para providers pagináveis;
22. fallback explícito para providers de search não pagináveis;
23. comprehensive warmer usando o mesmo paging namespace/contract;
24. Jellyfin pageLengths/catalogLengths/walkCursors;
25. Jellyfin collection memberCursors;
26. sourceMembershipSignature;
27. filterSignature;
28. paginationContractSignature;
29. cacheEpoch/source-cache schema dentro da identidade de paging;
30. cursor validUntil = mínimo de todas as fontes de mudança de membership;
31. source page stability deadline compatível com refresh-ahead;
32. virada de dia/timezone;
33. Worldwide 365-day boundary como transition explícita;
34. evidence freshness boundary;
35. dynamic watched-state boundary/fingerprint;
36. search provider pre-filters removidos;
37. EffectiveSearchSourceContext resolvido antes da search cache lookup;
38. EffectiveSearchSourceContext compartilhado por execução, paging, logs e métricas;
39. configuração global + flags per-catalog + override regional de TMDB Discover;
40. provenance explícita e persistida da região de Discover;
41. configs legadas;
42. config cache clone safety;
43. Collection Builder/imported Discover catalogs;
44. merged catalogs;
45. anime;
46. personal lists;
47. recommendations;
48. Jellyfin catalog/search bridge;
49. separação de episódios/Up Next;
50. response hygiene de evidence interna;
51. testes golden-master de Worldwide;
52. testes de migration de search/meta/cursor;
53. testes de source cache identity;
54. testes de filtered search page fill;
55. testes de cursor invalidation por freshness;
56. testes de page-size/CACHE_EPOCH changes;
57. concorrência e request budget;
58. performance;
59. observabilidade;
60. PR Guard e estratégia de divisão;
61. caller parity entre addon/index.ts e getCatalog.ts;
62. cacheWarmer.js com config sintética compatível e sem policy materializada;
63. AI catalog schema/generation/sanitizer/entity-resolver auditados;
64. setup streaming sem transformar watch_region em release policy implicitamente;
65. CatalogsSettings preservando overrides/metadata/provenance;
66. dashboard/telemetry com decisão explícita sobre releaseRegion;
67. deterministic evidence normalization;
68. global releaseRegion + override somente de TMDB Discover nesta feature;
69. discoverCatalogSignature preservado como legado, com params canônicos promovidos a strong source identity;
70. TMDB Collection metadata.hideUnreleased semanticamente isolado;
71. parseProps.js como oracle legado temporário;
72. Simkl V2 search + custom lists + ordering cobertos;
73. series ambiguous status fail-open;
74. test harness executável e CI seguro em pull_request;
75. occurrence gate final = zero ocorrência sem changed/covered/no-op/test;
76. delta V8→V9 classificado integralmente contra `6e83e22`;
77. correctness signatures fortes e versionadas, sem depender de MD5 32/40-bit;
78. raw release write monotônico/CAS para impedir stale overwrite concorrente;
79. budget exhaustion distinto de upstream exhaustion;
80. zero-visible-page progress contract para cursor;
81. dedupe antes de cursor accounting e com semântica entre páginas definida;
82. `sourceFetchedAt` obrigatório/factual e `fetchGeneration` monotônica para ordenar writes;
83. dynamic source state separado de dynamic filter state;
84. rollback/cache-namespace compatibility;
85. DST/non-hour-offset calendar tests;
86. deployment em duas fases com observability gate antes de expor UI regional.
87. raw namespace versionado com dual-read/single-write migration;
88. retention TTL desacoplada de freshness por consumer;
89. storage-monotonic fetchGeneration;
90. stale evidence nunca autorizada a HIDE;
91. exact arbitrary-skip walker;
92. zero-visible served=0 resume;
93. no guessed filtered-page fallback;
94. explicit cursor coordinate system;
95. DedupePolicy exata por surface;
96. Catalog Cursor V7 + Search Cursor V3;
97. cross-replica cursor CAS/conflict detection;
98. neutral page revision/page-set stability contract;
99. canonical serialization domain specification;
100. secure authenticated account scoping;
101. catalog sharing/export provenance fixtures;
102. countries selector failure-safe save;
103. regional runtime kill switch;
104. homogeneous-fleet deployment gate;
105. config forward-compatibility gate para rollback.
106. storage-authoritative sourceFetchedAt para shared raw cache freshness.
```

A arquitetura final não deve ser construída adicionando condições de região em providers:

```text
if (region === 'BR')
```

Ela deve centralizar **facts, clock, context, policy, freshness, source identity e pagination
identity**.

---

# 2. Arquitetura final

```text
                       UPSTREAM PROVIDERS
                               │
                               ▼
                     RAW RELEASE INFORMATION
                               │
                               ▼
                     RELEASE EVIDENCE LAYER
                     region-neutral / cacheable
                               │
                  ┌────────────┴────────────┐
                  │                         │
                MOVIE                     SERIES
                  │                         │
       TMDB release_dates        premiere date + status
                  │                         │
                  └────────────┬────────────┘
                               ▼
                      NORMALIZED EVIDENCE
                               │
                               ▼
                    SHARED NEUTRAL HOT CACHE
                               │
                               ▼
                  LAZY EVIDENCE COMPLETION
                    somente quando necessária
                               │
                               ▼
                    RESOLVE FILTER CONTEXT
               canonical / effective / immutable
                               │
                               ▼
                  RELEASE VISIBILITY ENGINE
                released / unreleased / unknown
                               │
                               ▼
                       FILTER POLICY
                  ┌────────────┴────────────┐
                  │                         │
               CATALOG                   SEARCH
                  │                         │
                  ▼                         ▼
          FILTERED PAGINATION          POST-CACHE FILTER
                  │
                  ▼
           FILTER CONTEXT SIGNATURE
                  │
        ┌─────────┼──────────┬──────────────┐
        ▼         ▼          ▼              ▼
     STANDARD   EXTERNAL   MERGED        JELLYFIN
      CURSOR     CURSOR     CURSOR      PAGING STATE
        │         │          │              │
        └─────────┴──────────┴──────────────┘
                               │
                               ▼
                   TEMPORAL VALIDITY CHECK
```

As responsabilidades devem permanecer separadas:

```text
Evidence
→ fatos conhecidos e sua freshness

FilterContext
→ configuração efetiva já resolvida

Visibility evaluator
→ interpretação semântica dos fatos

Filter policy
→ decisão SHOW/HIDE

Pagination identity
→ namespace do conjunto filtrado

Temporal validity
→ momento máximo até o qual aquele cursor continua correto
```

---

# 3. Invariantes arquiteturais

A implementação deve obedecer a estes invariantes.

```text
1. Região nunca entra em raw upstream cache.

2. Região nunca altera o fato armazenado.

3. O mesmo movie pode compartilhar evidence entre BR, US e Worldwide.

4. Policy específica de usuário acontece depois de cache neutro.

5. UNKNOWN não vira automaticamente UNRELEASED.

6. Worldwide mantém exatamente o comportamento legado observável.

7. Release Region afeta movie, não series.

8. Watch region e release region continuam conceitos distintos.

9. Episódio futuro não torna a série inteira unreleased.

10. Cursor de paginação deve corresponder exatamente ao conjunto filtrado
    que o originou.

11. Mudança de região, policy, definição do merged catalog ou contexto temporal
    não pode reutilizar cursor incompatível.

12. Nenhuma ausência de dado externo deve ser silenciosamente promovida
    a fato confirmado.

13. O mesmo canonical FilterContext deve alimentar:
    catalogFiltersActive(),
    evidence completion,
    evaluator,
    applyCatalogFilters(),
    filter signature
    e pagination validity.

14. Internal release evidence nunca deve vazar para a resposta Stremio/Jellyfin
    apenas por existir no cache interno.

15. Negative-by-absence evidence regional precisa de freshness limitada.
    "BR não apareceu no payload" não pode ficar congelado indefinidamente.

16. releaseEvidence não entra no cold store com TTL de 60/180 dias
    sem uma política de freshness específica por componente.

17. Uma alteração no schema de evidence não deve invalidar art/cast/links
    quando existir versionamento de componente mais estreito.

18. Search cache neutro nunca reutiliza payload antigo que tenha sido
    previamente filtrado por hide-unreleased.

19. Qualquer decisão capaz de mudar antes da próxima virada de dia deve
    fornecer uma boundary temporal que invalide o cursor naquele instante.

20. Secrets/API keys nunca entram em filter signature, logs ou reason codes.

21. Todos os callers de applyCatalogFilters()/catalogFiltersActive() devem usar
    o mesmo CanonicalFilterContext; addon/index.ts e getCatalog.ts não podem
    resolver policy/signature de forma independente.

22. Synthetic configs de warmers precisam normalizar releaseRegion como Worldwide
    e nunca podem aquecer cache neutro já filtrado por região.

23. watch_region criado por setup/AI catalog continua significando disponibilidade
    de provider; só pode virar release region quando a regra release-aware explícita
    de provenance autorizar.

24. Normalização de evidence deve produzir estruturas determinísticas:
    RegionCode uppercase, sem duplicatas e arrays de regiões ordenados.

25. A #742 não cria genericamente um seletor releaseRegion em todo catálogo.
    O contrato desta feature é global releaseRegion, com override de TMDB Discover
    quando params.region possuir provenance válida.

26. Freshness de releaseEvidence nunca pode ser maior na prática que a freshness
    factual do raw TMDB release_dates do qual ela foi derivada. Re-normalizar cache
    velho não renova sourceFetchedAt.

27. `tmdb:movie:release_dates:<id>` possui um único contrato de writer/schema/TTL.
    Helpers de certificação e de release visibility não podem competir escrevendo
    a mesma key com TTLs diferentes.

28. A identidade de paginação possui duas dimensões independentes:
    sourceMembershipSignature + filterSignature.

29. `discoverSig`/computeDiscoverSignature existente deve permanecer parte da
    identidade de um TMDB Discover e não pode ser perdido pelo novo FilterContext.

30. `metadata.hideUnreleased` de TMDB Collection é um prefilter legado baseado em
    `part.release_date`; não é sinônimo de hideUnreleasedDigital.

31. O helper legado `isReleasedDigitally()` não pode ser simultaneamente
    implementação nova e oracle do golden-master.

32. Search cache deve identificar a fonte efetivamente executada, não apenas o
    provider solicitado. Fallback por auth/capability muda o execution profile.

33. Tokens/secretos nunca entram em search source signatures.

34. Status de série ambíguo sem premiere confiável é UNKNOWN → SHOW.
    `In Production` sem first-air date não vira HIDE apenas por status.

35. Qualquer commit em `dev` posterior ao audit HEAD invalida a alegação de
    cobertura estática completa até o delta ser classificado.
```

---


## Invariantes adicionais V9

```text
36. Uma assinatura de correção não pode depender exclusivamente de `discoverSig` de 32 bits
    nem de `hashConfig()` de 40 bits. Hash curto permanece compatibilidade/diagnóstico.

37. Raw facts possuem ordem temporal de escrita. Um fetch iniciado/terminado antes não pode
    sobrescrever atomicamente um envelope com `sourceFetchedAt` mais novo.

38. `budgetExhausted` e `upstreamExhausted` são estados distintos. Nunca gravar ou logar
    budget exhaustion como se a fonte tivesse terminado.

39. Uma página com zero itens visíveis e source ainda não esgotada precisa preservar a posição
    upstream alcançada; o mesmo skip não pode reiniciar indefinidamente no mesmo ponto.

40. Dedupe que altera cardinalidade deve ocorrer antes de `served` ser calculado. A regra de
    dedupe faz parte de `paginationContractSignature`.

41. `sourceFetchedAt` é factual e obrigatório para evidence regional negativa. `normalizedAt`,
    se existir, é apenas observabilidade e nunca renova freshness.

42. Estado dinâmico que muda a **fonte** (watchlist, dropped shelf, recommendation snapshot)
    entra em source identity/stability; estado que muda somente o **pós-filtro** entra em
    RuntimeFilterState/filter validity. Nunca misturar as duas classes.

43. Rollback não pode fazer uma versão antiga ler namespaces V9 como se fossem antigos.
    Schema/namespace bump precisa ser unilateralmente seguro.

44. Próxima meia-noite local é calculada pelo timezone IANA, não por `now + 24h`.

45. Segredos, token IDs crus e API keys não entram em nenhuma nova source/filter/paging
    signature. Quando account scope for necessário, usar fingerprint opaco derivado.
```

# 4. Release Evidence Layer

A camada de evidence responde exclusivamente:

> Quais fatos relacionados a estreia/disponibilidade estão presentes nos dados que recebemos?

Ela não responde:

> O usuário deve ou não ver este título?

Portanto nenhuma função de evidence deve depender de:

```text
hideUnreleasedDigital
hideUnreleasedShows
releaseRegion do usuário
catalog override
search override

```

Essas são decisões de policy.

---

# 5. Movie evidence

Para filmes, a fonte de verdade para #742 continua:

```text
TMDB /movie/{id}/release_dates

```

Tipos TMDB:

```text
1 = Premiere
2 = Theatrical Limited
3 = Theatrical
4 = Digital
5 = Physical
6 = TV

```

Para `Hide Unreleased Movies`, home release continua definido por:

```text
4 | 5 | 6

```

Tipos `1/2/3` não comprovam disponibilidade digital/home.

---

# 6. CalendarDate

Criar tipo semântico:

```ts
type CalendarDate = `${number}-${number}-${number}`;

```

Não usar um `Date` como representação canônica de uma release regional.

Uma release do TMDB como:

```text
2026-10-20T00:00:00.000Z

```

deve ser normalizada semanticamente para:

```text
2026-10-20

```

quando utilizada como release-day evidence.

Não fazer:

```ts
new Date(value)
  .toISOString()

```

como etapa intermediária para decidir o dia regional.

Isso introduz semântica de instante onde a feature precisa de semântica de calendário.

---

# 7. Parser de CalendarDate

Criar helper central:

```ts
parseCalendarDate(value): CalendarDate | null

```

Responsabilidades:

```text
- aceitar string válida;
- extrair YYYY-MM-DD;
- validar ano/mês/dia;
- rejeitar data impossível;
- não converter timezone;
- não fabricar horário.

```

Exemplos:

```text
2026-10-20
→ 2026-10-20

2026-10-20T00:00:00Z
→ 2026-10-20

garbage
→ null

2026-02-31
→ null

```

---

# 8. `_releaseAvailability` Schema 2

O Schema 1 atual é insuficiente regionalmente.

O V5 também corrige uma incompatibilidade conceitual do V4:
Worldwide precisa preservar a semântica temporal legado, enquanto a policy regional
precisa de calendar-day semantics.

Portanto não usar o mesmo campo para as duas coisas.

Modelo recomendado:

```ts
const RELEASE_EVIDENCE_SCHEMA = 2;

type RegionCode = string & {
  readonly __regionCode: unique symbol;
};

type CalendarDate = string & {
  readonly __calendarDate: unique symbol;
};

interface ReleaseAvailabilityV2 {
  schema: 2;

  source: 'tmdb_release_dates';

  coverage:
    | 'available'
    | 'empty'
    | 'unavailable';

  /**
   * Compatibilidade com consumidores legados.
   * true quando TMDB entregou results como array,
   * inclusive vazio.
   */
  hasReleaseDateData: boolean;

  /**
   * Facts usados pelo Worldwide evaluator.
   * Devem preservar a mesma semântica temporal
   * que o algoritmo legado observava.
   */
  earliestAnyReleaseAt:
    | string
    | null;

  earliestHomeReleaseAt:
    | string
    | null;

  /**
   * Facts regionais.
   * São dias civis, não instantes UTC.
   */
  homeReleaseDaysByRegion:
    Record<RegionCode, CalendarDate>;

  regionsWithReleaseRecords:
    RegionCode[];

  /**
   * Opcional para revalidation/observability.
   * Não é policy e não participa da decisão regional,
   * exceto para avaliar freshness do cache.
   */
  sourceFetchedAt: string;

  /**
   * Opcional apenas para diagnóstico. Nunca participa da freshness factual.
   */
  normalizedAt?: string;
}
```

Regra fundamental:

```text
Worldwide
→ legacy instant semantics

Regional
→ CalendarDate semantics
```

Não converter os facts Worldwide para `YYYY-MM-DD` se isso puder alterar
o comportamento legado.

`CalendarDate` é construído apenas por helper validado; não aceitar cast arbitrário.

---

# 9. Semântica de `coverage`

É obrigatório distinguir:

```text
unavailable
empty
available

```

## `unavailable`

Exemplos:

```text
request falhou
release_dates ausente
results não é array
não conseguimos obter evidence

```

Não existe evidence confiável.

---

## `empty`

Exemplo:

```json
{
  "results": []
}

```

ou payload sem qualquer release entry utilizável.

O provider respondeu, mas não ofereceu release records utilizáveis.

Isso não é prova factual de que:

```text
nenhum país teve lançamento

```

---

## `available`

Existe ao menos um release record válido no payload.

Exemplo:

```text
US theatrical
US digital
GB digital
...

```

---

# 10. Compatibilidade do `hasReleaseDateData` e Golden Master Worldwide

Worldwide precisa preservar o algoritmo legado.

Hoje um:

```text
results=[]
```

é interpretado como:

```text
release data foi consultada
```

Portanto:

```ts
hasReleaseDateData =
  coverage !== 'unavailable';
```

O evaluator regional NÃO usa sozinho esse boolean.
Ele olha:

```text
coverage
homeReleaseDaysByRegion
```

O evaluator Worldwide usa os facts temporalmente compatíveis:

```text
earliestAnyReleaseAt
earliestHomeReleaseAt
```

e deve ser validado por golden-master:

```text
old isReleasedDigitally(rawMeta, fixedNow)
===
new evaluateWorldwideMovieRelease(normalizedV2, fixedNow)
```

para toda a matriz legado, incluindo:

```text
timestamp à meia-noite
timestamp não-meia-noite
offset timezone explícito
future primary release
365-day boundary
results=[]
invalid release entry
missing release evidence
```

A #742 não pode alterar Worldwide acidentalmente para conseguir regional support.

---

# 11. Construção do mapa regional

Para cada country result:

```text
iso_3166_1
```

normalizar para uppercase e validar.

Dentro de:

```text
release_dates
```

considerar apenas:

```text
type 4
type 5
type 6
```

Para o mapa regional, guardar a menor **calendar date válida**.

Exemplo:

```ts
homeReleaseDaysByRegion = {
  BR: '2026-10-20',
  US: '2026-09-10',
  GB: '2026-09-12',
};
```

Se houver:

```text
BR Digital 2026-10-20T12:30:00Z
BR TV      2026-11-15T00:00:00Z
```

o regional fact é:

```text
BR = 2026-10-20
```

Separadamente, a normalização mantém os earliest legacy instants para Worldwide.

Assim, uma única evidence V2 suporta as duas semânticas sem confundi-las.

---

# 12. `regionsWithReleaseRecords`

Além do mapa 4/5/6, manter:

```ts
regionsWithReleaseRecords

```

com países que possuem qualquer release entry válida.

Isso melhora debugging e futuras decisões.

Exemplo:

```text
BR possui apenas theatrical

```

Então:

```text
regionsWithReleaseRecords inclui BR

homeReleaseDaysByRegion.BR
não existe

```

---

# 13. Worldwide permanece legado

Config:

```text
Release Region = Worldwide

```

deve executar a semântica existente.

Isso inclui:

```text
primary release futura
→ HIDE

filme lançado há >=365 dias
→ assume RELEASED

filme recente
→ exige home release

nenhuma release evidence disponível
→ SHOW

```

O V5 não deve usar a mudança regional como desculpa para alterar a semântica atual do usuário existente.

---

# 14. Global Release Region

Adicionar ao config:

```ts
releaseRegion?: string;

```

Default:

```ts
releaseRegion: '';

```

Semântica:

```text
''   → Worldwide
BR   → Brazil
US   → United States
GB   → United Kingdom
...

```

Configs antigas sem o campo continuam:

```text
Worldwide

```

---

# 15. Não inferir release region pelo idioma

Nunca fazer globalmente:

```ts
releaseRegion =
  config.language.split('-')[1];

```

Exemplo:

```text
language=pt-BR

```

não deve transformar silenciosamente um usuário existente de:

```text
Worldwide

```

em:

```text
BR

```

Backward compatibility exige opt-in explícito.

---

# 16. `normalizeReleaseRegion`

Criar:

```ts
normalizeReleaseRegion(value)

```

Responsabilidades:

```text
trim
uppercase
validar comprimento 2
validar código conhecido
retornar null se inválido

```

Em código inválido:

```text
warning
+
Worldwide fallback

```

Nunca:

```text
ZZ
→ região legítima

```

---

# 17. Países suportados

A UI deve reutilizar a lista obtida pelo próprio TMDB via infraestrutura já existente.

Não manter manualmente uma tabela de países.

Ainda assim, antes do merge, comparar:

```text
TMDB /configuration/countries

```

com os códigos reconhecidos pelo mecanismo backend de validação.

Se TMDB possuir um código legítimo não reconhecido pela dependência utilizada:

```text
adicionar exceção explícita
+
teste
+
comentário/documentação

```

Não assumir paridade.

---

# 18. Release region e TMDB Discover

Backend não deve reinterpretar diretamente:

```text
watch_region

```

como release region em todo request.

Conceitos:

```text
watch_region
→ watch providers

region
→ release region do TMDB Discover

```

O Discover Builder já consegue materializar a decisão em:

```text
params.region

```

Portanto essa deve ser a fonte de verdade após a construção do catálogo.

---

# 19. Precedência definitiva de região + provenance

Não basta conhecer o código da região; é necessário conhecer de onde ele veio.

O builder atual consegue materializar `params.region` a partir de:
- seleção explícita de release region;
- watch region quando release-type semantics estão ativas;
- fallback do idioma em determinados fluxos de criação.

O V5 não deve permitir que essa provenance desapareça e depois trate todas as regiões
como se fossem explicitamente escolhidas pelo usuário.

Criar:

```ts
type ReleaseRegionSource =
  | 'explicit'
  | 'discover-explicit'
  | 'watch-region-derived'
  | 'legacy-normalized'
  | 'language-derived'
  | 'global'
  | 'worldwide';

interface EffectiveReleaseRegion {
  mode: 'worldwide' | 'regional';
  code?: RegionCode;
  source: ReleaseRegionSource;
}
```

Precedência para movie catalog:

```text
1. catalog.metadata.discover.params.region
   com provenance preservada quando conhecida

2. catalog.metadata.discoverParams.region
   legado, normalizado

3. config.releaseRegion

4. Worldwide
```

Policy recomendada:

```text
explicit / discover-explicit
→ sempre pode sobrescrever global

watch-region-derived
→ permitido para Discover release-aware,
   alinhado ao pedido da #742

language-derived
→ NÃO deve transformar silenciosamente
   Hide Unreleased global Worldwide em regional
   sem decisão explícita de produto
```

Se o projeto optar por considerar `language-derived` autoritativo, isso precisa ser
uma decisão explícita, documentada e coberta por teste. Não deixar emergir por acidente.

Criar função única:

```ts
resolveEffectiveMovieReleaseRegion({
  catalogConfig,
  config,
})
```

Nenhum provider ou cursor deve reinterpretar `watch_region` independentemente.

---

# 20. Config antiga com `watch_region`

Caso antigo:

```text
watch_region=BR
with_release_type=4|5|6
region ausente

```

Não manter para sempre uma inferência ambígua no evaluator.

Criar normalização de configuração que, somente quando a semântica for inequívoca, materialize em memória:

```text
region=BR

```

Essa migration deve ser idempotente.

---

# 21. Config cache atual — ajuste novo do V4

Na base atual, `configApi.js` possui:

```text
loadSharedConfig()

```

que retorna a configuração compartilhada/cacheada como objeto read-only por convenção.

E:

```text
loadConfigFromDatabase()

```

entrega uma cópia profunda que callers podem modificar.

Portanto:

> `normalizeReleaseVisibilityConfig()` NÃO deve mutar o objeto retornado por `loadSharedConfig()`.

Estratégia:

```text
loadSharedConfig
    ↓
deep clone
    ↓
normalizeReleaseVisibilityConfig
    ↓
runtime config

```

Ou aplicar a normalização em outro ponto após a cópia.

Não contaminar o objeto compartilhado.

---

# 22. Persistência da migration

A migration de config legada não precisa salvar silenciosamente no banco durante um read.

Recomendado:

```text
stored config
    ↓
runtime normalization
    ↓
uso normal

```

Quando o usuário salvar a configuração posteriormente, o formato moderno pode ser persistido.

Evitar side effect de write em rota de leitura.

---

# 23. Collection Builder e imports — alteração obrigatória

Na base V5, `addon/lib/collectionBuilder/catalogReconstruction.ts` NÃO é opcional
para a #742.

Hoje a reconstrução nativa preserva `watch_region`, mas não cobre integralmente:

```text
region
with_release_type
release_date.gte/lte
releaseRegion no formState
releasedOnly/tmdbMovieReleaseTypes no formState
```

Portanto o round-trip exigido pela própria feature não passa sem alteração explícita.

Regras obrigatórias:

```text
se catálogo importado possui region explícita
→ preservar params.region

se possui with_release_type
→ preservar exatamente a semântica suportada pelo builder

se with_release_type = 4|5|6
→ formState.releasedOnly = true

se possui release types específicos
→ restaurar formState.tmdbMovieReleaseTypes

se possui somente watch_region
→ preservar watch_region
→ não criar genericamente region sem a regra de migration/provenance

se combinação legada for inequivocamente release-aware
→ materializar runtime region com provenance legacy-normalized

edit → save
→ não pode remover params.region nem release-type semantics
```

`addon/utils/ai-catalog-config-builder.ts` já reconhece `params.region` e deve permanecer
semanticamente alinhado com `catalogReconstruction.ts`.

Os dois caminhos devem compartilhar testes de round-trip.

---

# 24. Teste de round-trip do Collection Builder

Criar teste:

```text
Discover catalog
region=BR
with_release_type=4|5|6

export/import/reconstruct
→ region continua BR

open editor
save
→ region continua BR

```

Também:

```text
watch_region=US
sem region
sem release-type semantics
→ NÃO criar region=US

```

---

# 25. Release Visibility Engine

Criar:

```text
addon/utils/releaseVisibility.ts
```

Tipos:

```ts
type ReleaseState =
  | 'released'
  | 'unreleased'
  | 'unknown';

type ReleaseReason =
  | 'legacy-future-primary-release'
  | 'legacy-over-one-year'
  | 'worldwide-home-release'
  | 'worldwide-home-release-missing'
  | 'regional-home-release'
  | 'regional-home-release-future'
  | 'regional-home-release-not-confirmed'
  | 'release-evidence-empty'
  | 'release-evidence-unavailable'
  | 'release-evidence-schema-legacy'
  | 'tmdb-id-unavailable'
  | 'invalid-release-date'
  | 'first-air-past'
  | 'first-air-future'
  | 'prerelease-status'
  | 'postrelease-status'
  | 'ambiguous-status';

interface ReleaseDecision {
  state: ReleaseState;
  reason: ReleaseReason;

  region?: RegionCode | null;

  /**
   * Menor instante conhecido em que esta decisão
   * pode deixar de ser válida sem novo upstream data.
   */
  nextTransitionAt?: Date | null;
}
```

Não usar `reason: string` livre.

`nextTransitionAt` é essencial para manter paginação correta quando Worldwide/Series
preservarem timestamps que podem cruzar durante o mesmo dia.

---

# 26. Policy padrão

```text
released
→ SHOW

unreleased
→ HIDE

unknown
→ SHOW

```

Isso é:

```text
fail-open

```

quando evidence confiável não existe.

O filtro deve evitar falso negativo agressivo causado por ausência de metadata.

---

# 27. Canonical FilterContext

Antes de avaliar visibility ou gerar assinatura, resolver uma única vez o contexto efetivo.

Criar algo conceitualmente como:

```ts
interface CanonicalFilterContext {
  surface: 'catalog' | 'search';
  mediaType: 'movie' | 'series' | 'anime' | 'all';

  releasePolicyVersion: number;
  releaseEvidenceSchema: number;

  movie: {
    hideUnreleased: boolean;
    releaseRegion: EffectiveReleaseRegion;
  };

  series: {
    hideUnreleased: boolean;
  };

  timezone: string;
  logicalDay: CalendarDate;

  ageRating: string | null;
  allowUnratedContent: boolean;

  exclusionKeywords: string[];
  exclusionGenres: string[];
  regexExclusionFilter: string | null;

  watched: {
    trakt: boolean;
    anilist: boolean;
    mdblist: boolean;
    simkl: boolean;
  };

  catalogIdentity: {
    cleanId: string;
    overrideFingerprint: string | null;
  };
}
```

Criar:

```ts
resolveCanonicalFilterContext(...)
```

e usar o MESMO objeto em:

```text
catalogFiltersActive
ensureReleaseEvidenceForFilter
evaluateMovieReleaseVisibility
evaluateSeriesReleaseVisibility
applyCatalogFilters
buildCatalogFilterSignature
cursor validity
logs/metrics
```

Isso elimina a classe de bug em que o filtro resolve uma região e a signature
acidentalmente hasheia outra.

---

# 28. Worldwide movie evaluator

Worldwide deve reproduzir a semântica legado observável.

Ideal:

```ts
evaluateWorldwideMovieRelease(...)
```

Durante a #742, não reescrever a policy Worldwide além do necessário para encaixá-la
no evaluator.

Os facts usados nesse caminho devem manter a semântica temporal antiga:

```text
meta.released
earliestAnyReleaseAt
earliestHomeReleaseAt
365-day threshold
```

O V5 proíbe uma simplificação silenciosa de timestamp → calendar date neste caminho.

Critério de equivalência:

```text
para o mesmo meta
+
mesmo fixed now
=
mesma decisão antiga e nova
```

Golden-master obrigatório antes de remover/depreciar `isReleasedDigitally()`.

---

# 29. Regional movie evaluator

Com:

```text
releaseRegion=BR

```

regras:

```text
schema 2
+
coverage=available
+
BR home date existe
+
date <= hoje BR
→ RELEASED

```

```text
BR home date existe
+
date > hoje BR
→ UNRELEASED

```

```text
coverage=available
+
nenhuma home release 4/5/6 em BR
→ UNRELEASED

```

```text
coverage=empty
→ UNKNOWN

```

```text
coverage=unavailable
→ UNKNOWN

```

```text
schema 1
→ UNKNOWN

```

após tentar, quando possível, completar a evidence.

---

# 30. Importante: ausência de BR não é fato absoluto

Quando:

```text
coverage=available
US possui Digital
BR não possui 4/5/6

```

a policy regional pode decidir:

```text
UNRELEASED

```

porque a feature foi definida como:

> mostrar somente quando houver home release confirmada na região selecionada.

Mas reason code e documentação não devem afirmar:

```text
TMDB provou que nunca lançou no Brasil

```

Melhor reason:

```text
regional-home-release-not-confirmed

```

e não:

```text
definitely-not-released-in-region

```

---

# 31. Regional mode não usa fallback de 365 dias

Exemplo:

```text
Theatrical worldwide:
2020

Release Region:
BR

Nenhuma home release BR confirmada

```

Não fazer:

```text
já passou um ano
→ RELEASED

```

No modo regional isso destruiria justamente a feature solicitada pela #742.

---

# 32. Timezone regional e validade temporal

Criar helper central:

```ts
todayInTimezone(
  now,
  timezone
): CalendarDate
```

e:

```ts
hasCalendarDateArrived(
  releaseDate,
  today
): boolean
```

Também:

```ts
nextLocalMidnight(
  now,
  timezone
): Date
```

Timezone inválido não pode derrubar catálogo/search.

Resolver por regra única:

```text
config.timezone válida
→ usar

senão process.env.TZ válida
→ usar

senão
→ UTC
→ warning deduplicado
```

Nunca inferir timezone a partir de release region:
um país pode possuir múltiplos fusos.

Para Regional:

```text
release=2026-10-20
America/Fortaleza
2026-10-19 23:59 → false
2026-10-20 00:00 → true
```

Quando a decisão depender apenas do dia regional, `nextTransitionAt` pode ser
a próxima meia-noite local relevante.

Worldwide/Series podem possuir transition boundaries dentro do dia e não devem
ser reduzidos artificialmente ao bucket diário se isso quebrar legacy behavior.

---

# 33. Exact release hour

Não prometer precisão inexistente.

TMDB release date não garante universalmente:

```text
o minuto exato em que arquivo digital ficou disponível

```

A maior precisão justificável por esses dados é:

```text
calendar day

```

---

# 34. Series NÃO usa Release Region

`releaseRegion` é exclusivamente movie release policy.

Não aplicar a:

```text
series

```

Disponibilidade regional de séries por serviços de streaming é outra feature.

---

# 35. Future feature regional streaming

Se necessário futuramente:

```text
Hide Titles Without Regional Streaming Availability

```

poderá usar:

```text
watch_region
watch providers

```

para filmes e séries.

Isso NÃO faz parte da semântica de:

```text
Hide Unreleased

```

---

# 36. Series evaluator

Criar:

```ts
evaluateSeriesReleaseVisibility(
  meta,
  context
)

```

Sem `releaseRegion`.

---

# 37. Ordem de decisão de Series

```text
1. Existe premiere/released válido?

   data <= agora/hoje
   → RELEASED

   data futura
   → UNRELEASED


2. Não existe data confiável?

   pre-release status inequívoco
   → UNRELEASED

   post-release status inequívoco
   → RELEASED

   restante
   → UNKNOWN

```

Data confiável tem precedência sobre status.

---

# 38. Por que data tem prioridade

Exemplo:

```text
first_air_date=2023
status=In Production

```

Significa possivelmente:

```text
nova temporada em produção

```

A série já estreou.

Resultado:

```text
RELEASED

```

---

# 39. Status normalization

Retirar normalização dispersa de dentro de:

```text
catalogFilters.ts

```

Criar normalização compartilhada:

```ts
normalizeReleaseStatus(value)

```

Evitar dependência conceitual da release feature com a lógica inteira do cold-store.

Pode extrair a transformação genérica hoje presente em:

```text
metaColdStore/stability.ts

```

para utility comum.

---

# 40. Pre-release statuses

Mapear variantes conhecidas:

```text
not yet aired
not_yet_aired

upcoming

not yet released
not_yet_released

planned

unreleased

tba

pre production
pre-production

not_yet_released

```

Normalizar:

```text
trim
lowercase
underscore/hyphen/spacing normalization

```

antes da classificação.

---

# 41. Post-release statuses

Sem data, estes podem ser tratados como released quando semanticamente inequívocos:

```text
ended
finished airing
currently airing
continuing
returning series

```

Statuses ambíguos:

```text
canceled
cancelled
in production
pilot
outros não inequívocos
→ UNKNOWN
```

`canceled/cancelled` sem premiere não prova que a série chegou a estrear; um projeto
pode ser cancelado antes da primeira exibição. Se existir first-air/released válida,
a data continua tendo precedência e resolve o estado.


---

# 42. `In Production`

Regra:

```text
past release date + In Production
→ RELEASED
```

Sem release date confiável:

```text
In Production
→ UNKNOWN
→ SHOW
```

Motivo: a policy global do plano é fail-open quando a evidence não prova premiere.
Além disso, o comportamento legado atual não classifica `In Production` como
`UNRELEASED_STATUSES`; transformar esse caso em HIDE dentro da #742 seria regressão
agressiva sem evidence suficiente.

A mesma regra vale para qualquer status cuja semântica não prove, isoladamente,
que a primeira exibição ainda não aconteceu.

Essa decisão fica isolada no evaluator para poder mudar futuramente sem mexer em providers.

---

# 43. Separar evidence, policy, cache e signature versions

Não usar uma constante para conceitos diferentes.

Criar/versionar separadamente:

```ts
export const RAW_RELEASE_DATES_CACHE_SCHEMA = 2;
export const RAW_RELEASE_DATES_REQUEST_PROFILE_VERSION = 1;
export const RELEASE_EVIDENCE_SCHEMA = 2;
export const RELEASE_VISIBILITY_POLICY_VERSION = 1;
export const RELEASE_ENTITY_KIND_CONTRACT_VERSION = 1;
export const TMDB_ID_RESOLUTION_CONTRACT_VERSION = 1;
export const SEARCH_RESULT_CACHE_SCHEMA_VERSION = 2;
export const CATALOG_SOURCE_SIGNATURE_VERSION = 1;
export const CATALOG_FILTER_SIGNATURE_VERSION = 1;
export const PAGINATION_CONTRACT_SIGNATURE_VERSION = 1;
export const CATALOG_CURSOR_SCHEMA_VERSION = 7;
export const SEARCH_CURSOR_SCHEMA_VERSION = 3;
```

Diferença:

```text
Raw cache schema
→ envelope do fato recebido do TMDB

Evidence schema
→ formato/significado dos facts normalizados

Policy version
→ regras released/unreleased/unknown

Search result cache schema
→ garante que payload antigo filtrado não vire neutral result

Source signature version
→ contrato que define a sequência upstream

Filter signature version
→ contrato que define o subconjunto pós-cache

Pagination contract version
→ page size, paging mode, dedupe/fill semantics e cache epoch

Cursor schema
→ estrutura persistida da posição paginada
```

Uma mudança de policy não exige evidence schema bump.

Uma neutralização do search cache não deve depender de "o hash mudou por acaso":
a migration precisa de namespace/versionamento explícito.

`CACHE_EPOCH` não deve ser bumpado só por esta feature; porém o valor efetivo do epoch
**participa do pagination contract** para que cursores sobreviventes não apontem para um
universo de page-cache diferente após um futuro bump operacional.

---

# 44. `applyCatalogFilters()` continua chokepoint

Manter:

```text
addon/utils/catalogFilters.ts
```

como ponto central de policy.

Novo fluxo:

```text
resolveCanonicalFilterContext
      ↓
catalogFiltersActive(context)
      ↓
ensureReleaseEvidenceForFilter
      ↓
evaluate movie/series visibility
      ↓
apply demais membership filters
      ↓
FilterResult {
  metas,
  nextTransitionAt
}
```

`applyCatalogFilters()` pode continuar expondo compatibilidade com callers atuais,
mas internamente deve ser possível obter a boundary temporal agregada.

Substituir:

```text
movie:
isReleasedDigitally()

series:
filtro inline
```

por evaluators centrais.

A signature nunca deve recalcular precedence por conta própria.

---

# 45. Flags existentes permanecem

Não renomear nesta feature:

```text
hideUnreleasedDigital
hideUnreleasedDigitalSearch
hideUnreleasedShows
hideUnreleasedShowsSearch

```

Compatibilidade é mais valiosa que limpeza estética.

---

# 46. Overrides per-catalog

Semântica atual permanece para as flags de Hide Unreleased.
Para `releaseRegion`, esta feature NÃO adiciona um campo genérico em metadata de
todo catálogo: o override regional é restrito ao TMDB Discover materializado em
`discover.params.region`, com provenance. Isso evita duas fontes concorrentes de região.

Semântica atual permanece:

```text
catalog metadata explicit ON/OFF
→ vence global

sem override
→ global

```

Para movie region:

```text
catalog Discover explicit region
→ vence global releaseRegion

sem region explícita
→ global

sem global
→ Worldwide

```

---

# 47. Search IDs

Já validado:

```text
search.*
→ cleanId=search

people_search.*
→ cleanId=people_search

gemini.search
→ cleanId=gemini.search

```

Portanto todos convergem ao mesmo filter chokepoint.

---

# 48. AI Search

Resultados mistos podem conter:

```text
movie
series

```

Então o filtro deve avaliar:

```ts
meta.type

```

item por item.

Não avaliar o catálogo inteiro como um único media type.

---

# 49. TVDB Collections Search

> **Correção normativa V14:** o snapshot pode codificar `tvdbc:*` com `meta.type='movie'`; aplicabilidade usa semantic entity kind, não apenas `meta.type` (seção 361).

É:

```text
collection

```

Não é movie/series.

Não aplicar Hide Unreleased aos objetos collection.

---

# 50. Search architecture — problema atual

Hoje `getSearch.ts` contém vários pontos onde:

```text
provider fetch
→ release enrichment condicionado ao hide flag
→ provider-level release filtering
→ search cache
→ route-level filtering
```

Foram localizados pre-filters em TMDB, Simkl, Trakt, MDBList, AI Search e caminhos
adjacentes.

Isso duplica policy e permite que o search cache seja contaminado por uma configuração
específica.

Também o search cache atual inclui `hideUnreleasedDigitalSearch` na identidade.
A neutralização V5 precisa de migration explícita; não basta remover o campo e assumir
que payload antigo filtrado nunca colidirá.

---

# 51. Search architecture final

Objetivo:

```text
SEARCH PROVIDER
      ↓
neutral result
      ↓
SEARCH CACHE v2
      ↓
evidence completion
somente se necessária
      ↓
Canonical FilterContext
      ↓
Release Visibility
      ↓
applyCatalogFilters()
```

Provider adapters podem produzir facts.
Eles não decidem SHOW/HIDE para Hide Unreleased.

Search cache v2 deve ser incompatível com cache antigo que possa conter
resultado já filtrado.

---

# 52. Search cache deve ser release-policy-neutral

Depois da limpeza:

```text
releaseRegion
visibility day
hideUnreleasedDigitalSearch
hideUnreleasedShowsSearch
```

NÃO participam da identidade do **neutral search result**.

Participam apenas fatores que alteram o resultado upstream/hydration neutro.

No V8 o provider efetivamente executado é resolvido **antes** do cache e vira a única
source context usada por cache, execução, paginação, logs e métricas:

```ts
interface EffectiveSearchSourceContext {
  requestedProvider: string;
  effectiveProvider: string;
  authMode: 'none' | 'v1-client' | 'v2-user' | 'other';
  capabilityRevision: string | null;

  pagingMode: 'page' | 'offset' | 'none';
  pageSize: number | null;
  supportsFilteredFill: boolean;

  // Somente quando comprovadamente necessário.
  accountScopeFingerprint?: string | null;
}
```

Resolver neste único helper:

```text
Simkl disabled → default provider
Simkl V2-only sem token → default provider
Simkl V2-user conectado → Simkl + authMode=v2-user
Lumiere sem LUMIERE_API_BASE → default provider
Gemini/people/fixed routes → source context explícito
```

Nunca resolver fallback de novo dentro de `getSearch()` de forma divergente.

Caso obrigatório:

```text
requested = simkl.search
sem token V2
→ fallback cached

conecta Simkl
→ effectiveProvider/authMode mudam
→ cache antigo não pode mascarar Simkl por 12h
```

Não colocar token/API key/tokenId cru no profile. Se um provider variar materialmente por
conta/entitlement, usar fingerprint opaco ou user scope. Se a resposta autenticada for
comprovadamente user-invariant, documentar a prova e não segmentar desnecessariamente.

Obrigatório incluir:

```text
SEARCH_RESULT_CACHE_SCHEMA_VERSION
+ effective search source profile
```

na key/profile.

Enquanto search cache ainda transportar `_releaseAvailability`, incluir também
`RELEASE_EVIDENCE_SCHEMA`; evidence carregada do page cache continua **advisory** e precisa
passar pelo freshness gate antes de decidir HIDE.

Teste de deploy obrigatório:

```text
old version grava filtered search cache
→ upgrade
→ new version
→ NÃO reutiliza esse payload como neutral
```

---

# 53. Search evidence schema e page-cache evidence

O search cache pode continuar armazenando metadata com evidence normalizada na primeira
implementação, desde que duas regras sejam absolutas:

```text
1. schema incompatível nunca é tratado como Schema 2;
2. sourceFetchedAt/freshness da evidence é validada contra o raw owner canônico antes de HIDE.
```

Enquanto `_releaseAvailability` estiver dentro do payload de busca:

```text
RELEASE_EVIDENCE_SCHEMA
```

deverá participar da identidade do search cache.

A otimização arquitetural preferível para uma etapa posterior é:

```text
neutral search/catalog page cache
→ sem releaseEvidence persistida

release facts
→ canonical raw release cache
→ optional releaseEvidence meta component
```

Isso reduz duplicação de freshness, porém **não é requisito para correção** se o V8 freshness
gate for obedecido. O importante é: evidence embutida em page cache nunca pode ser aceita só
porque "existe".

---

# 54. Lazy evidence completion

Não desligar light search para tudo apenas porque existe Hide Unreleased.

Criar algo conceitualmente como:

```ts
ensureReleaseEvidenceForFilter(
  metas,
  context
)

```

ou:

```ts
ensureMovieReleaseEvidence(...)

```

chamado somente quando:

```text
movie hide-unreleased está ativo
+
evidence necessária está ausente/incompatível

```

---

# 55. Lazy movie evidence

Fluxo:

```text
meta já possui Schema 2 adequado
→ zero request adicional

meta possui tmdbId mas evidence ausente/schema1
→ buscar/reusar TMDB release_dates cache
→ normalizar Schema 2

sem tmdbId
→ UNKNOWN

```

Não realizar network call regional.

A chamada upstream continua region-neutral.

---

# 56. Concurrency e request budget da evidence completion

Não usar concorrência irrestrita.

Definir explicitamente:

```text
single-flight key
= tmdbId + RELEASE_EVIDENCE_SCHEMA

max concurrent release evidence fetches
= limiter existente ou limite explícito

max additional evidence lookups per catalog/search request
= budget controlado

timeout
= bounded

failure/UNKNOWN cache
= curto e distinto de success evidence
```

Se o budget for excedido:

```text
UNKNOWN
→ SHOW
```

é preferível a bloquear a request inteira ou criar fanout descontrolado.

A chamada upstream continua region-neutral.
Nunca criar single-flight separado por BR/US/usuário.

---

# 57. Movie metadata provider — TMDB

Já possui:

```text
release_dates

```

Schema 2 pode ser construído diretamente.

---

# 58. Movie metadata provider — TVDB

Quando resolve TMDB ID, já consegue consultar:

```text
movieReleaseDates(tmdbId)

```

Continuar.

Regional behavior funciona independentemente do metadata provider escolhido quando houver mapping TMDB.

---

# 59. Movie metadata provider — IMDb/Cinemeta

Quando há TMDB ID, o builder já faz TMDB enrichment com:

```text
release_dates

```

Continuar.

---

# 60. Movie sem TMDB mapping

Não existe fonte equivalente confiável para #742.

Resultado:

```text
UNKNOWN
→ SHOW

```

Isso é comportamento deliberado.

---

# 61. Anime movie

> **Correção normativa V14:** `anime.movie` é movie-like somente após resolução semântica/typed movie identity; veja seções 361–362.

Se mapping TMDB existir:

```text
movie evaluator normal

```

Anime movie não deve escapar do filtro apenas porque veio de:

```text
MAL
Kitsu
AniList

```

Sem TMDB mapping:

```text
UNKNOWN

```

---

# 62. Series — TMDB full meta

Evidence existente:

```text
first_air_date
status

```

Adequado após normalização.

---

# 63. Series — TVDB full meta

Evidence:

```text
firstAired
status.name

```

Adequado.

---

# 64. Series — IMDb/Cinemeta gap

`buildImdbSeriesResponse()` atualmente faz TMDB enrichment para:

```text
content_ratings
videos

```

Quando `tmdbId` existe, aproveitar o `tvInfo` já consultado para completar, quando ausentes:

```text
released / first_air_date
status

```

Não adicionar segunda TMDB request se os dados já estiverem no mesmo response.

---

# 65. `parseMedia()` TMDB

Corrigir:

```ts
released:
  new Date(el.first_air_date)

```

quando campo é ausente.

Usar helper:

```ts
parseValidReleaseDate(...)

```

Também preservar:

```text
status

```

para series.

---

# 66. TMDB Search Light

Não obrigar full hydration para toda série.

Se:

```text
first_air_date presente

```

isso normalmente basta:

```text
passada → RELEASED
futura  → UNRELEASED

```

Somente resultado ambíguo sem date e com filtro ativo precisa de enrichment de status, se isso for economicamente justificável.

Caso contrário:

```text
UNKNOWN

```

é seguro.

---

# 67. TMDB People Search

Corrigir o mesmo risco de:

```text
new Date(undefined)

```

Não transformar ausência em `Invalid Date`.

Status enrichment seletivo segue a mesma regra da busca comum.

---

# 68. AI Search

Como faz TMDB match/enrichment, correções em:

```text
parseMedia
release evidence
central filter

```

devem cobrir esse caminho.

Remover policy duplicada do próprio branch.

---

# 69. IMDb Suggestions e Lumiere

Como acabam hidratando por fluxos TMDB, devem herdar o comportamento central.

Não criar regras paralelas.

---

# 70. TVDB Search

Já obtém extended details com:

```text
firstAired
status

```

Integrar ao evaluator central.

---

# 71. TVMaze Search

`parseTvmazeResult()` atualmente preserva:

```text
premiered

```

mas não:

```text
show.status

```

Adicionar:

```ts
status: show.status || null

```

---

# 72. Trakt Search

Já possui evidence utilizável:

```text
first_aired/released
status

```

Não criar branch de policy separado.

---

# 73. MDBList Search

Já possui:

```text
released
status

```

Centralizar avaliação.

---

# 74. Simkl Search

Já possui:

```text
released
status

```

Remover movie policy duplicada do provider após neutralização da search.

---

# 75. Kitsu

Preserva:

```text
startDate
status

```

Integrar.

---

# 76. MAL/Jikan

Fluxos normais preservam:

```text
aired.from
status

```

Integrar.

---

# 77. AniList bug

Hoje existe caminho que fabrica status usando apenas `endDate`:

```text
endDate
→ Finished Airing

sem endDate
→ Currently Airing

```

Isso destrói:

```text
NOT_YET_RELEASED

```

Preservar/mapear o status real do AniList.

---

# 78. MAL User List / Suggestions

As chamadas atuais incluem:

```text
start_date
end_date

```

mas não:

```text
status

```

Adicionar `status` aos fields.

Não fabricar status apenas com `end_date`.

Preservar:

```ts
node.status

```

---

# 79. Anime parser não-batch

Garantir que:

```text
released
status

```

tenham semântica equivalente no parser batch e non-batch.

---

# 80. StremThru standard items

Quando passam por:

```text
getMeta()

```

usar evidence completa disponível.

Fallback item sem:

```text
released
status
tmdb mapping

```

permanece:

```text
UNKNOWN

```

---

# 81. Custom manifests

Mesma filosofia.

```text
pode hidratar
→ evidence

não pode hidratar
→ UNKNOWN

```

Não inventar dados.

---

# 82. Recommendations

Picks hidratados por `getMeta()` e enviados pelo catálogo normal devem receber a policy comum.

Não implementar filtro separado em recommendations.

---

# 83. Personal lists

Também devem continuar passando pelo pipeline normal.

Nenhum bypass regional específico.

---

# 84. Jellyfin

O browser interno que consome a rota Stremio do próprio AIOmetadata herda catalog filtering.

Endpoints Jellyfin específicos como:

```text
people
similar items
resume internals
playback
playstate

```

não entram automaticamente na feature.

---

# 85. Merged catalogs

Regra:

```text
merged catalog explicit region
→ global releaseRegion
→ Worldwide

```

Nunca tentar combinar:

```text
source A = US
source B = BR
source C = GB

```

para produzir uma região implícita.

A resposta final é governada pelo contexto do merged catalog.

---

# 86. Episódio/Up Next permanece separado

Preservar semânticas próprias como:

```text
MDBList Up Next metadata.hideUnreleased

```

Não converter isso para title Release Visibility.

---

# 87. Calendar catalogs

Mesmo princípio para:

```text
Trakt Calendar
Simkl Calendar

```

Episódio futuro:

```text
≠
série inteira unreleased

```

---

# 88. Caches e estados relevantes para correctness

A auditoria V5 confirmou mais superfícies que as quatro listadas anteriormente.

Existem pelo menos estas classes:

```text
1. Catalog result cache
2. Search result cache
3. Meta/component hot cache
4. Standard filtered-pagination cursor
5. Custom/StremThru cursor
6. Merged catalog cursor
7. Comprehensive warmer cursor coupling
8. Jellyfin pageLengths/catalogLengths
9. Jellyfin walkCursors
10. Jellyfin Collection Builder memberCursors
11. Cold store component rows
```

Nem todas armazenam payload de catálogo, mas todas podem preservar uma decisão
de membership/offset produzida sob um contexto antigo.

Correctness exige tratar explicitamente cada uma.

---

# 89. Catalog cache

O catálogo upstream/cacheado deve continuar region-neutral.

Adicionar ao profile quando o payload puder conter release evidence normalizada:

```ts
releaseEvidenceSchema:
  RELEASE_EVIDENCE_SCHEMA

```

Não adicionar:

```text
releaseRegion

```

ao neutral catalog cache.

---

# 90. Search cache

Após neutralização:

```text
region
hide flag
visibility day

```

não participam.

Enquanto o payload cacheado carregar Schema 2:

```text
releaseEvidenceSchema

```

participa.

---

# 91. Meta/component cache — problema

Hoje `_releaseAvailability` é armazenado dentro do componente:

```text
basic

```

Mas o mesmo `commonHash` também identifica componentes como:

```text
basic
cast
director
writer
links
trailers
extras

```

Colocar:

```text
RELEASE_EVIDENCE_SCHEMA

```

no `commonHash` inteiro funcionaria, mas invalidaria mais metadata do que necessário.

---

# 92. Meta/component cache — solução ideal V5

Criar componente próprio:

```text
releaseEvidence
```

Exemplo conceitual:

```text
meta-h:<identity>:<id>

basic
poster:<hash>
background:<hash>
logo:<hash>
videos:<hash>
cast
director
writer
links
trailers
extras
releaseEvidence:v2
```

Integração obrigatória em `getCache.ts`:

```text
buildMetaComponentCacheKeys
buildMetaHashLayout
writer
reconstructor
integrity/manifest semantics
legacy inline stripping
component refresh/upsert
```

Também revisar:

```text
metaHashMigration.ts
```

para que o novo prefixo/componente não fique fora de futuras rotinas de migração.

O componente precisa de uma operação de refresh/upsert própria:
`writeMetaHashFill()` com FNX não é suficiente para atualizar evidence envelhecida.

---

# 93. Remover evidence de `basic` e definir o meta-hash contract

Na HEAD auditada, `_releaseAvailability` é gravado dentro do componente `basic` do meta hash.
Isso amarra a freshness do fato de release à lifetime do metadata básico.

Novo writer:

```text
basic
→ sem _releaseAvailability
```

Componente opcional separado:

```ts
{
  _releaseAvailability: ReleaseAvailabilityV2
}
```

com layout conceitual:

```text
meta-h:<identity>:<id>
  basic
  poster...
  releaseEvidence:v2   ← optional, TTL próprio
```

Requisitos para `getCache.ts` + `metaHashStore.ts`:

```text
- releaseEvidence NÃO entra em MANIFEST_COMPONENTS obrigatórios;
- expirar releaseEvidence NÃO torna o meta "corrupted";
- writeMetaHashReplace do basic não renova evidence;
- evidence deve ser escrita/fill em operação com TTL próprio;
- TTL do component <= freshness factual do raw source;
- sourceFetchedAt é herdado do raw envelope, nunca = write time do component;
- cold-store write-through omite releaseEvidence na primeira implementação;
- leitura de basic antigo contendo Schema 1 faz strip/ignore para regional policy;
- ausência do component → lazy completion quando a policy exigir.
```

A infraestrutura `HSETEX`/TTL-per-field existente pode ser reutilizada; `metaHashStore.ts`
é **must-audit/must-test** mesmo que a implementação final não exija um diff nele.

A correção da feature não pode depender de o component estar presente. O owner factual
continua sendo o raw TMDB release-dates cache.

---

# 94. Vantagem e limite do componente separado

Mudança de evidence:

```text
Schema 2 → Schema 3
```

não precisa invalidar:

```text
cast
directors
writers
links
trailers
art
basic textual metadata
```

Apenas `releaseEvidence` é reconstruído.

Mas o component é uma **hot optimization**, não uma segunda fonte de verdade.

```text
raw TMDB envelope
→ factual source + sourceFetchedAt

releaseEvidence component
→ derivação normalizada cacheável
```

Se os dois discordarem por freshness, o raw owner/freshness contract vence.

---

# 95. Compatibilidade com basic antigo

Um cache antigo pode conter:

```text
basic._releaseAvailability.schema=1

```

Ao reconstruir na nova versão:

```text
não aceitar esse campo como regional Schema 2

```

Opções:

```text
strip/ignore inline legacy evidence

```

e buscar:

```text
releaseEvidence:v2

```

Se não existir:

```text
rehydrate
ou
UNKNOWN

```

---

# 96. Cold store — regra V5

Não colocar `releaseEvidence` no cold store genérico na primeira implementação.

Motivo:

```text
META_TTL hot default ~7d

cold stable default ~60d
cold frozen default ~180d
```

Uma ausência regional:

```text
coverage=available
BR sem 4/5/6 hoje
```

pode mudar amanhã se o TMDB receber nova informação.

Congelar esse negative-by-absence fact por 60/180 dias faria o read-through reintroduzir
evidence velha depois que o Redis expirasse.

Estratégia inicial recomendada:

```text
basic/art/cast/etc
→ cold store normal

releaseEvidence
→ hot cache only
→ TTL/freshness bounded
→ rehydrate via raw TMDB cache/upstream quando necessário
```

Evolução futura aceitável:

```text
component-specific cold TTL
+
stored/observed timestamp
+
read rejection quando evidence stale
```

Teste obrigatório:

```text
old cold-store basic Schema 1
→ deploy novo
→ read-through
→ Schema 1 não reaparece como Schema 2
```

e:

```text
regional evidence ausente
→ hot TTL expira
→ upstream/raw cache recebe novo BR release
→ old cold row NÃO pode ressuscitar ausência
```

---

# 97. Solução intermediária aceitável

Se o componente separado tornar o PR #742 grande demais:

```text
bump do commonHash

```

é funcionalmente aceitável.

Mas deve ser documentado como:

```text
invalidação ampla transitória

```

e não solução ótima.

---

# 98. Não alterar CACHE_EPOCH global

Evitar:

```text
CACHE_EPOCH bump

```

porque invalidaria cache não relacionado.

Usar versionamento específico da feature.

---

# 99. Raw TMDB `release_dates` — contrato único de freshness, writer e refetch

A HEAD auditada possui dois consumidores que competem pela mesma key:

```text
tmdb:movie:release_dates:<id>
```

com contratos atuais diferentes:

```text
movieReleaseDates()
→ raw request
→ TTL 7 dias

getMovieCertifications()
→ normalizeTmdbReleaseDatesForCache()
→ TTL 24 horas
→ mesma key
```

Isso torna a freshness efetiva dependente de qual writer venceu primeiro.

## Owner obrigatório V8

Criar um único primitive/cache owner, por exemplo:

```ts
getCachedTmdbMovieReleaseDates(
  tmdbId,
  config,
  {
    maxAgeMs?,
    requireUpstreamRevalidation?: boolean,
  }
)
```

retornando internalmente algo como:

```ts
interface CachedReleaseDatesEnvelope {
  schema: 1;
  source: 'tmdb_release_dates';
  sourceFetchedAt: string;
  payload: TmdbReleaseDates;
}

interface ReleaseDatesRead {
  envelope: CachedReleaseDatesEnvelope | null;
  fresh: boolean;
  cacheState: 'hit' | 'miss' | 'revalidated' | 'stale' | 'error';
  freshUntilMs: number | null;
}
```

Todos os consumidores — certification, movie metadata, search enrichment e
`ensureMovieReleaseEvidence()` — reutilizam esse primitive.

A key permanece region-neutral e possui:

```text
raw cache schema/version
canonical normalizer
single TTL/freshness contract
single-flight
sourceFetchedAt real
```

`normalizeTmdbReleaseDatesForCache()` continua preservando, de forma determinística:

```text
iso_3166_1
release_date
type
certification/note quando necessários para consumidores existentes
```

## Freshness recomendada

Para manter pelo menos a freshness do writer mais conservador atual:

```text
raw success TTL nominal = 24h
regional negative max age = 6h
transient revalidation failure backoff = ~5 min
```

Os valores podem virar constantes/settings se o maintainer preferir; os testes usam relógio
injetado e não números mágicos espalhados.

## Forced factual revalidation

`cacheWrapGlobal()` hoje possui bypass de read ligado ao conceito de `sourceList`.
Release dates precisam de um caminho explícito e semanticamente próprio.

Não fazer:

```text
DEL key
→ fetch
```

porque abre race com readers normais.

Fazer uma destas implementações:

```text
A. generalizar cacheWrapGlobal com forceRefetch seguro
   + flightKey distinto de read normal
   + atomic overwrite on success
```

ou:

```text
B. owner release-dates implementa seu próprio refetch single-flight
   + chama upstream diretamente
   + writeGlobalCache apenas após sucesso
```

Em ambos:

```text
stale cached value não satisfaz requireUpstreamRevalidation
refetch não se junta a um plain-read flight já em curso
failure não rejuvenesce sourceFetchedAt
failure não sobrescreve um last-known-good envelope
regional stale-negative + failure → UNKNOWN → SHOW
```

Nunca:

```text
raw payload lido do Redis com 6 dias
→ normalizar hoje
→ sourceFetchedAt = agora
```

Isso lava a idade do fato.

Não é necessário invalidar `CACHE_EPOCH` global; versionar este namespace/schema.

---

# 100. Filtered pagination — gap crítico do V3

`catalogPagination.ts` mantém cursor para continuar catálogos depois de filters removerem itens.

A chave atual é conceitualmente:

```text
userUUID
catalog
type
genre

```

Mas o cursor depende do conjunto de itens que sobreviveu ao filtro.

Portanto um cursor produzido com:

```text
BR

```

não pode ser reutilizado por:

```text
US

```

nem:

```text
Worldwide

```

---

# 101. Exemplo de bug de cursor

Upstream:

```text
A → BR
B → US only
C → BR
D → US only
E → BR

```

Com BR:

```text
visible:
A C E

```

Cursor aprende a posição upstream correspondente.

Usuário muda para US.

Se a chave for a mesma, a próxima página pode:

```text
pular item
duplicar item
ficar curta
começar no offset errado

```

Mesmo se o evaluator estiver perfeito.

---

# 102. Virada de dia e cursor

Também:

```text
19/10 23:59

BR release 20/10
→ HIDE

```

cursor é calculado.

À meia-noite:

```text
20/10 00:00
→ SHOW

```

Se o cursor antigo continuar no mesmo namespace:

```text
paginações podem continuar inconsistentes

```

---

# 103. Canonical Source Profile + Filter Signature + Pagination Contract

O V8 separa três dimensões independentes:

```text
sourceMembershipSignature
→ qual sequência upstream/ordem está sendo paginada

filterSignature
→ qual subconjunto pós-cache sobrevive

paginationContractSignature
→ como offsets/pages/cursors são interpretados
```

Criar um **CanonicalCatalogSourceProfile** e derivar dele duas coisas sem duplicar lógica:

```text
1. neutral page-cache identity
2. sourceMembershipSignature do cursor
```

Isso é obrigatório. Não pode existir um conjunto de inputs no page cache e outro diferente
no cursor.

Para TMDB Discover, o source profile incorpora/reutiliza `computeDiscoverSignature()`.

Para TMDB Collection, inclui ao menos:

```text
collection id
sortDirection
metadata.hideUnreleased
UTC logical day quando legacy hideUnreleased=true
```

Para merged/external/provider lists, incluir somente inputs que mudam membership/ordem.

Criar/versionar:

```ts
CATALOG_SOURCE_SIGNATURE_VERSION = 1;
CATALOG_FILTER_SIGNATURE_VERSION = 1;
PAGINATION_CONTRACT_SIGNATURE_VERSION = 1;
```

`paginationContractSignature` inclui pelo menos:

```text
CACHE_EPOCH efetivo
cursor schema
pagingMode
resolved upstream pageSize
target filtered pageSize
fill/dedupe policy version
max-page/budget policy version quando alterar observável
```

Então a identidade de paging é:

```ts
interface PagingIdentity {
  sourceMembershipSignature: string;
  filterSignature: string;
  paginationContractSignature: string;
}
```

A filter signature recebe APENAS o contexto efetivo/canônico já resolvido.

Não hashear:

```text
API keys
tokens
secrets
whole raw config
whole raw catalog metadata
```

Canonicalização obrigatória:

```text
objetos → stableStringify
arrays semanticamente unordered → sort + dedupe
region → uppercase normalizada
regex → string exata
undefined/null/default → uma forma canônica
```

Testes obrigatórios:

```text
mesma policy efetiva com ordem de objeto diferente → mesma signature
BR → US → diferente
hide ON → OFF → diferente
API key A → B sem mudança de membership → mesma filter signature
CATALOG_LIST_ITEMS_SIZE 20 → 30 → paginationContractSignature diferente
CACHE_EPOCH 2 → 3 → paginationContractSignature diferente
Collection sortDirection asc → desc → source signature e page-cache identity diferentes
Collection hideUnreleased OFF → ON → source signature e page-cache identity diferentes
```

---

# 104. Filter profile recomendado

O profile deve ser derivado de `CanonicalFilterContext`, por exemplo:

```ts
{
  version:
    CATALOG_FILTER_SIGNATURE_VERSION,

  releasePolicyVersion:
    RELEASE_VISIBILITY_POLICY_VERSION,

  releaseEvidenceSchema:
    RELEASE_EVIDENCE_SCHEMA,

  mediaType,
  surface,

  movieHideUnreleased,
  seriesHideUnreleased,

  effectiveReleaseRegion,

  ageRating,
  allowUnratedContent,

  exclusionKeywords,
  exclusionGenres,
  regexExclusionFilter,

  hideWatchedTrakt,
  hideWatchedAnilist,
  hideWatchedMdblist,
  hideWatchedSimkl,

  effectiveCatalogOverrideFingerprint
}
```

`logicalDay` entra no namespace quando a policy daquele fluxo depende de calendar-day.

Decisões com boundary intra-day usam `validUntil`, não uma falsa granularidade diária.

Não colocar `catalogOverrides` inteiro; somente valores efetivos que alteram membership.

---

# 105. Minimum release-specific context

Mesmo numa divisão de PRs, a camada release visibility precisa no mínimo de:

```text
signature version
release policy version
evidence schema
effective release region
request evaluation clock
visibility day/boundary
effective hide flag
catalog override/provenance
```

Porém, se o PR tocar filtered pagination/cursor, o V8 **não permite** omitir:

```text
sourceMembershipSignature
filterSignature
paginationContractSignature
validUntil aggregate
```

A divisão em PRs pode separar implementação; não pode criar um estado intermediário em que o
novo filtro escreva/consuma cursor sem essas identidades.

---

# 106. Dynamic watched state

Hide Watched altera membership sem necessariamente alterar config. Como o V8 já modifica o
contrato de cursor, deixar esse estado fora da identidade criaria uma incoerência conhecida.

Resolver `RuntimeFilterState` uma vez por request e derivar revision/validity para:

```text
Trakt watched dataset/activity fingerprint
AniList watched dataset/revision
MDBList watched dataset/revision
Simkl watched dataset/activity fingerprint
```

Não usar credential como revision.

Se um provider não expuser revision barata, usar hash determinístico do conjunto já carregado
para aplicar o filtro; isso não exige nova chamada apenas para assinar o cursor.

A mudança de runtime revision invalida o cursor mesmo quando `CanonicalFilterContext` está
idêntico.

Search atualmente exclui Hide Watched por regra existente, portanto não recebe essa dimensão
até que essa policy seja alterada em change separado.

---

# 107. Standard cursor key V8

Evoluir conceitualmente de:

```text
catalog-cursor:v3:
userUUID:
cleanId:
type:
genre
```

para:

```text
e<CACHE_EPOCH>:catalog-cursor:v5:
userUUID:
cleanId:
type:
genre:
sourceMembershipSignature:
filterSignature:
paginationContractSignature
```

Cursor payload recomendado:

```ts
interface FilteredCursorV5 {
  schema: 5;
  served: number;
  upstreamPage: number;
  upstreamOffset: number;

  sourceMembershipSignature: string;
  filterSignature: string;
  paginationContractSignature: string;

  /**
   * Menor deadline agregado de temporal/evidence/runtime/source stability.
   */
  validUntilMs?: number | null;
}
```

`startOffset` pode continuar como nome interno se já usado pelo helper, mas o contrato deve
ser unívoco: é offset dentro da upstream page indicada, não skip global.

Cursor sem schema/identity V8 é miss, nunca best-effort reuse.

---

# 108. Custom/StremThru cursor — segundo sistema

`getCatalog.ts` possui cursor independente para external/custom addons.

Ele também precisa de:

```text
filterSignature
validUntilMs
namespace versionado
```

Não corrigir apenas `catalogPagination.ts`.

Criar key builder compartilhado, por exemplo:

```ts
buildExternalCatalogCursorKey(...)
```

Nenhum caller, inclusive warmer, deve reconstruir a string manualmente.

---

# 109. External cursor key

Conceitualmente:

```text
catalog-cursor:external:v2:
userUUID:
catalogId:
type:
genre:
filterSignature
```

Payload:

```text
served
upstreamOffset
seenIds
validUntilMs
```

Ao mudar região/policy/dia ou atingir `validUntilMs`:
o cursor anterior não é reutilizado.

---

# 110. Merged cursor — terceiro sistema obrigatório

A base atual possui também:

```text
merged-cursor:
userUUID:
catalogId:
genre
```

dentro de `getCatalog.ts`.

Esse cursor é produzido DEPOIS que cada source page passa por `applyCatalogFilters()`.
Logo ele depende diretamente de membership e não pode ficar fora da #742.

Evoluir para algo como:

```text
merged-cursor:v2:
userUUID:
catalogId:
type:
genre:
mergedDefinitionSignature:
filterSignature
```

`mergedDefinitionSignature` deve capturar, pelo menos:

```text
ordered source catalog ids
source types
source genres/defaults relevantes
merge mode
```

para impedir que editar a composição do merged catalog reutilize um cursor antigo.

Payload também deve carregar:

```text
validUntilMs
```

Testes:

```text
BR page1/page2 → US
midnight boundary
source order change
merge mode change
```

---

# 111. Jellyfin pagination state — quarta superfície

Jellyfin herda o filtro pela rota Stremio, mas mantém estado próprio em memória/Redis:

```text
pageLengths
catalogLengths
walkCursors
Collection Builder memberCursors
```

As keys atuais são baseadas em usuário/catálogo/extras/tags, mas não carregam
a filter signature efetiva.

Portanto V5 exige um `pagingScope`/`filterSignature` no Jellyfin.

Exemplo:

```text
jf:v2:<user>:<catalog>:<extras>:<profile>:<filterSignature>
```

Para collection member cursors com múltiplas sources:

```text
combinedSourcePagingSignature
=
hash(
  source identity
  + each source filter signature
  + collection/folder definition
)
```

Também invalidar por temporal boundary.

Arquivos esperados:

```text
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
addon/lib/jellyfin/index.ts
quando necessário para propagar o scope
```

Jellyfin Search/Hints usa as rotas de search dos catálogos e herda a policy de Search.
Não criar segundo evaluator de release dentro do Jellyfin.

---

# 112. Temporal validity e filtered Search pagination

A afirmação anterior de que Search podia simplesmente "filtrar a página atual" é insuficiente.
Search é paginada para vários providers. Se 20 resultados upstream virarem 3 após os filtros,
existem resultados elegíveis na página seguinte que devem subir para preencher a página.

## Regra V8

O search cache continua neutro, mas a camada pós-cache ganha page fill quando a fonte suporta
paginação.

```text
neutral search page N
→ lazy evidence completion
→ applyCatalogFilters
→ se ainda faltam itens
→ neutral search page N+1
→ repetir até full/exhausted/budget
```

Resolver no `EffectiveSearchSourceContext`:

```ts
pagingMode: 'page' | 'offset' | 'none';
pageSize: number | null;
supportsFilteredFill: boolean;
```

### Sources pagináveis

Usar cursor/position mapping específico de Search, separado de catálogo:

```text
search-cursor:v1:
user:
searchSurface:
mediaType:
queryHash:
effectiveSourceSignature:
filterSignature:
paginationContractSignature
```

Não colocar query em claro no log/key se um hash estável for suficiente.

### Sources não pagináveis

```text
pagingMode=none
→ filtra a resposta única
→ página curta é comportamento inevitável/documentado
→ não inventar novas chamadas upstream
```

### Validade temporal

Regional day-only, Worldwide/Series timestamps e evidence freshness usam a mesma validade
agregada dos catálogos.

```text
Date.now() >= validUntilMs
→ cursor inválido
→ recomputar a posição segura
```

Search cursor guarda posição/identidade, nunca payload user-specific.

---

# 113. Evidence freshness, runtime state e paginação

`fillFilteredPage()` e o equivalente de Search devem receber um callback/contexto capaz de:

```text
completar evidence necessária
→ resolver runtime filter state uma vez
→ avaliar visibility
→ aplicar demais filtros
→ retornar metas + validity contributions
```

O cursor só é gravado depois do conjunto final estar definido.

## Freshness factual

```text
freshness efetiva de evidence
=
min(
  freshness do releaseEvidence component,
  freshness factual do raw release_dates que o originou
)
```

Para negative-by-absence:

```text
raw source age >= regionalNegativeMaxAge
→ não basta re-normalizar o mesmo raw cache
→ fresh upstream revalidation
→ falhou: UNKNOWN → SHOW
```

## `validUntilMs` obrigatório

A boundary do cursor é o mínimo de **todas** as condições conhecidas capazes de mudar
membership/posição:

```text
validUntilMs = min(
  temporalTransitionAt,
  releaseEvidenceFreshUntil,
  dynamicFilterStateValidUntil,
  sourcePageStableUntil,
  explicitCursorMaxTtlDeadline
)
```

Contribuição inexistente = `Infinity`, não `0`.

Exemplos:

```text
movie BR ausente + negative evidence fresh por mais 2h
→ cursor não vive além dessas 2h

movie BR future date daqui a 10 dias + raw fact fresh por 6h
→ cursor expira em 6h para permitir mudança factual

series estreia às 14:00 hoje
→ temporal transition = 14:00

Worldwide recente sem home release
→ temporal transition pode ser min(homeReleaseAt, releasedAt + 365d)
```

Future date já conhecida não exige refetch no instante da virada; o evaluator muda a decisão
com o relógio. Refetch serve para descobrir fatos novos/alterados.

---

# 114. Config persistence

`releaseRegion` pode ser persistido como parte normal do config.

Sem whitelist adicional da feature.

Ainda assim criar teste explícito:

```text
save
reload
→ releaseRegion preservada

```

---

# 115. Export/import de config

Testar explicitamente:

```text
BR
→ export
→ import
→ BR

```

e:

```text
config antiga sem releaseRegion
→ import
→ Worldwide

```

---

# 116. UI — Filters Settings

Movie card:

```text
Digital Release Filter

[ ] Hide Unreleased Movies in Catalogs

[ ] Hide Unreleased Movies in Search

Release Region
[ Worldwide — current behavior ▼ ]

```

---

# 117. UI — Series

Continuar separado:

```text
Unreleased Shows Filter

[ ] Hide Unreleased Shows in Catalogs

[ ] Hide Unreleased Shows in Search

```

Não exibir Release Region como se afetasse séries.

---

# 118. Country picker

Reutilizar países TMDB.

Ordenação recomendada:

```text
Worldwide
──────────
países em ordem alfabética localizada

```

Valor salvo:

```text
ISO 3166-1 alpha-2

```

---

# 119. Settings Search

Adicionar termos:

```text
Release Region
Digital Release Region
Regional Release
Country
Hide Unreleased Region
Movie Release Region

```

Apontar para o setting correto.

---

# 120. Config import validation

Config importada contendo:

```text
releaseRegion=br

```

deve normalizar:

```text
BR

```

Inválida:

```text
ZZ

```

→ Worldwide em runtime.

Idealmente UI também sinaliza configuração inválida em vez de salvar novamente silenciosamente.

---

# 121. `parseValidReleaseDate`

Criar helper único para timestamps de series e metadata geral.

Retorno:

```text
Date válido
ou null

```

Nunca deixar:

```text
Invalid Date

```

entrar no evaluator.

---

# 122. Reason codes — Movie

Sugestão:

```text
legacy-future-primary-release
legacy-over-one-year
worldwide-home-release
worldwide-home-release-missing

regional-home-release
regional-home-release-future
regional-home-release-not-confirmed

release-evidence-empty
release-evidence-unavailable
release-evidence-schema-legacy

tmdb-id-unavailable
invalid-release-date

```

---

# 123. Reason codes — Series

```text
first-air-past
first-air-future

prerelease-status
postrelease-status

release-evidence-unavailable
invalid-release-date
ambiguous-status

```

---

# 124. Logs

Não logar cada item em `info`.

Usar agregados em `debug`.

Exemplo:

```text
ReleaseVisibility:
surface=catalog
catalog=tmdb.trending
type=movie
region=BR
day=2026-09-23
released=15
unreleased=5
unknown=2
evidenceFetches=3

```

---

# 125. Métricas opcionais

Se integrado ao dashboard/metrics:

```text
release_visibility_evaluated
release_visibility_released
release_visibility_unreleased
release_visibility_unknown
release_evidence_lazy_fetch
release_evidence_lazy_fetch_failed

```

Evitar cardinalidade alta com IDs individuais.

---

# 126. Test infrastructure

Projeto continua sem Jest/Vitest dedicado para essa feature.

Usar:

```text
node:test

```

com TypeScript via infraestrutura disponível.

Evitar adicionar framework grande apenas para #742.

---

# 127. Unit tests — CalendarDate

Testar:

```text
valid YYYY-MM-DD

TMDB timestamp
→ same calendar date

invalid string

invalid leap day

valid leap day

month 13

day 00

```

---

# 128. Unit tests — evidence normalization

Testar:

```text
results missing
→ coverage unavailable

results=[]
→ coverage empty

results with invalid entries only
→ coverage empty

US theatrical only
→ available
→ US in regionsWithReleaseRecords
→ no US home date

US digital
→ US home date

US physical earlier than digital
→ earliest chosen

multiple countries
→ map complete

```

---

# 129. Movie Worldwide matrix

Obrigatório:

```text
future primary release
recent + digital past
recent + digital future
recent + no home release
older than 365 days
no released field
Schema 1
Schema 2
results=[]
no release data

```

Resultado deve corresponder ao comportamento legado.

---

# 130. Movie regional matrix

```text
BR Digital past
BR Digital future

BR Physical past
BR Physical future

BR TV past
BR TV future

BR theatrical only

US home release past
BR absent

US home release future
BR absent

coverage empty

coverage unavailable

Schema 1

no TMDB id

invalid region

lowercase br

timezone boundary

```

---

# 131. Teste principal da #742

Dados:

```text
US Digital:
2026-09-10

BR Digital:
2026-10-20

```

Em:

```text
2026-09-23

```

Resultado:

```text
Worldwide → SHOW
US        → SHOW
BR        → HIDE

```

Em:

```text
2026-10-20

```

após início do dia local BR:

```text
BR → SHOW

```

---

# 132. Series matrix

```text
past date + Continuing
→ SHOW

past date + In Production
→ SHOW

past date + Planned
→ SHOW pela prioridade da data

future date
→ HIDE

future date + Continuing
→ HIDE pela prioridade da data

no date + Upcoming
→ HIDE

no date + Planned
→ HIDE

no date + Not Yet Aired
→ HIDE

no date + NOT_YET_RELEASED
→ HIDE

no date + In Production
→ HIDE

no date + Finished Airing
→ SHOW

no date + Currently Airing
→ SHOW

no date + Ended
→ SHOW

no date + unknown status
→ UNKNOWN → SHOW

invalid date + no status
→ UNKNOWN → SHOW

```

---

# 133. Provider matrix

Validar evidence final produzida por:

```text
TMDB
TVDB
IMDb/Cinemeta
TVMaze
Trakt
MDBList
Simkl
Kitsu
MAL/Jikan
AniList
StremThru
Custom

```

Não basta testar só evaluator com mocks perfeitos.

---

# 134. Search matrix

```text
search.movie
search.series

search.anime_movie
search.anime_series

people_search.movie
people_search.series

gemini.search

IMDb suggestion
Lumiere
TVDB search
TMDB search
Trakt search
MDBList search
Simkl search
TVMaze search

```

---

# 135. Search neutrality test

Primeiro request:

```text
Hide Unreleased Search = OFF

```

aquecer cache.

Segundo:

```text
Hide Unreleased Search = ON
BR

```

Resultado precisa ser filtrado corretamente SEM depender de rebuild do search cache regional.

Depois:

```text
US

```

mesmo neutral search cache pode ser reutilizado com decisão diferente.

---

# 136. Catalog matrix

No mínimo:

```text
TMDB
TVDB
Trakt
MDBList
Simkl
Letterboxd
MovieLens
PublicMetaDB
FlixPatrol
MAL
AniList
Streaming
Recommendations
Custom
StremThru
Merged
personal lists
imported Discover catalogs

```

---

# 137. Cursor matrix — obrigatória

Cobrir todos os sistemas de cursor/paging state.

```text
STANDARD
BR page1
BR page2
switch US
→ US sequence limpa

EXTERNAL CUSTOM/STREMTHRU
BR page1/page2
switch Worldwide
→ sem skip/duplicate/gap

MERGED
BR page1/page2
switch US
→ sem cursor antigo

MERGED DEFINITION
source order A,B
→ change B,A
→ old cursor not reused

JELLYFIN
catalogLengths/walkCursor under BR
→ switch US
→ no stale StartIndex mapping

JELLYFIN COLLECTION
memberCursor with BR
→ switch US
→ no stale sourceOffset/seen
```

Falhas proibidas:

```text
duplicate
gap
short page causada por cursor antigo
wrong upstream offset
stale TotalRecordCount
```

---

# 138. Temporal transition matrix

Regional:

```text
BR 19/10 23:59
→ hidden

BR 20/10 00:00
→ visible

cursor 19/10
→ não reutilizado no dia 20
```

Worldwide/Series:

```text
future timestamp 14:30
cursor produzido 14:29
decision flips 14:30
→ validUntilMs invalida o cursor
```

365-day legacy boundary:

```text
releaseAt + 365d
→ cursor anterior não pode sobreviver à boundary
```

Timezone inválido:

```text
no crash
deterministic fallback
warning deduplicado
```

---

# 139. Custom/StremThru + warmer cursor matrix

Além da paginação normal, testar o warmer.

```text
external catalog
filter active
warm page 1
warmer reads next cursor using shared key builder
warm page 2
→ succeeds
```

Depois:

```text
BR → US
→ new key/signature
→ warmer does not continue BR cursor
```

O teste deve falhar se `comprehensiveCatalogWarmer.js`
hardcodar o namespace antigo.

---

# 140. Multi-user isolation

Mesmo cached movie:

```text
User A:
BR

User B:
US

```

Evidence:

```text
uma só

```

Policy:

```text
A → HIDE
B → SHOW

```

Sem duplicar raw/meta evidence por região.

---

# 141. Cache matrix

```text
CATALOG CACHE
neutral payload shared across BR/US

SEARCH CACHE
v2 neutral payload
old filtered cache cannot collide

META HOT CACHE
Schema 1 basic
→ ignored for regional

releaseEvidence:v2
→ shared across users/regions

COLD STORE
releaseEvidence absent by default
→ cannot resurrect stale missing-BR evidence

RAW TMDB
release_dates cache retained
→ can rebuild Schema 2

RESPONSE
internal release evidence stripped
→ never leaked to client
```

---

# 142. Evidence component migration + freshness tests

Obrigatório:

```text
old hot basic with Schema 1
→ new reader
→ regional evaluator does not trust as Schema 2

new releaseEvidence:v2
→ reconstructed internally

response serialization
→ no _releaseAvailability leak

hot releaseEvidence expires
→ old cold store does not restore it

TMDB/raw evidence gains BR record
→ next rehydrate observes BR

component refresh
→ replaces stale v2
→ does not require invalidating cast/art/links
```

---

# 143. Config matrix

```text
old config
new Worldwide
new BR
new US

save/reload

export/import

lowercase code

invalid code

legacy watch_region + release-type

runtime normalization

loadSharedConfig remains unmodified

```

---

# 144. Collection Builder matrix

Obrigatório:

```text
Discover catalog
region=BR
with_release_type=4|5|6

export/import/reconstruct
→ region continua BR
→ release type continua 4|5|6
→ formState.releaseRegion = BR
→ releasedOnly continua semanticamente equivalente

open editor
save
→ params.region continua BR
```

Também:

```text
watch_region=US
sem region
sem release-aware semantics
→ NÃO criar region=US
```

E provenance:

```text
region derivada apenas do idioma
+
global Release Region=Worldwide
→ comportamento definido explicitamente
→ não depender de efeito colateral do builder
```

---

# 145. Per-catalog override matrix

Movies:

```text
Global ON + catalog Global
Global ON + catalog Off
Global OFF + catalog On

```

Séries:

```text
Global ON + catalog Global
Global ON + catalog Off
Global OFF + catalog On

```

---

# 146. Performance tests

Medir no mínimo:

```text
p50
p95
p99

TMDB extra calls
release evidence cache hit rate

search latency:
filter OFF
filter ON

catalog latency:
cold
warm

```

Particularmente observar:

```text
search movie lazy release enrichment
ambiguous series search enrichment

```

---

# 147. Concurrency test

Executar simultaneamente:

```text
BR
US
Worldwide

```

para mesmos titles durante cold cache.

Validar:

```text
single-flight funciona
region não contamina evidence
resultado por user permanece correto

```

---

# 148. Failure tests

Simular:

```text
TMDB timeout
TMDB 429
TMDB 500
malformed release_dates
missing tmdb mapping
bad date
Redis temporarily unavailable
cold store stale Schema 1

```

Policy deve tender a:

```text
UNKNOWN → SHOW

```

quando não houver fato confiável.

---

# 149. Warmup

Warmup deve permanecer compatível com neutral caches.

Regras:

```text
não materializar regional policy em shared catalog/search cache

não criar evidence regional
→ somente normalized neutral evidence

não reconstruir cursor key manualmente
```

Achado V5 obrigatório:

`addon/lib/comprehensiveCatalogWarmer.js` hoje lê diretamente:

```text
catalog-cursor:<uuid>:<catalogId>:<type>:<genre>
```

após `getCatalog()` para continuar external custom/StremThru warming.

Ao versionar o external cursor, esse código quebraria depois da primeira página.

Correção:

```text
shared buildExternalCatalogCursorKey()
ou
API de getCatalog/fill que retorne próximo cursor/offset
```

Preferir não duplicar key format entre runtime e warmer.

Teste de warmup multi-page obrigatório.

---

# 150. ConfigVersion

`configVersion` não deve substituir a canonical filter signature nos caches compartilhados.

Para cursors/paging state user-scoped, pode ser usado como safety invalidator adicional
quando a estrutura do catálogo muda por fatores fora do filter profile.

Recomendação:

```text
filterSignature
→ semântica de membership

mergedDefinitionSignature
→ composição do merged catalog

configVersion
→ safety fallback user-scoped, quando útil
```

Evitar usar configVersion como identidade de shared neutral result cache,
porque invalida por mudanças sem relação.

---

# 151. PR strategy final V5

A implementação não deve ser um mega-PR.

O PR Guard atual limita, fora das isenções aplicáveis:

```text
changed files <= 25
additions + deletions <= 1200
```

Com as superfícies V5, um único PR A tende a ficar grande demais.

Sequência recomendada:

```text
PR 0
Search neutrality + SEARCH_RESULT_CACHE_SCHEMA_VERSION
+ remoção de provider-level Hide Unreleased policy

PR A1
Evidence Schema 2 dual semantics
+ CalendarDate helpers
+ Worldwide golden-master
+ releaseVisibility foundation
sem UI/regional behavior ainda

PR A2
releaseRegion config/UI
+ canonical FilterContext
+ regional evaluator
+ catalog/search policy
+ Discover provenance
+ Collection Builder reconstruction

PR A3
pagination correctness
+ standard cursor
+ external cursor
+ merged cursor
+ temporal validUntil
+ comprehensive warmer

PR A4
Jellyfin paging-state isolation
+ walk/length/member cursors

INTEGRATION PR / final PR in chain
Fixes #742
somente quando A1-A4 estiverem integrados

PR B
Series evidence hardening

PR C
releaseEvidence meta component
+ hot-only freshness
+ legacy basic migration

PR D
future regional streaming availability
fora da #742
```

Se PR C for necessário para correctness antes de #742 ser fechado,
mover sua parte mínima para A1/A2 e deixar apenas otimização/refactor no PR C.

Não colocar `Fixes #742` em PR intermediário que ainda deixa cursor/warmer/Jellyfin incorretos.

---

# 152. PR 0 — Search/filter architecture preparation

Objetivo:

```text
neutralizar search antes de #742

```

Escopo:

```text
remover provider-level duplicate
Hide Unreleased movie decisions

separar evidence acquisition de policy

garantir post-cache applyCatalogFilters

introduzir helpers necessários
sem mudar comportamento visível

```

Esse PR reduz muito o risco do PR #742.

---

# 153. PR A — Foundation + #742

Fecha:

```text
#742

```

Escopo:

```text
RELEASE_EVIDENCE_SCHEMA=2

RELEASE_VISIBILITY_POLICY_VERSION=1

CalendarDate helpers

coverage:
available/empty/unavailable

homeReleaseDaysByRegion

releaseRegion global

region validation

effective region resolver

runtime config normalization

regional movie evaluator

Worldwide legacy evaluator

catalog/search integration

filter signature

standard cursor isolation

custom/StremThru cursor isolation

timezone/day semantics

UI

settings search

movie tests

cache/search/cursor tests

```

---

# 154. PR B — Series Evidence Hardening

Escopo:

```text
series evaluator

status normalization

parseMedia Invalid Date

parseMedia status

IMDb/Cinemeta TMDB series enrichment

TVMaze status

AniList real status

MAL API real status

anime batch/non-batch consistency

series test matrix

```

---

# 155. PR C — Release evidence meta component

Se não entrar no PR A:

```text
releaseEvidence component

remove inline evidence from basic

old basic Schema 1 sanitation

cold store component

component-specific schema versioning

migration tests

```

Se o tamanho ainda respeitar PR Guard e reviewability, A+C podem ser unidos.

---

# 156. PR D — Regional streaming availability

Feature separada:

```text
Hide content unavailable from watch providers in selected region

```

Usaria:

```text
watch_region
provider availability

```

Não usar:

```text
release_dates

```

como substituto.

---

# 157. Arquivos esperados — PRs da #742

A auditoria V5 transforma alguns arquivos antes opcionais em obrigatórios.

```text
FOUNDATION / EVIDENCE
addon/utils/releaseAvailability.ts
addon/utils/releaseVisibility.ts      NEW
addon/utils/releaseRegion.ts          NEW
addon/utils/catalogFilterContext.ts   NEW ou equivalente
addon/utils/catalogFilterSignature.ts NEW
addon/utils/catalogFilters.ts
addon/utils/parseProps.js

SEARCH
addon/lib/getSearch.ts
addon/lib/getCache.ts

CONFIG / UI
addon/lib/configApi.js
addon/types/index.ts
configure/src/contexts/config.ts
configure/src/contexts/ConfigContext.tsx
configure/src/components/sections/FiltersSettings.tsx
configure/src/components/sections/CatalogsSettings.tsx
configure/src/lib/settingsSearchIndex.ts

DASHBOARD / TELEMETRY — DECISÃO EXPLÍCITA
addon/lib/dashboardApi.js
configure/src/components/dashboard/DashboardSystem.tsx

DISCOVER / IMPORT / AI CATALOG — OBRIGATÓRIO AUDITAR
configure/src/components/sections/DiscoverBuilderDialog.tsx
configure/src/lib/setup/streaming.ts
configure/src/components/setup/StreamingPickerDialog.tsx
addon/lib/collectionBuilder/catalogReconstruction.ts
addon/utils/ai-catalog-config-builder.ts
addon/utils/ai-catalog-schema.ts
addon/utils/ai-catalog-generation.ts
addon/utils/ai-catalog-sanitizer.ts
addon/utils/ai-catalog-entity-resolver.ts
addon/lib/tmdbDiscoverDateTokens.ts

Regra: nem todos esses arquivos necessariamente exigem diff, mas todos precisam
de teste/inspeção de contrato para garantir que region/watch_region/with_release_type
e release_date.* não sejam descartados, reescritos ou promovidos a release policy
sem provenance.

PAGINATION / ROUTE CALLERS — OBRIGATÓRIO
addon/lib/catalogPagination.ts
addon/lib/getCatalog.ts
addon/index.ts
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js

JELLYFIN — OBRIGATÓRIO PARA FULL PROJECT COVERAGE
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
addon/lib/jellyfin/index.ts
quando necessário para propagar paging scope

META COMPONENT / MIGRATION
addon/lib/getCache.ts
addon/lib/metaHashMigration.ts
addon/lib/metaColdStore/*
somente se a implementação tocar cold-storage behavior

TESTS
node:test files
fixtures de legacy/worldwide/region/cursor/cache

package.json
somente se adicionar script de test
```

Não tratar `catalogReconstruction.ts` nem `comprehensiveCatalogWarmer.js` como opcionais:
há comportamento concreto a corrigir neles.

---

# 158. Arquivos esperados — Series PR

```text
addon/utils/releaseVisibility.ts

addon/utils/parseProps.js

addon/lib/getMeta.js

addon/lib/getSearch.ts

addon/lib/getCatalog.ts

addon/lib/malTracker.ts

addon/utils/catalogFilters.ts

tests

```

---

# 159. Build validation

Obrigatório:

```bash
npm ci

npm run build:backend

npm run build

npm run lint:backend

npm run lint:frontend

npm run lint:repo

```

Também:

```bash
npm run lint

```

quando possível.

E:

```bash
npm test

```

ou script equivalente adicionado para `node:test`.

---

# 160. PR Guard

Workflow atual exige atenção para:

```text
changed files <= 25

total additions + deletions <= 1200

```

quando não houver bypass de trusted collaborator.

Também exige template completo.

Portanto cada PR precisa ser revisado antes de abrir.

Se ultrapassar:

```text
dividir

```

não tentar contornar.

---

# 161. PR body

Incluir:

```text
## Summary

## Linked Issue

## Type of Change

## Why This Approach

## Testing

## Documentation

## Author Checklist

## AI Usage Disclosure

```

E linkar explicitamente:

```text
Fixes #742

```

no PR que realmente fecha a issue.

---

# 162. Snapshot drift audit

O V3 foi escrito sobre:

```text
7ef886c6...

```

Antes do V5 ser fechado, `dev` avançou 8 commits para:

```text
26523cf4...

```

Arquivos centrais como:

```text
releaseAvailability.ts
catalogFilters.ts
getSearch.ts
getCache.ts
catalogPagination.ts
parseProps.js
getMeta.js
getCatalog.ts

```

não receberam alteração nesse delta que invalide os achados centrais.

Mudanças relevantes ao plano ocorreram principalmente em:

```text
configApi.js
index.ts
collectionBuilder/catalogReconstruction.ts

```

Por isso o V5 incorporou:

```text
loadSharedConfig clone safety

Collection Builder/import round-trip

novo snapshot

```

---

# 163. Rebase Gate definitivo

Antes da implementação:

```bash
git fetch origin dev
```

Confirmar HEAD.

Se não for:

```text
26523cf4e0be9a0b0fd513b4ec8530d346e87e18
```

refazer tree/search/compare em pelo menos:

```text
releaseAvailability
isReleasedDigitally
hideUnreleasedDigital
hideUnreleasedDigitalSearch
hideUnreleasedShows
hideUnreleasedShowsSearch

applyCatalogFilters
catalogFiltersActive

catalogPagination
catalog-cursor
merged-cursor

comprehensiveCatalogWarmer
warmExternalAddonCatalog

Jellyfin:
pageLengths
catalogLengths
walkCursors
memberCursors

getSearch
getCache
getMeta
getCatalog
parseMedia

releaseRegion
watch_region
with_release_type
discover.params.region
DiscoverBuilderDialog

loadSharedConfig
catalogReconstruction
cacheWarmer
dashboardApi
DashboardSystem
CatalogsSettings
ai-catalog-schema
ai-catalog-generation
ai-catalog-sanitizer
ai-catalog-entity-resolver
tmdbDiscoverDateTokens
setup/streaming
StreamingPickerDialog
addon/index.ts

metaHashStore
metaHashMigration
metaColdStore
```

Não implementar baseado cegamente neste snapshot se `dev` mudar.

---

# 164. Definition of Done — Movie #742

Cenário:

```text
US Digital:
2026-09-10

BR Digital:
2026-10-20

```

Data lógica:

```text
2026-09-23

```

Esperado:

```text
Worldwide → SHOW
US        → SHOW
BR        → HIDE

```

Em:

```text
America/Fortaleza
2026-10-19 23:59

```

BR:

```text
HIDE

```

Em:

```text
2026-10-20 00:00

```

BR:

```text
SHOW

```

---

# 165. Definition of Done — missing region

```text
US Digital = past
GB Digital = past

BR = nenhum 4/5/6

coverage=available

Release Region=BR

```

Esperado segundo a policy da feature:

```text
HIDE

```

Reason:

```text
regional-home-release-not-confirmed

```

---

# 166. Definition of Done — empty evidence

```text
TMDB results=[]
Release Region=BR

```

Esperado:

```text
UNKNOWN
→ SHOW

```

Não afirmar falsamente:

```text
confirmado não lançado

```

---

# 167. Definition of Done — Series

```text
first_air_date=2027
→ HIDE

```

```text
first_air_date=2023
status=In Production
→ SHOW

```

```text
released=null
status=Planned
→ HIDE

```

```text
released=null
status=null
→ UNKNOWN
→ SHOW

```

---

# 168. Definition of Done — Search Cache

Aquecer search com:

```text
Hide OFF

```

Depois:

```text
Hide ON + BR

```

Não exigir search cache regional separado para produzir resultado correto.

Trocar:

```text
BR → US

```

deve reutilizar o mesmo neutral search result quando possível e apenas mudar policy.

---

# 169. Definition of Done — Pagination/Cursors

Depois de aquecer BR:

```text
page 1
page 2
```

mudar para US.

US deve começar com sua própria sequência lógica.

Isso precisa ser verdadeiro para:

```text
standard filtered cursor
custom/StremThru external cursor
merged cursor
Jellyfin walk cursor
Jellyfin catalog length state
Jellyfin collection member cursor
```

Não pode ocorrer:

```text
skip
duplicate
gap
short page por cursor antigo
stale count
wrong source offset
```

Mesmo requisito na virada de dia e em qualquer `validUntilMs` intra-day.

Warmer externo precisa continuar múltiplas páginas usando o MESMO key builder do runtime.

---

# 170. Definition of Done — Meta/Evidence Cache

Um cache antigo contendo:

```text
Schema 1
```

não pode fazer o regional evaluator concluir:

```text
BR não lançado
```

O sistema precisa:

```text
rehydrate Schema 2
ou
UNKNOWN
```

Além disso:

```text
releaseEvidence não fica preso no basic novo

releaseEvidence stale pode ser refreshed/upserted

cold store não ressuscita missing-region evidence por 60/180 dias

internal _releaseAvailability não vaza na resposta

Schema 2 → Schema 3
não invalida art/cast/links se component versioning estiver implementado
```

---

# 171. Definition of Done — Provider Independence

Com TMDB mapping disponível, movie regional filtering deve funcionar mesmo se o metadata provider principal for:

```text
TMDB
TVDB
IMDb/Cinemeta
anime provider

```

Não exigir que:

```text
providers.movie=tmdb

```

para a feature funcionar.

---

# 172. Definition of Done — Imported Discover

Catálogo com:

```text
region=BR
with_release_type=4|5|6
```

não pode perder essas informações ao passar por:

```text
Collection Builder
import
edit
save
reconstruction
```

Também deve preservar formState suficiente para o editor reabrir sem destruir a query.

`watch_region` sozinho não cria `region` sem regra explícita de migration/provenance.

---

# 173. O que foi validado estaticamente com alta confiança

No código da base V5 foram localizados/confirmados:

```text
branch dev
base 26523cf4...
tree completa não truncada
544 arquivos/blob
issue #742 aberta

quatro flags hide-unreleased
applyCatalogFilters
catalogFiltersActive
isReleasedDigitally
_releaseAvailability
releaseAvailability normalizer

Search ID normalization
AI Search routing
People Search routing
Movie/Series/Anime routing

TMDB movie release_dates
TVDB movie TMDB mapping/enrichment
IMDb movie TMDB release enrichment

TMDB series date/status
TVDB series date/status
IMDb series evidence gap
TVMaze status gap
AniList synthetic-status bug
MAL user-list status gap
parseMedia Invalid Date risk

Catalog cache
Search cache
Meta component cache
Basic component release evidence
Cold-store integration points e TTLs

Standard CatalogPagination cursor
Custom/StremThru cursor
Merged catalog cursor

ComprehensiveCatalogWarmer hardcoded external cursor key

Jellyfin:
pageLengths
catalogLengths
walkCursors
Collection Builder memberCursors
Search/Hints bridge

Recommendations
Personal lists
episode/Up Next separation

Discover Builder region derivation
watch-region/language fallback behavior
current config persistence
configVersion
loadSharedConfig/loadConfigFromDatabase split

Collection Builder catalog reconstruction
AI catalog reconstruction mapping

PR Guard limits
build/lint scripts

Achados adicionais da auditoria V6:
addon/index.ts chama catalogFiltersActive/applyCatalogFilters diretamente;
cacheWarmer.js possui config sintética com hide-unreleased;
dashboardApi.js e DashboardSystem.tsx modelam estatísticas das flags;
CatalogsSettings.tsx salva overrides hide-unreleased em múltiplos dialogs;
AI catalog schema/generation/sanitizer e setup streaming manipulam
watch_region/region/with_release_type/release_date.*.
```

A base `dev` continua exatamente no SHA auditado durante esta auditoria.

---

# 174. O que NÃO pode ser garantido por auditoria estática

## TMDB factual completeness

Não existe como provar pelo código que:

```text
TMDB possui toda release date real do Brasil

```

A implementação pode garantir:

```text
interpretação correta do dado recebido

```

Não:

```text
completude factual do upstream

```

---

# 175. Provider contracts futuros

APIs podem mudar:

```text
Trakt
Simkl
MDBList
TVDB
MAL
AniList
Kitsu
TVMaze
Cinemeta
TMDB

```

O plano cobre os contracts e adapters atuais.

Não existe garantia eterna sem monitoramento/testes contínuos.

---

# 176. Private/authenticated catalogs

Fluxos podem ser auditados estaticamente.

End-to-end real de:

```text
private Trakt
private Simkl
MAL account
TMDB OAuth
MovieLens
outros dados autenticados

```

exige contas/credenciais de teste.

---

# 177. Redis + cold store real

Leitura de código confirmou uma incompatibilidade potencial importante:

```text
hot META_TTL ~7d
cold stable ~60d
cold frozen ~180d
```

Por isso o V5 define `releaseEvidence` como hot-only inicialmente.

Ainda assim, auditoria estática não prova integralmente:

```text
deploy old
→ populate Redis
→ populate cold store
→ upgrade
→ restart
→ warmup
→ read-through
```

Executar integration test real.

O teste deve demonstrar especificamente que:

```text
old missing-BR evidence
não reaparece do cold store
depois que upstream passou a fornecer BR release
```

---

# 178. Concorrência real

Não é possível provar somente estaticamente:

```text
20/50/100 requests simultâneos

```

e medir:

```text
single-flight
race
Redis ordering
latency

```

Executar integration/load test.

---

# 179. Performance real

Não prometer:

```text
zero impacto

```

sem benchmark.

Particularmente medir:

```text
lazy TMDB evidence requests
ambiguous series search
cold regional request

```

---

# 180. Country parity

A lista TMDB e a library backend devem ser comparadas em runtime/test.

Esse ponto continua não provado até executar a comparação.

---

# 181. Escopo de “100% do projeto”

“100%” neste plano significa:

> todos os caminhos localizados que podem produzir, transformar, armazenar, cachear, paginar, filtrar ou apresentar movie/series em catálogos e buscas, além das configurações e estados auxiliares dos quais Hide Unreleased depende.

Não significa alterar funcionalidades sem relação com o problema, como:

```text
subtitle delivery
stream playback
OAuth genérico
poster image processing
admin unrelated APIs
Jellyfin playback internals

```

---

# 182. Não aplicar filtro em Meta individual

A issue trata de:

```text
Hide Unreleased em Catalogs/Search

```

Abrir diretamente:

```text
/meta/movie/...

```

não deve retornar `404` somente porque o título está oculto de um catálogo.

Isso seria uma mudança de produto diferente.

---

# 183. Não aplicar filtro em Stream

Também não bloquear:

```text
/stream/

```

com base nessa policy.

Catalog/search visibility não é autorização de playback.

---

# 184. Não aplicar a Subtitles

Mesma regra:

```text
subtitle route

```

não deve ganhar Release Visibility policy.

---

# 185. Arquitetura final resumida

```text
                 PROVIDER DATA
                      │
                      ▼
            NORMALIZED RELEASE EVIDENCE
            ┌─────────┴─────────┐
            │                   │
     legacy instants       regional days
            │                   │
            └─────────┬─────────┘
                      ▼
            REGION-NEUTRAL HOT CACHE
                      │
                      ▼
          LAZY EVIDENCE COMPLETION
          com freshness/request budget
                      │
                      ▼
          CANONICAL FILTER CONTEXT
                      │
                      ▼
           RELEASE VISIBILITY ENGINE
                      │
          released / unreleased / unknown
                      │
                      ▼
              FILTER POLICY
               ┌──────┴──────┐
               │             │
            CATALOG        SEARCH
               │             │
               ▼             ▼
       FILTERED PAGE      POST-CACHE
               │
               ▼
       FILTER SIGNATURE
               │
     ┌─────────┼──────────┬───────────┐
     ▼         ▼          ▼           ▼
  standard   external   merged      Jellyfin
   cursor     cursor     cursor     paging state
     │         │          │           │
     └─────────┴──────────┴───────────┘
                      │
                      ▼
             TEMPORAL VALIDITY
```

---

# 186. Filme

```text
TMDB release_dates
+
Schema 2
+
homeReleaseDaysByRegion
+
Release Region
+
calendar-day comparison

```

---

# 187. Série

```text
first premiere evidence
+
real provider status
+
central status normalization

```

Sem region.

---

# 188. Episódios

```text
lógica própria

```

Não misturar.

---

# 189. Streaming regional

```text
feature futura própria

```

Não misturar.

---

# 190. Resultado arquitetural esperado

Depois da implementação, a seguinte propriedade deve ser verdadeira:

```text
Mesmo upstream data
+
mesmo evidence schema
+
mesma evidence freshness state
+
mesma policy version
+
mesmo canonical FilterContext
+
mesma definição estrutural do catálogo
+
mesmo instante dentro da validade do cursor
=
mesma decisão
+
mesma paginação
```

Independentemente de:

```text
cache hit/miss
provider principal
warmup
restart
cold-store read-through
ordem de requests
outro usuário usando região diferente
Jellyfin vs Stremio catalog bridge
```

Quando o relógio ultrapassar `validUntilMs` ou mudar o logical day relevante,
a paginação antiga deve ser descartada/recalculada.

---

# 191. Critério final para considerar implementation-ready

A feature só está pronta quando forem validados conjuntamente:

```text
Evidence Schema 2
dual temporal semantics
Worldwide golden-master parity
Regional movie policy
Series policy
Canonical FilterContext

Search neutrality
Search cache migration/version
Catalog filtering

Standard cursor
Custom/StremThru cursor
Merged cursor
Comprehensive warmer
Temporal validUntil
Timezone/day transition

Jellyfin catalog lengths
Jellyfin walk cursors
Jellyfin collection member cursors
Jellyfin search inheritance

Meta hot cache
releaseEvidence refresh/upsert
legacy basic migration
Cold store stale-evidence protection
response hygiene

Config persistence
Config cache clone safety
Discover region provenance
Collection Builder round-trip

Multi-user isolation
Provider gaps
request budget/single-flight

Build
Lint
Tests
integration migration test
PR Guard
```

Não considerar implementation-ready apenas porque o evaluator unitário funciona.

---

# 192. Conclusão

A implementação robusta da #742 não é:

```text
adicionar releaseRegion dentro de
isReleasedDigitally()
```

Também não é duplicar filtros regionais em providers.

A solução V5 é:

```text
FACTS
↓
NORMALIZED EVIDENCE
↓
BOUNDED FRESHNESS
↓
NEUTRAL CACHE
↓
CANONICAL FILTER CONTEXT
↓
VISIBILITY EVALUATOR
↓
POLICY
↓
CATALOG/SEARCH
↓
FILTER-AWARE PAGINATION
↓
TEMPORAL VALIDITY
```

Para movie regional release:

```text
TMDB home-release evidence
+
explicit/traceable region provenance
+
calendar-day semantics
```

Para Worldwide:

```text
legacy temporal semantics
+
golden-master parity
```

E para correctness de paginação:

```text
standard
+
external
+
merged
+
Jellyfin
+
warmer
```

todos precisam compartilhar o mesmo contexto efetivo e respeitar a mesma validade temporal.

Com esses ajustes, o plano deixa de cobrir apenas o evaluator e os dois cursores mais óbvios
e passa a cobrir também os estados auxiliares reais que podem preservar membership antigo.

---

---

# 193. Achados novos da auditoria V5 — blockers confirmados

Os seguintes pontos foram encontrados diretamente na base auditada e são blockers
para declarar o plano implementation-ready:

```text
P0 — merged-cursor não estava incluído na estratégia de signature.

P0 — comprehensiveCatalogWarmer hardcodava a external cursor key.

P0 — Jellyfin mantém pageLengths/catalogLengths/walkCursors fora da
     filter signature.

P0 — Jellyfin Collection Builder mantém memberCursors com sourceOffset/seen
     sem filter signature.

P0 — cold store genérico pode preservar release evidence por 60/180 dias,
     incompatível com negative regional evidence mutável.

P0 — CalendarDate para todos os facts conflita com "Worldwide exatamente legado".

P0 — day-only cursor identity é insuficiente para decisões Worldwide/Series
     que possam mudar dentro do dia.

P0 — catalogReconstruction.ts precisa ser alterado obrigatoriamente para
     round-trip de region/release semantics.

P1 — Discover region provenance precisa ser explícita para evitar que região
     derivada de idioma seja tratada como escolha explícita.

P1 — search neutralization precisa de cache schema version.

P1 — releaseEvidence component exige refresh/upsert e integração completa
     no hash layout/reconstruction.

P1 — internal evidence response stripping precisa permanecer como invariant.

P1 — canonical FilterContext deve ser a única fonte de verdade para
     filtro + signature + pagination.
```

---

# 194. Release evidence freshness contract

Definir freshness independentemente de policy. `sourceFetchedAt` é factual; `normalizedAt`, se existir, é apenas diagnóstico.

```ts
interface ReleaseEvidenceFreshness {
  sourceFetchedAt: string;
  expiresAt?: string;
  normalizedAt?: string;
}
```

Não é necessário serializar isso para cliente.

Success evidence:

```text
TTL bounded
shared across region/user
```

Failure/unavailable:

```text
shorter TTL
não transformar transient upstream failure
em long-lived UNKNOWN cache
```

Missing region em `coverage=available`:

```text
policy pode HIDE hoje
mas evidence precisa ser revalidada depois
```

---

# 195. TMDB ID resolution contract

> **Correção normativa V14:** este contrato só aceita TMDB movie ID com media-kind provenance; veja seção 362. `tv_results` nunca é fallback para movie release evidence.

`ensureMovieReleaseEvidence()` deve resolver TMDB ID por ordem controlada:

```text
1. meta._tmdbId / tmdb id já presente
2. existing cached all-id mapping
3. existing provider mapping já obtido na request
4. optional bounded central mapping lookup
5. sem mapping → UNKNOWN
```

Não iniciar cascata de lookups arbitrária por provider.

Métrica:

```text
evidenceMappingHit
evidenceMappingLookup
evidenceMappingUnavailable
```

---

# 196. Response hygiene

Continuar executando stripping de internal release evidence antes da resposta externa.

Teste:

```text
catalog response
search response
meta response
Jellyfin bridge response
```

não devem expor:

```text
_releaseAvailability
internal ReleaseDecision
nextTransitionAt
filterSignature
secrets
```

a menos que exista API pública explicitamente criada para debugging.

---

# 197. Canonical signature security

`stableStringify(config)` inteiro é proibido para filter signature.

A signature deve conter somente dados membership-relevant.

Teste de segurança:

```text
TMDB API key
Trakt token
Simkl token
MDBList key
admin key
```

nunca aparecem em:

```text
cursor key
debug log
metrics labels
reason
signature input dump
```

---

# 198. Request-level Release Evaluation Budget

Contrato operacional V14:

```text
provider-level TMDB admission controller obrigatório (não existe no snapshot)
+
request-local WorkBudget
+
credential-scoped cooldown
+
single-flight/lease
```

Se 100 metas chegarem sem evidence:

```text
não disparar 100 requests sem limite
```

Prioridade:

```text
items necessários para preencher a página atual
antes de itens além do page target
```

Isso evita gastar enrichment em itens que nunca serão retornados.

---

# 199. FilterResult contract

Para paginação, preferir:

```ts
interface FilterResult<T> {
  metas: T[];
  nextTransitionAt: Date | null;
}
```

`nextTransitionAt` é o menor instante futuro entre decisões avaliadas
capazes de mudar membership sem novo upstream data.

Assim:

```text
applyCatalogFiltersDetailed()
→ FilterResult

applyCatalogFilters()
→ compatibility wrapper que retorna somente metas
```

Permite migração incremental de callers.

---

# 200. Merged definition signature

Criar:

```ts
buildMergedDefinitionSignature(catalogConfig)
```

Input mínimo:

```text
mergeMode
ordered sources
source catalog id
source type
configured genre/default genre behavior relevante
```

Isso resolve bug preexistente de cursor sobrevivendo à edição estrutural do merged catalog.

---

# 201. Jellyfin paging scope

Criar helper:

```ts
buildJellyfinPagingScope({
  userUUID,
  catalog,
  extras,
  profileTags,
  keepKey,
  filterSignature,
  configVersion?,
})
```

Usar em:

```text
pageLengths
catalogLengths
walkCursors
Redis catalog/page length keys
```

Para memberCursors:

```text
collection id
folder id
source list
combined source paging scopes
```

---

# 202. Warmup API contract

Warmup não deve conhecer formato interno de cursor.

Preferência de design:

```text
getCatalog/fill result
→ optional pagination metadata
   nextRequestedSkip / cursorToken
```

Se isso for grande demais:

```text
shared cursor key builder
```

é requisito mínimo.

Teste garante que mudar namespace do cursor quebra compile/test se warmer não acompanhar.

---

# 203. Golden-master Worldwide suite

Antes de substituir o caminho legado, capturar matriz de comportamento.

Casos adicionais:

```text
released = invalid
released = exact instant future
released = exact instant past
release home same day but later hour
release timestamp with -03:00
release timestamp with +14:00
365d - 1ms
365d exactly
365d + 1ms
results=[]
release_dates missing
home types mixed
```

A nova implementação Worldwide só passa se produzir a mesma saída do legado
sob `now` injetado.

---

# 204. Migration integration test

Executar em ambiente descartável:

```text
VERSION OLD
populate:
- search cache
- catalog cache
- Schema 1 basic
- standard cursor
- external cursor
- merged cursor
- Jellyfin length/walk/member state
- cold store

UPGRADE V5
same Redis/cold store

assert:
- no old filtered search reused as neutral
- no old cursor namespace reused
- Schema 1 not trusted regionally
- cold old evidence not resurrected
- Worldwide remains equivalent
```

Esse teste é o mais próximo de provar correctness de deploy real.

---

# 205. Critério de fechamento da #742

Somente usar:

```text
Fixes #742
```

quando estiverem integrados:

```text
regional evaluator
config/UI
search neutrality
catalog policy
standard cursor
external cursor
merged cursor
warmer coupling
Jellyfin paging isolation
migration protections
Collection Builder round-trip
Worldwide compatibility tests
```

Caso contrário, usar:

```text
Part of #742
```

nos PRs intermediários.

---

# 206. Auditoria V6 — caller parity em `addon/index.ts`

A busca completa por `catalogFiltersActive` e `applyCatalogFilters` confirma que
`addon/index.ts` é caller direto do pipeline de filtros, além de `getCatalog.ts`.

Na base auditada ele:

```text
importa:
applyCatalogFilters
catalogFiltersActive
cursorKey
resolveStartPage
fillFilteredPage
fillOnce
```

e executa paginação filtrada diretamente.

Portanto é obrigatório:

```text
resolveCanonicalFilterContext uma vez
→ passar o mesmo context para catalogFiltersActive
→ passar o mesmo context para applyCatalogFiltersDetailed
→ construir filterSignature do mesmo context
→ construir cursor namespace do mesmo context
→ agregar nextTransitionAt/validUntil
```

Não é aceitável:

```text
getCatalog.ts usa CanonicalFilterContext
addon/index.ts continua passando {config,catalogConfig,cleanId}
e deixa cada helper resolver novamente
```

Teste obrigatório:

```text
mesmo request/catálogo
via caller interno de getCatalog
e via route path de addon/index.ts
→ mesma membership
→ mesma filterSignature
→ mesma cursor boundary
```

---

# 207. `cacheWarmer.js` — config sintética

`addon/lib/cacheWarmer.js` contém uma configuração sintética de warmup com:

```text
hideUnreleasedDigital=false
hideUnreleasedDigitalSearch=false
```

Ao adicionar `releaseRegion`, esse objeto deve ser explicitamente compatível.

Regra:

```text
releaseRegion=''
→ Worldwide
```

ou deve passar pelo mesmo runtime normalizer.

O warmer simples não pode:

```text
- materializar resultado regional em shared catalog/search cache;
- criar uma region implícita pelo language;
- divergir do default de config real;
- depender de undefined behavior para releaseRegion.
```

Teste:

```text
synthetic warmer config
→ normalizeReleaseVisibilityConfig
→ Worldwide
→ neutral cache key igual à semântica esperada
```

---

# 208. Dashboard / telemetry contract

`addon/lib/dashboardApi.js` agrega uso de:

```text
hideUnreleasedDigital
hideUnreleasedShows
```

e `DashboardSystem.tsx` exibe essas métricas.

A #742 deve tomar uma decisão explícita:

### Opção normativa V6

Adicionar uma distribuição agregada de modo de release:

```text
Worldwide
Regional
```

e, somente se o projeto já aceitar granularidade por país no dashboard, uma
distribuição por `releaseRegion`.

Não usar região como label de métrica de alta cardinalidade em runtime.

Se o dashboard não for alterado no PR da #742:

```text
documentar "no dashboard schema change"
+
teste garantindo que novo campo de config não quebra stats serialization
```

O importante é não deixar o comportamento implícito.

---

# 209. `CatalogsSettings.tsx` — preservação de metadata

`CatalogsSettings.tsx` possui múltiplos dialogs que salvam:

```text
hideUnreleasedDigital
hideUnreleasedShows
```

por catálogo.

Como o V6 restringe override de região ao TMDB Discover, esses dialogs genéricos
NÃO ganham automaticamente um `releaseRegion` próprio.

Mas cada save path precisa preservar:

```text
catalog.metadata.discover
catalog.metadata.discoverParams
region provenance
demais metadata desconhecida
```

Teste de regressão obrigatório:

```text
catalog Discover com params.region=BR
→ abrir settings genérico/per-provider
→ alterar Hide Unreleased ON/OFF
→ salvar
→ params.region continua BR
→ provenance continua intacta
```

Isso cobre perda acidental de estado em spread/reconstruction.

---

# 210. AI Catalog contract completo

A árvore atual possui estes participantes do contrato TMDB Discover:

```text
addon/utils/ai-catalog-schema.ts
addon/utils/ai-catalog-generation.ts
addon/utils/ai-catalog-config-builder.ts
addon/utils/ai-catalog-sanitizer.ts
addon/utils/ai-catalog-entity-resolver.ts
addon/lib/tmdbDiscoverDateTokens.ts
```

O schema aceita hoje:

```text
watch_region
region
with_release_type
release_date.gte
release_date.lte
```

O V6 exige round-trip semântico completo.

### Regras

```text
watch_region
→ disponibilidade de watch provider

region
→ TMDB release-region do Discover

with_release_type
→ semântica de tipo de release na query

release_date.*
→ janela dinâmica/estática da query
```

Nenhum sanitizer/generator pode:

```text
watch_region=BR
→ inventar region=BR
```

sem a regra explícita de provenance/release-aware.

Nenhum reconstruction/builder pode apagar:

```text
region
with_release_type
release_date.gte/lte
```

de um catálogo já válido.

---

# 211. AI generation — evitar falsa provenance

`ai-catalog-generation.ts` instrui o modelo a usar `watch_region` para resolver
watch providers.

Isso NÃO é escolha explícita de Release Region.

Logo catálogos gerados por IA com:

```text
watch_region=BR
```

mas sem:

```text
region
```

devem permanecer:

```text
release visibility → global releaseRegion
```

exceto quando uma regra release-aware inequívoca materializar `region` com source
`watch-region-derived`.

Teste:

```text
AI catalog:
watch_region=BR
with_watch_providers=...
sem with_release_type
sem region
global releaseRegion=Worldwide
→ Worldwide
```

E:

```text
AI catalog:
watch_region=BR
with_release_type=4|5|6
release_date.lte=today
sem region

runtime migration explicitamente reconhecida
→ region=BR
→ source=watch-region-derived ou legacy-normalized
```

---

# 212. AI sanitizer — campos dinâmicos

`ai-catalog-sanitizer.ts` valida/coage `release_date.gte/lte`.

`tmdbDiscoverDateTokens.ts` resolve campos de data dinâmicos.

A auditoria de #742 deve garantir que o contexto de release visibility use:

```text
effective Discover params
após resolução/normalização relevante
```

sem confundir:

```text
query date window
```

com:

```text
data factual de home release do título
```

`release_date.lte=today` no Discover reduz o universo upstream, mas não substitui
`_releaseAvailability` para provar release regional de cada item.

Invariante novo:

```text
Discover query semantics nunca são reutilizadas como item-level release evidence.
```

---

# 213. Setup Streaming — separação obrigatória

`configure/src/lib/setup/streaming.ts` cria catálogos com:

```text
watch_region=provider.region
with_watch_providers=...
```

e, quando `releasedOnly` está ativo para movie:

```text
with_release_type=4|5|6
release_date.lte=<today token>
```

Isso é um caso release-aware inequívoco para migration/provenance, mas precisa ser
materializado por regra central e testada.

Não espalhar lógica no setup e no backend.

Teste:

```text
Streaming setup BR + releasedOnly=true
→ catálogo round-trip
→ watch_region=BR preservado
→ release-type preservado
→ effective release region definida pela regra documentada
```

E:

```text
Streaming setup BR + releasedOnly=false
→ watch_region=BR
→ não força releaseRegion BR
```

---

# 214. Deterministic evidence normalization

Para reduzir diferenças por ordem de payload e simplificar testes/cache/debug:

```text
RegionCode
→ trim + uppercase + validation

regionsWithReleaseRecords
→ Set
→ sort lexicográfico

homeReleaseDaysByRegion
→ construir em ordem determinística ao serializar
```

Duplicatas de country entries:

```text
→ merge
→ menor home CalendarDate válida
```

Entradas inválidas não podem alterar `coverage=available` a menos que exista ao
menos um release record válido segundo o contrato já definido.

Teste:

```text
mesmos records em ordem diferente
→ evidence semanticamente e serializadamente idêntica
```

---

# 215. Distinção entre `coverage=empty` e malformed payload parcial

A definição de `coverage` deve especificar o caso misto.

Regra V6:

```text
results é array
+
ao menos um country/release record estruturalmente válido
→ available

results é array vazio
→ empty

results é array não vazio
mas nenhum record utilizável após validação
→ empty
+ diagnostic counter/reason interno

results ausente/não-array/request falhou
→ unavailable
```

Um payload parcialmente inválido com alguns records válidos:

```text
→ available
→ usar apenas records válidos
→ registrar malformed-entry count em debug/metric agregada
```

Nunca deixar uma entrada ruim descartar evidence válida do mesmo payload.

---

# 216. Release evidence refresh contract — stale-while-revalidate proibido para negativa vencida

Se o componente `releaseEvidence` estiver vencido e a decisão regional depende de:

```text
absence of selected region
```

não tratar automaticamente o valor stale como confirmação renovada.

Política segura:

```text
fresh evidence
→ decisão normal

stale positive evidence com home date passada
→ pode ser usada apenas se a implementação documentar SWR e risco aceito

stale negative-by-absence
→ revalidate dentro do budget
→ se revalidation falhar: UNKNOWN → SHOW
```

Isso evita manter HIDE com base em ausência regional já expirada.

Se o projeto optar por usar stale positive, criar testes e métricas separados.
Não é necessário para a primeira implementação.

---

# 217. Request budget e paginação — evitar página artificialmente curta

Quando o request-level evidence budget acabar, o V5 define:

```text
UNKNOWN → SHOW
```

Isso preserva disponibilidade, mas o algoritmo de paginação precisa manter
determinismo para o mesmo contexto/budget policy.

Regras:

```text
budget policy faz parte da versão de policy/implementation, não da filterSignature por request;
itens processados em ordem estável;
single-flight compartilhado;
timeout não reordena a lista;
falha de enrichment resolve UNKNOWN na posição original.
```

Não executar `Promise.race` que devolva itens conforme completion order.

Teste:

```text
mesmos 50 itens
latências upstream embaralhadas
→ mesma ordem final
→ mesma paginação
```

---

# 218. Abort / cancellation propagation

Lazy evidence completion pode adicionar chamadas TMDB extras.

Propagar, quando a infraestrutura atual permitir:

```text
AbortSignal/request cancellation
```

para não continuar fanout depois que o cliente abortar a request.

No mínimo:

```text
não iniciar novos lookups após abort
```

e garantir liberação correta do limiter/single-flight.

Isso é hardening de performance; se a stack atual não expõe AbortSignal até o
provider, registrar explicitamente como limitação não-blocking.

---

# 219. Error taxonomy

Separar internamente:

```text
mapping unavailable
upstream timeout
upstream 429
upstream 5xx
malformed payload
unsupported schema
budget exhausted
aborted
```

Todos podem resultar externamente em:

```text
UNKNOWN → SHOW
```

mas não devem ser indistinguíveis em logs/métricas.

Reason code público/interno de visibility continua de baixa cardinalidade; detalhes
de erro ficam em telemetry de evidence.

---

# 220. Search neutrality — regra de deploy mais forte

Além de `SEARCH_RESULT_CACHE_SCHEMA_VERSION`, preferir namespace explícito:

```text
search:v2:...
```

ou equivalente que torne colisão estruturalmente impossível.

O teste de migration precisa popular uma key antiga real e provar:

```text
new reader
→ não lê old filtered payload
```

Não depender apenas de TTL natural.

---

# 221. Config/UI accessibility e internacionalização

Ao adicionar `Release Region`:

```text
label
description
search keywords
select placeholder
Worldwide option
invalid imported value warning
```

devem seguir o padrão de componentes existente.

Não hardcodar nomes de países manualmente.

Se o projeto tiver tradução/i18n parcial ou futura, armazenar:

```text
ISO code
```

e derivar label da fonte/lista TMDB; não persistir nome localizado.

Teste de UI:

```text
select BR
save
reload
→ BR

keyboard navigation
→ Worldwide e países acessíveis

invalid imported code
→ fallback determinístico + indicação
```

---

# 222. Release-region product contract definitivo

Para remover a ambiguidade “global e per-catalog”, o contrato V6 é:

```text
GLOBAL
config.releaseRegion
→ vale para movie catalogs e movie search

TMDB DISCOVER OVERRIDE
catalog discover params.region com provenance válida
→ pode sobrescrever global para aquele catálogo

GENERIC NON-DISCOVER CATALOG
→ usa global
→ não ganha metadata.releaseRegion nesta feature

SEARCH
→ sempre usa global releaseRegion
→ não herda região de um catálogo
```

Esse contrato deve ser refletido em:

```text
UI
types
resolver
tests
docs
```

Uma futura feature pode adicionar override genérico por catálogo, mas não deve
aparecer acidentalmente durante #742.

---

# 223. Matriz adicional V6 — superfícies novas

Adicionar aos testes:

```text
ADDON INDEX
standard catalog filtered via route caller
→ same context/signature as getCatalog path

CACHE WARMER
synthetic config
→ Worldwide
→ no regional cache contamination

CATALOG SETTINGS
Discover region BR
→ toggle per-catalog hide flag
→ save
→ region/provenance preserved

AI CATALOG
watch_region only
→ does not override global

AI CATALOG RELEASE-AWARE
watch_region + with_release_type 4|5|6 + release_date
→ migration/provenance behavior exactly defined

SETUP STREAMING
releasedOnly off/on
→ correct provenance distinction

DASHBOARD
config with releaseRegion
→ stats endpoint does not break

EVIDENCE ORDER
same TMDB records shuffled
→ same normalized evidence

PARTIAL MALFORMED
one bad + one valid release record
→ available using valid record

BUDGET / LATENCY
random enrichment completion order
→ stable output order
```

---

# 224. Arquivos obrigatórios V6 — classificação final

## Deve mudar ou ter alteração altamente provável

```text
addon/utils/releaseAvailability.ts
addon/utils/releaseVisibility.ts
addon/utils/releaseRegion.ts
addon/utils/catalogFilterContext.ts
addon/utils/catalogFilterSignature.ts
addon/utils/catalogFilters.ts
addon/utils/parseProps.js
addon/lib/catalogPagination.ts
addon/lib/getCatalog.ts
addon/index.ts
addon/lib/getSearch.ts
addon/lib/getCache.ts
addon/lib/getTmdb.ts
addon/lib/configApi.js
addon/types/index.ts
configure/src/contexts/config.ts
configure/src/contexts/ConfigContext.tsx
configure/src/components/sections/FiltersSettings.tsx
configure/src/lib/settingsSearchIndex.ts
addon/lib/collectionBuilder/catalogReconstruction.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
```

## Must-audit / must-test; diff depende do design final

```text
configure/src/components/sections/CatalogsSettings.tsx
addon/lib/dashboardApi.js
configure/src/components/dashboard/DashboardSystem.tsx
configure/src/lib/setup/streaming.ts
configure/src/components/setup/StreamingPickerDialog.tsx
addon/utils/ai-catalog-config-builder.ts
addon/utils/ai-catalog-schema.ts
addon/utils/ai-catalog-generation.ts
addon/utils/ai-catalog-sanitizer.ts
addon/utils/ai-catalog-entity-resolver.ts
addon/lib/tmdbDiscoverDateTokens.ts
addon/lib/discoverCatalogSignature.ts
addon/lib/tmdbCacheNormalizers.ts
addon/lib/getMeta.js
configure/src/utils/catalogUtils.ts
configure/src/components/sections/TMDBIntegration.tsx
addon/utils/mdbList.ts
configure/src/components/sections/MDBListIntegration.tsx
addon/utils/simklUtils.ts
configure/src/components/sections/SimklIntegration.tsx
public/featured/*.json
addon/lib/jellyfin/index.ts
addon/lib/metaHashMigration.ts
addon/lib/metaColdStore/*
```

Não confundir “must-audit” com “forçar diff sem necessidade”.
O gate exige demonstrar por teste/inspeção que o contrato permanece correto.

---

# 225. Definition of Done V6 — cobertura estrutural

Antes de chamar o plano de implementation-ready, executar busca de código na HEAD por:

```text
hideUnreleasedDigital
hideUnreleasedDigitalSearch
hideUnreleasedShows
hideUnreleasedShowsSearch
hideUnreleased
isReleasedDigitally
_releaseAvailability
catalogFiltersActive
applyCatalogFilters
catalog-cursor
merged-cursor
pageLengths
catalogLengths
walkCursors
memberCursors
watch_region
with_release_type
release_date.gte
release_date.lte
params.region
discoverSig
computeDiscoverSignature
tmdb:movie:release_dates
movieReleaseDates
getMovieCertifications
normalizeTmdbReleaseDatesForCache
collectionMeta.hideUnreleased
tmdb.collection.
simkl.list.
simklUserTokenIfRequired
_currentSearchEngine
```

Cada ocorrência precisa cair em uma destas categorias:

```text
A. alterada pela implementação;
B. coberta por helper central;
C. explicitamente não relacionada com justificativa;
D. testada como preservação/no-op.
```

Nenhuma ocorrência pode ficar sem classificação.

Esse inventário é o gate mais forte contra “arquivo esquecido”.

---

# 226. Resultado da auditoria V6 — registro histórico superseded pelo V8

Após a auditoria integral do documento e revalidação da árvore no SHA:

```text
26523cf4e0be9a0b0fd513b4ec8530d346e87e18
```

o V5 estava muito próximo de implementation-ready, mas ainda deixava superfícies
reais sem classificação explícita.

O V6 fecha essas lacunas adicionando:

```text
addon/index.ts caller parity
cacheWarmer.js
CatalogsSettings.tsx preservation
dashboard/telemetry decision
AI catalog schema/generation/sanitizer/entity resolver
setup streaming contract
tmdbDiscoverDateTokens separation
deterministic evidence normalization
partial-malformed evidence semantics
stale-negative revalidation rule
stable-order request budget
abort/error taxonomy hardening
stronger search namespace migration
explicit release-region product contract
full occurrence-classification gate
```

Com isso, a arquitetura fica coberta não apenas nos evaluators/caches/cursors, mas
também nos pontos que criam, reconstroem, aquecem, exibem e encaminham a configuração.

Ainda permanecem fora de uma garantia puramente estática, pelos motivos já descritos:

```text
completude factual do TMDB;
contratos futuros de APIs externas;
E2E autenticado sem credenciais;
races/performance reais sem load test;
comportamento Redis/cold-store de upgrade sem integration test.
```

Por isso a formulação correta de “100% de precisão” é:

> cobertura estática completa e rastreável da árvore auditada + critérios de teste
> que tornam explícito tudo o que só pode ser provado em runtime ou contra upstream.



---


# 227. Reauditoria V9 — snapshot atual e delta obrigatório

A V9 foi fechada estaticamente contra:

```text
dev@6e83e22ab9de5093f9918a1871157f401feebb03
tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
583 entries
544 blobs
39 trees
release v3.1.0
```

O tree não adicionou/removeu paths em relação ao snapshot V8, mas o conteúdo avançou 4 commits:

```text
086b13521cac6106f76680f6f9f06ef824fd6919
feat(watch-tracking): exchange favourites, drops and pauses through watch_state

af08b30d3bf4b6499b05232c514c754b93daded7
fix(jellyfin): keep sign-ins in the database and extend them on use

c4de7522...
chore(dev): release 3.1.0

6e83e22ab9de5093f9918a1871157f401feebb03
Merge pull request #738 / release 3.1.0
```

Arquivos modificados V8→V9:

```text
.release-please-manifest.json
CHANGELOG.md
addon/lib/database.ts
addon/lib/getManifest.ts
addon/lib/jellyfin/context.ts
addon/lib/jellyfin/socket.ts
addon/lib/jellyfin/tokens.ts
addon/lib/jellyfin/watched.ts
addon/lib/jellyfin/watchlist.ts
addon/lib/playbackHandler.ts
addon/lib/settingsRegistry.ts
addon/lib/watchState.ts
configure/src/components/sections/GeneralSettings.tsx
docs/jellyfin.md
package-lock.json
package.json
```

Nenhum desses commits implementa a #742. Porém o primeiro altera estado dinâmico de watchlist/
dropped e, portanto, entra no audit de source/runtime identity mesmo sendo semanticamente separado
da release policy.

## Rebase Gate V9

Antes de codificar e novamente imediatamente antes de abrir/atualizar o PR:

```bash
git rev-parse dev
```

Se diferente de `6e83e22ab9de5093f9918a1871157f401feebb03`:

```text
1. compare 6e83e22..newHead;
2. listar commits + arquivos;
3. rerun occurrence gate completo;
4. rerun release/search/catalog/cache/cursor/Jellyfin/warmers surface search;
5. classificar cada ocorrência e cada arquivo do delta como A/B/C/D;
6. atualizar source capability matrix;
7. atualizar plano/PR notes antes de escrever código novo.
```

Tree count igual nunca substitui diff de conteúdo.

---

# 228. Classificação do delta V8 → V9

Classificação obrigatória do drift já observado:

```text
.release-please-manifest.json / CHANGELOG / package*.json
→ C: release/version metadata; no direct Release Visibility policy.

database.ts / jellyfin/tokens.ts / jellyfin/context.ts / jellyfin/socket.ts
→ C/D: Jellyfin authentication/session persistence; no release policy.
→ regression: account scoping não pode vazar para source/filter signatures.

watchState.ts / jellyfin/watchlist.ts / jellyfin/watched.ts / playbackHandler.ts
→ B/D: novo dynamic watch_state.
→ NÃO é automaticamente RuntimeFilterState de Hide Watched.
→ watchlist/dropped que define shelf/catalog é dynamic source state.
→ only datasets realmente consultados por applyCatalogFilters entram em filter state.

getManifest.ts / settingsRegistry.ts / GeneralSettings.tsx / docs/jellyfin.md
→ C/D: manifest/settings/docs do tracking; sem release evaluator.
```

**Conclusão do delta:** nenhum arquivo novo torna a arquitetura V8 inválida, mas a taxonomia
`RuntimeFilterState` precisa ser refinada para source-state vs filter-state, e as fixtures Jellyfin
precisam incorporar watchlist/dropped sem contaminar a #742.

---

# 229. Blocker V9 — signatures correctness-critical não podem usar hash curto legado

Fatos atuais confirmados no HEAD:

```text
addon/lib/discoverCatalogSignature.ts
computeDiscoverSignature()
→ MD5
→ substring(0, 8)
→ 32 bits

addon/lib/getCache.ts
hashConfig()
→ MD5
→ substring(0, 10)
→ 40 bits
```

Esses hashes já existem e podem continuar em cache keys legadas/debug. O erro seria promovê-los
sozinhos a contrato de correção de cursor/source.

## Contrato V9

Criar primitive própria para identidades novas:

```ts
interface CanonicalSignature {
  version: number;
  digest: string; // SHA-256; >=128 bits efetivos preservados
}

buildStrongSignature(domain, canonicalPayload)
```

Regras:

```text
stable/canonical serialization;
domain separation (`source:`, `filter:`, `paging:`...);
SHA-256;
>= 32 hex chars recomendados para 128 bits;
sem secrets;
versionamento explícito;
sem depender de JSON property insertion order acidental.
```

`discoverSig` permanece compatibilidade/hint, mas:

```text
CanonicalCatalogSourceProfile.params
→ strong sourceMembershipSignature
```

Teste obrigatório:

```text
mesmos dados em ordem de propriedades diferente → mesma assinatura;
1-bit semantic change → assinatura diferente;
legacy discoverSig igual/artificial collision fixture → strong signature diferente.
```

---

# 230. Canonical raw TMDB release_dates owner + monotonic write

A HEAD continua com competing writers para a mesma key:

```text
movieReleaseDates(id)
→ tmdb:movie:release_dates:<id>
→ 7d

getMovieCertifications(params)
→ mesma key
→ 24h
```

Isso continua blocker.

Criar um único owner:

```ts
interface CachedReleaseDatesEnvelopeV1 {
  schema: 1;
  sourceFetchedAt: string;
  fetchGeneration: string; // opaco/monotônico para race protection
  payload: TmdbReleaseDates;
}
```

API conceitual:

```ts
getTmdbMovieReleaseDatesCanonical(
  tmdbId,
  config,
  { requireFreshAfter, forceUpstream }
)
```

## Regra adicional V9: stale overwrite é proibido

O `cacheWrapGlobal()` atual separa flight normal de refetch, porém ambos terminam em `SET`
incondicional. Isso não é suficiente para correção em:

```text
plain fetch A inicia
forced refetch B inicia
B termina e grava newer facts
A termina depois e grava older observation
```

ou entre replicas/processos onde single-flight não é compartilhado.

O raw owner precisa de compare-and-set/atomic write baseado em geração/freshness:

```text
candidate.sourceFetchedAt >= stored.sourceFetchedAt
→ pode substituir

candidate.sourceFetchedAt < stored.sourceFetchedAt
→ descartar candidate write
```

Implementação recomendada:

```text
Redis Lua script / WATCH+MULTI / equivalente atômico
```

A correção não depende de distributed lock; lock pode reduzir fanout, mas o **monotonic CAS** é
o guard de verdade.

Falha de refetch:

```text
preservar last-known-good raw envelope;
para decisão regional stale-negative → UNKNOWN/SHOW naquela request;
não apagar facts bons por erro transitório.
```

---

# 231. Freshness factual — `sourceFetchedAt` é obrigatório

A evidence normalizada V2 deve carregar:

```ts
sourceFetchedAt: string;
```

copiado do raw envelope.

Não usar `observedAt` como nome ambíguo de freshness. Se quiser diagnóstico separado:

```ts
normalizedAt?: string;
```

mas:

```text
normalizedAt nunca renova source freshness;
cache hit nunca muda sourceFetchedAt;
meta reconstruction nunca muda sourceFetchedAt;
page/search cache reserialization nunca muda sourceFetchedAt.
```

## Negative regional evidence

```text
coverage=available
BR ausente
sourceFetchedAt fresh
→ UNRELEASED conforme policy regional

mesmo fact stale
→ force fresh raw fetch dentro do budget
→ success: reavaliar
→ failure: UNKNOWN/SHOW
```

`validUntil` do cursor nunca ultrapassa a freshness boundary da evidence negativa usada para
remover um item.

---

# 232. `tmdbCacheNormalizers.ts` — deterministic raw evidence contract

O normalizer atual preserva `iso_3166_1`, `release_date`, `type` e outros campos necessários,
mas a V9 torna determinismo explícito.

Raw normalized contract:

```text
country codes uppercase;
invalid country records ignorados/classificados;
release type normalizado para integer 1..6 quando válido;
release entries ordenadas por (country, calendar/timestamp, type, certification, note) ou
outra chave canônica documentada;
duplicatas factualmente equivalentes removidas;
sem timezone conversion do release day;
sem policy;
sem user region.
```

A ordenação do raw payload não precisa imitar TMDB; precisa produzir o mesmo canonical facts
para payload semanticamente igual.

Fixtures:

```text
BR/US/GB;
types 1..6;
payload shuffled;
duplicates;
invalid dates;
country lower/mixed case;
results=[];
results missing;
partial malformed;
```

---

# 233. TMDB upstream contracts revalidados

Contratos externos usados pela feature e que devem ser congelados em fixtures/documentação:

```text
/movie/{id}/release_dates
release types:
1 Premiere
2 Theatrical Limited
3 Theatrical
4 Digital
5 Physical
6 TV

/discover/movie
region = regional release-date context
with_release_type suporta 1..6 e trabalha em conjunto com region
watch_region = watch-provider context, conceito distinto

region usa ISO 3166-1
```

A V9 preserva a definição de home release para esta feature:

```text
4 | 5 | 6
```

Não reinterpretar type 1/2/3 como home release.

---

# 234. Discover source identity — correção da recomendação V8

O V8 estava correto em auditar `discoverCatalogSignature.ts`, mas V9 corrige uma nuance:

```text
NÃO: sourceMembershipSignature = discoverSig legado de 8 hex
```

Fazer:

```text
params completos, já materializados e canonicalizados
+
provider/source schema
+
relevant dynamic-token identity
→ StrongSourceSignature
```

`discoverSig` pode continuar no cache key atual para compatibilidade durante migração, mas o cursor
V9 e qualquer cache novo correctness-critical usam a strong signature.

Deve mudar com:

```text
region
watch_region
with_release_type
release_date.gte/lte
primary_release_date.gte/lte
sort_by
provider/genre/company/person/language filters
qualquer param efetivamente enviado ao upstream
```

Dynamic date tokens:

```text
stored token identity
!= resolved wall-clock value
```

Quando o valor resolvido altera membership, source stability/identity precisa expirar no boundary
correto.

---

# 235. Canonical source + filter + pagination identity V9

Criar uma única estrutura:

```ts
interface PagingIdentityV9 {
  sourceMembershipSignature: string;
  filterSignature: string;
  paginationContractSignature: string;
  sourceSnapshotRevision?: string | null;
}
```

As dimensões não são intercambiáveis:

```text
sourceMembershipSignature
→ o que a fonte pode retornar e em que ordem

filterSignature
→ quais itens neutros sobrevivem ao pós-filtro

paginationContractSignature
→ page size, offset/page mode, dedupe, fill, cursor schema, cache epoch

sourceSnapshotRevision/stability
→ qual snapshot concreto das páginas foi usado
```

Nunca colocar token/API key cru.

---

# 236. Filtered pagination V9 — exhaustion, budget e zero-visible progress

O helper atual possui `maxPages`, mas o contrato público só retorna `exhausted`.

V9 exige:

```ts
interface FillResultV9 {
  metas: any[];
  nextPage: number;
  nextOffset: number;
  pagesRead: number;
  upstreamExhausted: boolean;
  budgetExhausted: boolean;
  progressMade: boolean;
}
```

Regras:

```text
upstreamExhausted=true
→ somente quando a fonte realmente terminou

budgetExhausted=true
→ source pode continuar; nunca tratar como fim factual
```

Se `metas.length === 0` mas páginas upstream foram consumidas:

```text
persistir a posição upstream alcançada para o mesmo served offset
```

para evitar reiniciar indefinidamente no mesmo ponto.

## Limitação de protocolo explicitada

Se o cliente interpreta uma página curta/vazia como EOF e o protocolo não possui continuation token,
um budget finito não pode matematicamente garantir discoverability total quando filtros removem uma
sequência arbitrariamente longa. Portanto:

```text
- não chamar budget exhaustion de EOF;
- manter cursor/progresso correto;
- medir budget exhaustion;
- dimensionar budget por load test;
- manter fail-open apenas para UNKNOWN, nunca para known-unreleased;
- documentar esta limitação no DoD em vez de alegar garantia impossível.
```

---

# 237. Dedupe V9 — antes do cursor accounting

Na route atual, `fillFilteredPage()` avança upstream e o `Set` de dedupe é aplicado depois no
`fillChunk`. Isso pode reduzir `metas.length` após a posição upstream já ter avançado.

Contrato novo:

```text
fetch raw page
→ canonical item identity
→ filter
→ dedupe segundo policy versionada
→ take page slots
→ compute served + next position
→ persist cursor
```

`paginationContractSignature` inclui:

```text
dedupe version
canonical ID rule
cross-page dedupe policy
```

Decisão obrigatória:

```text
A. dedupe apenas dentro da resposta atual
OU
B. dedupe na caminhada inteira do cursor
```

Preferência V9: **B** para superfícies que prometem sequência sem repetição. O cursor pode manter um
bounded seen-set/fingerprint/window; se memória/custo for proibitivo, documentar A por surface e não
fingir semântica global.

Teste:

```text
page1 contém A,B,C
page2 contém C,D,E
filtro remove B
→ sequência servida e skips permanecem determinísticos
→ nenhuma posição se perde por C duplicado
```

---

# 238. Standard Catalog Cursor V6

Nova estrutura conceitual:

```ts
interface CatalogCursorV6 {
  schema: 6;
  served: number;
  upstreamPage: number;
  upstreamOffset: number;
  sourceSignature: string;
  filterSignature: string;
  paginationSignature: string;
  validUntilMs: number | null;
  sourceStableUntilMs: number | null;
  dedupeRevision: number;
}
```

Key:

```text
e<CACHE_EPOCH>:catalog-cursor:v6:
userScope:
catalog:
type:
genre:
sourceSig:
filterSig:
pagingSig
```

`userScope` não é necessariamente UUID cru em métricas/logs. Redis key pode continuar escopada ao
user quando requerido; telemetria usa hash/fingerprint não reversível.

Cursor invalidado por:

```text
policy/config change;
release region change;
logical-day/transition boundary;
evidence freshness boundary;
watched-filter revision;
source-state revision;
page cache refresh-ahead boundary;
page size/paging mode/dedupe change;
CACHE_EPOCH;
cursor schema bump.
```

---

# 239. RequestEvaluationClock — um clock por request

Capturar uma vez:

```ts
interface RequestEvaluationClock {
  nowMs: number;
  now: Date;
}
```

Todos os helpers usam o mesmo valor:

```text
todayInTimezone;
Worldwide evaluator;
Series evaluator;
Collection UTC day;
filter logicalDay;
nextTransitionAt;
validUntil;
source dynamic date resolution quando pertencente à mesma request;
logs/metrics do decision event.
```

Nenhum helper de membership chama `Date.now()`/`new Date()` independentemente dentro da mesma
avaliação lógica.

Warmer cria clock por execução lógica e testes injetam fixedNow.

---

# 240. CalendarDate + timezone + DST Gate

Regional release day continua CalendarDate, não instant.

`nextLocalMidnight()` deve usar timezone IANA corretamente.

Proibido:

```text
next = now + 24h
```

porque dias DST podem ter 23h/25h.

Fixtures mínimas:

```text
America/Fortaleza          # sem DST atual, baseline do usuário
America/New_York           # spring forward + fall back
Europe/London              # DST europeu
Asia/Kathmandu             # UTC+05:45
Pacific/Chatham            # offset de 45 min + DST
UTC
invalid timezone           # fallback + warning deduplicado
```

Validar:

```text
23:59:59.999 local → release ainda futura
00:00:00.000 local → arrived
next midnight sempre é próxima data civil local, não duração fixa
```

---

# 241. Worldwide evaluator + transition boundaries

Worldwide continua golden-master do legado.

Transitions:

```text
future primary release
→ primaryReleaseAt

recent + home release futura
→ min(homeReleaseAt, releasedAt + legacy 365d)

recent + sem home release
→ releasedAt + legacy 365d

over threshold
→ sem transition temporal conhecida
```

O `+365d` reproduz exatamente a aritmética observável do helper legado. Não substituir por `+1 year`
calendário.

Golden boundary:

```text
365d - 1ms
365d exato
365d + 1ms
```

---

# 242. Regional evaluator V9

Mesma policy central:

```text
fresh Schema 2 + coverage=available + region home day <= today
→ RELEASED

fresh Schema 2 + region home day > today
→ UNRELEASED

fresh Schema 2 + coverage=available + region sem 4/5/6
→ UNRELEASED / regional-home-release-not-confirmed

coverage empty/unavailable
→ UNKNOWN

stale negative após revalidation failure
→ UNKNOWN

Schema 1 sem upgrade possível
→ UNKNOWN
```

Regional mode não usa fallback de 365 dias.

`nextTransitionAt` para home day futura = início daquela data civil no timezone efetivo, limitado
por evidence/source boundaries mais cedo.

---

# 243. Series evaluator — preservar semântica temporal legacy

`releaseRegion` não entra em series.

Ordem:

```text
1. premiere/released confiável
   passada → RELEASED
   futura → UNRELEASED
2. sem date
   pre-release inequívoco → UNRELEASED
   post-release inequívoco → RELEASED
   ambíguo → UNKNOWN
```

`In Production`, `Canceled/Cancelled` sem premiere confiável continuam UNKNOWN/SHOW.

Não transformar date-only de TMDB/TVDB em calendar semantics regionais por acidente. A semântica
observável atual de Series precisa de fixture/golden própria antes de qualquer refactor.

---

# 244. CanonicalFilterContext + Dynamic State Taxonomy V9

Separar três coisas:

```ts
interface CanonicalFilterContext {
  // configuração/policy estática, já resolvida
}

interface RuntimeFilterState {
  // dados dinâmicos usados APENAS por pós-filtros
  watched?: {
    trakt?: RuntimeMembershipSet;
    anilist?: RuntimeMembershipSet;
    mdblist?: RuntimeMembershipSet;
    simkl?: RuntimeMembershipSet;
  };
}

interface RuntimeSourceState {
  // dados dinâmicos que alteram a própria fonte/shelf
  sourceRevision: string;
  validUntilMs: number | null;
}
```

## Impacto da v3.1.0

```text
Jellyfin/watch_state watchlist
Jellyfin dropped
pause/favourite events
```

são **source state** quando definem a shelf/lista, e não devem entrar automaticamente no
`filterSignature` da #742.

Somente o dataset que `applyCatalogFilters()` realmente consulta para Hide Watched pertence a
`RuntimeFilterState`.

Essa separação evita invalidar todos os cursores por eventos irrelevantes e evita, no sentido
oposto, manter cursor de uma shelf cuja source mudou.

---

# 245. Source page stability + refresh-ahead

`sourceMembershipSignature` descreve a definição da fonte; não prova que duas páginas vieram do
mesmo snapshot concreto.

Propagar metadata interna:

```ts
interface CacheReadMeta {
  cacheState: 'hit' | 'miss' | 'disabled';
  stableUntilMs: number | null;
  expiresAtMs: number | null;
  snapshotRevision?: string | null;
}
```

`stableUntilMs` = primeira boundary na qual refresh-ahead/expiry pode substituir aquela página.

Cursor:

```text
validUntil <= min(all source stableUntil, evidence freshness, runtime state, temporal transitions)
```

Se metadata de cache não puder ser exposta internamente, fallback conservador:

```text
disable refresh-ahead para reads que materializam cursor
+
cursor TTL <= actual page PTTL
```

---

# 246. Meta-hash evidence component — confirmado na HEAD V9

Na 3.1.0, `writeMetaComponentsWithConfig()` ainda faz:

```text
basicMeta[RELEASE_AVAILABILITY_FIELD] = meta[_releaseAvailability]
components.unshift({ name: 'basic', data: basicMeta })
writeMetaHashReplace(... same airWindowTtl ...)
coldStore.writeThrough(... basic ...)
```

Portanto o blocker não era falso: a evidence continua fisicamente dentro de `basic`.

V9 exige adicionar componente independente:

```text
releaseEvidence
```

com:

```text
own field/key identity;
own TTL;
own schema;
optional reconstruction;
no requirement for meta validity;
no initial cold-store write-through;
expiry independente de basic/art/cast/videos.
```

Migration:

```text
Schema 1 em basic antigo
→ advisory only / upgrade if raw fresh
→ nunca tratado como Schema 2 por cast
→ nova gravação deixa evidence fora de basic.
```

---

# 247. Cold store contract

Release regional negativa não pode herdar 60/180 dias de estabilidade do meta.

Primeira versão recomendada:

```text
releaseEvidence não entra no cold store
```

Se futuramente entrar:

```text
campo separado;
freshness factual preservada;
sourceFetchedAt preservado;
TTL próprio;
no negative freeze;
migration própria.
```

Cold-store `basic` legado contendo `_releaseAvailability` precisa ser sanitizado/ignorado na
reconstrução V9.

---

# 248. Search — EffectiveSearchSourceContext antes do cache

Resolver uma vez, antes de `cacheWrapSearch`:

```ts
interface EffectiveSearchSourceContext {
  requestedProvider: string;
  effectiveProvider: string;
  authMode: 'none' | 'v1-client' | 'v2-user' | 'other';
  capabilityRevision: string | null;
  pagingMode: 'page' | 'offset' | 'none';
  pageSize: number | null;
  supportsFilteredFill: boolean;
  accountScopeFingerprint?: string | null;
}
```

Casos atuais comprovados:

```text
Simkl disabled → default provider
Simkl V2 required sem connected account → default provider
Lumiere sem LUMIERE_API_BASE → default provider
```

Hoje esse fallback acontece dentro de `getSearch()` depois que a route já montou a search cache
key. V9 move a resolução para antes do cache e passa o mesmo contexto para execução/logs/metrics.

Nunca colocar token/tokenId/API key cru no context serializado.

---

# 249. Search cache V2 neutral + Schema V9

Remover da identidade do neutral search payload:

```text
hideUnreleasedDigitalSearch
hideUnreleasedShowsSearch
releaseRegion
logicalDay de visibility
```

Continuam na identidade apenas inputs que mudam upstream/hydration neutra.

A key/profile inclui:

```text
SEARCH_RESULT_CACHE_SCHEMA_VERSION
EffectiveSearchSourceContext sem secrets
neutral hydration profile
query/source paging input
RELEASE_EVIDENCE_SCHEMA apenas enquanto evidence continuar embutida no payload
```

Deploy migration:

```text
old filtered search cache
→ nunca lido como neutral V9
```

Provider adapters deixam de executar `Utils.isReleasedDigitally()` como policy local.

A HEAD atual ainda possui pre-filter em TMDB e Simkl, entre outros paths auditados; todos devem
ser removidos/classificados pelo occurrence gate.

---

# 250. Filtered Search Cursor V2

```ts
interface SearchCursorV2 {
  schema: 2;
  served: number;
  upstreamPage: number;
  upstreamOffset: number;
  sourceSignature: string;
  filterSignature: string;
  paginationSignature: string;
  validUntilMs: number | null;
  sourceStableUntilMs: number | null;
  dedupeRevision: number;
}
```

Key:

```text
e<CACHE_EPOCH>:search-cursor:v2:
userScope:
surface:
mediaType:
queryStrongHash:
sourceSig:
filterSig:
pagingSig
```

Providers pagináveis fazem neutral page fetch → evidence completion → filter → dedupe → fill.
Providers `pagingMode=none` filtram a resposta única e documentam short result.

Não simular page N repetindo provider não paginável.

---

# 251. Search capability matrix — deve ser codificada, não inferida ad hoc

Baseline auditada:

```text
TMDB keyword/people        → page
TVDB keyword/people        → page conforme adapter
MAL/Jikan                  → page
Kitsu                      → page
Simkl keyword/anime        → page

TVDB collections search    → none/current adapter unless proven otherwise
TVMaze composite           → none
Trakt current search       → none/current limited result
MDBList current search     → none/current adapter unless proven otherwise
IMDb Suggestions           → none
Lumiere current adapter    → none
Gemini/OpenRouter AI       → none unless explicit paging contract appears
```

Cada adapter ganha fixture que prova sua capability. Mudança de capability bumpa
`capabilityRevision` e source signature.

---

# 252. TMDB Collection legacy prefilter

Preservar `metadata.hideUnreleased` como feature distinta:

```text
part.release_date <= today UTC
```

Não é sinônimo de `hideUnreleasedDigital` e não usa 4/5/6.

Source profile/page cache/cursor precisam incluir:

```text
collection id;
sortDirection;
metadata.hideUnreleased;
UTC logical day quando hideUnreleased=true;
source schema.
```

Aplicar depois a policy central digital normalmente aos hydrated metas.

Golden-master congela a semântica UTC legacy deste toggle.

---

# 253. Release Region config + Discover provenance

Global:

```ts
releaseRegion?: string; // '' = Worldwide
```

Default de config antiga:

```text
Worldwide
```

Nunca inferir globalmente de `language=pt-BR`.

TMDB Discover pode sobrescrever global com `params.region` **somente com provenance válida**.

Persistir provenance fora dos params enviados ao TMDB:

```ts
metadata.discover.regionProvenance = {
  source: 'explicit' | 'watch-region-derived' | 'language-derived' | 'legacy-normalized';
  code: 'BR';
}
```

Regras:

```text
explicit/discover-explicit → override permitido;
watch-region-derived → permitido somente em Discover release-aware;
language-derived → não muda global Hide Unreleased silenciosamente;
legacy ambiguous → preserve + Worldwide policy até materialização inequívoca.
```

---

# 254. Countries UI/backend

Reutilizar a infraestrutura existente que chama:

```text
/configuration/countries
```

via endpoint de referência Discover já presente no projeto.

UI:

```text
Worldwide sempre disponível;
country codes normalizados ISO 3166-1;
reference failure não bloqueia config;
sem tabela manual duplicada.
```

Backend:

```text
trim + uppercase + known code validation;
invalid → warning deduplicado + Worldwide fallback;
UI list nunca substitui validação backend.
```

---

# 255. Collection Builder / import / export / AI / setup streaming

Round-trip obrigatório para:

```text
region
with_release_type
release_date.gte/lte
watch_region
releasedOnly
tmdbMovieReleaseTypes
region provenance
```

Arquivos centrais:

```text
addon/lib/collectionBuilder/catalogReconstruction.ts
addon/utils/ai-catalog-config-builder.ts
addon/utils/ai-catalog-generation.ts
addon/utils/ai-catalog-sanitizer.ts
addon/utils/ai-catalog-schema.ts
addon/utils/ai-catalog-entity-resolver.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
configure/src/components/sections/CatalogsSettings.tsx
configure/src/lib/setup/streaming.ts
```

Fixtures:

```text
region=BR + with_release_type=4|5|6
export/import/edit/save → permanece BR + provenance

watch_region=US sem release semantics
→ NÃO cria region=US

language-derived region
→ edit/save não promove automaticamente para explicit
```

---

# 256. Jellyfin, merged, external e warmers

A #742 só está completa quando os consumers alternativos usam os mesmos contratos.

## Jellyfin

Auditar:

```text
addon/lib/jellyfin/items.ts
  pageLengths
  catalogLengths
  walkCursors

addon/lib/jellyfin/collections.ts
  memberCursors

addon/lib/jellyfin/index.ts
addon/lib/jellyfin/people.ts
addon/lib/jellyfin/watchlist.ts
addon/lib/jellyfin/watched.ts
addon/lib/watchState.ts
```

`watch_state` V3.1 source state não vira release filter state.

## Merged catalogs

Identity inclui:

```text
ordered source definitions;
merge mode/order/randomization semantics;
each source strong identity;
filter signature;
paging contract;
source stability minimum.
```

## External/custom/StremThru

Cursor próprio precisa da mesma tríade source/filter/paging + validity.

## Warmers

```text
comprehensiveCatalogWarmer.js
cacheWarmer.js
malCatalogWarmer.js
```

usam o mesmo page-cache namespace/source profile e synthetic config com:

```text
releaseRegion=Worldwide
sem materializar user policy no neutral cache
mesma page-size/paging contract da route
```

---

# 257. Occurrence Gate V9 — baseline rastreada no HEAD

Code search no `dev@6e83e22` encontrou, entre outros:

```text
_releaseAvailability                  1 arquivo
releaseAvailability                   4
release_dates                         6
release_date                         28
first_air_date                       17
hideUnreleasedDigital               12
hideUnreleasedDigitalSearch          9
hideUnreleasedShows                  9
hideUnreleasedShowsSearch            6
watch_region                         11
with_release_type                     7
params.region                         2
applyCatalogFilters                   4 (inclui CHANGELOG; 3 code paths)
catalogFiltersActive                  3
discoverSig                           4
computeDiscoverSignature              1
tmdb:movie:release_dates              1
movieReleaseDates                     3
getMovieCertifications                3
normalizeTmdbReleaseDatesForCache     2
hideUnreleased                       19
simklUserTokenIfRequired              2
LUMIERE_API_BASE                      3
pageLengths                           1
catalogLengths                        2
walkCursors                           1
memberCursors                         1
cacheWrapSearch                       2
cacheWrapCatalog                      5
sourceRefetchRequested                2
runWithSourceRefetch                  3
CACHE_EPOCH                           5
hideWatchedTrakt                     10
hideWatchedAnilist                    9
hideWatchedMdblist                    9
hideWatchedSimkl                      9
/configuration/countries              1
```

Este baseline não substitui rerun antes do PR. Ele serve para detectar drift: qualquer contagem/path
novo precisa ser explicado.

## Paths de maior risco confirmados

```text
addon/utils/releaseAvailability.ts
addon/utils/catalogFilters.ts
addon/utils/parseProps.js
addon/lib/getCache.ts
addon/lib/getTmdb.ts
addon/lib/getSearch.ts
addon/lib/getCatalog.ts
addon/index.ts
addon/lib/catalogPagination.ts
addon/lib/discoverCatalogSignature.ts
addon/lib/tmdbCacheNormalizers.ts
addon/lib/cacheSourceRefetch.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/metaHashStore.ts
addon/lib/metaHashMigration.ts
addon/lib/metaColdStore/*
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
```

Cada ocorrência termina em exatamente um estado:

```text
A. changed
B. central helper covers it
C. explicit no-op with reason
D. regression test proves preservation
```

**Gate: zero unclassified.**

---

# 258. Mandatory file map V9

## Must-change / altamente provável

```text
addon/utils/releaseAvailability.ts
addon/utils/releaseVisibility.ts                 # novo
addon/utils/releaseRegion.ts                     # novo
addon/utils/catalogFilterContext.ts              # novo
addon/utils/catalogFilterSignature.ts            # novo
addon/utils/catalogSourceIdentity.ts             # novo
addon/utils/strongSignature.ts                    # novo
addon/utils/catalogFilters.ts
addon/utils/parseProps.js
addon/lib/catalogPagination.ts
addon/lib/getCatalog.ts
addon/index.ts
addon/lib/getSearch.ts
addon/lib/getCache.ts
addon/lib/getTmdb.ts
addon/lib/configApi.js
addon/types/index.ts

configure/src/contexts/config.ts
configure/src/contexts/ConfigContext.tsx
configure/src/components/sections/FiltersSettings.tsx
configure/src/lib/settingsSearchIndex.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
configure/src/components/sections/CatalogsSettings.tsx
addon/lib/collectionBuilder/catalogReconstruction.ts

addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
```

## Must-audit / fixture obrigatório

```text
addon/lib/metaHashStore.ts
addon/lib/metaHashMigration.ts
addon/lib/metaColdStore/*
addon/lib/cacheSourceRefetch.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/cacheEpoch.ts
addon/lib/tmdbCacheNormalizers.ts
addon/lib/discoverCatalogSignature.ts
addon/lib/tmdbDiscoverDateTokens.ts
addon/lib/getMeta.js
addon/lib/getTrending.ts
addon/utils/discoverParams.ts
addon/utils/mdbList.ts
addon/utils/simklUtils.ts
addon/lib/getPersonalLists.ts
addon/utils/recommendations/*
addon/utils/flixpatrolChart.ts
addon/lib/getManifest.ts
addon/lib/jellyfin/index.ts
addon/lib/jellyfin/people.ts
addon/lib/jellyfin/watchlist.ts
addon/lib/jellyfin/watched.ts
addon/lib/watchState.ts
configure/src/components/sections/TMDBIntegration.tsx
configure/src/utils/catalogUtils.ts
configure/src/lib/setup/streaming.ts
addon/utils/ai-catalog-*.ts
public/featured/*.json
package.json
tsconfig.backend.json
.github/workflows/pr-guard.yml
```

## Novos arquivos recomendados de teste/CI

```text
tests/release-visibility/*.test.ts
tests/integration/release-visibility-*.test.ts
tests/migration/release-visibility-*.test.ts
fixtures/release-visibility/*
tsconfig.test.json
.github/workflows/release-visibility-ci.yml
```

---

# 259. Test matrix V9 — unit/golden/integration/concurrency

Além de toda matriz V8, V9 torna obrigatórios:

```text
STRONG SIGNATURE
legacy 32/40-bit collision simulation
→ strong digest permanece distinto

RAW MONOTONIC WRITE
A fetch older termina depois de B newer
→ B continua armazenado

CROSS-PROCESS RACE
simular writers sem shared in-process single-flight
→ CAS impede stale overwrite

ZERO-VISIBLE PROGRESS
5 pages consumidas, 0 visible, source não exhausted
→ progress cursor persistido
→ budgetExhausted != upstreamExhausted

DEDUPE/CURSOR
cross-page duplicate + filtering
→ served/skip determinísticos

DST
NY spring/fall + London + Kathmandu/Chatham
→ next local midnight correto

V3.1 WATCH_STATE TAXONOMY
watchlist/dropped source muda
→ relevant Jellyfin source cursor invalidado
→ unrelated release filter signature não muda

ROLLBACK NAMESPACE
V9 escreve search/cursor/evidence namespace novo
→ V8 rollback não interpreta como antigo

DISCOVER STRONG SOURCE
same legacy discoverSig fixture / different canonical params
→ strong source signature distinta

SOURCE FETCHED AT
normalization/reconstruction/cache hit
→ sourceFetchedAt idêntico

SHORT PAGE BUDGET
budget exhausted com metas parciais
→ metric + non-terminal semantics
```

E manter:

```text
Worldwide golden master;
regional BR/US/GB;
results=[]/missing/malformed;
365d threshold;
series statuses;
Collection UTC semantics;
search neutral migration;
Simkl V2 auth scope;
Lumiere fallback;
page size/CACHE_EPOCH;
refresh-ahead;
Jellyfin cursors;
merged/custom cursors;
config round-trip;
response hygiene;
load/fanout budgets.
```

---

# 260. Test harness + CI

O `package.json` da v3.1.0 continua sem script de testes.

Usar preferencialmente o runtime já requerido:

```text
Node >=24 <25
node:test
assert/strict
ts-node ou build test dedicado
```

Scripts mínimos:

```json
{
  "test:release-visibility": "...",
  "test:integration": "...",
  "test:migration": "..."
}
```

Quality commands:

```text
npm run test:release-visibility
npm run test:integration
npm run test:migration
npm run build:backend
npm run build
npm run lint
```

CI:

```text
pull_request
permissions: contents: read
sem secrets de produção
Redis service container para integration/migration quando necessário
```

O atual `PR Guard` usa `pull_request_target`. Ele pode continuar fazendo somente metadata/API
checks, mas **não pode checkout/executar código não confiável do fork**.

PR Guard atual para contributor não isento:

```text
changed files <= 25
additions + deletions <= 1200
```

---

# 261. Migration matrix V9

Popular antes do upgrade:

```text
search cache antigo filtrado por hideUnreleasedDigitalSearch;
meta basic com ReleaseAvailability Schema 1;
raw release_dates gravado pelo writer 7d;
raw release_dates gravado pelo writer 24h;
catalog-cursor:v3;
qualquer cursor intermediário V4/V5 de branch de desenvolvimento;
custom/merged cursor legado;
cold-store basic com evidence antiga;
TMDB Collection cache old identity;
legacy discoverSig/cache entries;
```

Após upgrade:

```text
old filtered search não vira neutral;
Schema 1 não vira Schema 2 por cast;
raw namespace novo não herda stale TTL sem envelope factual;
old cursor não é desserializado como V6;
old search cursor não é V2;
cold basic não ressuscita evidence stale;
Collection cache não cruza sort/hide/day definition;
strong source signature não depende do legacy hash curto.
```

Preferir namespace/schema bump estreito; não usar `CACHE_EPOCH` global como martelo da feature.

---

# 262. Rollout e rollback V9

A feature tem default Worldwide, mas mudanças de cache/search/cursor afetam infraestrutura comum.
Por isso rollout em duas fases:

## Fase A — plumbing sem mudança de comportamento

```text
strong signature helpers;
raw owner + freshness envelope;
new cache/search namespaces;
new cursor schemas;
CanonicalFilterContext;
test harness/metrics;
Worldwide evaluator em shadow/golden parity quando possível.
```

UI regional ainda não exposta.

Gate:

```text
Worldwide parity;
error rate;
TMDB call amplification;
cache hit ratio;
p95/p99 catalog/search;
budget exhaustion;
revalidation failures.
```

## Fase B — feature regional opt-in

```text
Release Region UI;
Discover provenance;
regional evaluator;
lazy evidence completion ativa quando necessária.
```

## Rollback

```text
V9 namespaces possuem prefix/schema próprios;
V8 não lê V9 cursor/search/evidence como legado;
rollback pode abandonar V9 keys sem data migration destrutiva;
no silent DB write migration durante config read.
```

---

# 263. Observabilidade + cardinality/privacy

Counters/histograms recomendados:

```text
release_visibility_decision{surface,type,mode,state,reason}
release_evidence_fetch{cacheState,result}
release_revalidation{reason,result}
raw_release_write{result=written|discarded_older|failed}
filtered_paging_pages_read{surface,source}
filtered_paging_budget_exhausted{surface,source}
filtered_paging_zero_visible_progress{surface,source}
cursor_invalidated{reason}
search_source_resolved{requested,effective,authMode,pagingMode}
```

Evitar high-cardinality labels:

```text
movie id
query text
user id
region+catalog id combinados sem necessidade
raw SHA/signature completa como label
```

Nunca logar:

```text
access/refresh token;
raw tokenId;
API key;
full config;
full raw release payload;
watch history set.
```

Debug pode usar digest curto **somente para correlação**, nunca para correção.

---

# 264. Performance/budget contract

Lazy evidence completion é bounded:

```text
single-flight local por tmdbId/schema;
monotonic raw CAS para correção entre flights/replicas;
max concurrency explícita;
request-level lookup budget;
upstream timeout/retry limitado;
AbortSignal propagation;
negative/failure TTL curto;
UNKNOWN/SHOW quando budget/failure impede prova.
```

Load test mínimo:

```text
catalog 20 items, 0/25/50/90% sem evidence;
search 20 items, 0/25/50/90% sem evidence;
TMDB cache cold/hot/stale;
1, 10, 50 concurrent requests;
with/without Redis;
refresh-ahead concorrente;
```

Aceitação precisa definir números antes do merge, por exemplo:

```text
p95 added latency target;
max TMDB calls/request;
max in-flight release fetches;
max budget-exhausted rate em fixture realista.
```

Não inventar thresholds no plano; registrar os valores acordados no PR.

---

# 265. Implementation order V9

Para respeitar o PR Guard e evitar estado intermediário incorreto:

```text
PR 1 — contracts + strong signatures + test harness
  CalendarDate / Region / Clock
  evidence Schema 2
  strongSignature
  Worldwide/Regional/Series evaluators
  golden fixtures

PR 2 — canonical raw release_dates owner
  single writer
  sourceFetchedAt
  monotonic CAS
  forced fresh revalidation
  certification/meta/search callers

PR 3 — meta evidence component + canonical filter context
  releaseEvidence fora de basic/cold
  lazy completion
  freshness
  response hygiene

PR 4 — standard source/cache/paging V9
  CanonicalCatalogSourceProfile
  strong source/filter/paging signatures
  Cursor V6
  budget/exhaustion/progress
  dedupe contract
  TMDB Collection identity

PR 5 — Search neutral V2 + cursor V2
  EffectiveSearchSourceContext
  remove provider release prefilters
  search cache schema bump
  paged fill/nonpaged matrix

PR 6 — config/UI/builders/provenance
  global releaseRegion
  countries reuse
  Discover provenance
  reconstruction/import/export/setup/AI

PR 7 — merged/external/Jellyfin/warmers parity
  source/filter/runtime taxonomy
  cursor/stability parity
  v3.1 watch_state regression

PR 8 — rollout/observability/migration/perf
  metrics
  migration/rollback smoke
  concurrency/load
  docs
```

Se um PR depender de um namespace novo, ele deve ser semanticamente completo: não ativar novo filtro
sobre cursor/cache antigo.

---

# 266. Definition of Done V9 — gates cumulativos

## A. Snapshot Gate

```text
HEAD == 6e83e22ab9de5093f9918a1871157f401feebb03
OU delta posterior 100% classificado A/B/C/D.
```

## B. Occurrence Gate

Rerun todos os termos da seção 257 + novos:

```text
hashConfig
createHash('md5')
substring(0, 8)
substring(0, 10)
budgetExhausted
upstreamExhausted
fillOnce
writeCursor
watchState
watchlistEntries
droppedUnread
sourceFetchedAt
```

Zero unclassified.

## C. Raw Fact Gate

```text
one owner/writer;
one raw schema/TTL policy;
sourceFetchedAt factual;
monotonic CAS;
forced fresh realmente chega upstream;
last-known-good preservado;
replica/out-of-order race test passa.
```

## D. Evidence Gate

```text
Schema 2 deterministic;
sourceFetchedAt required;
negative freshness bounded;
releaseEvidence fora de basic/cold;
optional reconstruction;
response hygiene.
```

## E. Policy Gate

```text
Worldwide golden parity;
Regional 4/5/6 + CalendarDate;
Series region-independent;
UNKNOWN fail-open;
no 365d fallback regional.
```

## F. Source Identity Gate

```text
canonical source profile;
strong signature >=128 bits;
Discover params complete;
TMDB Collection sort/hide/day;
merged/external source identity;
secrets excluded.
```

## G. Pagination Gate

```text
Catalog Cursor V6;
Search Cursor V2;
filter/source/paging signatures;
validUntil;
source stability;
budget != exhaustion;
zero-visible progress;
dedupe before accounting;
page-size/CACHE_EPOCH invalidation.
```

## H. Search Gate

```text
EffectiveSearchSourceContext before cache;
neutral Search Cache V2;
provider prefilters removed;
paged fill;
nonpaged documented;
Simkl/Lumiere fallback cache-safe;
auth scope decision proven.
```

## I. Dynamic State Gate

```text
filter state != source state;
watched datasets loaded once/request;
v3.1 Jellyfin watchlist/dropped source revisions tested;
no unrelated cursor invalidation;
no secret in signatures/logs.
```

## J. Config/Builder Gate

```text
old config = Worldwide;
releaseRegion validation;
Discover provenance;
watch_region != global releaseRegion;
round-trip import/edit/save;
AI/setup streaming parity;
Countries reuse.
```

## K. Time Gate

```text
one RequestEvaluationClock;
365d exact boundaries;
regional CalendarDate;
DST/non-hour-offset tests;
midnight race test.
```

## L. Migration/Rollback Gate

```text
old search/meta/raw/cursor/cold populated;
upgrade safe;
rollback namespace-safe;
no destructive read migration;
no global epoch bump required solely for feature.
```

## M. Quality/CI Gate

```text
unit/golden;
integration Redis;
migration;
concurrency;
load/perf smoke;
backend build;
frontend build;
lint;
read-only pull_request CI;
PR Guard constraints.
```

---

# 267. Final pre-merge checklist V9

```text
[ ] HEAD `6e83e22...` revalidada ou delta classificado
[ ] issue #742 ainda aberta/escopo compatível
[ ] occurrence gate = zero unclassified
[ ] V8→V9 4-commit drift classificado
[ ] one raw release_dates owner
[ ] raw writer CAS monotônico
[ ] sourceFetchedAt factual/required
[ ] stale-negative forced revalidation provada
[ ] ReleaseAvailability Schema 2 deterministic
[ ] releaseEvidence fora de basic
[ ] cold store não congela evidence regional negativa
[ ] Worldwide golden parity
[ ] 365d -1ms/exact/+1ms
[ ] Regional BR/US/GB fixtures
[ ] Series ambiguous status fail-open
[ ] one RequestEvaluationClock/request
[ ] DST + fractional-offset calendar tests
[ ] strong source/filter/paging signatures
[ ] legacy 32/40-bit hashes não são correctness authority
[ ] TMDB Discover full source identity
[ ] TMDB Collection sort/hide/day identity
[ ] Catalog Cursor V6
[ ] Search Cursor V2
[ ] budgetExhausted separado de upstreamExhausted
[ ] zero-visible progress persistido
[ ] dedupe antes de served accounting
[ ] source refresh-ahead stability no validUntil
[ ] page-size + CACHE_EPOCH invalidam cursor
[ ] Search Cache V2 neutral
[ ] provider-level hide-unreleased removido
[ ] EffectiveSearchSourceContext único
[ ] Simkl V2/account scope provado
[ ] Lumiere fallback cache-safe
[ ] global releaseRegion default Worldwide
[ ] watch_region != global releaseRegion
[ ] Discover provenance round-trip
[ ] Collection Builder/import/export round-trip
[ ] AI/setup streaming parity
[ ] countries endpoint existente reutilizado
[ ] filter-state != source-state
[ ] v3.1 watchlist/dropped regressions
[ ] merged/external/Jellyfin/warmers parity
[ ] response hygiene
[ ] migration smoke
[ ] rollback smoke
[ ] concurrency race smoke
[ ] load/perf budgets definidos e aprovados
[ ] npm test scripts existem
[ ] read-only PR CI passa
[ ] build backend/frontend + lint passam
[ ] PR Guard passa ou split aprovado
```

---

# 268. Resultado final da auditoria V9

## O que está estaticamente validado

```text
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
Tree: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
583 entries / 544 blobs / 39 trees
V8→V9: 4 commits / 16 modified paths / no path add-delete
Issue #742: open / no comments no snapshot auditado
Package: 3.1.0 / Node >=24 <25 / sem test script
PR Guard: pull_request_target metadata checks; 25 files / 1200 total changes para não isentos
```

Também foi confirmado no código atual:

```text
_releaseAvailability Schema 1 ainda existe;
_releaseAvailability ainda é escrito dentro de basicMeta;
movieReleaseDates e getMovieCertifications competem pela mesma raw key com TTLs 7d/24h;
search cache ainda inclui hideUnreleasedDigitalSearch;
TMDB/Simkl ainda possuem provider-level digital filtering;
Simkl/Lumiere fallbacks acontecem dentro de getSearch após a route formar a cache request;
catalog cursor atual é v3 sem source/filter/paging signatures;
fillOnce não grava cursor quando metas.length === 0;
dedupe standard ocorre depois do fill;
discoverSig é MD5 8 hex;
hashConfig é MD5 10 hex;
source refetch e plain read possuem flights distintos mas final write é SET incondicional;
TMDB countries endpoint/reference já existe;
v3.1 adicionou dynamic watch_state/watchlist/dropped que precisa de source-state taxonomy.
```

## Novos blockers fechados pelo desenho V9

A V9 adiciona aos acertos do V8:

```text
strong correctness signatures;
monotonic raw-write CAS;
zero-visible progress;
budget-vs-exhaustion semantics;
dedupe/cursor accounting contract;
sourceFetchedAt obrigatório;
source-state vs filter-state taxonomy;
DST/fractional-offset calendar gate;
rollout/rollback namespace safety;
V8→V9 drift classification.
```

## Estado correto

```text
V9 = implementation-ready engineering design
```

**somente** quando os gates executáveis da seção 266 forem cumpridos.

---

# 269. O que “100% de precisão” significa neste documento

É defensável afirmar:

> **cobertura estática rastreável do snapshot `6e83e22` para as superfícies localizadas da #742,
> com occurrence/delta gates explícitos e desenho de testes para os fatos que só podem ser provados
> em runtime/upstream.**

Não é defensável afirmar antes de executar os gates:

```text
100% de completude factual do TMDB;
100% de ausência de race em Redis/replicas sem concurrency test;
100% de account-invariance Simkl sem fixture autenticada;
100% de performance sob produção sem load test;
100% de migration/rollback sem Redis/cold-store integration test;
100% de cobertura de commits posteriores ao audit HEAD.
```

Essas limitações não são buracos escondidos; são requisitos mensuráveis do DoD.

---

# 270. Limitações da sessão de auditoria

Esta V9 foi revalidada por inspeção estática do arquivo V8 completo, GitHub tree/compare/code search
e leitura direcionada dos arquivos críticos no HEAD `6e83e22`.

Não foi possível executar nesta sessão:

```text
checkout local completo do repositório;
TypeScript build do HEAD em workspace local;
Redis integration suite;
TMDB live fixtures com credenciais;
Simkl multi-account fixture;
load/concurrency benchmark real.
```

Um clone direto no ambiente local da sessão não resolveu DNS para `github.com`; por isso a auditoria
de código atual foi feita pela API/conector GitHub e não é apresentada como runtime validation.

Essa separação permanece obrigatória:

```text
VERIFIED STATIC FACT
→ comprovado no snapshot/código

DESIGN REQUIREMENT
→ mudança que a implementação deve realizar

RUNTIME GATE
→ só pode ser marcado após execução real
```

Essa é a forma tecnicamente correta de tornar o plano “o mais abrangente possível” sem transformar
incerteza de runtime em falsa certeza.
---

# 271. Reauditoria V10 — camada normativa final sobre a V9

Esta V10 é uma **re-auditoria corretiva** da V9 contra o mesmo snapshot de código:

```text
dev@6e83e22ab9de5093f9918a1871157f401feebb03
tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release v3.1.0
issue #742: open / 0 comments no momento da revalidação V10
```

Não houve drift de `dev` entre o fechamento estático da V9 e esta reauditoria V10. Portanto a V10
não reabre o delta inteiro por mudança de HEAD; ela corrige **gaps de contrato encontrados ao cruzar
o plano V9 com as implementações reais de paginação, raw cache, sharing/export e rollout**.

> **Precedência V10:** em qualquer conflito com as seções 1–270, as seções 271+ prevalecem.
> As seções antigas permanecem como trilha de auditoria e contexto histórico, mas não são a fonte
> normativa quando a V10 tornar um contrato mais estrito.

A alegação defensável continua sendo de **cobertura estática rastreável do snapshot**. Runtime,
Redis multi-replica, TMDB live, Simkl multi-account, load e rollback só se tornam fatos depois dos
gates executáveis definidos abaixo.

---

# 272. Novos blockers encontrados na V10

Além dos blockers A–Z já acumulados, a V10 acrescenta e fecha no desenho:

```text
AA. zero-visible checkpoint em served=0 é inútil se resolveStartPage() continuar retornando
    page 1 imediatamente para skip===0 antes de consultar o cursor;

AB. filtered pagination não pode cair para legacyPage/guess quando o cursor exato não foi alcançado;
    servir uma página estimada pode produzir gaps/overlap silenciosos;

AC. a preferência V9 por cross-page dedupe não é implementável de forma exata apenas com
    dedupeRevision/fingerprint; membership de dedupe exige estado exato ou policy response-only;

AD. upstreamOffset precisa ter sistema de coordenadas explícito. O helper atual faz slice(offset)
    depois do filtro; um cursor novo não pode chamar isso de raw upstream offset por ambiguidade;

AE. fillOnce é single-flight apenas no processo. Redis HSET incondicional permite conflito de
    cursor entre replicas quando duas materializações do mesmo served offset divergem;

AF. sourceSnapshotRevision não pode fingir snapshot global que o upstream não oferece. A garantia
    real deve ser definida como conjunto de páginas neutras imutáveis durante a validade do cursor;

AG. o novo envelope raw não pode sobrescrever a key legacy no rollout: rollback para baseline pre-V10 (`v3.1.0`) poderia ler
    envelope V10 como se fosse o payload TMDB antigo;

AH. storage retention e consumer freshness são conceitos distintos. Certifications precisa preservar
    SLA de ~24h, regional-negative pode exigir ~6h e outros consumidores podem aceitar facts mais
    antigos sem que existam dois writers/TTLs competindo;

AI. sourceFetchedAt é fato de observação, não relógio seguro de ordenação distribuída. CAS de raw
    writes deve usar fetchGeneration alocada monotonicamente pelo storage compartilhado;

AJ. stale evidence nunca pode produzir HIDE. Isso inclui home date futura stale, não apenas ausência
    regional stale; revalidation failure degrada para UNKNOWN/SHOW;

AK. account scope não pode ser derivado por hash simples de access token/tokenId. Preferir namespace
    por usuário; quando compartilhamento account-scoped for necessário, usar identificador estável
    não secreto + HMAC/versionamento, nunca secret hash reversível por dicionário;

AL. rollout precisa de kill switch e gate de frota homogênea. UI regional não pode ser ativada
    enquanto replicas antigas ainda puderem servir requests;

AM. rollback precisa provar forward-compat de config: V8 deve conseguir ler config salva pela V10
    sem crash e sem reinterpretar releaseRegion como outra coisa;

AN. falha ao carregar a lista de países na UI não pode apagar releaseRegion já salvo ao clicar Save;

AO. catalogSharing.ts/configure catalogShare usam sanitizer allowlist; provenance precisa de fixture
    explícita de share/export/import para não ser descartada por mudança estrutural futura;

AP. validade de cursor precisa de semântica de borda explícita: válido somente quando
    nowMs < validUntilMs e nowMs < sourceStableUntilMs, nunca na igualdade;

AQ. Redis TTL é limpeza de recurso, não autoridade de correção. Toda leitura de cursor revalida
    schema/signatures/boundaries mesmo quando a key ainda existe;

AR. skip arbitrário precisa ser atingido exatamente; um skip que cai dentro de um chunk não pode
    usar fallback de página. O walker deve conseguir avançar somente N itens visíveis até o target;

AS. a política de canonical serialization das strong signatures precisa ser especificada por domínio;
    arrays que são sets são ordenados, arrays cuja ordem altera source order não são reordenados.
```

Nenhum desses pontos exige alterar o objetivo funcional da #742. Eles fecham correção de
infraestrutura e de migração em torno da feature.

---

# 273. Raw TMDB release_dates V10 — namespace, retention, freshness e writer order

A V10 substitui a leitura ambígua de "single TTL/freshness contract" por quatro contratos separados:

```text
1. um único owner/writer;
2. um único schema de storage;
3. uma retention TTL de last-known-good;
4. freshness SLA por consumidor.
```

## 273.1. Namespace versionado obrigatório

**Não gravar o envelope novo na key legacy:**

```text
tmdb:movie:release_dates:<id>
```

Criar namespace novo, por exemplo:

```text
tmdb:movie:release_dates:v2:<id>
```

A versão da key e a versão do envelope podem evoluir independentemente, mas precisam ser explícitas.

Migration segura:

```text
read V10:
  new key v2
  → se ausente, pode ler legacy payload como seed advisory
  → normaliza
  → fresh fetch quando a policy exigir

write V10:
  somente new key v2

rollback para baseline pre-V10 (`v3.1.0`):
  continua vendo a legacy key no formato que já conhecia
  e nunca desserializa o envelope V10
```

**Proibido dual-write V10 envelope → legacy key.** Dual-write só seria permitido se o valor legado
fosse exatamente o payload antigo e houvesse necessidade operacional comprovada.

## 273.2. Envelope final

```ts
interface CachedReleaseDatesEnvelopeV2 {
  schema: 2;
  source: 'tmdb_release_dates';

  /** Ordem de fetch alocada pelo storage; autoridade para stale-write CAS. */
  fetchGeneration: number;

  /** Momento em que o upstream response bem-sucedido foi observado. */
  /** Clock autoritativo do storage quando compartilhado; usado para freshness. */
  sourceFetchedAtMs: number;
  sourceFetchedAt: string;

  /** Payload factual neutro e deterministicamente normalizado. */
  payload: TmdbReleaseDates;
}
```

`sourceFetchedAtMs` é a autoridade canônica de **idade factual** no raw shared cache; `sourceFetchedAt`
é o espelho ISO derivado do mesmo instante. Nenhum dos dois é a autoridade de
ordenação concorrente.

## 273.2.1. Clock autoritativo para freshness compartilhada

Quando o raw cache é compartilhado entre replicas, `sourceFetchedAtMs` não deve depender do
`Date.now()` de cada worker. O CAS de sucesso deve obter o tempo do próprio storage compartilhado
(ex.: `TIME` dentro do fluxo/Lua Redis) e derivar `sourceFetchedAt` ISO desse mesmo instante.

```text
shared Redis
→ storage time = freshness authority

in-memory/local-only
→ process clock permitido porque o estado não é compartilhado entre replicas
```

Isso separa três conceitos:

```text
fetchGeneration → write ordering
sourceFetchedAtMs → factual freshness age
RequestEvaluationClock → decisão temporal do request
```

Clock skew de host não pode fazer uma evidence de outra replica parecer artificialmente mais nova
ou mais velha no cache compartilhado.

## 273.3. Geração monotônica

Quando Redis for o storage compartilhado:

```text
fetch start
→ INCR tmdb:movie:release_dates:v2:generation:<id>
→ geração G reservada
→ upstream fetch
→ CAS write somente se G >= stored.fetchGeneration
```

Se um fetch de geração maior falhar, ele não grava nada e não impede um fetch anterior ainda válido
de preencher uma key ausente. Se uma geração maior já tiver gravado sucesso, geração menor é
descartada.

Sem storage compartilhado, a geração pode ser monotônica no processo porque não existe write
compartilhado entre replicas naquele modo. O teste deve cobrir ambos os backends suportados.

## 273.4. Retention != freshness

Definir:

```ts
interface ReleaseDatesFreshnessRequirement {
  maxAgeMs: number;
  forceUpstream?: boolean;
  purpose:
    | 'regional-release-hide'
    | 'certification'
    | 'meta-enrichment'
    | 'search-enrichment'
    | 'other';
}
```

Freshness defaults recomendados, preservando os contratos já observados:

```text
regional negative/future-HIDE max age ≈ 6h
certification max age <= 24h
outros consumers: explicitamente definidos, não herdados por acidente
```

A **retention TTL** da new raw key deve ser maior que os freshness SLAs relevantes e existir para
preservar last-known-good em falhas transitórias. Não usar a retention TTL para responder "fresh?";
calcular idade por `sourceFetchedAtMs`.

Constraint operacional:

```text
RAW_RETENTION_TTL > max(configured consumer maxAgeMs) + retry/backoff margin
```

Validar isso no startup/settings registry quando os valores forem configuráveis.

## 273.5. Last-known-good e failure

```text
fresh fetch success
→ CAS write new envelope

fresh fetch failure + LKG presente
→ não tocar sourceFetchedAt
→ não estender freshness
→ retornar stale/LKG como advisory

fresh fetch failure + sem LKG
→ unavailable
```

`lastAttemptAt`, error counters e retry/backoff pertencem à observabilidade/coordenação, não ao
fato normalizado que o evaluator consome.

---

# 274. Freshness V10 — regra universal para qualquer HIDE regional

A V9 explicitava stale-negative revalidation. A V10 generaliza a regra para remover outro falso
negativo possível:

> **Nenhuma evidence stale pode, sozinha, produzir `UNRELEASED → HIDE` em modo regional.**

Isso cobre:

```text
A. BR sem 4/5/6 em payload antigo;
B. BR home date futura em payload antigo;
C. payload available antigo cuja composição regional pode ter mudado.
```

Fluxo:

```text
candidate decision com evidence stale = HIDE
→ requireFreshAfter(regional policy SLA)
→ canonical raw revalidation

success
→ renormaliza
→ reavalia

failure
→ UNKNOWN
→ SHOW
```

Uma evidence stale que aponta `RELEASED` pode continuar como last-known-positive para SHOW sob a
policy fail-open, porque o risco assumido pela feature é evitar falso HIDE. Essa decisão deve ser
reason-coded (`stale-positive-fail-open`) e metrificada.

Worldwide continua preso ao golden-master legado; não importar esta mudança para Worldwide sem um
teste que prove equivalência observável.

---

# 275. releaseEvidence component V10 — storage advisory, freshness factual externa

A separação de `_releaseAvailability` para componente `releaseEvidence` continua obrigatória, mas a
V10 corrige a relação entre TTL físico e freshness:

```text
component storage TTL
→ retenção/cache efficiency

component.sourceFetchedAt
→ idade factual

canonical raw owner
→ autoridade para fresh refetch
```

Portanto o componente pode sobreviver fisicamente além da janela em que ele é autorizado a HIDE,
desde que:

```text
- schema seja validado;
- sourceFetchedAt seja preservado;
- evaluator consulte freshness antes de HIDE;
- stale evidence seja advisory;
- component read nunca renove sourceFetchedAt.
```

Isso evita acoplar a lifetime de `basic`/art/cast à factualidade de release e evita destruir
last-known-good só porque uma janela de decisão venceu.

---

# 276. Filtered pagination V10 — resolver exato, sem guessed fallback

A V10 substitui o contrato de `resolveStartPage()` por uma resolução discriminada.

```ts
type ResolveCursorResult =
  | {
      status: 'exact';
      served: number;
      position: UpstreamRawPosition;
    }
  | {
      status: 'upstream-exhausted';
      served: number;
      position: UpstreamRawPosition;
    }
  | {
      status: 'walk-budget-exhausted';
      served: number;
      position: UpstreamRawPosition;
    }
  | {
      status: 'invalidated';
      reason: CursorInvalidationReason;
    };
```

Para filtered pagination ativa:

```text
PROIBIDO:
unknown cursor
→ legacyPage guess
→ serve response como se fosse correta
```

Se o budget acabar antes de alcançar `requestedSkip`, a route não pode fabricar uma posição. Ela
retorna o comportamento degradado documentado da surface, não grava EOF e registra
`walk_budget_exhausted`.

Para clientes sem continuation token, a limitação de discoverability após página vazia continua
explicitada; correção não deve ser trocada por uma página silenciosamente incorreta.

---

# 277. Zero-visible progress V10 — corrigir especificamente served=0

O código atual possui o fast-path conceitual:

```text
skip === 0
→ start page 1
```

Antes de implementar o checkpoint zero-visible, alterar a ordem:

```text
1. validar cursor family/signatures;
2. procurar checkpoint exato de served=0;
3. somente se não existir, usar source start page 1/offset 0.
```

Quando um fill consome upstream mas retorna zero itens:

```text
served continua 0
position avança
progressMade=true
budgetExhausted=true|false
upstreamExhausted=false|true conforme fato
→ write checkpoint served=0
```

Teste obrigatório:

```text
request #1 skip=0
→ pages 1..N removidas por filtro
→ response vazia por budget
→ checkpoint 0 aponta depois de N

request #2 skip=0
→ começa no checkpoint
→ NÃO refaz pages 1..N
```

Se upstream estiver realmente esgotado, o cursor pode registrar exhaustion terminal para evitar
refetch sem necessidade dentro da mesma validade.

---

# 278. Skip arbitrário V10 — atingir o served target, não a página aproximada

`requestedSkip` é uma posição na **sequência pós-filtro servida**, não uma página upstream.

O walker precisa aceitar limite variável:

```ts
advanceFilteredSequence({
  from,
  targetServed,
  maxPages,
})
```

Exemplo com `pageSize=20`:

```text
known checkpoint served=0
request skip=17
→ consumir exatamente 17 itens visíveis
→ persist checkpoint served=17
→ então preencher até 20 itens da resposta
```

Nunca caminhar 20 e depois tentar voltar/estimar 17.

Matriz obrigatória:

```text
skip 0
skip 1
skip pageSize-1
skip pageSize
skip pageSize+1
skip arbitrário após página com muitos itens filtrados
skip arbitrário após zero-visible checkpoint
```

A normalização atual de cache-key `skip → page` pode continuar apenas para **neutral source pages**
quando semanticamente correta. Ela não define a posição do filtered cursor.

---

# 279. Sistema de coordenadas do cursor — `upstreamRawOffset`

Para remover a ambiguidade de `slice(offset)` pós-filtro, a V10 define a posição canônica como:

```ts
interface UpstreamRawPosition {
  page: number;
  rawOffset: number; // índice dentro da neutral raw/source page, antes de policy filtering
}
```

Pipeline de fill:

```text
fetch neutral raw page
→ enumerate { rawIndex, meta }
→ evidence completion em batch quando necessária
→ apply policy mantendo rawIndex
→ dedupe conforme policy
→ consumir candidatos visíveis
→ next rawOffset = rawIndex seguinte ao último raw item efetivamente consumido
```

Não usar `slice(offset)` sobre a lista já filtrada como representação de um campo chamado
`upstreamOffset`.

Se uma surface não consegue expor raw item position, ela precisa declarar outro coordinate system
explicitamente (`transformedOffset`) e incluí-lo no `paginationContractSignature`. Sistemas de
coordenadas diferentes nunca compartilham cursor schema sem discriminator.

---

# 280. Dedupe V10 — política exata por surface

A V10 remove a frase ambígua "bounded seen-set/fingerprint/window" como solução genérica.

**Fingerprint/Bloom/digest não pode responder membership correctness-critical.** Ele pode detectar
mudança, não decidir com exatidão se um ID já foi servido.

Policies permitidas:

```ts
type DedupePolicy =
  | { mode: 'response-only'; revision: number }
  | {
      mode: 'cursor-exact';
      revision: number;
      state: 'inline-exact-ids' | 'redis-set';
      stateRef: string;
    };
```

Regra:

```text
response-only
→ remove duplicatas antes do slot accounting dentro daquela resposta/walk;
→ NÃO promete ausência de duplicatas entre requests/páginas.

cursor-exact
→ usa membership exata;
→ seen state possui a mesma identity/TTL/validUntil do cursor family;
→ nenhum fallback probabilístico.
```

Escolha por surface deve ser documentada na capability matrix. Ativar `cursor-exact` somente onde o
custo é conhecido ou a source é bounded. Se a source já garante IDs únicos, registrar
`dedupe=source-guaranteed` no pagination contract e não manter seen-set redundante.

Quando um limite operacional de seen-state for atingido, não mudar silenciosamente para outra
semântica dentro da mesma signature. Invalidar/criar novo contract revision ou manter response-only
desde o início.

---

# 281. Catalog Cursor V7 e Search Cursor V3

A V6/V2 da V9 não contém informação suficiente para o contrato V10. Substituir por:

```ts
interface CursorPageSetState {
  /** Digest rolling das page revisions efetivamente consumidas. */
  revisionDigest: string;
  stableUntilMs: number | null;
}

interface CatalogCursorV7 {
  schema: 7;
  served: number;
  position: UpstreamRawPosition;

  sourceSignature: string;
  filterSignature: string;
  paginationSignature: string;

  pageSet: CursorPageSetState;

  validUntilMs: number | null;
  sourceStableUntilMs: number | null;

  dedupePolicy: DedupePolicy;
}

interface SearchCursorV3 {
  schema: 3;
  served: number;
  position: UpstreamRawPosition;

  sourceSignature: string;
  filterSignature: string;
  paginationSignature: string;

  pageSet: CursorPageSetState;

  validUntilMs: number | null;
  sourceStableUntilMs: number | null;

  dedupePolicy: DedupePolicy;
}
```

Keys:

```text
e<CACHE_EPOCH>:catalog-cursor:v7:...
e<CACHE_EPOCH>:search-cursor:v3:...
```

V6/V2 nunca são reinterpretados como V7/V3.

---

# 282. Cursor validity V10 — boundary semantics e TTL

Validade é read-time correctness:

```ts
function cursorStillValid(cursor, clock): boolean {
  return
    schema/signatures match &&
    (cursor.validUntilMs == null || clock.nowMs < cursor.validUntilMs) &&
    (cursor.sourceStableUntilMs == null || clock.nowMs < cursor.sourceStableUntilMs) &&
    pageSet still compatible;
}
```

Na igualdade:

```text
nowMs === validUntilMs
→ INVALID

nowMs === sourceStableUntilMs
→ INVALID
```

Redis TTL/LRU TTL deve ser no máximo o cleanup horizon desejado, idealmente limitado pelo menor
boundary conhecido, porém **a existência da key nunca implica validade**.

Ao ler cursor inválido:

```text
ignore
+ best-effort delete/expire
+ metric reason
```

Boundary tests:

```text
-1ms → valid
exact → invalid
+1ms → invalid
```

---

# 283. Cursor write concurrency V10 — detectar divergência entre replicas

`fillOnce()` local continua útil para reduzir trabalho, mas não é mutex distribuído.

Para um mesmo:

```text
cursor family + served offset
```

o write no storage compartilhado deve ser compare-and-set:

```text
field absent
→ write

field presente + canonical cursor equal
→ idempotent success / TTL refresh permitido

field presente + cursor diferente
→ NÃO last-write-wins
→ increment cursor_conflict
→ invalidar/bloquear a family corrente
→ request atual pode servir o resultado computado, mas não o apresenta como checkpoint estável
```

Uma divergência deveria ser impossível quando source pages e contexts realmente estão estáveis;
portanto ela é **invariant violation**, não condição normal.

Teste multi-client/multi-worker com barrier:

```text
worker A materializa served=20
worker B materializa served=20
interleaving controlado
→ mesmo cursor = idempotente
→ cursor divergente = conflict detectado, nunca overwrite silencioso
```

---

# 284. Source page-set consistency V10 — não prometer snapshot global inexistente

TMDB/Trakt/etc. não oferecem necessariamente snapshot token global entre páginas. Portanto a
terminologia normativa passa a ser:

```text
sourceMembershipSignature
→ definição da fonte

neutral page revision
→ revisão concreta de cada página cacheada

cursor page-set revisionDigest
→ composição das páginas realmente consumidas

sourceStableUntilMs
→ menor boundary em que alguma dessas páginas pode ser substituída
```

Não declarar que páginas 1..N vieram do mesmo instante upstream quando isso não pode ser provado.
A garantia V10 é:

> durante a validade do cursor, as neutral pages já consumidas que compõem a caminhada não mudam
> silenciosamente sob o cursor.

`CacheReadMeta` passa a exigir:

```ts
interface CacheReadMetaV10 {
  cacheState: 'hit' | 'miss' | 'disabled';
  revision: string;              // strong digest/version da neutral page concreta
  fetchedAtMs: number | null;
  stableUntilMs: number | null;
  expiresAtMs: number | null;
}
```

`revisionDigest` é identificador de conflito/diagnóstico e composição, **não** uma estrutura de
membership capaz de provar sozinho que todas as páginas antigas continuam presentes. A autoridade de
correção é a imutabilidade garantida até `stableUntilMs`; quando uma página consumida for relida, sua
`revision` exata deve ser comparada antes de continuar.

Se uma cache layer não consegue fornecer revision/stability confiável, essa surface não pode usar o
mesmo strong cursor path sem fallback conservador já definido (refresh-ahead off + bounded TTL +
local-only cursor quando aplicável).

---

# 285. Strong signatures V10 — canonical serialization specification

`buildStrongSignature(domain, payload)` permanece SHA-256 com >=128 bits efetivos, mas a entrada
precisa ser canônica por domínio.

Regras comuns:

```text
- object keys: ordem lexicográfica;
- undefined: omitido de forma explícita e testada;
- null: preservado;
- booleans/numbers/strings: tipo preservado;
- NaN/Infinity: rejeitados antes da assinatura;
- RegionCode: normalizado antes do payload;
- strings: usar exatamente a string efetiva enviada ao provider após normalização oficial;
- arrays cuja ordem é semântica: preservar ordem;
- arrays/set params cuja ordem NÃO é semântica: canonical sort + dedupe antes de assinar;
- version/domain prefix obrigatório;
- nenhum secret.
```

Não aplicar um sort genérico em todos os arrays.

Exemplos:

```text
sort_by sequence/order
→ order-sensitive

exclusion genres tratados como set
→ order-insensitive após canonicalização

merged source ordering quando altera ranking
→ order-sensitive
```

Golden fixtures da canonical serialization devem rodar em processos separados para impedir que
cache/mutation local esconda nondeterminism.

---

# 286. Auth/account scope V10 — privacy e correctness

Ordem de preferência:

```text
1. resposta user-invariant provada
   → source compartilhável, sem account scope;

2. resposta user-specific
   → namespace por userUUID interno no storage;

3. sharing por conta é necessário e comprovadamente seguro
   → stable non-secret provider subject + HMAC-SHA-256 com key dedicada/versionada;
```

Nunca:

```text
SHA256(access_token)
SHA256(refresh_token)
SHA256(raw tokenId secreto)
```

como fingerprint de cache/log.

Se não houver identificador estável não secreto, **não compartilhar cache entre usuários**.

Telemetria nunca expõe userUUID/account subject; usa cardinality controlada ou hash operacional
separado dos keys de storage.

---

# 287. Config/import/export provenance V10

`regionProvenance` continua armazenada dentro de:

```text
catalog.metadata.discover.regionProvenance
```

porque o sharing sanitizer atual preserva `metadata.discover` como unidade allowlisted.

Mesmo assim, adicionar fixtures explícitas para:

```text
DiscoverBuilder save
→ config
→ catalog share export
→ catalog share import
→ collection export/import/reconstruction
→ open editor
→ save
```

com:

```text
params.region = BR
regionProvenance.source = discover-explicit
with_release_type = 4|5|6
```

Resultado final idêntico semanticamente.

Também testar:

```text
watch_region=US
sem region
sem release semantics
→ nenhuma provenance regional inventada
```

Se `regionProvenance` for movida para outro nível de `metadata`, atualizar `SAFE_METADATA` no mesmo
PR. Nunca depender de o sanitizer "provavelmente" preservar um campo novo.

---

# 288. Countries UI V10 — failure-safe editing

O endpoint de países TMDB continua sendo reutilizado. Adicionar comportamento de falha:

```text
stored releaseRegion = BR
countries fetch falha
→ UI continua mostrando/preservando BR como valor existente
→ Save sem mudança NÃO envia ''/Worldwide
→ warning não destrutivo
```

Config inválida nova continua sendo rejeitada/normalizada no backend, mas indisponibilidade temporária
da reference list não pode apagar configuração válida já persistida.

Teste também:

```text
stored legacy Worldwide + fetch failure
→ continua Worldwide

stored valid-but-unlisted provider code + backend exception allowlist
→ round-trip preserva
```

---

# 289. Rollout V10 — kill switch, mixed-version fleet e config rollback

## 289.1. Kill switch

Adicionar capability operacional, por exemplo:

```text
RELEASE_VISIBILITY_REGIONAL_ENABLED=false|true
```

Fase A:

```text
false
→ toda plumbing/cache/cursor/evidence V10 pode rodar
→ comportamento efetivo continua Worldwide
→ UI regional escondida/disabled
```

Fase B somente depois dos gates:

```text
true
→ UI regional disponível
→ regional policy ativa
```

O valor efetivo/capability revision participa do `filterSignature`/policy identity para que mudar o
switch nunca reutilize cursor incompatível.

## 289.2. Frota homogênea

Antes de `true`:

```text
100% das replicas que servem catalog/search
→ versão que entende V10 config + namespaces + cursor
```

Durante rolling deployment:

```text
new code deployed
+ kill switch false
→ aguardar health/version convergence
→ executar smoke Worldwide
→ habilitar feature
```

Não expor regional mode enquanto requests puderem alternar entre `v3.1.0`/V10 semantics.

## 289.3. Rollback operacional

Ordem:

```text
1. kill switch false;
2. esperar propagation/convergence;
3. invalidar somente cursor/filter namespaces V10 se necessário;
4. downgrade app;
5. legacy raw key continua intacta;
6. V10 new raw/search/cursor keys podem expirar abandonadas.
```

## 289.4. Forward compatibility de config

Gate obrigatório:

```text
V10 salva:
  releaseRegion=BR
  metadata.discover.regionProvenance

baseline `v3.1.0` lê essa config
→ não crasha
→ não reinterpreta como watch_region/language
→ serve comportamento legado/Worldwide
```

Depois:

```text
baseline `v3.1.0` salva uma alteração não relacionada
→ testar se campos V10 permanecem
```

Se o baseline `v3.1.0` remover campos desconhecidos ao salvar, isso vira **blocker de rollback com edição**. Soluções
aceitáveis:

```text
A. proibir config edits durante rollback window;
B. backport preservation de unknown fields;
C. persistir extensão versionada compatível.
```

Não aceitar perda silenciosa de `releaseRegion` como comportamento de rollback.

---

# 290. Search V10 — herdar integralmente o novo cursor contract

Filtered search paginável usa a mesma engine de sequência que catálogo sempre que possível:

```text
EffectiveSearchSourceContext
→ neutral Search Cache V2+
→ neutral raw page + CacheReadMetaV10
→ evidence completion
→ CanonicalFilterContext
→ filter/dedupe
→ Search Cursor V3
```

Aplicam-se igualmente:

```text
zero-visible served=0 checkpoint;
no legacy page guess;
arbitrary skip exact-walk;
rawOffset coordinate system;
DedupePolicy exata;
page-set stability;
read-time validity;
cross-replica cursor CAS;
budget != upstream exhaustion.
```

Provider `pagingMode='none'` continua sem promessa de fill completo. Não criar cursor artificial para
uma source que não possui próxima página/offset recuperável.

---

# 291. Mandatory file map V10 — autoritativo

Esta seção substitui a seção 258 como checklist final.

## Must-change / highly probable

```text
addon/utils/releaseAvailability.ts
addon/utils/releaseVisibility.ts                    # novo
addon/utils/releaseRegion.ts                        # novo
addon/utils/catalogFilterContext.ts                 # novo
addon/utils/catalogFilterSignature.ts               # novo
addon/utils/catalogSourceIdentity.ts                # novo
addon/utils/strongSignature.ts                      # novo
addon/utils/catalogFilters.ts
addon/utils/parseProps.js

addon/lib/catalogPagination.ts
addon/lib/getCatalog.ts
addon/index.ts
addon/lib/getSearch.ts
addon/lib/getCache.ts
addon/lib/getTmdb.ts
addon/lib/tmdbCacheNormalizers.ts
addon/lib/cacheSourceRefetch.ts                     # ou substituir pelo raw owner dedicado
addon/lib/metaHashStore.ts
addon/lib/configApi.js
addon/types/index.ts

addon/lib/collectionBuilder/catalogReconstruction.ts
addon/lib/collectionBuilder/catalogSharing.ts
configure/src/lib/catalogShare.ts

configure/src/contexts/config.ts
configure/src/contexts/ConfigContext.tsx
configure/src/components/sections/FiltersSettings.tsx
configure/src/lib/settingsSearchIndex.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
configure/src/components/sections/CatalogsSettings.tsx
configure/src/components/setup/StreamingPickerDialog.tsx

addon/lib/dashboardApi.js
configure/src/components/dashboard/DashboardSystem.tsx

addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/collections.ts
```

## Must-audit / fixture obrigatório

```text
addon/lib/metaHashMigration.ts
addon/lib/metaColdStore/*
addon/lib/cacheRefreshAhead.ts
addon/lib/cacheEpoch.ts
addon/lib/discoverCatalogSignature.ts
addon/lib/tmdbDiscoverDateTokens.ts
addon/lib/getMeta.js
addon/lib/getTrending.ts
addon/lib/getPersonalLists.ts
addon/lib/getManifest.ts

addon/utils/discoverParams.ts
addon/utils/mdbList.ts
addon/utils/simklUtils.ts
addon/utils/recommendations/*
addon/utils/flixpatrolChart.ts
addon/utils/ai-catalog-*.ts

addon/lib/collectionBuilder/importers.ts
addon/lib/collectionBuilder/fusionExport.ts
addon/lib/collectionBuilder/nuvioExport.ts
addon/lib/collectionBuilder/blueprintLookup.ts
addon/lib/collectionBuilder/types.ts

addon/lib/jellyfin/index.ts
addon/lib/jellyfin/people.ts
addon/lib/jellyfin/watchlist.ts
addon/lib/jellyfin/watched.ts
addon/lib/watchState.ts

configure/src/components/sections/TMDBIntegration.tsx
configure/src/utils/catalogUtils.ts
configure/src/lib/setup/streaming.ts
configure/src/lib/setup/templateShare.ts

addon/static/catalog-types.json
addon/static/translations.json
public/featured/*.json

docs/*                                  # se contratos/setting público forem documentados
.env.example                            # se kill switch/freshness tunables forem públicos
addon/lib/settingsRegistry.ts           # se houver env/settings novos
package.json
tsconfig.backend.json
.github/workflows/pr-guard.yml
```

Arquivos da lista `must-audit` podem terminar como no-op, mas cada um precisa de classificação
`changed / covered-by-helper / explicit-no-op / regression-test` no occurrence gate.

---

# 292. Occurrence Gate V10 — termos e superfícies adicionadas

Além dos termos V9, buscar/classificar no audit HEAD e novamente no merge HEAD:

```text
catalogSharing
sanitizeMetadata
buildShareableCatalog
releaseRegion
regionProvenance
params.region
watch_region
with_release_type
release_date.gte
release_date.lte

resolveStartPage
fillFilteredPage
fillOnce
writeCursor
readCursor
clearCursor
legacyPage
startOffset
pageOffset
skip === 0

movieReleaseDates
getMovieCertifications
tmdb:movie:release_dates
cacheWrapGlobal
sourceFetchedAt
fetchGeneration

CacheReadMeta
stableUntilMs
snapshotRevision
refresh-ahead

accountScopeFingerprint
simklTokenId
access_token
refresh_token
```

Gate final:

```text
zero occurrence relevante sem classificação
+
zero path novo do delta de merge sem classificação
```

---

# 293. Test matrix V10 — novos casos obrigatórios

A matriz V9 continua válida e ganha:

## Raw owner / freshness

```text
1. legacy raw payload presente → V10 dual-read seed, single-write v2;
2. V10 envelope nunca escrito na legacy key;
3. certification pede <=24h e força refresh quando necessário;
4. regional HIDE pede <=configured regional SLA;
5. retention key existe além de freshness sem ser considerada fresh;
6. refresh failure preserva LKG e sourceFetchedAt;
7. generation 1 lento vs generation 2 rápido → gen2 vence;
8. generation 2 falha + gen1 sucesso com key ausente → gen1 pode preencher;
9. clock skew entre workers não decide write order nem freshness age no shared cache;
10. sourceFetchedAtMs compartilhado vem do storage clock;
11. stale future date que daria HIDE → revalidate; failure → UNKNOWN/SHOW.
```

## Cursor / pagination

```text
12. zero-visible skip=0 checkpoint é lido no request seguinte;
13. cursor exact lookup acontece antes do skip=0 source start;
14. walk budget exhausted nunca cai em legacyPage guess;
15. arbitrary skip 1 / pageSize-1 / pageSize+1 alcançado exatamente;
16. rawOffset aponta para neutral source coordinate, não filtered slice coordinate;
17. response-only dedupe tem contract/fixture explícita;
18. cursor-exact dedupe usa exact membership; fingerprint-only fixture deve falhar review;
19. duplicate crossing page boundary não desloca served accounting conforme a policy escolhida;
20. cursor boundary -1ms/exact/+1ms;
21. expired Redis cursor ainda presente é rejeitado read-time;
22. two workers same served same cursor → idempotent;
23. two workers same served different cursor → conflict, no last-write-wins;
24. source page revision muda antes de resume → cursor invalidado;
25. refresh-ahead boundary anterior ao cursor TTL → boundary vence;
26. Search Cursor V3 repete 12–25 nas providers pagináveis.
```

## Config / sharing / rollout

```text
27. share/export/import preserva discover.regionProvenance;
28. sanitizer allowlist change não apaga provenance;
29. countries request falha + stored BR + Save → BR preservado;
30. kill switch false + releaseRegion BR → effective Worldwide;
31. kill switch true → filter signature diferente;
32. mixed-version rollout: UI permanece off até fleet convergence;
33. V10-save → `v3.1.0`-read sem crash;
34. V10-save → `v3.1.0`-edit unrelated → V10 fields preservados OU rollback gate bloqueia release;
35. rollback não lê new raw/search/cursor namespace como legacy.
```

## Signature/privacy

```text
36. canonical object property order não muda digest;
37. order-sensitive array reorder muda digest;
38. set-like array reorder não muda digest após domain normalization;
39. undefined/null continuam distintos conforme spec;
40. token/API key nunca aparece em canonical payload/log snapshot;
41. user-specific authenticated cache não compartilha entre dois users sem prova explícita.
```

---

# 294. Observabilidade V10 — métricas novas

Adicionar métricas/reason codes de baixa cardinalidade:

```text
release_raw_cache_state{hit,stale,revalidated,error}
release_raw_write{accepted,stale_generation_discarded}
release_raw_age_bucket
release_revalidation_reason{negative_missing,future_date,certification,...}
release_hide_blocked_by_stale_evidence

filtered_cursor_resolve{exact,upstream_exhausted,walk_budget_exhausted,invalidated}
filtered_cursor_zero_visible_checkpoint_total
filtered_cursor_conflict_total
filtered_cursor_invalidation_reason
filtered_cursor_page_revision_mismatch_total

filtered_dedupe_mode{response_only,cursor_exact,source_guaranteed}
regional_feature_enabled{0|1}
```

Nunca usar como label:

```text
user UUID
TMDB title/id em cardinalidade aberta
query string livre
region por usuário individual
access token/token id
raw cursor key
```

Logs debug podem usar IDs técnicos somente onde a política existente do projeto já permitir e sem
secrets; métricas permanecem bounded.

---

# 295. Performance/budget V10

Além dos budgets V9, medir:

```text
raw revalidation amplification por 1k catalog items;
Redis INCR/CAS overhead do raw owner;
cursor CAS conflict rate;
raw-position bookkeeping overhead;
page revision digest overhead;
exact-dedupe memory quando habilitado;
zero-visible retries;
walk-to-arbitrary-skip page reads;
```

Proteções:

```text
batch evidence resolution;
per-request TMDB budget;
local single-flight obrigatório; distributed refresh lease obrigatório quando múltiplas replicas
compartilharem o raw namespace (single-replica pode manter o distributed lease como no-op/dispensável);
negative/transient backoff;
no correctness downgrade quando budget acabar;
```

Um distributed refresh lease pode reduzir chamadas duplicadas, mas **não substitui** generation/CAS:
lease é otimização; CAS é correção.

---

# 296. Implementation order V10

Ordem recomendada para reduzir superfície de regressão:

```text
PR 0 — Test harness / snapshot gate
  package test scripts
  fixed clocks
  Redis integration harness
  golden Worldwide
  occurrence/delta scripts

PR 1 — Strong identities + raw owner v2
  strongSignature canonicalization
  versioned raw namespace
  generation allocator + CAS
  retention/freshness split
  no behavior change

PR 2 — Evidence storage separation
  ReleaseAvailability Schema 2
  releaseEvidence component
  cold-store response hygiene
  canonical freshness checks

PR 3 — Policy/context
  CanonicalFilterContext
  RequestEvaluationClock
  movie Worldwide evaluator golden parity
  regional evaluator behind kill switch
  series evaluator hardening

PR 4 — Standard filtered sequence engine
  raw-position walker
  exact arbitrary skip
  zero-visible checkpoint
  DedupePolicy
  Catalog Cursor V7
  cursor CAS + page revisions

PR 5 — Search / custom / merged / Jellyfin / warmers
  EffectiveSearchSourceContext
  neutral Search Cache V2+
  Search Cursor V3
  source-specific cursor adapters
  warmer same contracts

PR 6 — Config/UI/builder/sharing
  global releaseRegion
  TMDB Discover provenance
  countries selector failure-safe
  reconstruction/share/export/import round-trips
  dashboard/telemetry decision

PR 7 — Rollout/observability/docs
  kill switch
  fleet convergence gate
  forward/rollback compatibility smoke
  metrics/load tests
  user-facing docs
```

PR Guard continua mandatório; se os limites do repositório impedirem um PR, dividir por esta ordem e
manter os feature flags desativados até o conjunto necessário estar presente.

---

# 297. Definition of Done V10 — gates cumulativos finais

Esta seção substitui a seção 266 como DoD autoritativo.

## A. Snapshot / delta

```text
[ ] merge HEAD conhecido
[ ] base audit HEAD conhecida
[ ] tree/delta classificados
[ ] issue #742 revalidada
[ ] zero changed path sem classificação
```

## B. Raw facts

```text
[ ] new versioned raw key; legacy key nunca recebe envelope novo
[ ] one writer/owner
[ ] fetchGeneration monotônica pelo storage compartilhado
[ ] CAS rejeita stale generation
[ ] sourceFetchedAt factual e não renovado em read/normalize
[ ] sourceFetchedAtMs do shared cache vem do storage clock
[ ] retention != freshness
[ ] certification <=24h contract preservado
[ ] regional HIDE freshness contract preservado
[ ] LKG sobrevive a transient refresh failure
```

## C. Evidence / policy

```text
[ ] Schema 2 deterministic
[ ] releaseEvidence fora de basic/cold authoritative path
[ ] stale evidence nunca produz regional HIDE
[ ] Worldwide golden parity
[ ] Regional 4/5/6 CalendarDate
[ ] Series region-independent
[ ] UNKNOWN fail-open
```

## D. Source/filter identity

```text
[ ] canonical source profile completo
[ ] canonical filter context único
[ ] strong digest >=128 bits
[ ] canonical serialization domain-tested
[ ] Discover full params/provenance
[ ] Collection sort/hide/day identity
[ ] secrets excluded
[ ] authenticated user-specific source scoped corretamente
```

## E. Pagination

```text
[ ] Catalog Cursor V7
[ ] Search Cursor V3
[ ] exact raw-position coordinate
[ ] arbitrary skip exact-walk
[ ] skip=0 lê checkpoint antes do source start
[ ] zero-visible progress persistido
[ ] no legacyPage guess em filtered path
[ ] budget != upstream exhaustion
[ ] DedupePolicy explícita por surface
[ ] no probabilistic membership para correctness
[ ] page revision/stability bound
[ ] cursor read-time boundary validation
[ ] cursor cross-replica CAS/conflict detection
[ ] page-size/paging/dedupe/CACHE_EPOCH invalidation
```

## F. Search / providers

```text
[ ] EffectiveSearchSourceContext antes do cache
[ ] neutral Search Cache namespace incompatível com legacy filtered cache
[ ] provider-level hide-unreleased removido
[ ] Simkl V1/V2/fallback/account scope testados
[ ] Lumiere fallback testado
[ ] paged providers usam V3 sequence contract
[ ] nonpaged providers documentados
```

## G. Config/UI/sharing

```text
[ ] old config = Worldwide
[ ] region validation/reference endpoint reuse
[ ] countries failure não apaga stored region
[ ] watch_region != global releaseRegion
[ ] Discover provenance round-trip
[ ] Catalog Builder reconstruction round-trip
[ ] catalogSharing/catalogShare preservation round-trip
[ ] AI/setup streaming parity
[ ] dashboard telemetry privacy decision
```

## H. Dynamic state / Jellyfin / merged / warmers

```text
[ ] RuntimeSourceState != RuntimeFilterState
[ ] v3.1 watchlist/dropped source revisions
[ ] watched filter revisions
[ ] merged source identity
[ ] external/custom cursor parity
[ ] Jellyfin pageLengths/catalogLengths/member cursors parity
[ ] comprehensive warmer uses same contract
[ ] synthetic warmer config remains Worldwide-neutral
```

## I. Time

```text
[ ] one RequestEvaluationClock
[ ] Worldwide 365d exact golden
[ ] regional CalendarDate
[ ] nextLocalMidnight IANA
[ ] DST + 30/45-minute offsets
[ ] cursor exact boundary invalidation
```

## J. Migration / rollout / rollback

```text
[ ] legacy raw/search/meta/cursor/cold fixtures populated
[ ] upgrade smoke
[ ] kill switch defaults safely for Phase A
[ ] 100% fleet convergence before Phase B
[ ] V10-save → `v3.1.0`-read smoke
[ ] `v3.1.0` unrelated-save preservation proven or rollback edit freeze documented
[ ] disable feature before downgrade
[ ] old app never parses V10 raw/search/cursor schema
[ ] no destructive read migration
```

## K. Quality / CI / performance

```text
[ ] unit/golden
[ ] Redis integration
[ ] concurrency/barrier tests
[ ] migration/rollback
[ ] backend build
[ ] frontend build
[ ] lint
[ ] read-only pull_request CI
[ ] PR Guard
[ ] TMDB call amplification budget
[ ] p95/p99 catalog/search smoke
[ ] cursor conflict = zero in normal stable-source test
```

---

# 298. Final pre-merge checklist V10

```text
[ ] HEAD atual revalidada no momento do merge
[ ] issue #742 escopo/status revalidado
[ ] occurrence gate V10 = zero unclassified
[ ] delta gate = zero changed path unclassified

[ ] raw key v2 versionada
[ ] legacy raw key preservada para rollback
[ ] retention TTL separada de freshness SLA
[ ] fetchGeneration storage-monotonic
[ ] shared sourceFetchedAtMs usa storage-authoritative clock
[ ] raw CAS race test passa
[ ] stale evidence nunca produz HIDE
[ ] certification freshness regression passa

[ ] ReleaseAvailability Schema 2
[ ] releaseEvidence component independente
[ ] sourceFetchedAt obrigatório
[ ] response hygiene
[ ] cold store não vira freshness authority

[ ] Worldwide golden parity
[ ] Regional BR/US/GB + absent/future/stale fixtures
[ ] no regional 365d fallback
[ ] Series ambiguous fail-open
[ ] one RequestEvaluationClock
[ ] DST/fractional offsets

[ ] strong canonical signatures
[ ] order-sensitive vs set-like array fixtures
[ ] legacy MD5 não é correctness authority
[ ] no secrets/token hashes em signatures

[ ] Catalog Cursor V7
[ ] Search Cursor V3
[ ] zero-visible served=0 resume
[ ] no guessed legacyPage fallback
[ ] arbitrary skip exact
[ ] rawOffset coordinate test
[ ] budgetExhausted != upstreamExhausted
[ ] DedupePolicy explícita por surface
[ ] cursor-exact usa membership exata
[ ] read-time cursor validity
[ ] page revision stability
[ ] cross-replica cursor CAS/conflict detection

[ ] EffectiveSearchSourceContext único
[ ] Search Cache neutral/versionada
[ ] provider prefilters removidos
[ ] Simkl auth/account scope seguro
[ ] Lumiere fallback seguro

[ ] global releaseRegion defaults Worldwide
[ ] kill switch false mantém Worldwide
[ ] watch_region separado de releaseRegion
[ ] Discover provenance preservada
[ ] countries fetch failure não apaga region
[ ] Catalog Builder round-trip
[ ] catalogSharing/export/import round-trip
[ ] AI/setup streaming parity
[ ] dashboard/telemetry classificado

[ ] v3.1 source-state/filter-state tests
[ ] custom/StremThru/merged/Jellyfin/warmers parity

[ ] mixed-version deployment gate
[ ] V10 config forward-compatible com rollback para `v3.1.0`
[ ] rollback smoke
[ ] migration smoke
[ ] concurrency smoke
[ ] load/perf budgets aprovados
[ ] CI/build/lint/PR Guard passam
```

---

# 299. Resultado final da reauditoria V10

## Confirmado estaticamente nesta V10

```text
HEAD dev ainda = 6e83e22ab9de5093f9918a1871157f401feebb03
Tree ainda = 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
Release correspondente = v3.1.0
Issue #742 continua aberta e sem comentários na revalidação

catalogPagination atual:
- cursor v3 contém apenas served/upstreamPage/pageOffset;
- skip===0 retorna source start antes de consultar cursor exato;
- fillOnce só grava cursor quando metas.length > 0;
- resolveStartPage pode cair em legacyPage quando não alcança skip;
- dedupe da route ocorre depois de fillFilteredPage;

raw release_dates atual:
- movieReleaseDates grava mesma key por 7d;
- getMovieCertifications grava mesma key por 24h;
- nenhum envelope/generation/CAS canônico existe no snapshot;

sharing atual:
- catalogSharing usa SAFE_METADATA allowlist;
- metadata.discover é preservada como unidade;
- provenance aninhada em discover pode sobreviver, mas faltava fixture normativa final.
```

## O que mudou de verdade da V9 para V10

A V9 já tinha a arquitetura principal correta. A V10 fecha os pontos onde o desenho ainda não era
implementável sem interpretação do desenvolvedor:

```text
- checkpoint zero-visible agora funciona também para served=0;
- cursor miss não pode mais virar guessed page;
- skip arbitrário ganha algoritmo exato;
- cursor offset passa a ter coordinate system definido;
- dedupe deixa de aceitar fingerprint probabilística como membership;
- cursor schema sobe para Catalog V7 / Search V3;
- cursor write ganha CAS/conflict detection entre replicas;
- page-set consistency substitui a alegação vaga de snapshot global;
- raw cache ganha namespace rollback-safe;
- fetchGeneration, não wall clock, ordena writes;
- retention e freshness por consumidor são separados;
- qualquer stale evidence é proibida de causar HIDE;
- account scope ganha regra segura de privacy;
- sharing/export entra no mandatory map;
- countries UI ganha save failure-safety;
- rollout ganha kill switch + homogeneous-fleet gate;
- rollback passa a incluir compatibilidade de config, não apenas de Redis namespaces.
```

## Estado correto do plano

```text
V10 = implementation-ready engineering design para o snapshot 6e83e22
```

**somente** com a seguinte interpretação:

> o design cobre estaticamente as superfícies localizadas e transforma tudo que depende de execução,
> upstream, concorrência ou deployment em gate mensurável. Nenhum gate não executado deve ser marcado
> como “100% provado”.

Se `dev` avançar um único commit antes da implementação/merge, executar novamente:

```text
Rebase Gate
+ Delta File Gate
+ Occurrence Gate V10
+ reclassificação de qualquer path tocado
```

antes de manter a alegação de cobertura completa do snapshot.
---

# 300. Reauditoria V11 — fechamento final sobre a V10

Esta V11 foi construída **sobre a V10 inteira**, sem remover a trilha histórica. O objetivo desta
camada é eliminar as últimas ambiguidades encontradas ao cruzar o plano com o snapshot real do
repositório e com os contratos públicos atuais do TMDB.

> **Precedência V11:** em qualquer conflito com as seções 1–299, as seções 300+ prevalecem.
> As seções 271–299 continuam sendo a base normativa V10; a V11 apenas torna mais estritos os pontos
> explicitamente corrigidos abaixo.

## 300.1. Snapshot revalidado novamente

```text
repo                       cedya77/aiometadata
branch                     dev
HEAD                       6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA                   00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release correspondente     v3.1.0
entradas na tree           583
blobs                      544
diretórios                 39
issue #742                 aberta / 0 comentários
V8 → V10                   4 commits / 16 arquivos modificados
```

Não houve drift novo entre a V10 e esta V11. Portanto **não é necessário reabrir o delta de código**;
a V11 é uma reauditoria de contratos e superfícies do mesmo snapshot.

## 300.2. Validação externa TMDB reexecutada

A documentação oficial atual continua confirmando:

```text
/movie/{movie_id}/release_dates
release type 4 = Digital
release type 5 = Physical
release type 6 = TV

/configuration/countries
→ lista de países ISO 3166-1 usada pelo TMDB

discover/movie
region + with_release_type
→ possuem semântica regional própria do TMDB
```

Logo a premissa funcional central da #742 permanece válida.

## 300.3. Limite da alegação de precisão

A V11 pode afirmar:

```text
cobertura estática rastreável do snapshot exato
+ contratos finais sem ambiguidades conhecidas
+ gates executáveis para runtime/upstream/concurrency/deployment
```

Ela **não** transforma em fato o que ainda depende de execução real. Os gates de Redis concorrente,
TMDB live, Simkl por conta, rollout/rollback, performance e CI continuam obrigatórios antes de dizer
que esses comportamentos foram provados em runtime.

---

# 301. Novos blockers fechados pela V11

Adicionar cumulativamente aos blockers A–AT:

```text
AU. O mandatory file map V10 não incluía o round-trip da configuração global por
    ConfigImportExport.tsx, exportConfigFile.ts e SaveContext.tsx. releaseRegion é global e precisa
    sobreviver a esses caminhos, não apenas ao catalog sharing.

AV. Neutral catalog/search payload pode ser contaminado se evidence completion pós-cache mutar o
    mesmo objeto mantido/reutilizado por uma cache em memória. Neutralidade exige também
    imutabilidade/request-local mutation safety, não apenas key neutra.

AW. Fail-open transitório (stale revalidation failure, storage failure, request budget exhaustion)
    pode mudar membership entre dois requests antes de qualquer validUntil normal. Um resultado
    transitório não pode gerar checkpoint/cursor apresentado como estável.

AX. sourceFetchedAtMs precisa representar o instante de observação do upstream response, não o
    instante tardio do CAS/write. Capturar o clock compartilhado apenas no final do write pode
    rejuvenescer artificialmente um fetch lento ou uma normalização atrasada.

AY. A V10 descrevia modo local/in-memory como se fosse backend de produção suportado. No snapshot
    real, Redis é requisito de startup e o servidor espera Redis ficar ready antes de servir.
    In-memory branches são test seams/fallbacks locais, não um deployment mode normativo.

AZ. Runtime Redis failure depois do boot precisa de semântica explícita para operações
    correctness-critical. Nunca cair silenciosamente para last-write-wins, freshness local ou cursor
    distribuído fictício.

BA. Cursor-exact dedupe precisa de resource bounds exatos. "membership exata" sem limite de IDs,
    bytes e política de overflow abre caminho para crescimento não limitado de Redis/memória.

BB. Neutral Search Cache precisa de prova de equivalência: ligar/desligar Hide Unreleased não pode
    mudar a key nem o payload upstream/hydration neutro. Remover o hide flag da key sem remover
    conditional enrichment/prefilter não basta.
```

---

# 302. Config global V11 — save/export/import/cache round-trip obrigatório

A V10 já cobre `configApi.js`, tipos, defaults e UI principal, porém a feature adiciona um campo
**global**:

```ts
releaseRegion?: string;
```

O snapshot real possui caminhos genéricos adicionais que hoje tendem a preservar campos por object
spread. Essa propriedade é favorável, porém precisa ser **provada por fixture**.

## 302.1. Superfícies adicionais

Classificar obrigatoriamente:

```text
configure/src/components/ConfigImportExport.tsx
configure/src/lib/exportConfigFile.ts
configure/src/contexts/SaveContext.tsx
addon/lib/configCache.ts
addon/lib/configAccess.ts
```

Também classificar qualquer helper chamado por esses fluxos que:

```text
- projete AppConfig para outro objeto;
- faça whitelist/pick/omit de settings;
- serialize/deserializa config;
- calcule dirty fingerprint;
- clone config compartilhada;
- reconcilie imports.
```

## 302.2. Contrato

```text
stored config releaseRegion=BR
→ load UI
→ save unrelated field
→ releaseRegion continua BR

stored config releaseRegion=BR
→ export full config
→ import
→ releaseRegion continua BR

export com API keys excluídas
→ releaseRegion continua BR

config cache hit
→ runtime normalization NÃO muta shared object
→ stored/cache value bruto continua semanticamente igual
```

O código atual de export usa spread de `config`, e o import usa spread de `importData.config`; isso
faz o caminho parecer compatível hoje. Mesmo assim, a fixture entra no DoD porque uma whitelist
futura ou refactor pode quebrar a feature silenciosamente.

## 302.3. Stored vs effective region

Separar conceitualmente:

```ts
interface RuntimeReleaseRegionResolution {
  storedValue: string | null;       // preservado para round-trip/UI
  effective: EffectiveReleaseRegion; // validado + kill switch + provenance
}
```

Se um valor persistido deixar de ser reconhecido temporariamente:

```text
runtime → Worldwide fail-safe + warning
save unrelated → não apagar automaticamente storedValue
```

Somente uma ação explícita do usuário deve substituir o valor persistido por Worldwide.

---

# 303. Neutral payload immutability V11

Neutral cache significa duas coisas independentes:

```text
A. neutral cache identity;
B. neutral cached object state.
```

A V10 fecha A. A V11 torna B obrigatório.

## 303.1. Regra

Qualquer etapa pós-cache que dependa de usuário/policy:

```text
ensureReleaseEvidenceForFilter
release visibility
watched filtering
region-specific decoration usada somente para policy
request-local reason/debug state
```

NÃO pode mutar o objeto compartilhado armazenado/reutilizado pela neutral cache.

Implementações aceitas:

```text
1. evidence sidecar/component fora do neutral page payload; OU
2. clone request-local somente dos metas/campos que serão enriquecidos; OU
3. funções persistent/immutable que retornam novos objetos.
```

Não exigir deep-clone indiscriminado de todo meta se houver opção mais barata; exigir apenas
**ausência de aliasing mutável entre cache owner e request policy**.

## 303.2. Testes poison-pill

```text
1. deep-freeze neutral cached payload
   → executar evidence completion + filter
   → zero mutation exception

2. request A: BR + hide ON
   → filtra regionalmente
   request B: Worldwide + hide OFF usando a mesma neutral key
   → recebe payload neutro completo

3. request A falha durante enrichment
   → nenhum campo parcial fica preso na neutral cache para request B
```

---

# 304. Transient Filter Stability V11 — fail-open não pode virar cursor estável

A regra V10:

```text
stale evidence que produziria HIDE
→ revalidate
→ failure
→ UNKNOWN/SHOW
```

é correta para visibilidade, mas falta um segundo efeito: **a decisão ficou transitoriamente
instável**.

Exemplo:

```text
request 1
stale BR-negative
TMDB timeout
→ SHOW fail-open

request 2, 10 s depois
TMDB responde
→ HIDE
```

Se o request 1 tiver persistido um cursor estável como se membership fosse durável, o request 2 pode
produzir overlap/gap mesmo com signatures iguais.

## 304.1. Novo resultado agregado

Estender conceitualmente o resultado do filtro:

```ts
type StabilityCause =
  | 'stable'
  | 'release-revalidation-failed'
  | 'release-budget-exhausted'
  | 'correctness-storage-unavailable'
  | 'dynamic-filter-refresh-failed'
  | 'other-transient';

interface FilterResultV11 {
  metas: any[];
  nextTransitionAt: Date | null;
  stableUntilMs: number | null;
  checkpointable: boolean;
  stabilityCause: StabilityCause;
}
```

Regras:

```text
normal fresh evaluation
→ checkpointable=true

fail-open por erro transitório capaz de mudar membership no próximo request
→ checkpointable=false

request budget acabou antes da evidence obrigatória para uma decisão estável
→ checkpointable=false
```

A resposta atual pode ser servida. O que não pode é publicá-la como uma posição durável de uma
sequência estável.

## 304.2. Cursor behavior

Quando `checkpointable=false`:

```text
- não gravar cursor estável para o served boundary produzido;
- não refreshar TTL de cursor antigo incompatível;
- se necessário, invalidar a family quando a instabilidade ocorreu no meio de um walk;
- próximo request resolve por checkpoint estável anterior e reexecuta o trecho;
- reason/metric obrigatório.
```

Isso é diferente de `upstreamExhausted` e de `walkBudgetExhausted`.

---

# 305. Raw owner V11 — sourceFetchedAt é acquisition time, não commit time

A V10 corretamente separa:

```text
fetchGeneration → ordering
sourceFetchedAtMs → freshness
```

A V11 fixa o **ponto exato de captura**.

## 305.1. Sequência final

```text
1. reservar fetchGeneration G no Redis;
2. executar TMDB request;
3. upstream response válido chega;
4. imediatamente obter Redis TIME;
5. guardar observedAtMs desse Redis TIME;
6. normalizar/validar payload;
7. CAS write usando G como autoridade de ordering;
8. persistir sourceFetchedAtMs = observedAtMs.
```

Nunca:

```text
upstream response chega
→ 30 s de fila/normalização
→ Redis TIME no write
→ sourceFetchedAt = 30 s mais novo que o fato observado
```

## 305.2. Se Redis TIME falhar após um fetch upstream bem-sucedido

O payload pode ser usado **somente no request atual** como evidence fresca request-local, desde que a
resposta TMDB tenha sido validada.

```text
não persistir envelope compartilhado com timestamp de host fingindo storage authority;
marcar correctness storage unstable;
checkpointable=false para sequência dependente dessa decisão;
```

Quando Redis voltar, uma nova operação pode materializar o raw owner normalmente.

---

# 306. Redis V11 — produção exige Redis; runtime failure é modo degradado, não backend alternativo

## 306.1. Correção normativa da V10

No snapshot auditado:

```text
redisClient.ts
→ instancia ioredis sempre

server.ts
→ waitForRedisReady()
→ assertMetaHashSupport()
→ só então readiness redis
```

Portanto remover da interpretação normativa qualquer frase do tipo:

```text
"backend local/in-memory suportado em produção"
```

A implementação pode manter fallback/mocks em helpers para unit tests, mas o deployment suportado da
feature herda o requisito Redis do AIOmetadata.

## 306.2. Falha de Redis após boot

Separar operações:

```text
best-effort cache optimization
vs
correctness-critical coordination
```

São correctness-critical nesta feature:

```text
raw fetchGeneration allocation
raw CAS write/read freshness authority
cursor CAS
cursor read/write quando filtered pagination depende de continuidade distribuída
page revision/stability metadata quando compartilhada
```

Se uma delas falhar:

```text
NÃO inventar generation local compartilhável;
NÃO usar host Date.now como shared freshness authority;
NÃO last-write-wins;
NÃO gravar checkpoint distribuído estável;
```

A route pode:

```text
A. servir resultado request-local fail-open e checkpointable=false; OU
B. seguir a política global existente de erro/503 se aquela surface não puder ser servida com
   correção sem o storage.
```

A escolha deve ser única por surface e testada. Para Hide Unreleased, quando existe dúvida factual,
a preferência continua `UNKNOWN → SHOW`, mas **pagination state nunca finge estabilidade**.

---

# 307. Exact Dedupe V11 — resource budget obrigatório

`cursor-exact` exige membership exata. Isso não autoriza crescimento ilimitado.

Definir por surface:

```ts
interface ExactDedupeBudget {
  maxIds: number;
  maxSerializedBytes: number;
  ttlMs: number;
}
```

O budget entra em:

```text
PAGINATION_CONTRACT_SIGNATURE
```

quando sua alteração puder mudar o comportamento da sequência.

## 307.1. Overflow

Proibido:

```text
exact set atingiu limite
→ trocar silenciosamente para Bloom/filter fingerprint
```

Aceitável:

```text
A. invalidar family + exact re-walk com strategy declarada;
B. surface declaradamente response-only dedupe desde o início;
C. source-guaranteed unique quando isso for contrato comprovado.
```

Se `cursor-exact` for escolhido e o limite for alcançado sem caminho exato disponível:

```text
request atual pode terminar com status operacional explícito;
nenhum checkpoint incorreto é persistido.
```

Métricas:

```text
filtered_dedupe_exact_ids
filtered_dedupe_exact_bytes
filtered_dedupe_budget_exceeded_total
```

Nunca usar ID individual como label.

---

# 308. Search Cache V11 — prova de neutralidade por equivalência

A V10 já exige remover `hideUnreleasedDigitalSearch` da neutral identity e remover provider
pre-filters. A V11 adiciona uma prova que detecta os dois lados ao mesmo tempo.

## 308.1. Equivalence fixture

Para mesmo:

```text
query
mediaType
effective provider/auth/capability
language
neutral hydration inputs
```

executar:

```text
Run A: hideUnreleasedDigitalSearch=false, releaseRegion=Worldwide
Run B: hideUnreleasedDigitalSearch=true,  releaseRegion=BR
```

Antes da etapa de evidence completion/policy:

```text
neutral search key/profile A == B
neutral provider request sequence A == B
neutral cached payload semantic digest A == B
```

Depois do cache:

```text
FilterContext/signature A != B quando a policy efetiva for diferente
final response pode diferir
```

## 308.2. Conditional enrichment guard

Qualquer código equivalente a:

```text
if (hideUnreleased...) fetch/enrich release facts antes de gravar neutral search cache
```

é proibido, salvo se o enrichment fizer parte de **todos** os neutral requests independentemente da
policy. Preferência:

```text
neutral cache
→ request-local evidence completion
→ filter
```

Isso evita que duas configs gerem o mesmo cache key, mas payloads diferentes dependendo de quem
preencheu primeiro.

---

# 309. Contratos finais consolidados V11 — tabela anti-ambiguidade

Como as seções históricas mantêm snippets de versões antigas, esta tabela é a fonte rápida final.

```text
RAW release_dates namespace             tmdb:movie:release_dates:v2:<id> (ou equivalente versionado)
legacy raw namespace                    somente read advisory / nunca receber envelope V11
Release Evidence schema                 2
Release Visibility policy               versionada separadamente
Search neutral cache                    namespace/schema incompatível com legacy filtered cache
Catalog Cursor                          V7
Search Cursor                           V3
source position                         raw upstream coordinate
cursor miss filtered                    exact walk / exhausted / invalid / budget; nunca page guess
cursor boundary                         estritamente now < validUntil e sourceStableUntil
cursor concurrency                      CAS + conflict detect
release raw ordering                    fetchGeneration storage-monotonic
release freshness clock                 Redis TIME capturado imediatamente pós-upstream success
regional stale would-HIDE               revalidate; failure => UNKNOWN/SHOW
transient fail-open                     checkpointable=false
neutral cached payload                  immutable em relação à policy request-local
correctness signatures                  SHA-256 / >=128 bits efetivos / canonical domain encoding
short MD5 legacy                        debug/compat somente
production coordination                 Redis obrigatório no snapshot auditado
```

Qualquer snippet anterior com Cursor V6/V2, key legacy ou local-only production deve ser tratado como
**histórico**, não como implementação copiável.

---

# 310. Mandatory file map V11 — adições à seção 291

A seção 291 permanece válida e ganha:

## Must-audit / regression fixture obrigatório

```text
configure/src/components/ConfigImportExport.tsx
configure/src/lib/exportConfigFile.ts
configure/src/contexts/SaveContext.tsx
configure/src/components/ConfigurationManager.tsx

addon/lib/configCache.ts
addon/lib/configAccess.ts

addon/lib/collectionExportRoutes.js
configure/src/lib/collectionBuilder/*
configure/src/components/sections/collectionBuilder/*

addon/lib/redisClient.ts
addon/lib/redisReady.ts
addon/server.ts
```

Classificação permitida:

```text
changed
covered-by-helper
explicit-no-op
regression-test
```

Nenhum desses arquivos precisa obrigatoriamente mudar se o contrato atual já for genérico e seguro;
o requisito é **não deixá-los fora da prova**.

---

# 311. Occurrence Gate V11 — termos adicionais

Acrescentar ao gate V10:

```text
ConfigImportExport
exportConfigFile
configToSave
fingerprintConfig
setConfig
loadSharedConfig
configCache

normalizeReleaseAvailabilityInPayload
ensureReleaseEvidence
_releaseAvailability
releaseEvidence
Object.freeze
deepFreeze

checkpointable
stabilityCause
revalidation failure
budget exhausted
storage unavailable

waitForRedisReady
assertMetaHashSupport
redisClient
Redis TIME
fetchGeneration
CAS

exact dedupe
maxIds
maxSerializedBytes

hideUnreleasedDigitalSearch
hideUnreleasedShowsSearch
searchConfig
cacheWrapSearch
```

Gate final V11:

```text
zero ocorrência relevante sem classificação
+
zero arquivo novo encontrado por esses termos fora do file map/classification ledger
+
zero changed path do merge HEAD sem classificação
```

---

# 312. Test Matrix V11 — casos novos obrigatórios

A matriz V10 continua cumulativa e ganha:

## Config round-trip

```text
42. releaseRegion=BR → SaveContext save unrelated → BR preservado;
43. releaseRegion=BR → full export/import → BR preservado;
44. export sem API keys → BR preservado;
45. invalid stored region → runtime Worldwide, unrelated save não apaga stored value;
46. loadSharedConfig object não é mutado por runtime normalization.
```

## Neutral payload mutation safety

```text
47. deep-frozen neutral search payload + filter → zero mutation;
48. BR/hide ON request não contamina Worldwide/hide OFF request na mesma neutral cache;
49. partial enrichment failure não persiste fields incompletos no neutral payload;
50. equivalent neutral catalog page recebe a mesma proteção quando evidence completion é pós-cache.
```

## Transient stability

```text
51. stale would-HIDE + TMDB timeout → SHOW + checkpointable=false;
52. request seguinte revalidation success → HIDE sem overlap/gap porque cursor instável não foi salvo;
53. evidence budget exhausted → fail-open + checkpointable=false;
54. runtime Redis failure em raw coordination → nenhum shared timestamp/generation local inventado;
55. runtime Redis failure em cursor CAS → response pode ser servida, cursor estável não é gravado.
```

## Raw acquisition timestamp

```text
56. upstream success em T0 + normalization/write atrasado 30s → sourceFetchedAt ~= T0, não T0+30s;
57. gen2 mais novo escreve antes de gen1 → generation decide ordering mesmo que observedAt seja próximo;
58. Redis TIME failure após upstream success → request-local only / no shared envelope falso.
```

## Exact dedupe budget

```text
59. exact set abaixo do limite → resume perfeito;
60. exatamente no limite → comportamento definido;
61. limite+1 → nunca degrada para probabilístico silenciosamente;
62. budget change que altera sequência invalida pagination signature quando aplicável.
```

## Search neutral equivalence

```text
63. hide OFF Worldwide vs hide ON BR → neutral cache key igual;
64. mesmos runs → neutral provider request sequence igual;
65. mesmos runs → neutral cached payload semantic digest igual;
66. final filter signatures diferentes quando policy efetiva difere;
67. ordem de quem aquece a cache (ON primeiro vs OFF primeiro) não altera o segundo request.
```

---

# 313. Observabilidade V11 — complementos

Adicionar baixa cardinalidade:

```text
release_raw_observation_clock{redis_time,error}
release_raw_persist{stored,not_stored_storage_unavailable}
release_filter_stability{stable,revalidation_failed,budget_exhausted,storage_unavailable}
filtered_cursor_checkpoint{written,skipped_transient,conflict,invalid}
filtered_dedupe_budget_exceeded_total
neutral_cache_mutation_guard_total
search_neutral_equivalence_mismatch_total   # test/staging; não precisa ficar enabled em prod
config_release_region_roundtrip_error_total # somente se existir runtime validation path
```

Não adicionar labels de user/query/title/token.

---

# 314. Implementation Order V11 — ajustes finais

A ordem V10 continua, com quatro inserções para reduzir risco:

```text
antes de UI regional:
  1. consolidar raw owner + acquisition timestamp + Redis failure semantics;
  2. neutral payload immutability guard;
  3. transient FilterResult/checkpointable propagation;
  4. config global round-trip fixtures;

antes de habilitar filtered pagination V7/V3:
  5. exact dedupe budget/overflow contract;
  6. runtime Redis cursor failure fixture;

antes de merge:
  7. Search neutral equivalence test OFF/ON;
  8. occurrence gate V11;
  9. full config export/import/save gate;
  10. V11 pre-merge checklist.
```

A UI continua Phase B, depois de backend/namespace/observability e fleet convergence.

---

# 315. Definition of Done V11 — gates adicionais

Somar à seção 297:

```text
[ ] config full save/export/import preserva releaseRegion
[ ] config cache normalization não muta shared object
[ ] stored invalid region não é apagada por save não relacionado

[ ] neutral page/search payload não é mutado por request policy
[ ] deep-freeze mutation fixtures passam
[ ] order de cache warming por config não muda neutral payload

[ ] transient fail-open marca checkpointable=false
[ ] revalidation failure não persiste cursor estável
[ ] budget exhaustion não persiste cursor estável
[ ] correctness-critical Redis failure não inventa coordenação local compartilhável

[ ] sourceFetchedAtMs capturado imediatamente após upstream success via storage clock
[ ] write delay não rejuvenesce factual freshness

[ ] production contract documenta Redis obrigatório
[ ] in-memory paths classificados como test seam/fallback, não deployment backend

[ ] exact dedupe possui maxIds/maxBytes/TTL
[ ] exact dedupe overflow nunca vira probabilístico silenciosamente

[ ] hide OFF/Worldwide vs hide ON/BR têm neutral search key igual
[ ] neutral provider request sequence igual
[ ] neutral cached payload semantic digest igual
[ ] final FilterContext/signature diverge quando deve

[ ] novos files da seção 310 classificados no occurrence ledger
```

---

# 316. Final pre-merge checklist V11

Executar **depois** da checklist V10:

```text
[ ] HEAD no merge ainda = audit HEAD OU Rebase/Delta/Occurrence Gate rerodados
[ ] issue #742 status revalidado

[ ] ConfigImportExport/exportConfigFile/SaveContext classificados
[ ] releaseRegion full-config round-trip passa
[ ] config cache clone/mutation safety passa

[ ] neutral payload request-local mutation safety passa
[ ] deep-freeze poison test passa

[ ] stale revalidation failure => SHOW + checkpointable=false
[ ] request seguinte pode mudar membership sem usar cursor transitório antigo
[ ] runtime Redis failure não grava cursor/raw coordenação fictícia

[ ] sourceFetchedAt acquisition-time test passa
[ ] generation continua única ordering authority

[ ] exact dedupe resource overflow test passa
[ ] nenhuma fallback probabilística escondida

[ ] search neutral equivalence OFF/ON passa
[ ] neutral cache warm order invariance passa

[ ] Occurrence Gate V11 = zero unclassified
[ ] CI unit/golden/Redis/concurrency/migration/rollback/build/lint passa
[ ] rollout Phase A observability aprovado
[ ] fleet homogênea
[ ] Phase B regional UI habilitada
```

---

# 317. Resultado final da reauditoria V11

A V10 já era um plano extremamente abrangente e tecnicamente consistente. A reauditoria V11 não
mudou a arquitetura central; ela encontrou **gaps de integração e estabilidade transitória** que
valiam fechar antes de chamar o documento de implementation-ready final.

## Novidades materiais da V11

```text
1. full-config save/export/import entrou no mapa obrigatório;
2. neutral cache ganhou contrato de imutabilidade, não apenas key neutrality;
3. fail-open transitório ganhou checkpointable=false;
4. sourceFetchedAt passou a ter ponto de captura exato no upstream observation time;
5. Redis local-only deixou de ser tratado como deployment suportado;
6. runtime Redis failure ganhou contrato de correctness;
7. exact dedupe ganhou resource budget/overflow semantics;
8. Search Cache ganhou equivalence proof OFF/ON;
9. file map/occurrence gate/test matrix/DoD foram expandidos para cobrir esses pontos.
```

## Estado final defensável

```text
V11 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
```

com a interpretação estrita:

> a cobertura é **estática e rastreável para o snapshot**; qualquer comportamento que dependa de
> runtime, upstream, concorrência, carga ou deployment só recebe status de "provado" depois do gate
> executável correspondente passar.

Se `dev` avançar antes da implementação ou do merge:

```text
Rebase Gate
+ Delta File Gate
+ Occurrence Gate V11
+ classificação de todo changed path
```

são novamente obrigatórios.

---

# 318. Reauditoria V12 — fechamento adicional sobre a V11

Esta V12 foi construída **sobre a V11 inteira**, sem remover a trilha histórica das versões anteriores.
O objetivo desta camada é fechar os gaps restantes encontrados ao cruzar novamente:

```text
plano V11 completo
+
snapshot real dev@6e83e22ab9de5093f9918a1871157f401feebb03
+
callers diretos dos chokepoints críticos
+
comportamento atual das caches/single-flight
+
fluxos reais de setup/export/import
+
documentação oficial atual do TMDB
```

> **Precedência V12:** em qualquer conflito com as seções 1–317, as seções 318+ prevalecem.
> A V11 continua sendo a base normativa imediatamente anterior; a V12 torna mais estritos somente
> os contratos explicitamente corrigidos abaixo.

## 318.1. Snapshot revalidado

No momento desta reauditoria:

```text
repo                       cedya77/aiometadata
branch                     dev
HEAD                       6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA                   00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release correspondente     v3.1.0
entradas na tree           583
blobs                      544
diretórios                 39
issue #742                 aberta / 0 comentários
```

Não houve drift de código desde a V11. Logo os novos achados desta V12 são **gaps de contrato,
caller-closure e prova**, não mudanças provocadas por commit novo.

A regra continua absoluta:

```text
qualquer HEAD posterior a 6e83e22ab9de5093f9918a1871157f401feebb03
→ rerun Rebase Gate
→ rerun Delta File Gate
→ rerun Occurrence/Caller-Closure Gate V12
→ reclassificar todo changed path
```

## 318.2. Validação externa TMDB — nuance nova material

A documentação oficial do TMDB continua confirmando o endpoint canônico de release facts:

```text
/movie/{movie_id}/release_dates
```

com os tipos:

```text
4 = Digital
5 = Physical
6 = TV
```

Referências verificadas nesta reauditoria:

```text
https://developer.themoviedb.org/reference/movie-release-dates
https://developer.themoviedb.org/reference/discover-movie
https://developer.themoviedb.org/reference/configuration-countries
https://developer.themoviedb.org/docs/region-support
https://developer.themoviedb.org/docs/rate-limiting
```

A nuance que passa a ser normativa na V12 é:

> `region` em search/discover é contexto de apresentação/source selection do TMDB; em search,
> quando a região pedida não possui release date apropriada, o TMDB pode apresentar/fazer fallback
> para a primary release date. Portanto **`search/movie.release_date` nunca é prova suficiente de
> Digital/Physical/TV na região selecionada**.

A #742 continua devendo decidir regional release exclusivamente a partir da evidence normalizada do
endpoint canônico `/movie/{id}/release_dates`.

---

# 319. Novos blockers fechados pela V12

Adicionar cumulativamente aos blockers A–BB:

```text
BC. sourceFetchedAtMs está no domínio temporal do storage (Redis TIME), mas freshness continua
    incorreta se o "now" usado para calcular age vier do relógio local de outra replica. Shared
    freshness precisa comparar dois timestamps do MESMO clock domain.

BD. TMDB search `region` pode expor fallback para primary release date. `search/movie.release_date`,
    discover card dates ou datas hidratadas por adapters não podem ser promovidas a prova regional
    de home release. Só `/movie/{id}/release_dates` é evidence canônica da #742.

BE. O single-flight atual pode entregar a mesma referência de objeto para requests concorrentes; o
    helper `cloneJsonCompatibleResult()` existe, mas o caminho genérico usa clone identity. Portanto
    request A pode mutar um payload que request B recebeu do mesmo flight mesmo sem contaminar a key
    Redis. Neutral-cache safety precisa incluir ownership/aliasing, não só deep-freeze em fixtures.

BF. `stripReleaseAvailabilityForResponse()` é destrutivo/in-place no snapshot atual. Response hygiene
    precisa ser pura ou operar somente sobre payload request-owned; caso contrário um response path
    pode remover evidence de outro consumer que compartilha a mesma referência.

BG. `randomizePerPage` ocorre depois de filtered pagination/cursor accounting. Essa posição é correta
    e precisa virar contrato: randomização é transformação response-only e não pode alterar
    membership, dedupe, source/filter signatures, served, rawOffset ou checkpoint.

BH. O full-config backup executado por `configure/src/components/setup/ApplyPreviewDialog.tsx` usa
    `exportConfigFile()` e ficou fora do mandatory map V11. releaseRegion precisa sobreviver também
    a esse caminho de backup/restore.

BI. `configure/src/components/setup/StreamingPickerDialog.tsx` possui um selector chamado Region,
    porém semanticamente ele é watch/provider region. Ele deve ser classificado explicitamente para
    impedir que uma refatoração o transforme silenciosamente em global releaseRegion.

BJ. Presets/fixtures versionados como `public/featured/callandt95.json` já carregam TMDB Discover
    `with_release_type`, `releasedOnly`, `tmdbMovieReleaseTypes` e `formState.releaseRegion`. Esses
    artefatos precisam entrar no round-trip/provenance gate; fixture estática também é config input.

BK. Occurrence grep por termos da feature não fecha o call graph de helpers centrais. Alterações em
    cacheWrapMetaSmart/loadConfigFromDatabase/etc. exigem um Caller-Closure Gate que enumere todos os
    callers diretos do snapshot e classifique cada um como changed/covered-by-helper/explicit-no-op/test.

BL. O plano cita 429, mas não define backpressure operacional exato para o fanout adicional de
    `/release_dates`. 429/timeout/retry exhaustion nunca podem virar negative evidence; retry precisa
    obedecer budget/deadline e Retry-After quando fornecido.

BM. `coverage=available` depende da definição de "release record válido". Sem contrato sintático
    exato, payload parcialmente malformado pode ser promovido a available e, por ausência regional,
    causar HIDE incorreto.

BN. Post-cache mutators além do release filter — por exemplo response stripping, image-prefix e art
    decoration — também dependem de request ownership. O contrato de imutabilidade deve proteger a
    fronteira completa cache → request projection, não uma lista fechada de funções da #742.
```

---

# 320. Shared Freshness Clock V12 — dois relógios, dois propósitos

A V11 corretamente tornou `sourceFetchedAtMs` storage-authoritative. A V12 fecha a outra metade:
**o instante usado para medir a idade dessa evidence compartilhada também precisa vir do storage**.

## 320.1. Separar policy clock de shared freshness clock

Não usar um único `Date.now()` para tudo.

Modelo conceitual:

```ts
interface RequestEvaluationClockV12 {
  /** Capturado uma vez no processo para semântica de policy/calendário. */
  policyNowMs: number;
  policyNow: Date;

  /** Capturado no domínio temporal do shared storage quando necessário. */
  sharedFreshnessNowMs: number | null;

  sharedFreshnessClockAvailable: boolean;
}
```

Responsabilidades:

```text
policyNow/policyNowMs
→ Worldwide legacy instant semantics
→ Series instant semantics
→ CalendarDate/timezone
→ 365-day transition

sharedFreshnessNowMs
→ idade de raw/evidence compartilhada
→ decisão fresh/stale
→ freshness boundary de cursor
```

## 320.2. Regra de clock domain

Para evidence persistida:

```text
ageMs = sharedFreshnessNowMs - sourceFetchedAtMs
```

onde **ambos** são derivados do mesmo clock autoritativo do Redis.

Nunca:

```text
Date.now() numa replica A
-
sourceFetchedAtMs obtido por Redis TIME numa replica B
```

como autoridade para freshness correctness-critical.

## 320.3. Captura

Quando uma request realmente precisar validar freshness compartilhada:

```text
1. capturar Redis TIME uma única vez;
2. armazenar em RequestEvaluationClockV12.sharedFreshnessNowMs;
3. reutilizar o mesmo valor em todos os itens daquela request;
4. não chamar Redis TIME item a item;
5. não rejuvenescê-lo no meio da paginação.
```

Isso preserva consistência intra-request e evita fanout desnecessário.

## 320.4. Redis TIME indisponível

Se o storage clock falhar em runtime:

```text
shared cached evidence
→ freshness = indeterminada

shared cached evidence que produziria HIDE
→ não autoriza HIDE
→ UNKNOWN/SHOW ou revalidation live

live upstream fetch concluído na própria request
→ pode decidir a resposta request-local
→ não vira shared checkpoint/cursor estável enquanto coordination/storage estiver indisponível
```

Não fabricar:

```text
sharedFreshnessNowMs = Date.now()
```

como fallback silencioso.

## 320.5. Timestamp no futuro/corrompido

Mesmo no domínio Redis, proteger contra envelope corrompido:

```text
envelope lido do shared storage, já existente no instante da amostra,
sourceFetchedAtMs > sharedFreshnessNowMs + tolerance mínima documentada
→ evidence inválida para HIDE
→ metric + warning deduplicado
→ revalidation ou UNKNOWN/SHOW
```

Não usar `Math.max(age, 0)` para esconder corrupção temporal. Evidence obtida por live revalidation
na própria request é `fresh-by-observation` para aquela request e não passa por esse check contra uma
amostra anterior do storage clock; enquanto não houver coordination/storage confiável, permanece
request-local e `checkpointable=false`.

## 320.6. Cursor boundary

Se membership depende de release evidence:

```text
validUntil/stableUntil
→ calculado com a freshness deadline factual do envelope
→ comparado contra sharedFreshnessNowMs no mesmo clock domain
```

Calendar/day transitions continuam no policy clock/timezone.

O cursor precisa carregar boundaries semanticamente distintas se isso simplificar a implementação:

```ts
interface TemporalValidityV12 {
  policyValidUntilMs?: number;
  sharedFreshnessValidUntilMs?: number;
}
```

A validação final é a interseção das duas.

---

# 321. TMDB regional evidence V12 — source-of-truth estrito

## 321.1. Endpoint canônico

Para movie regional home release:

```text
TMDB /movie/{id}/release_dates
```

é a única source factual normativa desta feature.

Podem ajudar a formar source membership, cards ou hints, mas **não** são authority de regional release:

```text
/search/movie release_date
/discover/movie release_date
primary_release_date
meta.released sozinho
watch_region
provider availability
TMDB Discover params.region sozinho
```

## 321.2. Search region fallback regression

Fixture obrigatória:

```text
TMDB search(movie, region=BR)
→ card possui release_date=2026-09-01 por fallback/primary

/movie/{id}/release_dates
→ US Digital 2026-09-01
→ nenhuma BR 4/5/6

releaseRegion=BR
→ NÃO marcar RELEASED pela search release_date
→ usar evidence canônica
→ regional-home-release-not-confirmed quando evidence fresh/available
```

Outra fixture:

```text
/search/movie region=BR
→ release_date BR presente

/movie/{id}/release_dates
→ BR Digital 2026-09-20

hoje BR >= 2026-09-20
→ RELEASED
```

A segunda passa **porque `/release_dates` confirma**, não porque o search card carregou a data.

## 321.3. Discover prefilter não é evidence layer

Um catálogo TMDB Discover com:

```text
region=BR
with_release_type=4|5|6
```

pode naturalmente reduzir sua source membership pelo próprio TMDB.

Isso não autoriza:

```text
meta veio do Discover
→ portanto releaseEvidence.BR = released
```

O filtro central continua provider-independent.

## 321.4. Provenance continua relevante

`discover.params.region` pode participar de:

```text
EffectiveReleaseRegion
sourceMembershipSignature
Discover source identity
```

quando sua provenance autorizar o override, mas a **evidence factual** continua sendo construída do
raw `/release_dates`.

---

# 322. Request-owned cache values V12 — fechar aliasing de single-flight

A V11 exige neutral payload imutável. A V12 define a fronteira concreta de ownership necessária no
snapshot atual.

## 322.1. Problema real localizado

O helper genérico possui conceitualmente:

```text
singleFlight(key, factory, cloneResult = identity)
```

Logo dois callers concorrentes que entram no mesmo flight podem receber a mesma referência de objeto.

No mesmo snapshot existem transforms posteriores que mutam objetos:

```text
applyCatalogFilters/evidence completion legado
poster/background/logo decoration
applyImageCachePrefix
stripReleaseAvailabilityForResponse
outros projections request-local
```

Portanto:

> "não mutar a entrada no filter" é necessário, mas não suficiente; a cache/request boundary precisa
> definir quem possui cada objeto retornado.

## 322.2. Contrato de ownership

Adotar dois estados explícitos:

```text
SharedReadonly<T>
RequestOwned<T>
```

Sem necessariamente criar branded TypeScript types, a semântica deve ser documentada e testável.

### SharedReadonly

```text
- valor mantido em cache/shared flight;
- nenhum consumer pode alterá-lo;
- pode ser compartilhado entre callers;
- mutations são bug.
```

### RequestOwned

```text
- cópia exclusiva daquela request/consumer;
- transforms de resposta podem mutar se necessário;
- nunca é reinserida silenciosamente em neutral cache.
```

## 322.3. Fronteira recomendada

Para wrappers request-facing JSON-compatible:

```text
cacheWrapCatalog
cacheWrapSearch
cacheWrapMetaSmart
```

retornar payload **RequestOwned** antes de qualquer policy/projection request-local.

Opções aceitáveis:

```text
A. singleFlight(..., cloneJsonCompatibleResult)
B. clone explícito imediatamente no wrapper request-facing
C. tornar todo downstream puro/immutable e provar isso
```

Para o snapshot atual, A/B são retrofit menos arriscado porque já existem mutators legados.

Não clonar indiscriminadamente todo cache interno de baixo nível se ele for read-only e isso causar
custo desnecessário; a fronteira deve ser deliberada.

## 322.4. Leader e waiters

O teste não pode cobrir apenas waiters.

Garantir:

```text
flight leader recebe RequestOwned
flight waiter 1 recebe outro RequestOwned
flight waiter 2 recebe outro RequestOwned
shared/cache candidate permanece intacto
```

Se o leader recebe o mesmo objeto que será posteriormente usado como shared candidate, ainda existe
aliasing.

## 322.5. Redis hit vs local-flight hit

Os dois caminhos devem ter contrato equivalente:

```text
Redis decode
→ request-owned semantic value

same-process single-flight
→ request-owned semantic value
```

Não permitir que o bug apareça apenas sob concorrência local.

## 322.6. Config cache é exceção deliberada

`addon/lib/configCache.ts` pode continuar retornando shared-readonly porque o contrato já possui:

```text
loadSharedConfig()
→ shared/read-only

loadConfigFromDatabase()
→ deep clone mutável
```

A V12 não manda clonar toda leitura de config; manda preservar essa distinção e testar callers.

---

# 323. Response hygiene V12 — sanitizer não destrutivo

## 323.1. `stripReleaseAvailabilityForResponse`

O snapshot atual remove `_releaseAvailability`/equivalentes in-place.

Novo contrato preferencial:

```ts
projectPublicResponse(payload): PublicPayload
```

ou helper equivalente que:

```text
- não modifica o input;
- remove evidence interna;
- preserva estrutura pública;
- não compartilha nested refs mutáveis que serão alteradas depois;
- funciona para meta único, metas[], app_extras e estruturas aninhadas suportadas.
```

Se a implementação mantiver um sanitizer mutável por performance, ele só pode receber `RequestOwned`.
A prova de ownership então passa a ser blocker de merge.

## 323.2. Hygiene nunca altera cache factual

Teste obrigatório:

```text
neutral cached payload contém releaseEvidence interna
→ request projeta resposta pública
→ resposta não contém evidence
→ releitura da neutral cache ainda contém evidence intacta
```

## 323.3. Concurrent response poison test

```text
request A e B entram no mesmo single-flight
A chama response sanitizer primeiro
B ainda precisa enxergar evidence interna para seu filtro
→ B continua correto
```

Esse teste captura exatamente a classe de aliasing que deep-freeze isolado pode não reproduzir.

## 323.4. Todos os post-cache mutators

Classificar também:

```text
applyImageCachePrefix
custom poster/background/logo projection
rating poster projection
request debug fields
filter/evidence completion
response stripping
qualquer future post-cache map que escreva no meta
```

Regra universal:

```text
post-cache mutation
→ somente RequestOwned
```

---

# 324. `randomizePerPage` V12 — response-only, nunca pagination identity

O snapshot atual randomiza a página **depois** do fill/filter/dedupe/cursor accounting. Preservar essa
ordem.

## 324.1. Invariante

```text
source page(s)
→ neutral page
→ evidence/filter
→ dedupe
→ cursor accounting/checkpoint
→ response page membership fechado
→ randomizePerPage
→ response decoration
```

Nunca mover randomização antes de:

```text
served accounting
skip walking
dedupe membership
nextPage/nextOffset
source/filter signature
checkpoint write
```

## 324.2. Identidade

`randomizePerPage`:

```text
NÃO entra em sourceMembershipSignature
NÃO entra em filterSignature
NÃO altera set membership da página
NÃO altera cursor coordinate
```

Se futuramente o produto desejar randomização que altere **quais itens** pertencem a cada página,
essa seria outra pagination contract/version e exigiria seed estável.

## 324.3. Testes

```text
randomize OFF
→ ordem final determinística legado

randomize ON, mesma source/filter state
→ set(ids) da página igual ao pre-randomized set
→ next cursor semantic digest igual
→ served/raw coordinates iguais
→ somente a ordem de apresentação pode variar

request seguinte
→ usa cursor baseado na sequência pré-randomização
```

## 324.4. Dedupe

A dedupe normativa ocorre antes da randomização.

Randomização nunca pode reintroduzir:

```text
duplicata
item previamente visto
mudança de cardinalidade
```

---

# 325. Config/setup/presets V12 — round-trip completo

## 325.1. `ApplyPreviewDialog` entra no mandatory map

Adicionar:

```text
configure/src/components/setup/ApplyPreviewDialog.tsx
```

Motivo:

```text
setup replace flow
→ "Download backup"
→ exportConfigFile(config, ...)
```

Fixture:

```text
config.releaseRegion=BR
→ setup preview
→ download backup
→ import backup
→ releaseRegion=BR
```

## 325.2. `StreamingPickerDialog` é watch/provider region

Adicionar:

```text
configure/src/components/setup/StreamingPickerDialog.tsx
```

O selector `region` desse fluxo significa:

```text
região usada para listar/selecionar providers de streaming
```

Não significa automaticamente:

```text
global config.releaseRegion
```

Contrato:

```text
StreamingPicker region=BR
releasedOnly=false
→ NÃO altera releaseRegion global

StreamingPicker region=BR
releasedOnly=true
→ se o setup gerar TMDB Discover release-aware com params.region=BR,
   provenance = watch-region-derived
→ ainda NÃO sobrescreve silenciosamente config.releaseRegion global
```

Isso preserva a distinção Watch Region × Release Region da arquitetura.

## 325.3. Featured/static config inputs

Adicionar ao ledger:

```text
public/featured/callandt95.json
public/featured/*.json   # se occurrence gate encontrar semântica equivalente
```

Fixture mínima para preset com:

```text
with_release_type
releasedOnly
tmdbMovieReleaseTypes
formState.releaseRegion
metadata.discover.params.region
```

Round-trip:

```text
featured preset
→ import/apply
→ edit Discover
→ save
→ export
→ import
```

não pode:

```text
- perder releaseRegion do formState;
- fabricar global releaseRegion;
- confundir watch_region com region;
- remover release type semantics;
- perder provenance.
```

## 325.4. `ConfigContext` default/hydration

Adicionar explicitamente aos tipos/defaults:

```ts
releaseRegion?: string;
```

com default funcional:

```text
'' = Worldwide
```

Hydration de config antiga:

```text
campo ausente
→ Worldwide runtime
→ sem write lateral
```

Dirty fingerprint:

```text
releaseRegion é config real
→ deve participar de fingerprint de save
```

Manifest fingerprint:

```text
releaseRegion NÃO precisa obrigatoriamente participar
```

se a mudança é exclusivamente server-side e não altera o manifest Stremio. Não forçar reinstall por
uma configuração que o server lê em runtime.

---

# 326. Caller-Closure Gate V12 — além de occurrence grep

A V11 usa Occurrence Gate por termos, necessário mas insuficiente. A V12 adiciona uma prova de fechamento
do call graph dos helpers que a feature modifica ou dos quais ela depende.

## 326.1. Chokepoints obrigatórios

Enumerar callers diretos no audit HEAD para:

```text
applyCatalogFilters
catalogFiltersActive
cacheWrapCatalog
cacheWrapSearch
cacheWrapMetaSmart
loadSharedConfig
loadConfigFromDatabase
normalizeReleaseAvailabilityInPayload
stripReleaseAvailabilityForResponse
raw release_dates owner/writer
resolveCanonicalFilterContext       # após ser criado
ensureReleaseEvidenceForFilter      # após ser criado
```

## 326.2. Ledger de occurrences/caller-candidates de `cacheWrapMetaSmart` no snapshot auditado

A busca estática do HEAD localizou a definição/export e as superfícies de import/call em/através de:

```text
addon/lib/getCache.ts
addon/lib/getTrending.ts
addon/lib/tvmazeScheduleCatalog.ts
addon/utils/stremthru.js
addon/lib/getPersonalLists.ts
addon/lib/cacheWarmer.js
addon/utils/flixpatrolUtils.ts
addon/index.ts
addon/utils/letterboxdUtils.ts
addon/utils/publicmetadbUtils.ts
addon/utils/mdbList.ts
addon/lib/getCatalog.ts
addon/lib/getSearch.ts
addon/utils/simklUtils.ts
addon/utils/traktUtils.ts
addon/utils/parseProps.js
addon/lib/comprehensiveCatalogWarmer.js
```

`addon/lib/getCache.ts` contém a definição/export; os demais paths são caller/use candidates do snapshot.
Nem todo path precisa mudar. Todos precisam de classificação:

```text
changed
covered-by-helper
explicit-no-op
regression-test
```

## 326.3. Callers de config clone/shared semantics

`loadConfigFromDatabase` aparece em caminhos além da UI/route principal, incluindo:

```text
addon/utils/anilistUtils.ts
addon/utils/discoverParams.ts
addon/lib/malCatalogWarmer.js
addon/index.ts
addon/lib/cacheWarmer.js
addon/lib/getCache.ts
addon/utils/ai-catalog-entity-resolver.ts
addon/lib/comprehensiveCatalogWarmer.js
```

Além de `addon/lib/configApi.js`.

Cada caller deve provar uma das duas coisas:

```text
precisa mutar config
→ usa clone/request-owned

somente lê config
→ shared-readonly permitido
```

`addon/lib/jellyfin/context.ts`, caller de `loadSharedConfig`, também precisa permanecer classificado.

## 326.4. Gate automático

Criar script CI, por exemplo:

```text
scripts/check-release-visibility-callers.mjs
```

que:

```text
1. busca import/require/call dos chokepoints;
2. compara paths com allowlist versionada do ledger;
3. falha se surgir caller novo não classificado;
4. falha se helper for renomeado/removido sem atualização deliberada do ledger;
5. imprime diff de callers para review.
```

Para require dinâmico ou alias que o parser não reconhecer:

```text
grep/rg complementar
+
review manual classificado
```

O objetivo não é construir um analisador TypeScript perfeito; é impedir novo caminho silencioso.

---

# 327. TMDB 429/backpressure V12 — evidence fanout sob controle

Regional release pode provocar chamadas extras para `/movie/{id}/release_dates`. O plano já define
request budget, mas a reauditoria V14 confirmou que o snapshot **não possui provider-level TMDB
concurrency limiter**; por isso o throttling final exige também o admission controller da seção 358.

## 327.1. 429 nunca vira evidence

```text
HTTP 429
→ transient upstream failure
→ coverage NÃO vira empty
→ coverage NÃO vira available
→ não escrever negative evidence
→ não autorizar HIDE
```

Se existir LKG:

```text
LKG fresh segundo shared clock
→ usar normalmente

LKG stale e decisão seria HIDE
→ revalidation falhou
→ UNKNOWN/SHOW
→ checkpointable=false
```

## 327.2. Retry

Reutilizar o cliente TMDB central, mas não presumir concurrency limiter inexistente. Retry classifier,
admission control e WorkBudget devem formar **uma única stack central**, não uma stack paralela por feature.

Contrato:

```text
Retry-After presente e válido
→ respeitar dentro do request/deadline budget

Retry-After ausente
→ bounded exponential backoff + jitter

client abort/deadline excedido
→ parar imediatamente

request evidence budget esgotado
→ não iniciar retry adicional
```

Não prometer um número fixo de retries sem medir o sistema atual. O valor operacional deve ser
configurável/central e coberto por teste.

## 327.3. Stampede

Para mesmo movie id:

```text
cache miss/stale burst
→ local single-flight obrigatório
→ distributed refresh lease recomendado/obrigatório quando múltiplas replicas puderem revalidar
   o mesmo raw key simultaneamente
```

O loser da lease pode:

```text
aguardar bounded
→ reread raw
→ ou fail-open request-local
```

Nunca disparar N revalidations idênticas sem limite.

## 327.4. Métricas

Baixa cardinalidade:

```text
release_evidence_upstream_total{result=ok|429|timeout|5xx|invalid}
release_evidence_retry_total{cause=429|timeout|5xx}
release_evidence_backoff_seconds
release_evidence_budget_exhausted_total
release_evidence_revalidation_total{result=success|fail_open|lease_wait}
```

Sem movie id/user/query como label.

---

# 328. Release record validity V12 — impedir false HIDE por payload malformado

## 328.1. Três conceitos distintos

Não misturar:

```text
hasReleaseDateData
coverage
regional home fact
```

### `hasReleaseDateData`

Preserva exclusivamente compatibilidade Worldwide legado:

```text
results é array
→ true

results ausente/não-array
→ false
```

mesmo quando `results=[]`, conforme golden master já definido.

### `coverage`

Definição normativa V12:

```text
unavailable
→ request falhou, payload ausente ou results não-array

empty
→ results é array, mas nenhum release entry contém release_date sintaticamente utilizável

available
→ existe ao menos um release entry com release_date sintaticamente utilizável
```

`available` NÃO significa que a região selecionada teve home release.

### `regional home fact`

Adicionar ao mapa apenas quando todos forem válidos:

```text
country.iso_3166_1 normalizável
+
type ∈ {4,5,6}
+
parseCalendarDate(release_date) != null
```

## 328.2. `regionsWithReleaseRecords`

Incluir região apenas se:

```text
country code válido
+
existe ao menos um release entry com release_date utilizável
```

Não incluir país baseado apenas em container vazio/malformado.

## 328.3. Worldwide compatibility

A classificação `coverage` nova não pode alterar o golden-master Worldwide.

Worldwide continua usando:

```text
hasReleaseDateData
earliestAnyReleaseAt
earliestHomeReleaseAt
```

com regras temporais compatíveis com `isReleasedDigitally()` legado.

Se o algoritmo legado aceitava um timestamp que o parser regional rejeita como `CalendarDate`, o
fixture precisa provar que:

```text
Worldwide permanece legado
Regional trata o fact regional como inválido/ausente
```

sem forçar um parser único para semânticas diferentes.

## 328.4. Matriz malformed

Adicionar:

```text
results=null                            → unavailable
results={}                              → unavailable
results=[]                              → empty / hasReleaseDateData=true
country sem iso_3166_1 + data válida    → coverage available, sem regional map
country BR + release_dates=[]           → sem regional map
BR type=4 sem release_date              → não cria home fact
BR type=4 release_date=garbage           → não cria home fact
BR type=999 com data válida             → pode contribuir a generic dated coverage,
                                         não cria home fact
BR type=4 data impossível               → não cria home fact
US type=4 data válida; BR ausente        → available; BR not-confirmed policy somente se fresh
```

A última linha continua coerente com a semântica regional escolhida na V5/V10.

---

# 329. Mandatory file/occurrence map V12

Somar à seção 310:

```text
configure/src/components/setup/ApplyPreviewDialog.tsx
configure/src/components/setup/StreamingPickerDialog.tsx
public/featured/callandt95.json
public/featured/*.json                           # quando houver release/discover semantics

addon/lib/jellyfin/context.ts
addon/lib/jellyfin/profiles.ts

addon/lib/tvmazeScheduleCatalog.ts
addon/utils/stremthru.js
addon/utils/flixpatrolUtils.ts
addon/utils/letterboxdUtils.ts
addon/utils/publicmetadbUtils.ts
addon/utils/traktUtils.ts
addon/utils/anilistUtils.ts
addon/lib/malCatalogWarmer.js
```

Esses paths entram porque foram alcançados por caller/semantic closure; não significa que todos devam
receber diff de código.

## 329.1. Occurrence terms adicionais

```text
stripReleaseAvailabilityForResponse
cloneJsonCompatibleResult
singleFlight
inFlightRequests
applyImageCachePrefix
randomizePerPage
shuffleMetas

sharedFreshnessNowMs
sourceFetchedAtMs
Redis TIME
Date.now
freshness

movieReleaseDates
release_date
primary_release_date
region
watch_region
with_release_type
releasedOnly
tmdbMovieReleaseTypes

ApplyPreviewDialog
StreamingPickerDialog
public/featured

cacheWrapMetaSmart
loadConfigFromDatabase
loadSharedConfig
```

## 329.2. Gate final V12

```text
zero ocorrência relevante sem classificação
+
zero caller direto novo dos chokepoints sem classificação
+
zero config/setup/static fixture path com semantics region/release fora do ledger
+
zero changed path do merge HEAD sem classificação
```

---

# 330. Test Matrix V12 — casos novos obrigatórios

A matriz V11 continua cumulativa e ganha os seguintes casos.

## Shared freshness clock

```text
68. replica A host clock +5min, replica B -5min, mesmo Redis TIME → mesma freshness decision;
69. sourceFetchedAtMs/storageNow no mesmo domínio → boundary exata;
70. Redis TIME read failure + stale would-HIDE → UNKNOWN/SHOW + checkpointable=false;
71. sourceFetchedAtMs no futuro além da tolerance → evidence não autoriza HIDE;
72. uma request avalia N metas → um shared freshness clock sample, não N samples.
```

## TMDB canonical evidence

```text
73. search region fallback data sem BR 4/5/6 → não marca RELEASED;
74. Discover regional prefilter não sintetiza releaseEvidence;
75. `/release_dates` BR Digital passada → RELEASED;
76. `/release_dates` BR Digital futura → UNRELEASED;
77. search/discover date e canonical release_dates discordam → canonical vence para #742.
```

## Cache ownership / response hygiene

```text
78. dois callers no mesmo single-flight recebem objetos independentes no boundary request-facing;
79. request A strip evidence não altera request B;
80. request A art/poster mutation não altera request B;
81. neutral cached object semantic digest igual antes/depois de public response projection;
82. flight leader e waiter possuem ownership equivalente;
83. Redis hit e local-flight hit possuem ownership equivalente;
84. public response não vaza releaseEvidence interna.
```

## randomizePerPage

```text
85. randomize ON mantém set(ids) e cursor semantic digest;
86. randomize ON não muda served/raw coordinate;
87. randomize OFF preserva ordem legado;
88. dedupe acontece antes da randomização;
89. randomização não participa de source/filter signatures.
```

## Setup/config/presets

```text
90. ApplyPreview backup/restore preserva releaseRegion=BR;
91. StreamingPicker region=BR + releasedOnly=false não altera global releaseRegion;
92. StreamingPicker release-aware gera provenance watch-region-derived quando aplicável;
93. featured preset com formState.releaseRegion round-trip preserva campo;
94. featured preset não fabrica global releaseRegion;
95. config antiga sem releaseRegion hidrata Worldwide sem write lateral.
```

## Caller closure

```text
96. caller-closure script no audit HEAD produz ledger esperado;
97. fixture injeta caller novo não classificado → CI falha;
98. rename/remove de chokepoint sem atualização do ledger → CI falha de forma legível.
```

## 429/backpressure

```text
99. 429 nunca vira coverage=empty;
100. 429 nunca grava negative evidence;
101. Retry-After válido é respeitado dentro do budget;
102. Retry-After ausente usa backoff bounded+jitter;
103. client abort interrompe retry;
104. budget exhausted impede novo retry;
105. burst mesmo movie id colapsa via single-flight/lease;
106. stale would-HIDE + 429 → SHOW + checkpointable=false.
```

## Malformed release records

```text
107. results=[] → empty + hasReleaseDateData=true;
108. results não-array → unavailable;
109. BR type=4 sem data → sem home fact;
110. BR type=4 data impossível → sem home fact;
111. BR type desconhecido com data válida → não cria home fact;
112. country code inválido + data válida → não entra em regional map;
113. malformed regional facts não quebram Worldwide golden master.
```

---

# 331. Observabilidade V12 — complementos

Adicionar baixa cardinalidade:

```text
release_shared_clock_total{result=ok|unavailable|invalid_future_timestamp}
release_freshness_decision_total{state=fresh|stale|clock_unavailable|corrupt}

cache_request_ownership_total{surface=catalog|search|meta,result=cloned|readonly}
cache_alias_guard_failure_total
response_release_evidence_leak_total

release_evidence_source_total{source=canonical_release_dates|search_hint_ignored|discover_hint_ignored}
release_evidence_upstream_total{result=ok|429|timeout|5xx|invalid}
release_evidence_retry_total{cause=429|timeout|5xx}

release_record_normalization_total{result=valid_home|valid_nonhome|invalid_date|invalid_country|invalid_shape}

release_caller_closure_unclassified_total     # CI/staging preferred
release_config_static_fixture_failure_total    # CI/staging preferred
```

Não usar IDs de filme, query, usuário, token ou região arbitrária como label de alta cardinalidade.
`region` em métricas, se realmente necessário, deve seguir uma allowlist/aggregation deliberate; default é não usar.

---

# 332. Implementation Order V12 — ordem final recomendada

A ordem V11 permanece, com os seguintes ajustes antes da UI:

```text
Phase A0 — prova estática
1. congelar audit HEAD/tree;
2. rodar Occurrence Gate V12;
3. gerar Caller-Closure ledger;
4. classificar setup/static fixtures novas;

Phase A1 — facts e tempo
5. consolidar raw `/release_dates` owner;
6. fechar ReleaseAvailability schema/record validity;
7. implementar sourceFetchedAt acquisition-time;
8. implementar sharedFreshnessNowMs no mesmo Redis clock domain;
9. fechar 429/backpressure/revalidation semantics;

Phase A2 — cache ownership
10. definir SharedReadonly vs RequestOwned;
11. corrigir request-facing single-flight ownership;
12. tornar response sanitizer puro ou provar request ownership;
13. executar concurrent alias poison tests;

Phase A3 — policy/paging
14. CanonicalFilterContext + evaluators;
15. canonical TMDB evidence only;
16. filtered pagination/cursor/dedupe contracts V11;
17. preservar randomizePerPage como response-only;

Phase A4 — config/provenance
18. global releaseRegion types/default/load/save;
19. Discover provenance/round-trip;
20. ApplyPreview backup fixture;
21. StreamingPicker semantic isolation;
22. featured presets/static config fixtures;

Phase A5 — search
23. EffectiveSearchSourceContext;
24. neutral Search Cache migration;
25. search canonical-evidence rule;
26. neutral equivalence OFF/ON;

Phase A6 — deploy
27. full unit/golden/integration/concurrency/Redis/migration/rollback suite;
28. Phase A backend dark deploy + observability;
29. homogeneous fleet gate;
30. Phase B UI regional;
31. kill-switch drill;
32. post-enable metrics validation.
```

Essa ordem reduz o risco de expor a UI antes de clock/cache/evidence estarem corretos.

---

# 333. Definition of Done V12 — gates adicionais

Somar cumulativamente às seções 297 e 315:

```text
[ ] shared freshness usa storage-now e sourceFetchedAt no mesmo clock domain
[ ] host clock skew entre replicas não muda shared freshness decision
[ ] storage clock unavailable nunca autoriza stale HIDE

[ ] search/discover release_date não é usado como regional home-release evidence
[ ] canonical `/movie/{id}/release_dates` é a única authority da #742
[ ] search region fallback fixture passa

[ ] request-facing cache/single-flight possui ownership explícito
[ ] leader e waiters não compartilham referência mutável pós-cache
[ ] stripReleaseAvailabilityForResponse é puro OU recebe RequestOwned provado
[ ] art/image/response mutators só operam em RequestOwned
[ ] concurrent alias poison test passa

[ ] randomizePerPage permanece depois de filter/dedupe/cursor accounting
[ ] randomizePerPage não muda membership/signatures/cursor coordinates

[ ] ApplyPreview backup/restore preserva releaseRegion
[ ] StreamingPicker Region continua watch/provider region
[ ] release-aware setup usa provenance explícita sem sobrescrever global releaseRegion
[ ] featured/static configs com release semantics entram no round-trip gate

[ ] Caller-Closure Gate cobre todos os callers diretos dos chokepoints
[ ] novo caller não classificado quebra CI

[ ] 429 nunca vira negative evidence
[ ] Retry-After, quando presente, respeitado dentro do budget
[ ] backoff sem Retry-After é bounded e cancelável
[ ] stampede de revalidation é colapsado

[ ] coverage available/empty/unavailable possui record-validity contract executável
[ ] malformed records não causam false HIDE
[ ] Worldwide golden-master continua bit/decision-equivalent onde exigido

[ ] Occurrence Gate V12 = zero unclassified
[ ] Caller-Closure Gate V12 = zero unclassified
```

---

# 334. Final pre-merge checklist V12

Executar **depois** das checklists V10/V11:

```text
[ ] merge HEAD = audit HEAD OU Rebase/Delta/Occurrence/Caller-Closure Gates rerodados
[ ] issue #742 status revalidado
[ ] TMDB docs assumptions revalidadas se API/docs mudaram

[ ] sourceFetchedAt + sharedFreshnessNow usam mesmo storage clock domain
[ ] clock-skew integration fixture passa em duas replicas/processes simulados

[ ] search region fallback nunca é consumido como canonical release evidence
[ ] canonical release_dates fixture passa para BR/US/Worldwide

[ ] local single-flight aliasing test passa
[ ] response sanitizer concurrency test passa
[ ] neutral cache semantic digest não muda após request projections

[ ] randomizePerPage cursor invariance test passa

[ ] ApplyPreviewDialog classificado
[ ] StreamingPickerDialog classificado
[ ] public/featured release/discover fixtures classificadas
[ ] cacheWrapMetaSmart caller ledger fechado
[ ] loadConfigFromDatabase/loadSharedConfig caller ledger fechado

[ ] 429/retry/backoff/budget/cancel tests passam
[ ] malformed release payload matrix passa

[ ] Occurrence Gate V12 = zero unclassified
[ ] Caller-Closure Gate V12 = zero unclassified
[ ] build/backend build/lint passam
[ ] novo test harness/CI da feature passa
[ ] Redis/concurrency/migration/rollback suites passam
[ ] Phase A observability aprovado
[ ] fleet homogênea
[ ] Phase B UI habilitada
[ ] kill switch testado
```

---

# 335. Resultado final da reauditoria V12

A V11 já estava em nível muito alto e fechava a maior parte dos riscos de arquitetura. A V12 encontrou
**sete classes materiais adicionais** que impediam chamar a prova de cobertura de totalmente fechada:

```text
1. clock domain incompleto na leitura de shared freshness;
2. TMDB search-region fallback ainda não explicitamente proibido como evidence regional;
3. aliasing real de objeto em same-process single-flight;
4. response sanitizer destrutivo e outros post-cache mutators;
5. randomizePerPage fora do contrato formal de paginação;
6. setup/backups/presets/callers diretos ainda fora do closure ledger;
7. 429 + malformed-record semantics ainda insuficientemente executáveis.
```

Com as seções 318–334 incorporadas, o estado defensável passa a ser:

```text
V12 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
      com static occurrence + caller-closure coverage
      e runtime/upstream/concurrency/deployment transformados em gates executáveis
```

## 335.1. O que significa "100%" neste documento

A formulação tecnicamente defensável continua sendo:

> **100% da superfície estática localizada e classificada no snapshot auditado, com contratos
> explícitos para os caminhos correctness-critical e gates executáveis para aquilo que só pode ser
> provado em runtime.**

Não significa:

```text
- infalibilidade futura do TMDB;
- garantia sobre commits posteriores;
- prova de concorrência sem executar os testes Redis/multi-replica;
- prova de performance sem benchmark/carga;
- prova de rollback sem executar o drill correspondente.
```

## 335.2. Regra final de mudança

Qualquer uma destas mudanças invalida automaticamente a alegação de cobertura atual até rerun:

```text
- dev HEAD/tree mudou;
- TMDB mudou semântica documentada de release_dates/region;
- surgiu novo caller de chokepoint crítico;
- surgiu novo config/setup/preset path com region/release semantics;
- mudou cache/pagination/cursor schema;
- mudou Redis coordination/freshness contract;
- mudou definition de Hide Unreleased.
```

Gate obrigatório:

```text
Rebase Gate
+ Delta File Gate
+ Occurrence Gate V12
+ Caller-Closure Gate V12
+ golden/master + integration + concurrency + migration + rollback suites
```

Somente depois disso a alegação V12 pode ser mantida para o novo snapshot.
---

# 336. Reauditoria V13 — fechamento de geração, ingress, exhaustion e contratos ambíguos

A V12 fechou clock domain, source-of-truth TMDB, aliasing de single-flight, response hygiene,
`randomizePerPage`, caller closure, backpressure e malformed records. A reauditoria V13 cruza esses
contratos com os **pontos exatos de ingresso e concorrência** do snapshot e encontra uma camada ainda
mais estreita de problemas: freshness sem generation-coherence, raw CAS loser sem semântica de
consumo, ingress alternativo por `append_to_response`, lifecycle do allocator de geração, clock sample
anterior a um commit concorrente, ambiguity de provenance, exhaustion inferida por tamanho de página e
retry budget duplicável.

Snapshot revalidado nesta V13:

```text
repository: cedya77/aiometadata
branch: dev
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
tree: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue #742: aberta, sem comentários no snapshot revalidado
HEAD auditada → dev: 0 commits de drift
```

A documentação TMDB também foi revalidada em 2026-09-24:

```text
/movie/{movie_id}/release_dates
→ tipos 4 Digital, 5 Physical, 6 TV

/configuration/countries
→ lista de países ISO 3166-1 usada pelo TMDB

region support
→ search region pode cair para primary release date quando não existe data regional
→ Discover region + with_release_type afeta a data/source retornada

rate limiting
→ 429 deve ser respeitado; o limite operacional pode mudar
```

Referências:

```text
https://developer.themoviedb.org/reference/movie-release-dates
https://developer.themoviedb.org/reference/configuration-countries
https://developer.themoviedb.org/docs/region-support
https://developer.themoviedb.org/reference/discover-movie
https://developer.themoviedb.org/docs/rate-limiting
```

> **Precedência V13:** em qualquer conflito com as seções 1–335, as seções 336+ prevalecem.
> A V13 não muda o objetivo funcional da #742; ela torna executáveis contratos que ainda permitiam
> duas implementações aparentemente válidas, porém semanticamente diferentes.

---

# 337. Novos blockers encontrados na V13

Adicionar cumulativamente aos blockers A–BN:

```text
BO. Freshness não prova generation-coherence. Uma releaseEvidence derivada da geração raw G1 pode
    continuar dentro do SLA de 6h depois que o raw owner já avançou para G2. Sem vincular evidence à
    fetchGeneration, uma ausência regional antiga ainda poderia autorizar HIDE mesmo existindo um raw
    mais novo que confirma lançamento.

BP. O snapshot possui ingress alternativo real de release_dates: getMeta.js e getSearch.ts materializam
    app_extras.releaseDates a partir de movie detail/append_to_response, e releaseAvailability.ts hoje
    converte automaticamente esse campo em _releaseAvailability. Esses payloads não carregam o envelope
    canônico v2/sourceFetchedAt/fetchGeneration e não podem virar authority regional por acidente.

BQ. CAS write rejeitado não define qual fato o request usa. Se fetch G1 perde para G2 já committed, o
    candidate G1 deve ser descartado para decisão compartilhável; usar o candidate perdedor request-local
    ainda pode produzir HIDE contrário ao raw winner.

BR. O allocator V10 exemplificado como INCR por movie-id não possui lifecycle. Se nunca expira, cria uma
    key permanente por título; se expira antes do raw envelope, pode reiniciar em 1 enquanto o envelope
    guarda generation alta e bloquear writes corretos. O allocator precisa de lifecycle matematicamente
    seguro.

BS. Um único Redis TIME capturado cedo pode anteceder um commit concorrente legítimo. Depois de lease wait,
    CAS-loss reread ou refresh por outra replica, sourceFetchedAtMs pode ser maior que o sample do request
    sem corrupção. A V12 proíbe clamp silencioso, mas ainda precisa de regra de resample/clock advancement.

BT. A provenance está inconsistente no texto histórico: há `explicit`, `discover-explicit` e `global`
    como nomes parcialmente sobrepostos. Persisted Discover provenance e EffectiveReleaseRegion precisam
    de enums distintos e canônicos para não gerar signatures/round-trips diferentes.

BU. A seção histórica de merged catalogs fala em "merged catalog explicit region", enquanto o contrato
    global da feature proíbe releaseRegion genérica em metadata de qualquer catálogo. Merged precisa ter
    semântica única: nesta feature não possui override regional próprio.

BV. O helper atual infere EOF quando uma página fica menor que a maior página vista. A V9 exige
    upstreamExhausted factual, mas não fornece adapter contract para prová-lo. Short page por si só não é
    prova universal de fim e pode truncar filtered pagination.

BW. makeTmdbRequest() já possui retry interno (3 tentativas totais no snapshot) e timeout por tentativa.
    Se o raw owner adicionar outro loop de retry, pode ocorrer retry amplification multiplicativa. O budget
    e a ownership do retry precisam ser únicos e client-abort precisa ser distinto de timeout interno.

BX. O budget de evidence e o bounded TMDB-ID mapping estão descritos separadamente. Sem um WorkBudget único,
    um request pode respeitar o limite de release_dates e ainda exceder o orçamento por mapping + retries +
    revalidation/lease waits.

BY. todayInTimezone()/nextLocalMidnight() não especificam como construir YYYY-MM-DD. Depender de
    Intl.DateTimeFormat(...).format() e depois parsear a string é locale-shape-dependent. A construção deve
    usar formatToParts (ou primitive equivalente testada) e montar o CalendarDate explicitamente.

BZ. O raw key canônico precisa corresponder a um request profile canônico. Hoje getMovieCertifications(params)
    chama /release_dates com `params` arbitrários enquanto movieReleaseDates(id) chama sem query params, mas
    ambos compartilham a mesma key. O owner novo deve eliminar essa ambiguidade: movie id é o único input
    factual da chamada release_dates usada por esta feature.
```

Esses blockers são de classes diferentes:

```text
BO/BQ/BR/BS → concorrência e ordenação de fatos
BP/BZ       → source ingress e cache ownership
BT/BU       → config/provenance semantics
BV          → paginação/exhaustion
BW/BX       → backpressure e budget
BY          → temporal/calendar correctness
```

---

# 338. Release Evidence V13 — authority e generation-coherence

A V13 mantém `RELEASE_EVIDENCE_SCHEMA = 2` porque o schema ainda é de implementação futura neste
snapshot, mas torna o Schema 2 final mais explícito. Não é necessário criar Schema 3 apenas para corrigir
o desenho antes do primeiro merge.

## 338.1. Separar facts Worldwide de authority regional

Modelo normativo:

```ts
type RegionalEvidenceAuthority =
  | 'committed-shared'
  | 'request-local-live';

interface CanonicalRegionalReleaseEvidenceV2 {
  authority: RegionalEvidenceAuthority;

  rawNamespaceSchema: 2;

  /** Presente para authority committed-shared. */
  sourceFetchGeneration: number | null;

  sourceFetchedAtMs: number;
  sourceFetchedAt: string;

  coverage:
    | 'available'
    | 'empty'
    | 'unavailable';

  homeReleaseDaysByRegion:
    Record<RegionCode, CalendarDate>;

  regionsWithReleaseRecords: RegionCode[];
}

interface ReleaseAvailabilityV2 {
  schema: 2;
  source: 'tmdb_release_dates';

  /** Golden-master Worldwide. */
  hasReleaseDateData: boolean;
  earliestAnyReleaseAt: string | null;
  earliestHomeReleaseAt: string | null;

  /** Somente facts regionais com authority comprovada. */
  regional?: CanonicalRegionalReleaseEvidenceV2;

  /** Observabilidade apenas. */
  normalizedAt?: string;
}
```

A estrutura pode ser implementada com nomes ligeiramente diferentes, mas estas propriedades
semânticas são obrigatórias.

## 338.2. O que pode autorizar HIDE regional

```text
committed-shared
+ sourceFetchGeneration == geração committed atual do raw owner
+ freshness válida
+ evidence semanticamente válida
→ pode autorizar HIDE + checkpoint estável
```

ou:

```text
request-local-live
+ upstream response validada na própria request
+ nenhuma authority compartilhada conflitante conhecida
→ pode autorizar HIDE somente nesta resposta
→ checkpointable=false enquanto coordination/storage não puder materializar o fato
```

Nunca:

```text
embedded movie-detail release_dates sem raw provenance
legacy Schema 1
page-cache evidence sem generation tag
sourceFetchedAt fresco porém generation desconhecida
search/discover card date
→ HIDE regional autoritativo
```

## 338.3. Generation-coherence é independente de max-age

Exemplo obrigatório:

```text
10:00 raw G=100 → BR ausente
10:01 evidence component E(G=100) criado
10:05 raw G=101 → BR Digital 2026-09-24
10:06 E(G=100) ainda tem age=6min (< SLA 6h)
```

Resultado correto:

```text
E não pode HIDE
rawGeneration 101 > evidenceGeneration 100
→ rederive evidence de G101
→ RELEASED quando data já chegou
```

Freshness responde:

```text
"o fato é recente?"
```

Generation-coherence responde:

```text
"este derived fact ainda corresponde ao raw fact committed mais novo?"
```

São gates diferentes.

## 338.4. Evidence component/page cache permanece derivado

Se `releaseEvidence` continuar em meta component/page/search cache:

```text
- armazenar sourceFetchGeneration;
- nunca ter autoridade maior que o raw owner;
- generation mismatch invalida o regional subobject imediatamente;
- re-normalizar do raw atual é permitido;
- re-normalizar do mesmo raw velho não renova sourceFetchedAt nem generation.
```

A alternativa arquitetural ainda mais simples é não persistir regional evidence fora do raw owner e
normalizá-la deterministicamente no request. Se o custo for aceitável, essa opção reduz estados
coerentes que precisam ser mantidos.

---

# 339. Evidence Ingress Gate V13 — um único caminho para authority regional

A V12 define `/movie/{id}/release_dates` como source factual canônica. A V13 fecha **como** esse dado
pode entrar no Release Visibility Engine.

## 339.1. Ingress reais localizados no snapshot

Hoje existem, no mínimo:

```text
addon/lib/getMeta.js
→ movieInfo(... append_to_response: ...release_dates ...)
→ movieData.release_dates
→ app_extras.releaseDates

addon/lib/getSearch.ts
→ hydrated TMDB details.release_dates
→ parsed.app_extras.releaseDates

addon/utils/releaseAvailability.ts
→ normalizeMetaReleaseAvailability(meta)
→ se app_extras.releaseDates existir
→ summarizeTmdbReleaseDates(...)
→ cria _releaseAvailability automaticamente

addon/lib/getTmdb.ts
→ movieReleaseDates(id)
→ /movie/{id}/release_dates

addon/lib/getTmdb.ts
→ getMovieCertifications(params)
→ /movie/{id}/release_dates
```

O problema não é o TMDB devolver `release_dates` via append subresponse; o problema é **promover um
payload sem o envelope canônico de freshness/generation para authority regional**.

## 339.2. Único constructor autoritativo

Criar uma fronteira semântica única, por exemplo:

```ts
deriveCanonicalReleaseEvidence(
  envelope: CachedReleaseDatesEnvelopeV2,
): ReleaseAvailabilityV2
```

ou equivalente.

Regra:

```text
CanonicalRegionalReleaseEvidence
→ só pode ser criado a partir de:
   A. committed raw envelope v2; OU
   B. live upstream response da própria request marcada request-local-live.
```

`normalizeMetaReleaseAvailability()` deixa de ser uma authority factory genérica.

## 339.3. Embedded/appended release_dates

Payload recebido via:

```text
movie detail append_to_response
search hydration detail
legacy meta app_extras.releaseDates
```

pode continuar servindo para:

```text
- Golden-master Worldwide, se necessário para preservar comportamento legado;
- certification já derivada no mesmo build;
- debugging/hint não autoritativo;
```

mas para Regional:

```text
não possui sourceFetchGeneration
não possui sourceFetchedAt do raw owner
→ não cria regional.homeReleaseDaysByRegion autoritativo
→ ensureMovieReleaseEvidence() consulta o canonical owner quando necessário
```

Se futuramente a implementação quiser aproveitar um `append_to_response=release_dates` recém obtido
como raw factual para evitar uma segunda chamada, isso só é permitido se ele for **ingestado pelo
mesmo owner**:

```text
validar payload
→ reservar/associar generation canônica
→ capturar storage observation time
→ CAS/commit no namespace v2
→ só então derivar committed-shared evidence
```

Não criar um segundo writer informal.

## 339.4. Static Evidence Ingress Gate

Adicionar script/ledger que procura:

```text
release_dates
releaseDates
app_extras.releaseDates
summarizeTmdbReleaseDates
normalizeMetaReleaseAvailability
getReleaseAvailability
movieReleaseDates
getMovieCertifications
```

Cada ocorrência que consegue alimentar movie release visibility deve estar classificada como:

```text
canonical-owner
legacy-worldwide-only
certification-only
non-authoritative-hint
response-hygiene
explicit-no-op
test
```

Gate final:

```text
zero caminho que cria regional authority fora do canonical constructor
```

---

# 340. Raw owner V13 — CAS loser, committed winner e allocator lifecycle

## 340.1. Candidate não é committed fact

Separar explicitamente:

```ts
interface RawFetchCandidate {
  generation: number;
  observedAtMs: number;
  normalizedPayload: TmdbReleaseDates;
}

interface RawCommitResult {
  status:
    | 'accepted'
    | 'rejected-newer-committed'
    | 'storage-error';
  committedEnvelope?: CachedReleaseDatesEnvelopeV2;
}
```

O candidate só vira `committed-shared` depois de CAS aceito.

## 340.2. Regra do CAS loser

Cenário:

```text
A reserva G=100
B reserva G=101
B termina primeiro e grava G101
A termina depois e tenta gravar G100
CAS rejeita A
```

A request A deve:

```text
1. descartar G100 como authority compartilhável;
2. reler/receber o committed winner G101;
3. derivar evidence de G101;
4. decidir visibility usando G101;
```

Se o winner não puder ser lido por falha de storage:

```text
candidate G100 NÃO pode sobrescrever semanticamente o winner conhecido;
resultado regional que seria HIDE
→ UNKNOWN/SHOW
→ checkpointable=false
```

Somente quando coordination/storage estava indisponível **antes de existir qualquer conflito conhecido**
é que um live response validado pode ser tratado como `request-local-live` conforme V11/V13.

## 340.3. Allocator — proibir per-id counter com reset independente

O exemplo V10:

```text
INCR tmdb:movie:release_dates:v2:generation:<id>
```

não é a forma final recomendada sem lifecycle explícito.

Duas implementações corretas preferidas:

### Opção A — global monotonic allocator

```text
INCR aiometadata:release-dates:v2:global-generation
```

Características:

```text
- uma única key;
- sem TTL enquanto qualquer raw v2 puder existir;
- total order global, embora CAS continue por movie-id;
- sem key leak por título;
- reset do allocator só junto com reset/migration integral do raw namespace.
```

### Opção B — allocator co-located com lifecycle do raw record

Usar storage shape/atomic primitive em que:

```text
nextGeneration
committedGeneration
payload
```

vivam no mesmo namespace/lifecycle e um reset de counter nunca possa ocorrer enquanto o committed
record antigo permanece utilizável.

Proibido:

```text
counter per-id expira
raw envelope não expira
→ generation reinicia abaixo do committedGeneration
```

## 340.4. Allocator recovery invariant

Teste/guard obrigatório:

```text
candidateGeneration <= committedGeneration por allocator inconsistente
→ não loopar centenas de fetches até alcançar o número antigo
→ detectar invariant breach
→ recuperar/reseed atomicamente OU invalidar namespace de forma segura
→ metric + warning
```

Nunca mascarar isso como um simples CAS conflict normal.

---

# 341. Shared Freshness Clock V13 — commits posteriores ao sample

A V12 exige um único `sharedFreshnessNowMs` por request para evitar host skew. A V13 mantém a ideia,
mas corrige um race distribuído real.

## 341.1. Race

```text
T0 request captura Redis TIME = 1000
T1 outra replica revalida raw
T2 outra replica grava sourceFetchedAtMs = 1010
T3 request original, após lease wait/CAS loss, relê o envelope G novo
```

Então:

```text
sourceFetchedAtMs(1010) > sharedFreshnessNowMs(1000)
```

isso **não prova corrupção**; o envelope pode ter sido committed legitimamente depois do sample.

## 341.2. Regra de advancement monotônico

Modelo:

```ts
interface SharedFreshnessClockState {
  nowMs: number | null;
  samples: number;
}
```

Fluxo normal:

```text
1 baseline Redis TIME sample
→ reutilizar para N metas
```

Resample excepcional permitido/obrigatório quando ocorre um synchronization event:

```text
- lease wait seguido de reread;
- CAS loss seguido de winner reread;
- envelope compartilhado lido depois do baseline com sourceFetchedAtMs > nowMs + tolerance;
```

Então:

```text
newStorageNow = Redis TIME
nowMs = max(oldNowMs, newStorageNow)
```

Esse avanço:

```text
- nunca move o clock para trás;
- nunca rejuvenesce evidence;
- torna evidence anterior somente mais velha/conservadora;
- não usa Date.now() como fallback.
```

## 341.3. Future timestamp validation V13

Depois do resample:

```text
sourceFetchedAtMs <= nowMs + tolerance
→ timestamp pode ser legítimo

sourceFetchedAtMs > nowMs + tolerance
→ corrupt/invalid-future
→ não autoriza HIDE
```

A regra V12 "uma request → um sample" passa a significar:

> um **baseline** sample por request/batch, sem polling item-a-item, com resamples somente em eventos de
> sincronização que provam que o baseline pode ter ficado temporalmente anterior ao fato recém lido.

## 341.4. Cursor

Antes de persistir cursor checkpointable que depende de shared freshness:

```text
usar o SharedFreshnessClockState final/mais avançado da avaliação
```

Se um resample fizer alguma evidence cruzar o freshness boundary:

```text
reavaliar a decisão dependente antes do checkpoint
```

---

# 342. Region provenance V13 — enums canônicos + merged semantics

## 342.1. Dois enums, não um enum ambíguo

Persisted Discover provenance:

```ts
type DiscoverRegionProvenanceSource =
  | 'discover-explicit'
  | 'watch-region-derived'
  | 'legacy-normalized'
  | 'language-derived';

interface DiscoverRegionProvenance {
  source: DiscoverRegionProvenanceSource;
  code: RegionCode;
}
```

Effective runtime source:

```ts
type EffectiveReleaseRegionSource =
  | DiscoverRegionProvenanceSource
  | 'global'
  | 'worldwide';

interface EffectiveReleaseRegion {
  mode: 'worldwide' | 'regional';
  code?: RegionCode;
  source: EffectiveReleaseRegionSource;
}
```

`explicit` isolado deixa de ser escrito em config nova.

Se alguma fixture experimental/histórica já contiver:

```text
source='explicit'
```

normalizar em read-time para:

```text
discover-explicit
```

sem write lateral, e persistir canônico no próximo Save.

## 342.2. Consistency validation

`regionProvenance` só é válida quando:

```text
provenance.code normaliza
+
params.region normaliza
+
provenance.code == params.region
+
source é enum conhecido
+
source-specific preconditions passam
```

Exemplo:

```text
source=watch-region-derived
→ Discover precisa ser release-aware segundo a regra definida
```

Mismatch:

```text
params.region=BR
provenance.code=US
→ provenance inválida
→ não usar US nem inventar override
→ warning/metric
→ fallback para policy segura definida (global/Worldwide)
```

## 342.3. Merged catalogs — decisão final V13

Nesta feature, merged catalog **não possui** `releaseRegion` própria.

Logo a frase histórica:

```text
merged catalog explicit region
```

fica substituída normativamente por:

```text
merged final Release Visibility region
→ config.releaseRegion
→ Worldwide
```

As regiões dos source catalogs:

```text
TMDB Discover source A params.region=US
TMDB Discover source B params.region=BR
```

continuam participando de:

```text
sourceMembershipSignature de cada source
source fetch/filter do próprio TMDB Discover
```

mas **não são combinadas nem promovidas** para a policy regional final do merged catalog.

Se futuramente houver necessidade de override regional no merged:

```text
novo campo explícito
+ nova provenance
+ filterSignature version bump
+ cursor migration
```

não reinterpretar metadata existente.

---

# 343. Filtered Pagination V13 — SourcePageResult e prova de exhaustion

A V9 exige `upstreamExhausted` factual. A V13 define como obtê-lo.

## 343.1. Remover heuristic genérica de short page

O snapshot atual contém lógica conceitual equivalente a:

```text
raw.length < maior page size já visto
→ lastUpstreamPage=true
```

Isso não pode permanecer como authority genérica de EOF para filtered pagination.

Short pages podem ocorrer por:

```text
- provider filtering interno;
- API variable page size;
- sparse/intermediate pages;
- permission/auth differences;
- transient source behavior;
- source-specific pagination rules.
```

## 343.2. Contract final

```ts
type SourceExhaustionState =
  | 'more'
  | 'exhausted'
  | 'unknown';

interface SourcePageResult<T> {
  items: T[];

  exhaustion: SourceExhaustionState;

  /** Raw/source coordinate da próxima leitura, quando aplicável. */
  nextPosition?: unknown;

  /** Neutral page revision/stability do contrato V10/V11. */
  sourceRevision?: string | null;
  stableUntilMs?: number | null;
}
```

`fillFilteredPage()` e Search equivalentes consomem `SourcePageResult`, não inferem semântica da
cardinalidade do array.

## 343.3. Quando um adapter pode dizer `exhausted`

Somente quando seu contrato provar uma destas condições:

```text
- upstream total_pages/total/count demonstra fim;
- has_more=false/next token ausente segundo documentação daquele provider;
- cursor upstream sinaliza EOF;
- empty page é terminal segundo contrato explícito daquele adapter;
- source finita local foi integralmente consumida.
```

Caso contrário:

```text
short page → unknown ou more
```

Nunca:

```text
short page genérica → exhausted
```

## 343.4. Budget

```text
exhaustion=unknown
+
fill budget acabou
→ budgetExhausted=true
→ upstreamExhausted=false
```

A limitação de protocolo documentada na V9 continua válida: uma resposta curta por budget não pode ser
rotulada como EOF.

## 343.5. Superfícies

Aplicar a mesma semântica em:

```text
standard catalog
external/custom/StremThru
merged source walkers
filtered search paginável
Jellyfin walkers quando reutilizarem o contrato
```

Cada adapter precisa de fixture que demonstre seu exhaustion proof.

---

# 344. Evidence WorkBudget V13 — uma única autoridade para calls/retries/deadline

## 344.1. Estado atual localizado

No snapshot, `makeTmdbRequest()` já faz:

```text
maxRetries = 3   # na prática, 3 tentativas totais no loop atual
per-attempt timeout = 15s
429 Retry-After handling
network/timeout retry
```

Portanto o raw owner não pode adicionar casualmente:

```text
outer retry 3x
  × makeTmdbRequest inner attempts 3x
```

porque um único logical fetch poderia virar até 9 tentativas antes de outras camadas.

## 344.2. Retry ownership

Escolher uma autoridade:

### Preferido

Parametrizar/reutilizar `makeTmdbRequest()` com um budget externo:

```ts
interface RequestAttemptBudget {
  signal?: AbortSignal;
  deadlineAtMs: number;
  remainingAttempts: number;
}
```

O TMDB client consome o mesmo budget.

### Aceitável

Raw owner é retry owner **somente se** chamar um primitive TMDB de single-attempt, desabilitando o
retry interno.

Proibido:

```text
retry loops independentes empilhados
```

## 344.3. Client abort vs per-attempt timeout

O snapshot usa `AbortSignal.timeout(15000)` e classifica `AbortError`/`TimeoutError` como retryable.
A #742 precisa propagar o request/client signal separadamente.

Em Node suportado, usar primitive equivalente a:

```ts
AbortSignal.any([
  clientSignal,
  AbortSignal.timeout(perAttemptTimeoutMs),
])
```

ou mecanismo funcionalmente equivalente.

Regra:

```text
client disconnected / request cancelled
→ não retry
→ cancelar wait/backoff/fetch

per-attempt timeout com request ainda viva
→ retry somente se budget/deadline permitirem
```

O motivo do abort precisa permanecer distinguível.

## 344.4. Unified ReleaseEvidenceWorkBudget

```ts
interface ReleaseEvidenceWorkBudget {
  deadlineAtMs: number;

  maxTmdbMappingCalls: number;
  maxReleaseDateAttempts: number;
  maxConcurrentReleaseDateFetches: number;

  mappingCallsUsed: number;
  releaseDateAttemptsUsed: number;

  signal?: AbortSignal;
}
```

Conta dentro do mesmo request:

```text
- optional central TMDB ID mapping que faz network;
- raw /release_dates attempts;
- retry attempts;
- forced revalidation attempts.
```

Distributed lease wait:

```text
não consome network-attempt counter
mas consome wall-clock deadline
```

Cache hit/local mapping hit:

```text
não consome upstream-call counter
```

Budget exhaustion:

```text
não iniciar novo network attempt
→ UNKNOWN/SHOW quando evidence faltante impedir decisão segura
→ checkpointable=false quando membership ficou transient/indeterminada
```

## 344.5. Retry-After

Quando presente:

```text
delta-seconds válido OU HTTP-date parseável
→ delay bounded pelo deadline restante
```

Inválido/ausente:

```text
bounded exponential backoff + jitter
```

Nunca dormir além do request deadline para depois descobrir que o budget acabou.

---

# 345. Canonical raw request profile V13

A raw key só é semanticamente correta se representar **um request upstream canônico**.

## 345.1. Request profile

Para #742:

```text
GET /movie/{tmdbId}/release_dates
query params correctness-critical: nenhum
region: nenhum
language: nenhum
user/account: nenhum
```

`tmdbId` é o único input factual.

Se o projeto futuramente descobrir um parâmetro TMDB que altere o payload necessário:

```text
RAW_RELEASE_DATES_REQUEST_PROFILE_VERSION bump
+ raw namespace/source signature migration
```

não esconder essa mudança atrás da mesma key.

## 345.2. Certification consumer

`getMovieCertifications(params)` deixa de executar seu próprio request com `params` arbitrários para a
mesma key. Ele deve consumir:

```text
canonical raw owner
→ payload normalizado
→ certification projection
```

Certification continua com consumer freshness SLA própria, conforme V10.

## 345.3. Append-to-response

`movieInfo(... append_to_response=release_dates)` pode continuar existindo por eficiência de metadata e
certification, mas:

```text
- não escreve diretamente o raw owner v2;
- não fabrica committed-shared regional evidence;
- não altera sourceFetchedAt/generation;
```

Aproveitamento como canonical raw seed só passa pelo ingest flow definido na seção 339.3.

---

# 346. CalendarDate V13 — construção timezone-safe sem locale-string parsing

## 346.1. `todayInTimezone()`

Implementar com `Intl.DateTimeFormat(...).formatToParts()` ou primitive equivalente, extraindo:

```text
year
month
day
```

e montando explicitamente:

```text
YYYY-MM-DD
```

Não fazer:

```text
formatter.format(now)
→ assumir que a string sempre vem YYYY-MM-DD
→ split por '-' ou '/'
```

porque presentation shape é responsabilidade do locale/ICU, não contrato semântico do helper.

## 346.2. `nextLocalMidnight()`

Continuam valendo os invariantes V9/V10:

```text
- nunca now + 24h;
- timezone IANA validada;
- DST/non-hour offset;
- calendar next-day real;
```

O helper deve construir o próximo dia civil e resolver o primeiro instante correspondente ao início
desse dia no timezone, com teste para transições incomuns.

## 346.3. Matriz adicional

```text
UTC
America/Fortaleza
America/St_Johns          # offset de meia hora em partes do ano
Asia/Kathmandu            # UTC+05:45
Australia/Lord_Howe       # transição DST de 30 minutos
Pacific/Kiritimati        # UTC+14
```

O objetivo não é suportar só fusos de hora inteira.

---

# 347. Filter Pipeline V13 — lazy evidence verdadeiramente lazy

Isto é uma melhoria de performance/custo, não mudança de membership policy. Ela passa a ser
recomendada porque a #742 pode adicionar fanout de `/release_dates`.

## 347.1. Staging

Antes de evidence completion, aplicar somente filtros **puros, locais, deterministicamente equivalentes
e independentes de release facts**, por exemplo quando seus dados já estão no meta:

```text
age-rating cap
keyword/genre/regex exclusions
media-type applicability
```

Depois:

```text
survivors
→ ensure release evidence
→ release visibility
→ demais dynamic membership filters conforme contrato versionado
→ dedupe
→ cursor accounting
```

Isso evita consultar release dates para um item que já seria removido por uma regra local barata.

## 347.2. Não reordenar silenciosamente filtros com efeitos externos

Hide-watched pode consultar estado dinâmico e falhar/fail-open. Sua posição não deve ser movida somente
por otimização sem fixture de equivalência.

Qualquer mudança na ordem que possa alterar:

```text
membership sob failure
validity contributions
network calls observáveis
checkpointable
```

entra em:

```text
PAGINATION_CONTRACT_SIGNATURE_VERSION
```

ou mantém a ordem histórica.

## 347.3. Prova

Golden fixture:

```text
mesmo neutral meta set
→ pipeline antigo de referência
→ pipeline staged
→ mesmo visible id set quando todas as dependencies estão saudáveis
```

Medir:

```text
release evidence lookups avoided by prefilter
```

sem usar IDs como metric label.

---

# 348. Mandatory file/occurrence map V13

Somar ao mapa V12:

```text
addon/lib/getMeta.js
addon/lib/getSearch.ts
addon/lib/getTmdb.ts
addon/lib/tmdbCacheNormalizers.ts
addon/utils/releaseAvailability.ts
addon/lib/catalogPagination.ts
addon/lib/redisClient.ts
```

Os paths já podiam estar presentes em mapas históricos; a V13 muda **a razão de auditoria** e o
contrato exigido.

## 348.1. Occurrence terms V13

```text
app_extras.releaseDates
releaseDates:
append_to_response
release_dates
summarizeTmdbReleaseDates
normalizeMetaReleaseAvailability
getReleaseAvailability
sourceFetchGeneration
fetchGeneration
committedGeneration
global-generation
CAS
Retry-After
maxRetries
AbortSignal.timeout
AbortSignal.any
upstreamPageSize
lastUpstreamPage
raw.length
SourcePageResult
regionProvenance
explicit
discover-explicit
```

## 348.2. Evidence Authority Closure Gate

Além do Caller-Closure Gate:

```text
qualquer novo constructor/writer de _releaseAvailability/releaseEvidence
→ classificado

qualquer novo raw /release_dates caller
→ classificado

qualquer novo app_extras.releaseDates producer/consumer
→ classificado
```

Zero unclassified.

## 348.3. Retry Closure Gate

Qualquer wrapper em volta do TMDB raw owner que implemente:

```text
retry
backoff
timeout
AbortController
lease wait
```

deve provar que consome o mesmo WorkBudget ou que não inicia tentativa upstream adicional.

---

# 349. Test Matrix V13 — casos adicionais obrigatórios

A numeração continua a V12.

## Generation coherence / raw winner

```text
114. evidence G100 fresh + raw G101 newer → evidence G100 não pode HIDE;
115. raw G101 contém BR release passada → rederive → SHOW;
116. raw G101 contém BR release futura → rederive → HIDE somente se G101 fresh;
117. evidence generation == raw generation + fresh → pode decidir normalmente;
118. evidence generation > committed raw generation → corruption/invariant → revalidate ou UNKNOWN;
119. evidence sem generation tag → advisory only para Regional;
120. CAS G100 perde para committed G101 → request usa G101, não candidate G100;
121. CAS loser + winner reread falha → would-HIDE degrada UNKNOWN/SHOW + checkpointable=false;
122. request-local-live sem storage, sem conflito conhecido → pode decidir resposta; não checkpointa;
```

## Generation allocator

```text
123. global allocator produz generation estritamente crescente;
124. 1000 títulos não criam 1000 permanent generation keys quando opção global é usada;
125. allocator key reset enquanto raw existe é detectado como invariant breach;
126. cleanup/migration do raw namespace mantém allocator lifecycle coerente;
127. out-of-order fetch across replicas nunca sobrescreve generation maior;
```

## Evidence ingress

```text
128. movie detail append release_dates + sem raw envelope → não cria regional authority;
129. search hydration details.release_dates + sem raw envelope → não cria regional authority;
130. embedded release_dates ainda preserva Worldwide golden behavior quando necessário;
131. canonical raw envelope G55 → regional evidence sourceFetchGeneration=55;
132. novo app_extras.releaseDates caller não classificado → CI falha;
133. certification-only consumer não cria regional evidence;
```

## Shared clock advancement

```text
134. baseline Redis TIME=1000; winner committed at 1010; reread → bounded resample valida 1010;
135. resample avança clock monotonicamente, nunca para trás;
136. resample torna evidence anterior stale → decisão é reavaliada antes do checkpoint;
137. future timestamp continua futuro após resample → invalid/corrupt, não HIDE;
138. N metas sem sync event → um baseline sample, sem N Redis TIME calls;
```

## Provenance / merged

```text
139. new Discover explicit save grava `discover-explicit`, nunca `explicit`;
140. legacy/source='explicit' normaliza para discover-explicit em memória sem write lateral;
141. provenance.code != params.region → invalid provenance + safe fallback;
142. watch-region-derived sem release-aware semantics → provenance inválida para override;
143. merged com source US + source BR, global=GB → final Release Visibility usa GB;
144. merged sem global → Worldwide;
145. child Discover region continua em source identity, não vira merged filter region;
```

## Source exhaustion

```text
146. páginas [20, 7, 20] não tratam a página 7 como EOF somente por ser curta;
147. explicit has_more=false → upstreamExhausted=true;
148. total_pages atingido → upstreamExhausted=true;
149. short page sem proof → exhaustion=unknown;
150. unknown + maxPages atingido → budgetExhausted=true e upstreamExhausted=false;
151. adapter terminal-empty contract → empty final page pode provar EOF;
152. standard/search/external adapter fixtures usam o mesmo semantic enum;
```

## Retry / unified budget

```text
153. raw owner não multiplica retry interno de makeTmdbRequest;
154. budget maxReleaseDateAttempts=3 → no máximo 3 upstream attempts totais;
155. mapping network call consome mapping budget;
156. cache mapping hit não consome network budget;
157. forced revalidation retry consome o mesmo release attempt budget;
158. client abort durante backoff cancela sem nova tentativa;
159. client abort durante fetch não é reclassificado como retryable timeout;
160. per-attempt timeout pode retry apenas dentro de deadline/attempt budget;
161. Retry-After maior que deadline restante → não dormir além do deadline;
162. lease wait consome deadline, não upstream-attempt counter;
```

## Calendar helpers

```text
163. todayInTimezone usa parts e produz YYYY-MM-DD em todos os locales suportados;
164. Asia/Kathmandu boundary (+05:45) correta;
165. Australia/Lord_Howe DST 30min correto;
166. Pacific/Kiritimati UTC+14 correto;
167. nextLocalMidnight nunca é implementado como +24h;
```

## Raw request profile

```text
168. canonical /release_dates call não varia por language/region/user;
169. certification consumer reutiliza canonical owner sem params arbitrários;
170. request profile version change exige namespace/schema migration test;
```

## Staged filtering

```text
171. local exclusion remove item antes de evidence fetch → zero release lookup para esse item;
172. staging saudável preserva visible id set do reference pipeline;
173. reorder de dynamic/failure-sensitive filter sem contract bump → test falha;
```

---

# 350. Observabilidade V13 — complementos

Adicionar métricas de baixa cardinalidade:

```text
release_evidence_generation_total{result=match|raw_newer|evidence_ahead|missing_generation}
release_raw_commit_total{result=accepted|rejected_newer|storage_error}
release_generation_allocator_total{result=ok|reset_detected|recovered|error}
release_evidence_ingress_total{kind=canonical|embedded_hint|certification_only|legacy_worldwide}

release_shared_clock_resample_total{reason=lease_wait|cas_loss|post_sample_commit,result=ok|failed|still_future}

filtered_source_exhaustion_total{state=more|exhausted|unknown,proof=metadata|cursor|terminal_empty|local|none}
filtered_short_page_total{action=continue|unknown|terminal_by_contract}

release_work_budget_total{resource=mapping|release_attempt|deadline,result=consumed|exhausted}
release_retry_owner_total{owner=tmdb_client|raw_owner}
release_abort_total{cause=client|attempt_timeout|deadline}

release_provenance_validation_total{result=valid|code_mismatch|invalid_source|invalid_precondition}
```

Não usar:

```text
movie id
query
user id
raw token
full cursor key
```

como label.

Logs de invariant breach podem carregar IDs técnicos somente no nível/debug policy já aceito pelo
projeto e nunca secrets.

---

# 351. Implementation Order V13 — ordem consolidada final

A ordem V12 é preservada, mas os novos gates entram antes das camadas que dependem deles.

```text
Phase A0 — snapshot + static closure
1. confirmar HEAD/tree;
2. Occurrence Gate V13;
3. Caller-Closure Gate V13;
4. Evidence Ingress Gate V13;
5. Retry Closure Gate V13;

Phase A1 — raw factual owner
6. canonical raw request profile;
7. raw namespace v2;
8. lifecycle-safe generation allocator;
9. CAS committed winner semantics;
10. sourceFetchedAt acquisition-time + storage clock;
11. certification consumer migra para owner único;

Phase A2 — evidence authority
12. ReleaseAvailability Schema 2 final com regional authority/sourceFetchGeneration;
13. embedded/appended release_dates tornam-se non-authoritative para Regional;
14. generation-coherence check/rederive;
15. shared freshness baseline + monotonic resample rules;

Phase A3 — time + policy
16. CalendarDate parser;
17. todayInTimezone via formatToParts;
18. nextLocalMidnight DST/non-hour-safe;
19. Worldwide golden evaluator;
20. Regional evaluator;
21. Series evaluator;

Phase A4 — request ownership/cache
22. RequestOwned boundary;
23. releaseEvidence component/sidecar strategy;
24. response projection pure;
25. concurrent alias poison tests;

Phase A5 — pagination
26. SourcePageResult adapters;
27. exact raw coordinates;
28. budgetExhausted/upstreamExhausted split;
29. dedupe/cursor CAS/V7+V3;
30. no short-page heuristic genérica;

Phase A6 — config/provenance
31. global releaseRegion;
32. canonical DiscoverRegionProvenanceSource;
33. import/export/share/reconstruct round-trip;
34. merged uses global/Worldwide only;
35. setup/fixtures failure-safe;

Phase A7 — search
36. EffectiveSearchSourceContext;
37. neutral search cache namespace;
38. provider pre-filter removal;
39. canonical evidence ingress somente pós-cache;
40. filtered search paging adapters;

Phase A8 — work budget/backpressure
41. propagate client AbortSignal;
42. single retry owner/shared attempt budget;
43. unified mapping/release/deadline WorkBudget;
44. distributed lease com bounded wait;
45. 429/malformed/failure matrix;

Phase A9 — performance optional-safe
46. staged local prefilters;
47. benchmark release calls avoided;
48. load/Redis multi-replica tests;

Phase A10 — deploy
49. backend dark deploy;
50. observability gate;
51. homogeneous fleet;
52. UI enable;
53. rollback + kill-switch drill.
```

---

# 352. Definition of Done V13 — gates cumulativos finais

Somar às checklists V10–V12:

```text
[ ] ReleaseEvidence compartilhada carrega sourceFetchGeneration
[ ] evidence freshness e generation-coherence são gates separados
[ ] raw generation mais nova invalida evidence derivada antiga mesmo dentro do SLA
[ ] CAS loser nunca decide checkpointable HIDE usando candidate rejeitado
[ ] CAS loser relê/usa committed winner

[ ] generation allocator possui lifecycle matematicamente seguro
[ ] nenhuma per-title generation key leak/reset pode bloquear future writes
[ ] allocator reset/invariant breach é detectado e testado

[ ] app_extras.releaseDates/append_to_response não cria regional authority informal
[ ] único canonical regional evidence constructor recebe raw envelope/live-authoritative input
[ ] Evidence Ingress Gate = zero unclassified

[ ] baseline shared freshness clock aceita bounded monotonic resample após sync event
[ ] legitimate post-sample commit não é tratado como timestamp corrupto
[ ] future timestamp realmente inválido continua fail-open

[ ] persisted Discover provenance usa enum canônico
[ ] `explicit`/`discover-explicit` ambiguity eliminada
[ ] provenance code/params.region consistency validada
[ ] merged catalog não possui implicit/generic releaseRegion override
[ ] child source region não contamina merged final policy

[ ] generic filtered pagination não infere EOF por short page
[ ] cada adapter possui exhaustion proof explícito
[ ] unknown exhaustion + budget end != upstream exhausted

[ ] exatamente uma retry authority por logical raw fetch
[ ] evidence WorkBudget conta mapping + release attempts + retries + deadline
[ ] client abort não vira retryable internal timeout
[ ] Retry-After nunca ultrapassa remaining deadline

[ ] canonical raw request profile é region/language/user-neutral
[ ] certification reutiliza raw owner único

[ ] todayInTimezone não depende de locale formatted string shape
[ ] nextLocalMidnight passa DST + non-hour offset matrix

[ ] Occurrence Gate V13 = zero unclassified
[ ] Caller-Closure Gate V13 = zero unclassified
[ ] Evidence Ingress Gate V13 = zero unclassified
[ ] Retry Closure Gate V13 = zero unclassified
```

---

# 353. Final pre-merge checklist V13

Executar depois das checklists históricas:

```text
[ ] dev HEAD == 6e83e22ab9de5093f9918a1871157f401feebb03
    OU Rebase/Delta/Occurrence/Caller/Evidence-Ingress/Retry Closure Gates rerodados

[ ] issue #742 status revalidado
[ ] TMDB release_dates/region/rate-limit docs revalidadas

[ ] getMeta.js append release_dates classificado
[ ] getSearch.ts releaseDates producers classificados
[ ] releaseAvailability.ts não promove embedded hint a canonical regional authority
[ ] getMovieCertifications usa canonical owner

[ ] evidence G old + raw G new regression passa
[ ] CAS-loser winner reread regression passa
[ ] generation allocator lifecycle/reset regression passa
[ ] post-sample committed raw + Redis TIME resample regression passa

[ ] provenance enum possui um único formato de write
[ ] merged region semantics fixture passa

[ ] catalogPagination generic short-page EOF heuristic removida/substituída
[ ] SourcePageResult adapter matrix passa

[ ] retry amplification test prova max upstream attempts
[ ] client abort/backoff cancellation test passa
[ ] unified WorkBudget test passa

[ ] Kathmandu/Lord_Howe/Kiritimati CalendarDate tests passam

[ ] neutral cache semantic digest/ownership tests V12 continuam passando
[ ] Worldwide golden-master continua equivalente
[ ] Regional BR/US fixtures continuam passando
[ ] Series golden fixtures continuam passando

[ ] build frontend passa
[ ] build backend passa
[ ] lint passa
[ ] test harness passa
[ ] Redis multi-replica/concurrency suite passa
[ ] migration/rollback suite passa
[ ] load benchmark passa

[ ] Phase A dark deploy aprovado
[ ] fleet homogênea
[ ] Phase B UI aprovada
[ ] kill switch e rollback drill executados
```

---

# 354. Resultado final da reauditoria V13

A V12 já era um plano de engenharia excepcionalmente abrangente no sentido técnico: ela cobria a
maioria das superfícies de provider, cache, search, catalog, cursor, config, Jellyfin, warmers,
rollout e observabilidade. A V13 não altera a direção; ela fecha **dez classes finais de ambiguidade**
que poderiam produzir implementações diferentes a partir do mesmo texto:

```text
1. freshness sem generation-coherence;
2. alternate evidence ingress via append/app_extras;
3. candidate raw que perdeu CAS sem semântica de consumo;
4. generation allocator sem lifecycle seguro;
5. shared clock sample anterior a commit concorrente legítimo;
6. provenance `explicit` vs `discover-explicit` inconsistente;
7. merged "explicit region" incompatível com o próprio scope da feature;
8. upstream exhaustion exigida como fato, mas inferida por short-page heuristic;
9. retry/backoff podendo existir em mais de uma camada;
10. evidence work budget fragmentado entre mapping/revalidation/retry.
```

E adiciona dois hardenings de implementação:

```text
11. CalendarDate via formatToParts, sem locale-string assumption;
12. canonical raw request profile sem params region/language/account.
```

Com as seções 336–353 incorporadas, a formulação defensável passa a ser:

```text
V13 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
      com static occurrence + caller closure + evidence-ingress closure + retry closure,
      generation-coherent release evidence,
      factual source exhaustion,
      e runtime/upstream/concurrency/deployment transformados em gates executáveis.
```

## 354.1. O que a V13 chama de cobertura completa

A alegação continua deliberadamente restrita ao que engenharia consegue provar:

> **100% da superfície estática localizada e classificada no snapshot auditado, com um único contrato
> autoritativo para cada boundary correctness-critical e gates executáveis para o que depende de
> runtime, storage distribuído, upstream vivo, concorrência, carga ou deploy.**

Não significa infalibilidade futura.

## 354.2. Rebase rule final

Qualquer alteração após o snapshot exige:

```text
Rebase Gate
+ Delta File Gate
+ Occurrence Gate V13
+ Caller-Closure Gate V13
+ Evidence Ingress Gate V13
+ Retry Closure Gate V13
+ Worldwide/Regional/Series golden suites
+ pagination/source-exhaustion suite
+ Redis generation/CAS/clock suite
+ migration/rollback suite
```

antes de manter a alegação V13.

## 354.3. Regra de implementação final

Se durante o PR surgir uma escolha entre:

```text
"usar o dado que já está no meta"
vs
"provar authority/freshness/generation pelo contrato canônico"
```

para uma decisão que pode ocultar conteúdo, escolher o segundo caminho.

Se não for possível provar:

```text
UNKNOWN → SHOW
```

e nunca persistir um cursor/checkpoint que finja estabilidade quando a decisão foi transitória.
---

# 355. Reauditoria V14 — resultado da auditoria final sobre a V13

A V13 já fechava a maior parte das classes de erro arquitetural relevantes para a #742. A V14
reexecutou a auditoria sobre o mesmo snapshot, sem drift:

```text
dev HEAD  = 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA  = 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
Tree      = 583 entradas
Blobs     = 544
Dirs      = 39
Release   = v3.1.0
Issue 742 = aberta, sem comentários no snapshot revalidado
```

A árvore retornada pelo GitHub não está truncada. Portanto a reauditoria está comparando o plano
contra a mesma árvore que a V13 declara, e não contra uma aproximação por branch móvel.

A V14 encontrou **oito classes adicionais** que precisam ficar explícitas para a implementação ser
unívoca e correctness-first:

```text
CA. cursor temporalmente válido ainda pode ficar semanticamente velho se raw release evidence
    puder receber uma geração nova antes de cursor.validUntil;

CB. o snapshot não possui um provider-level TMDB concurrency limiter no makeTmdbRequest();
    request-local budget sozinho não protege o processo/frota contra bursts de IDs distintos;

CC. factual cache identity e transport credential identity são conceitos diferentes: release_dates
    é fato público compartilhável, mas retry/429/single-flight não devem acoplar chaves TMDB distintas;

CD. o comentário atual trata 5xx como retryable, porém o catch de makeTmdbRequest() só retrya
    isRetryable/network/Undici/timeout; 5xx genérico cai direto para erro;

CE. release applicability não pode depender somente de meta.type: TVDB Collections Search produz
    objeto semântico de collection com type='movie', enquanto anime.movie precisa ser movie-like;

CF. TMDB ID resolution usado para HIDE precisa ser media-type-safe e possuir provenance/freshness;
    o id-resolver atual pode escolher movie_results[0] OU tv_results[0] independentemente do type;

CG. o registro histórico de versões contém valores obsoletos (raw schema 1, cursor 6/search 2)
    enquanto as camadas normativas posteriores exigem raw v2 e Catalog Cursor V7/Search Cursor V3;

CH. with_release_type é order-sensitive no TMDB Discover; 2|3 e 3|2 não são canonicalmente
    intercambiáveis e precisam de fixture/source-signature explícita.
```

Esses pontos não mudam a direção da arquitetura V13. Eles fecham as últimas dependências entre
**evidence mutation, cursor stability, transport control, semantic entity kind e identity mapping**.

---

# 356. Regra de precedência V14

As seções 1–354 preservam a trilha histórica V8→V13 e continuam úteis como rationale/evidence ledger.
As correções inline feitas nesta V14 e as seções **355+** são normativas.

Em qualquer conflito sobre:

```text
raw schema/version
cursor schema/version
raw mutation stability
provider concurrency
credential scoping de transporte
retry classification
media/entity applicability
TMDB ID mapping authority
with_release_type ordering
DoD/pre-merge
```

**V14 prevalece**.

---

# 357. Cursor × raw evidence V14 — mutation stability obrigatória

A V13 separa corretamente freshness de generation-coherence, mas existe uma terceira propriedade:

> um cursor só é estável se nenhum fato capaz de alterar membership puder ser substituído antes do
> boundary temporal gravado naquele cursor.

## 357.1. Race que precisa ser proibida

```text
10:00 raw G100 → BR home release ausente
10:01 página filtrada produz cursor C, validUntil=16:00
10:30 outro consumer/force refresh grava raw G101 → BR Digital hoje
10:31 C ainda passa no teste now < validUntil
```

Se o cursor não souber que a dependência factual mudou, a posição upstream já não corresponde ao
mesmo conjunto filtrado.

Generation-coherence protege **uma decisão no momento da avaliação**. Ela não protege automaticamente
um cursor já emitido depois que o raw owner avança.

## 357.2. Contrato preferido para a primeira implementação: raw mutation floor

Adicionar ao envelope/read do owner um boundary factual:

```ts
interface ReleaseDatesReadV14 {
  envelope: CachedReleaseDatesEnvelopeV2 | null;
  fresh: boolean;
  freshUntilMs: number | null;

  /**
   * Instante mais cedo em que uma request normal pode substituir este raw winner.
   * Não é retention TTL.
   */
  stableUntilMs: number | null;
}
```

Regra:

```text
normal shared raw commit G
→ define stableUntilMs centralmente
→ nenhum consumer normal pode force-refetch/commit antes desse boundary
→ filtered cursor.validUntil <= menor stableUntilMs das release dependencies avaliadas
```

O `stableUntilMs` precisa ser derivado da **menor freshness configurada capaz de autorizar HIDE**,
não do maior TTL de retenção.

Se settings permitirem mudar esse mínimo em runtime:

```text
mudança que encurta o mutation floor
→ bump de policy/pagination namespace OU invalidação deliberada antes de aplicar
```

Nunca deixar uma configuração nova de 1h conviver com envelope/cursor que assumiu 6h sem migration.

## 357.3. Early force refresh

Para a primeira implementação, `forceUpstream=true` antes de `stableUntilMs` não é uma primitive de
request comum.

Aceitável:

```text
A. negar/ignorar early force e usar winner atual até stableUntil; OU
B. operação administrativa excepcional faz early commit e também avança um
   RELEASE_RAW_MUTATION_EPOCH correctness-critical lido pelos cursores.
```

Se B existir, o epoch entra na validação do cursor, não como métrica/debug.

Não fazer:

```text
early force commit silencioso
+
cursor antigo continua válido apenas porque o relógio ainda não venceu
```

## 357.4. Alternativa futura

Se o projeto precisar de refresh antecipado frequente, substituir o mutation-floor simples por
**exact release dependency validation**: cada checkpoint carrega dependências cumulativas
`(tmdbId, committedGeneration)` ou estrutura exata equivalente e as valida no resume.

Bloom/fingerprint sem possibilidade de provar membership continua proibido.

## 357.5. Race de check→checkpoint

O raw envelope precisa carregar sua própria `fetchGeneration`. A leitura usada para decisão deve
retornar payload + generation + stableUntil como um único snapshot lógico.

Antes de persistir checkpoint:

```text
shared clock ainda < stableUntil
+
nenhum correctness epoch relevante mudou
→ checkpoint permitido

boundary cruzou durante o walk
→ checkpointable=false/restart do trecho conforme contrato existente
```

---

# 358. TMDB Transport V14 — admission control real, não presumido

## 358.1. Correção factual da V13

No snapshot auditado, `addon/lib/getTmdb.ts::makeTmdbRequest()` possui timeout/retry e observa headers
de rate limit, mas **não possui semaphore/token bucket/provider-level concurrency limiter**.

Portanto a frase histórica "limitador global/provider existente" não pode ser requisito de implementação.
O limiter precisa ser introduzido ou provado por um primitive central novo.

## 358.2. Central TmdbAdmissionController

Criar uma autoridade única no cliente TMDB, conceitualmente:

```ts
interface TmdbAdmissionContext {
  credentialScope: string;      // fingerprint opaco, nunca secret cru
  deadlineAtMs: number;
  signal?: AbortSignal;
  purpose:
    | 'release-dates'
    | 'id-find'
    | 'metadata'
    | 'search'
    | 'other';
}
```

Responsabilidades:

```text
- max in-flight process-wide configurável;
- opcional sublimit por credentialScope;
- queue bounded;
- deadline-aware admission;
- client abort remove waiter da fila;
- 429 cria cooldown compartilhado para a credential correta;
- slot sempre liberado em success/error/abort;
- nenhuma fila sem limite.
```

Não hardcode "40 req/s" como contrato. TMDB documenta apenas um upper limit aproximado e mutável;
`429` é a autoridade operacional.

## 358.3. Request budget + provider admission são gates diferentes

```text
request WorkBudget
→ impede uma request de monopolizar chamadas

provider admission controller
→ impede muitas requests/IDs distintos de saturarem TMDB em conjunto

single-flight/lease
→ colapsa duplicatas do mesmo fato
```

Os três são necessários; nenhum substitui os outros.

## 358.4. Escopo

O melhor ponto de integração é o cliente TMDB central para que release evidence não seja protegida
por um limiter enquanto search/meta paralelos continuam consumindo a mesma capacidade sem coordenação.

Rollout seguro:

```text
controller default conservador/configurável
→ métricas de queue/in-flight/429
→ load test
→ tuning
```

---

# 359. Data identity × credential identity V14

`/movie/{id}/release_dates` é um endpoint factual público. A key canônica continua:

```text
movie id + raw request profile version
```

Não colocar API key na **factual cache identity**.

Mas transporte não pode fingir que todas as credenciais são iguais.

## 359.1. Credential scope opaco

Derivar:

```text
credentialScope = HMAC-SHA-256(versioned server-only key, effective TMDB credential)
                 truncado com >=128 bits efetivos
```

Nunca:

```text
raw API key em Redis/log/metric
SHA simples de API key
últimos caracteres da key como identidade
```

O fingerprint é apenas coordenação interna de transporte.

## 359.2. Single-flight/lease

Para evitar que uma API key inválida ou rate-limited prenda callers com outra key válida:

```text
local upstream flight key
= canonicalRawKey + credentialScope
```

O commit continua global por `canonicalRawKey` e usa generation/CAS.

Para multi-replica, o lease pode seguir a mesma granularidade de credential scope. Assim:

```text
mesmo movie + mesma credential
→ colapsa

mesmo movie + credenciais diferentes
→ podem competir
→ CAS escolhe winner factual
```

Isso troca um pequeno número de duplicate fetches por isolamento correto de falha/autorização.

## 359.3. Auth failure

```text
401/403 de credential A
→ não grava raw negative
→ não marca movie como unavailable compartilhado durável
→ libera flight/lease imediatamente
→ não cria cooldown para credential B
```

## 359.4. 429 cooldown

Cooldown é transport-scoped:

```text
credential A recebeu 429
→ A aguarda segundo Retry-After/deadline

credential B
→ não é bloqueada automaticamente
```

Se a instância usa uma única built-in key, todos naturalmente caem no mesmo scope.

Métricas nunca usam `credentialScope` como label de alta cardinalidade.

---

# 360. Retry classifier V14 — corrigir a divergência 5xx

## 360.1. Estado atual

O snapshot possui comentário:

```text
// Retryable server errors (500, 502, etc)
```

mas a implementação lança `new Error(...)` sem `isRetryable=true`. O `catch` somente repete quando:

```text
error.isRetryable
OR Undici error
OR network fetch failure
OR TimeoutError/AbortError
```

Logo 5xx HTTP normal **não retrya** hoje.

## 360.2. Classificador explícito

Criar uma função única:

```ts
type TmdbRetryClass =
  | 'success'
  | 'non-retryable-http'
  | 'rate-limited'
  | 'transient-http'
  | 'attempt-timeout'
  | 'network'
  | 'client-abort'
  | 'invalid-payload';
```

Política mínima para release evidence:

```text
400/401/403/404/422
→ non-retryable-http

429
→ rate-limited
→ Retry-After quando válido

408 e 5xx transitórios
→ transient-http
→ retry somente se unified WorkBudget/deadline permitir

client abort
→ nunca retry

per-attempt timeout/network transport
→ retry somente dentro do budget

200 com payload semanticamente inválido
→ nunca vira empty/negative evidence
→ retry no máximo conforme política central explícita; caso contrário unavailable
```

Não espalhar `if (status===...)` em release owner e `makeTmdbRequest` separadamente.

## 360.3. Error metadata

Todo erro HTTP retornado ao retry owner precisa preservar:

```text
statusCode
retryClass
retryAfterMs quando aplicável
attempt number
```

sem URL com API key.

---

# 361. Release applicability V14 — semantic entity kind

## 361.1. Problema concreto

A regra "AI Search avalia meta.type item a item" é insuficiente como regra universal.

No snapshot, TVDB Collections Search monta um item de collection com:

```ts
id: `tvdbc:${collectionId}`,
type: 'movie',
```

Esse `type: 'movie'` é encoding de compatibilidade, não prova de que a entidade é um filme sujeito a
Hide Unreleased.

Ao mesmo tempo, requests `anime.movie` precisam ser tratados como movie-like quando existe identidade
TMDB movie autoritativa.

## 361.2. Resolver semântica uma vez

Criar:

```ts
type ReleaseVisibilityEntityKind =
  | 'movie'
  | 'series'
  | 'non-title'
  | 'unknown';

interface EntityKindResolution {
  kind: ReleaseVisibilityEntityKind;
  source:
    | 'request-type'
    | 'meta-type'
    | 'id-prefix'
    | 'provider-contract'
    | 'unknown';
}
```

E:

```ts
resolveReleaseVisibilityEntityKind({
  surface,
  cleanId,
  requestType,
  providerId,
  meta,
})
```

## 361.3. Precedência normativa

```text
1. route/provider semanticamente non-title (collection/person/etc.)
   → non-title

2. id prefix conhecido de collection (`tvdbc:` etc.)
   → non-title

3. request type anime.movie + item de título
   → movie

4. request type anime.series + item de título
   → series

5. meta.type movie/series em surface que realmente transporta títulos
   → correspondente

6. restante
   → unknown
```

Não fazer:

```text
meta.type === 'movie'
→ sempre aplicar movie release policy
```

## 361.4. CanonicalFilterContext

`CanonicalFilterContext.mediaType` deixa de ser authority suficiente para surfaces mistas. Ele pode
ser mantido como hint/request class, mas a decisão por item usa `EntityKindResolution`.

Se o union continuar público no código, usar ao menos:

```ts
'movie' | 'series' | 'anime.movie' | 'anime.series' | 'collection' | 'all'
```

## 361.5. Policy

```text
movie  → movie evaluator
series → series evaluator
non-title → release filter não aplicável
unknown → UNKNOWN/not-applicable → SHOW
```

`ReleaseVisibilityEntityKind`/resolver version participa da policy/filter contract quando mudar
membership observável.

---

# 362. TMDB ID Resolution V14 — mapping também é evidence correctness-critical

## 362.1. Problema concreto no snapshot

`addon/lib/id-resolver.ts` faz TMDB Find por IMDb e atualmente resolve:

```ts
const tmdbId = res.movie_results?.[0]?.id || res.tv_results?.[0]?.id || null;
```

sem condicionar essa escolha ao `type` solicitado.

TMDB `/find` procura múltiplos tipos de objeto. Um numeric TV id não pode ser usado como movie id para
`/movie/{id}/release_dates`; os namespaces numéricos não são uma prova de media kind.

## 362.2. Resultado tipado

Para Release Visibility, usar uma resolução específica:

```ts
type TmdbMovieIdResolutionState =
  | 'resolved'
  | 'not-found'
  | 'unavailable'
  | 'ambiguous';

interface TmdbMovieIdResolution {
  state: TmdbMovieIdResolutionState;
  tmdbId?: string;
  provenance:
    | 'native-movie-id'
    | 'typed-static-mapping'
    | 'typed-id-cache'
    | 'tmdb-find-imdb-movie'
    | 'other-authoritative'
    | 'none';
  observedAtMs?: number;
  stableUntilMs?: number | null;
}
```

## 362.3. Sources autorizadas a conduzir HIDE

```text
meta._tmdbId / native id
→ somente quando o producer contract prova movie-kind

typed wiki/anime/id mapping
→ somente quando mapping type é movie

TMDB /find/{imdb}?external_source=imdb_id
→ para movie, considerar SOMENTE movie_results
→ tv_results nunca é fallback de movie release evidence
```

Se houver mais de um candidate incompatível/sem prova:

```text
ambiguous → UNKNOWN → SHOW
```

Fuzzy text/title/year search:

```text
pode ajudar UI/enrichment
→ NÃO autoriza HIDE regional
```

A feature não deve esconder conteúdo com base em identidade probabilística.

## 362.4. Negative mapping freshness

`not-found` também pode envelhecer quando mapping datasets/TMDB mudam.

```text
not-found autoritativo fresh
→ UNKNOWN/SHOW
→ cursor stableUntil inclui mappingFreshUntil

mapping lookup timeout/429/storage failure
→ unavailable
→ SHOW
→ checkpointable=false

static mapping miss com próximo refresh conhecido
→ stableUntil = próximo refresh boundary

miss sem boundary comprovável
→ checkpointable=false
```

Assim, "sem TMDB mapping" deixa de ser somente um boolean e passa a contribuir corretamente para
pagination stability.

## 362.5. WorkBudget

TMDB `/find` usado por este fluxo:

```text
- consome o mesmo ReleaseEvidenceWorkBudget;
- passa pelo mesmo TmdbAdmissionController;
- usa o mesmo retry classifier;
- não ganha loop de retries oculto fora do Retry Closure Gate.
```

---

# 363. Version Registry V14 — uma única tabela copiável

A seção histórica 43 foi corrigida inline. Esta é a authority final antes do primeiro merge:

```ts
export const RAW_RELEASE_DATES_CACHE_SCHEMA = 2;
export const RAW_RELEASE_DATES_REQUEST_PROFILE_VERSION = 1;

export const RELEASE_EVIDENCE_SCHEMA = 2;
export const RELEASE_VISIBILITY_POLICY_VERSION = 1;
export const RELEASE_ENTITY_KIND_CONTRACT_VERSION = 1;
export const TMDB_ID_RESOLUTION_CONTRACT_VERSION = 1;

export const SEARCH_RESULT_CACHE_SCHEMA_VERSION = 2;
export const CATALOG_SOURCE_SIGNATURE_VERSION = 1;
export const CATALOG_FILTER_SIGNATURE_VERSION = 1;
export const PAGINATION_CONTRACT_SIGNATURE_VERSION = 1;

export const CATALOG_CURSOR_SCHEMA_VERSION = 7;
export const SEARCH_CURSOR_SCHEMA_VERSION = 3;
```

Observação:

```text
V7/V3 e raw v2 ainda não foram publicados no snapshot auditado.
A V14 está fechando o primeiro formato a ser implementado, não migrando uma V7/V3 já deployed.
```

Regras de bump:

```text
raw payload/request semantics mudaram
→ RAW schema/request profile bump

released/unreleased/unknown semantics mudaram
→ policy version bump

entity-kind applicability mudou
→ entity-kind version + filter/pagination incompatibility

TMDB identity sources que podem autorizar HIDE mudaram
→ id-resolution version + filter/pagination incompatibility quando membership puder mudar

cursor payload/storage mudou depois de deployed
→ cursor schema bump
```

Transport tuning que não altera membership determinístico não entra em filter signature; quando
budget/failure semantics mudarem a sequência observável, versionar `paginationContractSignature`.

---

# 364. TMDB Discover V14 — `with_release_type` é order-sensitive

TMDB documenta que a ordem dos release types pode mudar a data regional retornada. Logo:

```text
with_release_type=2|3
!=
with_release_type=3|2
```

para source semantics.

## 364.1. Canonicalização

```text
- preservar ordem dos tokens;
- trim/validar tokens;
- não sort genérico;
- se dedupe for aplicado, preservar first-occurrence order;
- sourceMembershipSignature usa o valor efetivo nessa ordem;
- export/import/reconstruct preserva a ordem.
```

A regra geral V10 sobre arrays order-sensitive já apontava a direção; V14 transforma
`with_release_type` em fixture explícita para impedir uma canonicalização "bonita" porém incorreta.

---

# 365. Mandatory file/occurrence map V14

Somar ao gate V13:

```text
addon/lib/getTmdb.ts
→ makeTmdbRequest
→ NON_RETRYABLE_CODES
→ 429/retry classifier
→ getApiKey
→ provider admission

addon/lib/id-resolver.ts
→ moviedb.find
→ movie_results
→ tv_results
→ mapping provenance/type

addon/lib/getSearch.ts
→ tvdbc:
→ collection result type
→ anime.movie/anime.series

addon/utils/catalogFilters.ts
→ release applicability
→ item type routing

addon/lib/catalogPagination.ts
→ cursor validUntil/stableUntil
→ checkpoint before raw mutation boundary
```

Novos terms do Occurrence Gate:

```text
movie_results
tv_results
tvdbc:
anime.movie
anime.series
NON_RETRYABLE_CODES
statusCode
isRetryable
retryDelay
requestTracker.trackProviderCall
getApiKey
TMDB_API_KEY
BUILT_IN_TMDB_API_KEY
stableUntilMs
forceUpstream
requireUpstreamRevalidation
with_release_type
```

Novos closure gates:

```text
TMDB Transport Closure Gate
→ toda chamada TMDB que possa competir pela mesma credential passa pelo admission/cooldown contract

Movie Identity Closure Gate
→ todo caminho que fornece tmdbId ao Regional evaluator possui media-kind provenance classificada

Entity Kind Closure Gate
→ todo type/id-prefix/provider class que chega ao chokepoint é movie/series/non-title/unknown classificado
```

---

# 366. Test Matrix V14 — casos adicionais obrigatórios

Continuar após a matriz V13.

## Raw mutation / cursor stability

```text
174. cursor C usa raw G100 com stableUntil=16:00; G101 normal não pode commit 10:30;
175. cursor.validUntil nunca excede menor raw stableUntil de decisões que afetaram o walk;
176. settings encurta min freshness 6h→1h sem namespace/invalidation → teste deve falhar;
177. early operator force com mutation epoch → cursor antigo rejeitado;
178. boundary stableUntil cruza antes do cursor write → checkpointable=false/retry do trecho;
179. generation mismatch detectado no mesmo request continua rederive antes de decisão;
```

## Provider admission / transport scope

```text
180. 100 requests × IDs distintos respeitam process-wide TMDB in-flight ceiling;
181. fila bounded rejeita/fail-open ao exceder deadline, sem memory growth ilimitado;
182. client abort enquanto aguarda slot remove waiter e não consome network attempt;
183. mesma credential + mesmo raw key colapsa em flight;
184. credentials A/B + mesmo movie usam transport scopes distintos e CAS global factual;
185. credential A 401 não impede B de buscar/gravar winner;
186. credential A 429 cooldown não bloqueia B;
187. built-in credential compartilhada colapsa corretamente entre users;
188. API key/fingerprint não aparece em logs/metrics/signature dumps;
```

## Retry classifier

```text
189. HTTP 500 é classificado transient e retrya somente dentro do budget configurado;
190. HTTP 503 idem;
191. HTTP 401 não retrya;
192. HTTP 404 release_dates → unavailable/not-found semantics, nunca coverage=empty;
193. 429 delta-seconds válido respeitado dentro do deadline;
194. 429 HTTP-date válido respeitado dentro do deadline;
195. 200 malformed JSON/payload nunca grava negative evidence;
196. client abort durante 5xx backoff não inicia nova tentativa;
197. maxReleaseDateAttempts inclui 5xx/429/timeout attempts sem amplificação externa;
```

## Semantic entity kind

```text
198. type=collection + id=tvdbc:123 + meta.type=movie → non-title → não aplicar Hide Unreleased;
199. request anime.movie + typed movie mapping → movie evaluator;
200. request anime.series → series evaluator, releaseRegion ignorada;
201. mixed AI Search movie → movie evaluator;
202. mixed AI Search series → series evaluator;
203. unknown/non-title → SHOW sem release evidence fanout;
204. entity-kind contract change sem filter/pagination versioning → gate falha;
```

## TMDB movie identity

```text
205. expected movie + /find movie_results=[M], tv_results=[T] → usar M;
206. expected movie + movie_results=[] + tv_results=[T] → NOT usar T; UNKNOWN/SHOW;
207. expected series + tv_results=[T] → series path, nunca movie release_dates;
208. wrong numeric namespace collision não pode produzir /movie/{tvId}/release_dates;
209. typed static anime movie mapping → resolved authoritative;
210. fuzzy title candidate → advisory only, não HIDE;
211. mapping timeout/429 → unavailable + checkpointable=false;
212. authoritative mapping not-found fresh → SHOW + cursor bounded por mappingFreshUntil;
213. mapping negative boundary cruza → cursor inválido/re-evalua;
```

## Discover ordering/version registry

```text
214. with_release_type=2|3 e 3|2 → sourceMembershipSignature diferentes;
215. export/import/reconstruct preserva 2|3 exatamente;
216. generic canonical sort que transforma 3|2 em 2|3 → test falha;
217. constants compile-time registry = raw2/evidence2/catalogCursor7/searchCursor3;
218. old literal cursor schema 6/search 2 em código novo → static guard falha;
```

---

# 367. Observabilidade V14

Adicionar baixa cardinalidade:

```text
tmdb_admission_inflight
tmdb_admission_queue_depth
tmdb_admission_total{result=admitted|deadline|aborted|queue_full}
tmdb_transport_retry_total{class=rate_limited|transient_http|timeout|network}
tmdb_transport_failure_total{class=auth|not_found|invalid_payload|other}

release_identity_resolution_total{state=resolved|not_found|unavailable|ambiguous,source=native|static|cache|tmdb_find|other}
release_entity_kind_total{kind=movie|series|non_title|unknown}
release_cursor_stability_total{result=stable|raw_boundary|mapping_boundary|mutation_epoch|transient}
```

Não usar como labels:

```text
credentialScope
movie id
imdb id
userUUID
query
releaseRegion livre
cursor key
```

Para debugging pontual, IDs técnicos podem ficar somente em logs já sujeitos à política existente,
nunca em métricas cardinality-unbounded e nunca junto de secrets.

---

# 368. Implementation Order V14 — ordem consolidada final

A ordem V13 é preservada, com quatro gates antecipados.

```text
Phase A0 — immutable snapshot + closure
1. confirmar HEAD/tree exatos;
2. Delta File Gate;
3. Occurrence Gate V14;
4. Caller-Closure Gate;
5. Evidence Ingress Gate;
6. Retry Closure Gate;
7. TMDB Transport Closure Gate;
8. Movie Identity Closure Gate;
9. Entity Kind Closure Gate;

Phase A1 — test harness/registry primeiro
10. adicionar test script/harness seguro;
11. authoritative Version Registry V14;
12. static guard contra literals/versions obsoletos;

Phase A2 — TMDB transport foundation
13. explicit retry classifier;
14. client abort vs attempt timeout;
15. TmdbAdmissionController process-wide;
16. credentialScope HMAC;
17. shared/per-scope 429 cooldown semantics;
18. unified WorkBudget integration para find + release_dates;

Phase A3 — typed movie identity
19. ReleaseVisibilityEntityKind resolver;
20. typed TmdbMovieIdResolution;
21. remover tv_results fallback para movie release authority;
22. negative mapping freshness/stability;

Phase A4 — raw factual owner
23. canonical raw request profile;
24. raw namespace v2;
25. generation allocator lifecycle-safe;
26. CAS committed winner;
27. sourceFetchedAt via storage clock;
28. raw stableUntil/mutation floor;
29. certification consumer migra para owner único;

Phase A5 — evidence authority
30. ReleaseAvailability Schema 2 final;
31. embedded/appended release_dates advisory only;
32. generation-coherence/rederive;
33. freshness + raw stability boundaries;

Phase A6 — time + policy
34. CalendarDate parser;
35. todayInTimezone formatToParts;
36. nextLocalMidnight DST/non-hour safe;
37. Worldwide golden master;
38. Regional evaluator;
39. Series evaluator;
40. non-title applicability bypass;

Phase A7 — request ownership/cache
41. RequestOwned boundary;
42. releaseEvidence component/sidecar;
43. response projection pure;
44. alias poison/concurrency tests;

Phase A8 — pagination
45. SourcePageResult adapters;
46. exact raw coordinates;
47. exhaustion vs budget split;
48. exact dedupe/CAS cursors V7+V3;
49. cursor.validUntil inclui raw/mapping stability;
50. mutation epoch validation se early-force existir;
51. no generic short-page EOF;

Phase A9 — config/provenance
52. global releaseRegion;
53. Discover provenance canônica;
54. with_release_type order-preserving round-trip;
55. import/export/share/reconstruct;
56. merged global/Worldwide only;
57. countries failure-safe UI;

Phase A10 — search
58. EffectiveSearchSourceContext;
59. neutral search cache namespace;
60. remover provider-level release policy;
61. post-cache canonical evidence completion;
62. filtered search paging adapters;

Phase A11 — performance/load
63. staged pure local prefilters;
64. benchmark evidence calls avoided;
65. burst IDs distintos contra TMDB admission;
66. Redis multi-replica/CAS/lease suite;

Phase A12 — deploy
67. backend dark deploy;
68. observability gate;
69. homogeneous fleet;
70. UI regional enable;
71. kill-switch + rollback drill.
```

---

# 369. Definition of Done V14 — gates cumulativos finais

Somar a todas as checklists anteriores:

```text
[ ] dev HEAD/tree revalidados no merge HEAD
[ ] tree traversal não truncada

[ ] Version Registry tem raw schema 2
[ ] Catalog Cursor final é V7
[ ] Search Cursor final é V3
[ ] static guard não deixa literals antigos reaparecerem em código novo

[ ] raw read expõe stableUntil/mutation boundary
[ ] cursor.validUntil <= todas as boundaries factuais usadas no walk
[ ] normal raw refresh não consegue commit antes de stableUntil
[ ] early-force, se existir, invalida cursor por correctness epoch/exact dependency
[ ] generation check + stability check são independentes e ambos passam

[ ] existe TMDB provider-level admission controller real
[ ] process-wide in-flight é bounded
[ ] queue é bounded/deadline-aware/abort-aware
[ ] request budget e provider budget são independentes
[ ] 429 respeita credential scope

[ ] factual raw key não contém API key/credential fingerprint
[ ] transport flight/cooldown usa fingerprint HMAC opaco
[ ] credential auth failure nunca grava global negative
[ ] credential A não bloqueia credential B indevidamente

[ ] 5xx retry behavior corresponde ao comentário/contrato executável
[ ] 401/403/404/422 classification explícita
[ ] client abort nunca é reclassificado como retryable timeout
[ ] malformed success nunca vira negative evidence

[ ] semantic entity-kind resolver existe
[ ] tvdbc collection encoded as movie não passa movie evaluator
[ ] anime.movie com mapping válido passa movie evaluator
[ ] non-title não causa release evidence fanout

[ ] movie TMDB mapping é media-type-safe
[ ] `/find` para movie usa somente movie_results
[ ] tv_results nunca alimenta /movie/{id}/release_dates
[ ] fuzzy title mapping nunca autoriza HIDE
[ ] mapping transient failure => checkpointable=false
[ ] negative mapping freshness contribui para cursor validity

[ ] with_release_type order é preservada em source identity
[ ] 2|3 != 3|2 em signature fixture
[ ] export/import/reconstruct mantém order

[ ] TMDB Transport Closure Gate = zero unclassified
[ ] Movie Identity Closure Gate = zero unclassified
[ ] Entity Kind Closure Gate = zero unclassified
[ ] Occurrence/Caller/Evidence/Retry gates anteriores continuam zero unclassified
```

---

# 370. Final pre-merge checklist V14

```text
[ ] branch dev ainda aponta para 6e83e22ab9de5093f9918a1871157f401feebb03
    OU todos os gates foram rerodados contra o novo merge HEAD

[ ] release/issue status revalidado
[ ] TMDB release_dates docs revalidadas
[ ] TMDB countries docs revalidadas
[ ] TMDB Discover region/with_release_type docs revalidadas
[ ] TMDB rate-limit docs revalidadas
[ ] TMDB Find-by-ID multi-type semantics revalidadas

[ ] makeTmdbRequest retry classifier tests passam
[ ] 5xx real entra na classe esperada
[ ] admission controller burst/load test passa
[ ] dual-credential isolation fixture passa

[ ] id-resolver movie-vs-tv type safety fixture passa
[ ] tvdbc collection applicability fixture passa
[ ] anime.movie applicability fixture passa

[ ] raw mutation-floor/cursor race fixture passa
[ ] early-force behavior é proibido ou invalidation-safe
[ ] mapping-negative cursor boundary fixture passa

[ ] raw/certification single-owner tests V13 continuam passando
[ ] CAS/generation/clock tests V13 continuam passando
[ ] SourcePageResult/exhaustion tests V13 continuam passando
[ ] Worldwide golden-master continua idêntico
[ ] BR/US regional matrix continua passando
[ ] Series matrix continua passando
[ ] response hygiene continua passando

[ ] frontend build
[ ] backend build
[ ] lint
[ ] test harness
[ ] Redis multi-replica suite
[ ] load benchmark
[ ] migration/rollback suite
[ ] dark deploy metrics gate
[ ] homogeneous fleet gate
[ ] UI enable
[ ] kill switch drill
[ ] rollback drill
```

---

# 371. Evidências externas/código revalidadas na V14

A reauditoria V14 confirmou contra o snapshot e documentação atual:

```text
AIOmetadata
- dev HEAD/tree exatos e tree completa 583/544/39;
- package.json continua sem test script;
- getTmdb.ts possui 3 attempts + 15s attempt timeout;
- getTmdb.ts não possui provider concurrency limiter;
- 5xx lança Error genérico e não satisfaz o retry predicate atual;
- movieReleaseDates e getMovieCertifications ainda competem pela release_dates key no snapshot;
- TVDB Collections Search pode retornar tvdbc:* com meta.type='movie';
- id-resolver TMDB Find escolhe movie_results[0] || tv_results[0] sem type gate.

TMDB
- /movie/{id}/release_dates define 1 Premiere, 2 Limited, 3 Theatrical,
  4 Digital, 5 Physical, 6 TV;
- /configuration/countries fornece ISO 3166-1 usados pelo TMDB;
- Discover `region` altera release-date semantics e `with_release_type` é order-sensitive;
- watch_region é usado com watch-provider filters e não é sinônimo de release region;
- rate limits são deliberadamente aproximados/mutáveis e 429 deve ser respeitado;
- /find/{external_id} busca múltiplos tipos de objeto, exigindo media-kind selection explícita.
```

---

# 372. O que continua impossível afirmar só com auditoria estática

Mesmo após V14, não marcar como "provado" antes de executar os gates correspondentes:

```text
- comportamento real de Redis sob failover/latência/restart;
- CAS/Lua sob múltiplas replicas reais;
- carga/queue latency do TMDB admission controller;
- distribuição real de 429 do TMDB;
- payloads live incompletos/malformados/atualizados pelo TMDB;
- custo real de mapping + release_dates fanout;
- compatibilidade de rollback com edição de config no baseline;
- todos os clientes Stremio/Jellyfin/Nuvio sob páginas transitórias;
- performance P95/P99 depois da feature;
- deployment homogêneo real.
```

Isso não é falta de cobertura do plano. É exatamente a fronteira entre **prova estática** e
**prova executável/runtime**, e cada item acima já possui gate/teste definido.

---

# 373. Resultado final da reauditoria V14

A conclusão V13 "implementation-ready" é substituída por esta formulação mais forte:

```text
V14 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,
      com static source/caller/evidence/retry/transport/identity/entity-kind closure,
      raw release facts generation-coherent e mutation-stable,
      typed movie identity,
      provider-level TMDB backpressure,
      factual filtered-pagination cursor semantics,
      e runtime/upstream/concurrency/deployment convertidos em gates executáveis.
```

## 373.1. Definição precisa de "100% coberto"

> **100% da superfície estática localizada no snapshot foi classificada ou transformada em gate de
> closure; todo boundary capaz de alterar membership, posição paginada, factual authority ou cache
> ownership possui uma autoridade definida; e tudo que depende de runtime/upstream/storage/carga
> possui teste/gate executável antes de merge/deploy.**

Não significa "TMDB jamais mudará" nem "concorrência distribuída está provada sem executar testes".
Significa que o plano não depende de essas incertezas permanecerem invisíveis.

## 373.2. Novos blockers que precisam estar resolvidos antes de código regional ser ativado

```text
P0
- CA raw mutation stability ↔ cursor validity
- CB provider-level TMDB admission
- CE semantic entity-kind resolver
- CF media-type-safe TMDB movie identity
- CG authoritative version registry

P1 correctness/resilience
- CC transport credential isolation
- CD explicit retry classifier/5xx correction
- CH with_release_type order fixture
```

Nenhum P0 pode ser adiado para "hardening pós-merge" se a UI regional já estiver ativa.

---

# 374. Checklist ultra-curto para o Codex/implementador

Antes de escrever a primeira linha funcional da #742:

```text
1. fixe o SHA/tree;
2. adicione o test harness;
3. aplique o Version Registry V14;
4. feche entity-kind + typed TMDB movie identity;
5. feche TMDB retry/admission/credential transport;
6. implemente raw owner v2 + generation/CAS/storage clock/stableUntil;
7. derive evidence V2 somente do owner autoritativo;
8. preserve Worldwide por golden master;
9. implemente Regional fail-open e Series separado;
10. neutralize search/cache policy;
11. implemente V7/V3 filtered cursors com raw/mapping stability;
12. feche config/provenance/round-trip;
13. rode closure gates + matrices + multi-replica/load;
14. dark deploy;
15. só então exponha UI regional.
```

Se qualquer passo produzir um novo caller, novo evidence ingress, novo retry layer, novo semantic type
ou novo TMDB ID source, o respectivo Closure Gate precisa falhar até a nova ocorrência ser classificada.

---

# 375. Reauditoria V15 — fechamento final sobre a V14

A V14 já estava muito próxima de um design correctness-first completo. Esta V15 revalidou o mesmo
snapshot em 2026-09-24 e encontrou **nove classes adicionais** que precisavam virar contrato explícito
antes de sustentar a alegação de cobertura estática máxima:

```text
CI.  addon/lib/configApi.js possui um caminho TMDB real fora de makeTmdbRequest(): a validação de
     API key chama api.themoviedb.org diretamente via serviceRequest(). Logo o Transport Closure Gate
     V14 não era realmente completo por construção.

CJ.  a validação de uma candidate TMDB key precisa provar exatamente a candidate; ao centralizá-la,
     getApiKey(config) não pode fazer fallback silencioso para BUILT_IN_TMDB_API_KEY e produzir falso
     "valid" para uma key inválida.

CK.  credentialScope usa HMAC, mas a V14 não define lifecycle da chave HMAC. Em multi-replica, uma
     chave aleatória/ephemeral por processo produz scopes diferentes para a mesma credential e quebra
     lease/cooldown distribuído; rotação sem protocolo produz o mesmo problema durante rolling deploy.

CL.  TmdbAdmissionController V14 é process-wide. Duas replicas com a mesma built-in credential ainda
     podem exceder em conjunto a capacidade operacional do TMDB e observar 429 em cascata. Local
     backpressure e fleet coordination são camadas diferentes.

CM.  a seção histórica de status normalization permite extrair a transformação de
     metaColdStore/stability.ts. O cold store hoje usa trim+lowercase; a visibility engine pretende
     normalizar underscore/hyphen/spacing. Compartilhar o classificador sem golden master pode alterar
     stable/frozen de metas sem relação com a #742.

CN.  typed-id-cache não é provenance. O redis-id-cache atual preserva type nos pointers, mas seu
     payload guarda apenas ids + updated_at e tem TTL genérico de 90 dias. Ele não informa se tmdb_id
     veio de native id, wiki mapping, TMDB /find, TVDB remoteIds, Cinemeta ou outra origem. Uma cache
     hit não pode elevar uma origem advisory a authority capaz de HIDE.

CO.  a V14 especifica freshness principalmente para mapping negativo. Mapping positivo que autoriza
     HIDE também pode ser corrigido/substituído e precisa de provenance, generation/revision e
     stableUntil/mutation semantics compatíveis com cursor.

CP.  a classe de regressão do issue #579 (filtered row curta) está arquiteturalmente coberta pela nova
     paginação, mas não estava ligada explicitamente ao acceptance gate da #742. O regional filter é
     mais seletivo e aumenta a chance de reproduzir exatamente essa classe de falha.

CQ.  os novos knobs de admission/distributed coordination/HMAC deixam de ser opcionais como
     documentação operacional: settings registry, .env.example, ENVIRONMENT_VARIABLES e redaction
     precisam fazer parte do mesmo change-set que introduz o transporte.
```

Snapshot V15:

```text
repository: cedya77/aiometadata
branch: dev
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue #742: OPEN, 0 comments
issue #579: CLOSED em 2026-07-16 — usado apenas como regression lineage
```

A V15 não altera o objetivo funcional da #742. Ela fecha **transport bypass, fleet scope, origin
provenance e domain coupling** que ainda poderiam permitir uma implementação aparentemente correta,
mas inconsistente sob cache antigo, múltiplas replicas ou refactor de status.

---

# 376. Regra de precedência V15

As seções 1–374 permanecem como rationale, inventário histórico, matrizes e decisões acumuladas.
As seções **375+** são normativas quando houver conflito.

A V15 prevalece especificamente sobre:

```text
- o significado de "provider-level" no admission controller;
- qualquer uso de typed-id-cache como provenance por si só;
- qualquer compartilhamento automático de status normalizer entre release visibility e cold store;
- qualquer caminho TMDB de validação/config que bypass makeTmdbRequest/TmdbTransport;
- lifecycle/rotação do credentialScope HMAC;
- mapping positivo sem stability boundary;
- acceptance de filtered page fill;
- registro/documentação dos novos settings de transporte.
```

Os números finais de schema/cursor da V14 continuam válidos **porque ainda não foram publicados**;
a V15 dobra estes novos campos/contratos no primeiro formato a ser implementado.

---

# 377. TMDB Direct-Network Closure V15 — incluir o control plane

## 377.1. Evidência concreta do snapshot

No HEAD auditado, `addon/lib/configApi.js` possui um helper próprio:

```text
serviceRequest(url, options, retries=2)
→ undici.request(... AbortSignal.timeout(5000))
→ retry próprio com sleep fixo de 500 ms
```

E a validação TMDB faz conceitualmente:

```text
https://api.themoviedb.org/3/configuration?api_key=<candidate>
→ serviceRequest(...)
```

Esse caminho:

```text
- compete pela mesma infraestrutura TMDB;
- não passa pelo TmdbAdmissionController V14;
- não usa o mesmo retry classifier;
- não compartilha o mesmo 429 cooldown;
- não usa o mesmo structured redaction;
- possui retry loop próprio;
- constrói URL secret-bearing no caller.
```

Portanto `makeTmdbRequest()` sozinho não é um chokepoint suficiente.

## 377.2. Authority recomendada

Extrair/centralizar o transporte em uma primitive que possa ser usada tanto pelo data plane quanto
pelo control plane, por exemplo:

```ts
interface TmdbTransportRequest {
  endpoint: string;                  // path relativo, nunca URL já contendo secret
  method?: 'GET' | 'POST';
  params?: Record<string, unknown>;
  credential: string;                // candidate explícita ou effective credential
  credentialMode: 'explicit' | 'effective';
  purpose:
    | 'credential-validation'
    | 'release-dates'
    | 'id-find'
    | 'metadata'
    | 'search'
    | 'configuration'
    | 'other';
  deadlineAtMs: number;
  signal?: AbortSignal;
}
```

`makeTmdbRequest()` vira um consumer dessa primitive, não a única definição de transporte.

## 377.3. Validação de credential

Criar:

```ts
validateTmdbCredential(candidateCredential, context)
```

Regras:

```text
candidateCredential é obrigatório e é a credential realmente testada;
nunca chamar getApiKey(config) dentro desse path;
nunca cair para TMDB_API_KEY/TMDB_API/BUILT_IN_TMDB_API_KEY;
401/403 → invalid;
429/408/5xx/network/timeout → transient/error, NÃO invalid;
client abort → aborted;
200 + payload esperado → valid.
```

Usar preferencialmente o endpoint TMDB dedicado a validação:

```text
GET /authentication
```

A documentação atual do TMDB o define como "Test your API Key to see if it's valid". Se a integração
mantiver v3 `api_key` como query parameter, o secret só é anexado **dentro do transport builder** depois
de structured logging; nenhum caller recebe/loga a URL final secret-bearing.

## 377.4. Budget correto

Credential validation:

```text
NÃO consome ReleaseEvidenceWorkBudget;
USA um TmdbControlPlaneBudget/deadline próprio;
PASSA pelo mesmo provider/fleet admission;
USA o mesmo retry classifier;
USA o mesmo credential-scoped 429 cooldown.
```

Assim ela compete honestamente por capacidade sem distorcer o budget de uma página de catálogo.

## 377.5. Direct TMDB Network Gate

CI obrigatório:

```text
rg -n "api\\.themoviedb\\.org|serviceRequest\\(|undici\\.request|fetch\\(" addon
```

Classificar toda ocorrência que possa atingir TMDB:

```text
central transport owner
approved wrapper
log-only/no-network
explicit no-op
test fixture
```

No snapshot atual, no mínimo:

```text
addon/lib/getTmdb.ts       → transport/data-plane owner atual
addon/lib/configApi.js      → MUST CHANGE; direct credential-validation bypass
addon/lib/getCatalog.ts     → literal de URL para logging/debug; explicit no-op ou remover literal
```

Após implementação, qualquer nova chamada real a `api.themoviedb.org` fora do owner aprovado falha CI.

---

# 378. CredentialScope HMAC V15 — lifecycle, cluster consistency e rotação

A fórmula V14 permanece correta, mas a chave usada pelo HMAC precisa de contrato operacional.

## 378.1. Configuração

Adicionar secret dedicado:

```text
TMDB_CREDENTIAL_SCOPE_HMAC_KEY
```

Propriedades:

```text
- server-only;
- sensitive=true no settings registry;
- requiresRestart=true;
- nunca entra em config de usuário;
- nunca entra em export/share/manifest;
- nunca aparece em logs/metrics/API de settings sem redaction;
- mesmo valor em todas as replicas que compartilham leases/cooldown.
```

Adicionar domínio/versionamento:

```ts
export const TMDB_CREDENTIAL_SCOPE_VERSION = 1;
const TMDB_CREDENTIAL_SCOPE_DOMAIN = 'aiometadata:tmdb-credential-scope:v1';
```

Derivação:

```text
scope = HMAC-SHA-256(derivedDomainKey, canonicalCredential)
        → >=128 bits efetivos, encoding estável
```

`canonicalCredential` inclui o tipo de autenticação quando houver mais de um modo suportado; dois
representantes diferentes não devem colidir por normalização frouxa.

## 378.2. Single-replica × distributed

```text
single replica / coordination local only
→ secret ephemeral pode ser tecnicamente aceitável para memória local,
  mas não deve ser persistido nem chamado de fleet scope.

distributed lease/cooldown/admission habilitado
→ secret cluster-stable é obrigatório.
```

Se `distributed-required` estiver ativo e a chave faltar:

```text
readiness = fail/degraded explícito
UI regional não é promovida
não gerar secret aleatório silenciosamente por replica
```

## 378.3. Fleet key consistency check

Opcionalmente materializar um identificador não reversível de consistência:

```text
scopeKeyId = HMAC(scopeKey, 'aiometadata:tmdb-scope-key-check:v1') truncado
```

Cada replica anuncia apenas `scopeKeyId` + deployment epoch em Redis/health interno.

```text
mesmo deployment + scopeKeyId divergente
→ homogeneous-fleet gate falha
→ distributed transport readiness=false
```

Nunca expor `scopeKeyId` como label pública; é somente diagnóstico interno de baixa cardinalidade por
fleet/deployment.

## 378.4. Rotação

Não rotacionar a chave HMAC de forma independente durante rolling deploy.

Opções válidas:

```text
A. drain/esperar TTL máximo de lease+cooldown e trocar homogeneamente;
ou
B. active+previous key por janela curta, com namespace versionado e dual-read controlado.
```

Rotação não altera factual raw key nem filter signature; altera apenas coordination namespace.

---

# 379. TMDB Fleet Admission V15 — local backpressure não é fleet rate control

## 379.1. Duas camadas obrigatórias quando houver múltiplas replicas

```text
LocalAdmission
→ bounded queue/memory
→ max local in-flight
→ abort/deadline

DistributedCredentialAdmission
→ coordena request starts por credentialScope entre replicas
→ shared 429 cooldown
→ crash-safe leases/tokens
```

A primeira protege processo. A segunda protege a credential compartilhada.

## 379.2. Não hardcode o "40 req/s"

A documentação TMDB continua dizendo que o limite antigo 40/10s foi removido e que existe um upper
limit aproximado na faixa de 40 req/s, sujeito a mudança.

Portanto:

```text
soft start-rate/concurrency ceiling = configurável
429 = feedback operacional autoritativo
Retry-After = respeitado
nenhum literal "40" vira correctness contract
```

## 379.3. Redis distributed mode

Quando replicas compartilham Redis + credential:

```text
credentialScope/version
→ Redis TIME
→ token/sliding-window ou primitive equivalente atômica
→ lease/permit com TTL
→ shared cooldown key
```

Requisitos:

```text
- atomicidade por Lua/MULTI primitive comprovada;
- crash não pode prender permit sem TTL;
- waiter respeita request deadline;
- abort remove wait local;
- Retry-After maior que deadline não mantém request pendurada;
- credential A não bloqueia B;
- built-in key compartilhada naturalmente coordena todos os users;
- Redis key nunca contém secret cru.
```

## 379.4. Fairness

`purpose` não deve ser apenas métrica decorativa.

A fila precisa provar ao menos:

```text
- ausência de starvation entre release-dates/id-find/metadata/search/control-plane;
- uma request não enfileira fanout ilimitado antes das demais;
- WorkBudget limita fanout individual;
- credential validation não recebe bypass de capacidade.
```

FIFO bounded é aceitável se os testes de starvation/load passarem; scheduler sofisticado não é
obrigatório sem evidência de necessidade.

## 379.5. Redis unavailable

Definir modo explícito:

```text
local-only deployment
→ continua local admission normalmente.

distributed-required + Redis coordination indisponível
→ não fingir fleet-safety;
→ emitir health/metric;
→ release evidence que não puder obter upstream dentro do budget = UNKNOWN/SHOW;
→ fresh committed evidence existente pode continuar sendo usada segundo seu próprio freshness contract.
```

Um fetch que efetivamente concluiu e passou pelos validators continua factual; falha do limiter não
transforma sucesso em evidence inválida. A degradação é de disponibilidade/backpressure, não de verdade.

---

# 380. Stability Domain Gate V15 — release status e cold store não compartilham policy

## 380.1. Estado atual que precisa ser preservado

`addon/lib/metaColdStore/stability.ts` hoje normaliza status conceitualmente como:

```text
String(status ?? '').trim().toLowerCase()
```

E usa isso para decidir `ongoing/stable/frozen` do cache.

A Release Visibility, por outro lado, precisa reconhecer variantes lexicalmente mais amplas:

```text
not_yet_aired
not-yet-aired
not yet aired
pre-production
pre production
...
```

Esses domínios têm objetivos diferentes.

## 380.2. Regra normativa

Não substituir `metaColdStore/stability.ts::normalizeStatus()` pela normalization mais agressiva da
visibility engine sem golden master específico.

Preferência:

```text
normalizeVisibilityStatus()
→ lexical normalization para release policy

normalizeStabilityStatus()
→ preserva exatamente comportamento do cold store atual
```

Se existir helper lexical compartilhado, classificadores e mappings continuam separados e o golden
master do cold store precisa provar equivalência byte/decision-level.

## 380.3. Proibições

```text
releaseRegion não entra em classifyMetaStability;
regional home evidence não torna meta frozen/stable;
UNKNOWN/UNRELEASED da visibility não altera settle/frozen tier;
status synonym novo da visibility não altera cold-store tier por acidente.
```

## 380.4. Stability-Domain Closure Gate

Classificar ao menos:

```text
addon/lib/metaColdStore/stability.ts
addon/lib/getCache.ts
addon/utils/catalogFilters.ts
addon/utils/releaseVisibility.ts          # novo
addon/utils/parseProps.js
addon/utils/recommendations/rank.ts        # release_date aqui é source/ranking-only: explicit no-op
```

Todo uso de `released/status/release_date/first_air_date` precisa declarar um domínio:

```text
visibility-policy
release-evidence
cache-stability
source-ranking/display
response-only
explicit-no-op
```

Nenhum occurrence pode migrar de domínio silenciosamente durante refactor.

---

# 381. TMDB Movie Identity V15 — cache storage não substitui origin provenance

Esta seção supersede a interpretação V14 de `typed-id-cache` como provenance suficiente.

## 381.1. Evidência concreta do snapshot

`addon/lib/redis-id-cache.ts` atualmente persiste aproximadamente:

```ts
interface IdMapping {
  tmdb_id: string | null;
  tvdb_id: string | null;
  imdb_id: string | null;
  tvmaze_id: string | null;
  updated_at: string;
}
```

com:

```text
TTL = 90 dias
pointer type-scoped
SETEX incondicional
```

Isso corrigiu a importante colisão movie/series de pointer, mas ainda **não informa a origem do
`tmdb_id`**.

`id-resolver.ts` pode agregar IDs a partir de fontes diferentes. Logo:

```text
"veio do redis-id-cache"
!=
"foi originalmente provado por uma fonte autorizada a conduzir HIDE"
```

## 381.2. Regra de authority

Para Release Visibility:

```text
cache location = storage provenance
origin provenance = factual/identity authority
```

Somente `origin provenance` pode autorizar o próximo passo de release evidence.

Novo resultado conceitual:

```ts
interface TmdbMovieIdResolution {
  state: 'resolved' | 'not-found' | 'unavailable' | 'ambiguous';
  tmdbId?: string;

  origin:
    | 'native-movie-id'
    | 'typed-static-mapping'
    | 'tmdb-find-imdb-movie'
    | 'typed-tvdb-movie-remote-id'
    | 'other-explicitly-approved'
    | 'none';

  storage: 'request' | 'release-id-cache' | 'none';

  sourceRevision?: string | null;
  observedAtMs?: number;
  mappingGeneration?: string | number;
  stableUntilMs?: number | null;
}
```

`typed-id-cache` deixa de ser um `origin`.

## 381.3. Estratégia recomendada para a primeira implementação

Não transformar o `id_map:*` genérico inteiro em correctness authority da #742.

Criar um owner/cache estreito, por exemplo:

```text
release-id-map:v1:<typed-external-key>
```

que só recebe mapping aprovado pelo `Movie Identity Closure Gate` e persiste:

```text
schema
expectedKind=movie
external id + external source
resolved tmdbId/state
origin provenance
sourceRevision/fetchGeneration
sourceFetchedAt/observedAt por clock autoritativo quando compartilhado
stableUntil
```

O `redis-id-cache` legado pode:

```text
- fornecer candidate/advisory;
- acelerar enrichment;
- continuar atendendo callers antigos;
```

mas uma entrada legacy sem origin provenance **não autoriza HIDE**.

## 381.4. TMDB Find

Para IMDb movie identity:

```text
/find/{imdbId}?external_source=imdb_id
→ considerar somente movie_results
```

A documentação TMDB confirma que `/find` retorna múltiplos tipos em uma resposta. O current
`getSearch.ts` já seleciona `movie_results` quando `type==='movie'`; esse caminho é **explicit-no-op /
regression-preserve**, não deve ser degradado ao centralizar resolver.

A documentação também mostra que TheTVDB external IDs no `/find` são suportados para TV, seasons e
episodes, não para movie. Portanto **não inventar** um `/find(... external_source=tvdb_id)` como movie
fallback. Se um TMDB movie id vier de TVDB, a authority precisa ser o remote-id do endpoint TVDB de
movie, com provenance tipada e fixture própria, ou outro source explicitamente aprovado.

## 381.5. Fuzzy/Cinemeta/advisory

```text
text/title/year fuzzy search
→ advisory only

legacy Cinemeta moviedb_id
→ advisory por default para HIDE, salvo se um contrato separado provar/verificar authority

legacy redis-id-cache hit sem origin
→ advisory only
```

Esses candidates podem reduzir trabalho de enrichment, mas não mudam `UNKNOWN → SHOW` para `HIDE`.

---

# 382. Positive Mapping Stability V15 — resolved também envelhece/muta

A V14 detalha `not-found` freshness. A mesma disciplina vale para um `resolved` usado para HIDE.

## 382.1. Invariante

```text
Se mapping M participou de uma decisão que removeu item da sequência,
o cursor não pode sobreviver a uma substituição incompatível de M.
```

## 382.2. Sources

```text
native movie tmdb id vindo da própria source page
→ estabilidade herdada da source page/page-set contract;
→ não criar cache mapping artificial.

typed static mapping
→ sourceRevision + próximo dataset refresh boundary;
→ hot swap antes da boundary exige mapping mutation epoch/invalidation.

TMDB /find authoritative
→ release-id-map owner com freshness própria;
→ retention TTL separado de consumer freshness;
→ normal refresh não substitui winner antes de stableUntil.
```

## 382.3. Legacy 90-day ID cache

O TTL genérico de 90 dias **não é consumer freshness SLA** para release hiding.

Nunca fazer:

```text
id_map entry exists
→ mapping é fresh por 90d
→ HIDE autorizado
```

Se a entrada não possui o novo envelope/provenance:

```text
revalidate authoritative source
OU
UNKNOWN → SHOW
```

## 382.4. Cursor

Adicionar ao dependency accumulator:

```text
mappingStableUntilMs
mappingMutationEpoch/revision quando aplicável
```

`cursor.validUntil` continua sendo o mínimo de todas as boundaries que podem mudar membership.

Early operator force/mapping correction antes de `stableUntil` segue a mesma escolha da raw evidence:

```text
proibir commit normal
OU
bump mutation epoch que invalida cursor antigo
```

## 382.5. CAS/provenance preservation

Se o novo release-id-map for compartilhado:

```text
- generation monotônica/CAS ou equivalente;
- loser lê committed winner;
- cache hit preserva origin provenance;
- reserialize/rewrite não rejuvenece sourceFetchedAt;
- storage location nunca substitui origin;
- conflito de dois origins incompatíveis → ambiguous/UNKNOWN até resolução autoritativa.
```

---

# 383. Filtered Page Fill V15 — regression lineage do issue #579

O issue histórico:

```text
#579 — Row not filled with filtering unreleased content
```

foi fechado em 2026-07-16. A V15 **não presume regressão atual nem reabre o issue**.

Ele é usado como fixture de produto porque documenta exatamente a falha observável que um filtro
regional mais seletivo tende a amplificar:

```text
upstream page contém N itens
→ Hide Unreleased remove vários
→ UI recebe row curta apesar de existirem itens elegíveis nas páginas seguintes
```

Acceptance obrigatório da #742:

```text
Popular - Movie / qualquer standard paginável
+ page size P
+ BR remove mais itens que Worldwide
+ existem >=P itens elegíveis no universo alcançável dentro do budget
→ retornar P itens visíveis
→ sem duplicate
→ ordem preservada
→ cursor aponta para posição raw exata após os itens realmente consumidos
```

Se o budget acabar antes de preencher:

```text
short page permitida
+ budgetExhausted=true
+ upstreamExhausted=false
+ progress checkpoint preservado
+ próximo request continua de onde parou
```

Esse fixture precisa existir para standard catalog, search paginável e pelo menos uma superfície
custom/merged representativa que use o mesmo contract.

---

# 384. Operational Settings Closure V15

Os settings criados pelo transporte deixam de ser comentário abstrato.

## 384.1. Superfícies obrigatórias

```text
addon/lib/settingsRegistry.ts
docs/ENVIRONMENT_VARIABLES.md
.env.example
configure/src/components/dashboard/DashboardSettings.tsx   # quando setting for administrável
startup validation / health
```

## 384.2. Settings mínimos

Nomes podem ser ajustados ao estilo final do projeto, mas o contrato precisa cobrir explicitamente:

```text
TMDB admission max local in-flight
TMDB admission max queue
TMDB admission wait/deadline cap
optional per-credential local ceiling
fleet/distributed admission mode: off | auto | required
fleet start-rate/permit tuning
credential-scope HMAC secret
shared 429 cooldown cap/policy
```

Não copiar "40 req/s" para default como se fosse garantia TMDB. O default final precisa ser definido
antes do merge por load test conservador + documentação.

## 384.3. Secret handling

`TMDB_CREDENTIAL_SCOPE_HMAC_KEY`:

```text
sensitive=true
requiresRestart=true
não retornado pelo settings API em claro
não incluído em diagnostics dump
não incluído em config export/import
não enviado ao frontend salvo placeholder/redacted state já suportado pelo dashboard
```

Se o settings registry permitir update runtime de secrets, esta chave deve exigir restart/homogeneous
rollout antes de o novo scope entrar em uso.

---

# 385. Mandatory File/Occurrence Map V15

Somar aos mapas V10–V14:

```text
addon/lib/configApi.js
→ testFunctions.tmdb
→ serviceRequest
→ shouldRetryApiKeyTestError
→ direct TMDB host

addon/lib/getTmdb.ts
→ transport request builder
→ credential injection/redaction
→ admission/retry/cooldown

addon/lib/redis-id-cache.ts
→ id_map:data / id_map:ptr
→ 90-day TTL
→ updated_at
→ unconditional save semantics
→ explicit advisory-only status para Release Visibility legacy entries

addon/lib/id-resolver.ts
→ every tmdbId origin
→ moviedb.find movie_results/tv_results
→ TVDB remoteIds
→ Cinemeta candidate
→ wiki/id-mapper provenance

addon/lib/getSearch.ts
→ typed IMDb /find path já seguro
→ regression-preserve/no-op classification

addon/lib/metaColdStore/stability.ts
→ normalizeStatus
→ ENDED_STATUSES
→ deriveStabilityStamp
→ classifyMetaStability

addon/utils/recommendations/rank.ts
→ release_date/first_air_date são ranking/display facts, não release policy

docs/ENVIRONMENT_VARIABLES.md
.env.example
addon/lib/settingsRegistry.ts
configure/src/components/dashboard/DashboardSettings.tsx
```

Novos terms do Occurrence Gate:

```text
api.themoviedb.org
/authentication
serviceRequest
retries =
shouldRetryApiKeyTestError
createHmac
credentialScope
TMDB_CREDENTIAL_SCOPE_HMAC_KEY
redisIdCache
id_map:data
id_map:ptr
updated_at
normalizeStatus
ENDED_STATUSES
deriveStabilityStamp
classifyMetaStability
moviedb.find
movie_results
tv_results
```

Novos closure gates:

```text
TMDB Direct-Network Gate
→ zero live TMDB caller fora do central transport sem classificação.

TMDB Credential-Validation Gate
→ candidate exata, sem fallback, retry/admission/cooldown unificados.

Credential-Scope Lifecycle Gate
→ cluster-stable secret/version/rotation/readiness definidos.

Fleet Admission Gate
→ topology multi-replica não é confundida com process-local limiter.

Mapping-Provenance Gate
→ todo tmdbId capaz de conduzir HIDE carrega origin authority; storage cache não inventa origin.

Mapping-Stability Gate
→ resolved/not-found possuem boundary/mutation semantics ou checkpointable=false.

Stability-Domain Gate
→ release visibility não muda cold-store stability por side effect.

Page-Fill Regression Gate
→ #579-class fixture continua preenchendo página quando source permite.
```

---

# 386. Version Registry V15 — adições sem alterar schemas ainda não publicados

Manter o registry V14 e acrescentar:

```ts
export const TMDB_CREDENTIAL_SCOPE_VERSION = 1;
export const TMDB_RELEASE_ID_MAP_CACHE_SCHEMA = 1;
```

Registry completo relevante continua:

```ts
export const RAW_RELEASE_DATES_CACHE_SCHEMA = 2;
export const RAW_RELEASE_DATES_REQUEST_PROFILE_VERSION = 1;
export const RELEASE_EVIDENCE_SCHEMA = 2;
export const RELEASE_VISIBILITY_POLICY_VERSION = 1;
export const RELEASE_ENTITY_KIND_CONTRACT_VERSION = 1;
export const TMDB_ID_RESOLUTION_CONTRACT_VERSION = 1;
export const TMDB_CREDENTIAL_SCOPE_VERSION = 1;
export const TMDB_RELEASE_ID_MAP_CACHE_SCHEMA = 1;
export const SEARCH_RESULT_CACHE_SCHEMA_VERSION = 2;
export const CATALOG_SOURCE_SIGNATURE_VERSION = 1;
export const CATALOG_FILTER_SIGNATURE_VERSION = 1;
export const PAGINATION_CONTRACT_SIGNATURE_VERSION = 1;
export const CATALOG_CURSOR_SCHEMA_VERSION = 7;
export const SEARCH_CURSOR_SCHEMA_VERSION = 3;
```

Por que `TMDB_ID_RESOLUTION_CONTRACT_VERSION` ainda é 1?

```text
O contrato V14 nunca foi deployed. A V15 corrige a primeira forma antes do primeiro merge.
```

O Catalog Cursor permanece V7 pelo mesmo motivo, mas sua definição V15 inclui mapping stability/
mutation dependency. Se qualquer V7 intermediário for publicado antes disso, fazer bump para V8 em vez
de reinterpretar payload já deployed.

---

# 387. Test Matrix V15 — casos 219–253

## TMDB control-plane transport

```text
219. candidate A inválida + built-in B válida → validate(A)=invalid; nunca fallback B;
220. TMDB key validation passa pelo mesmo local admission usado pelo restante do cliente;
221. validation 401/403 → invalid sem retry indevido;
222. validation 429 → transient/error + Retry-After/cooldown; não invalid;
223. validation 500/503 → unified retry classifier/budget;
224. validation client abort → zero tentativa posterior;
225. API key não aparece em URL de log/error/metric snapshot;
226. novo direct api.themoviedb.org caller fora do allowlist → CI falha;
```

## Credential scope lifecycle

```text
227. mesma credential + mesma scope key em replicas A/B → mesmo credentialScope;
228. credentials diferentes → scopes diferentes;
229. distributed-required sem HMAC key → readiness falha/degrada explicitamente;
230. rolling fleet com scopeKeyId divergente → homogeneous-fleet gate falha;
231. rotação válida não expõe secret e não reutiliza namespace ambíguo;
```

## Fleet admission

```text
232. 2 replicas × burst de IDs distintos respeitam aggregate permit/start-rate configurado;
233. 429 recebido por replica A cria cooldown visível à B para a mesma credential;
234. credential B não herda cooldown de A;
235. replica morre segurando permit → TTL libera sem intervenção manual;
236. Redis coordination indisponível em distributed-required → health explícito + no fake fleet-safe;
237. release-dates não sofre starvation indefinido por search/meta/control-plane;
```

## Mapping provenance/authority

```text
238. legacy id_map hit com tmdb_id e sem origin provenance → não autoriza HIDE;
239. legacy cache candidate + TMDB authoritative revalidation → origin novo persistido corretamente;
240. cache hit novo preserva origin original; não retorna origin='cache' como autoridade;
241. source advisory/Cinemeta candidate não vira authoritative só porque foi cacheado;
242. expected movie + generic resolver tv_results only → UNKNOWN/SHOW, nunca /movie/{tvId}/release_dates;
243. getSearch direct IMDb lookup movie continua usando movie_results somente;
244. approved typed TVDB movie remote-id fixture mantém kind/provenance explícitos;
245. conflicting authoritative origins → ambiguous/UNKNOWN até reconciliation;
```

## Positive mapping stability

```text
246. resolved mapping M1 com stableUntil T não pode ser substituído normalmente antes de T;
247. early mapping correction com mutation epoch invalida cursor antigo;
248. legacy 90d retention não é interpretada como 90d freshness;
249. sourceFetchedAt/observedAt do mapping não rejuvenescem em cache rewrite;
250. stale mapping + revalidation transient failure → UNKNOWN/SHOW + checkpointable=false;
```

## Cold-store domain isolation

```text
251. corpus de statuses atual produz exatamente os mesmos StabilityResult antes/depois do refactor;
252. visibility normaliza not_yet_aired/not-yet-aired sem alterar cold-store classifier;
253. releaseRegion/evidence regional não participa de classifyMetaStability;
```

Além desses 35 novos casos, manter **todos** os 218 testes V14 e matrizes V8–V13.

---

# 388. Page-Fill Acceptance Matrix V15

Adicionar fixtures de produto, não apenas unitárias:

```text
A. Worldwide + Popular Movie + 20 raw / 8 hidden / next page disponível
   → preencher até page size se budget permitir.

B. BR + mesmo source + mais títulos sem BR home release
   → walker continua páginas seguintes; não retorna row curta só porque primeira raw page encolheu.

C. first request skip=0 encontra zero visible em raw page 1
   → checkpoint/progress persiste; request não reinicia eternamente page 1.

D. second client request com skip=P
   → sequência equivale a consumir P itens visíveis da stream filtrada desde zero.

E. budget exhaustion antes de P
   → short page explícita, non-terminal, resume cursor salvo.

F. factual upstream exhaustion
   → terminal; não confundir com budget/deadline/429.

G. duplicates entre raw pages
   → dedupe antes de served accounting; page 2 não repete item.

H. raw/mapping boundary cruza durante fill
   → checkpoint não é emitido como estável; trecho revalida/reinicia conforme contrato.
```

O caso B é o acceptance mais próximo da necessidade real da #742.

---

# 389. Observabilidade V15

Adicionar baixa cardinalidade:

```text
tmdb_transport_path_total{purpose=credential_validation|release_dates|id_find|metadata|search|configuration|other}
tmdb_transport_direct_bypass_total              # deve permanecer 0; preferencialmente static-only

tmdb_fleet_admission_total{result=admitted|deadline|cooldown|redis_unavailable|queue_full}
tmdb_fleet_admission_wait_seconds

tmdb_scope_readiness{mode=local|distributed_required,result=ready|missing_secret|key_mismatch|redis_unavailable}

release_id_resolution_total{state=resolved|not_found|unavailable|ambiguous,origin=native|static|tmdb_find|tvdb_remote|other|none}
release_id_legacy_cache_candidate_total{result=used_advisory|revalidated|rejected}
release_id_mapping_stability_total{result=fresh|stale|mutation_epoch|no_boundary}

release_page_fill_total{result=full|budget_short|upstream_exhausted|transient}
release_page_fill_pages_consumed_bucket

release_stability_domain_regression_total        # test/diagnostic, esperado 0
```

Nunca labels:

```text
credentialScope/scopeKeyId
API key/token
movie/imdb/tmdb id
userUUID
query
raw cursor key
free-form releaseRegion
```

`scopeKeyId` pode aparecer apenas em health/debug interno redigido para comparação de fleet, não como
métrica pública de cardinalidade variável.

---

# 390. Implementation Order V15 — inserções obrigatórias na ordem V14

A ordem V14 continua válida, com estes passos antecipados/substituídos:

```text
Phase A0 — snapshot + closure
1. confirmar HEAD/tree;
2. Delta File Gate;
3. Occurrence/Caller/Evidence/Retry Gates;
4. TMDB Direct-Network Gate;
5. TMDB Credential-Validation Gate;
6. Entity Kind Gate;
7. Movie Identity Gate;
8. Mapping-Provenance Gate;
9. Stability-Domain Gate;
10. Fleet Admission topology gate;

Phase A1 — harness + authoritative registry
11. node:test harness;
12. Version Registry V15;
13. static allowlists/gates em CI;
14. cold-store stability golden master ANTES de extrair qualquer normalizer;

Phase A2 — TMDB transport foundation
15. central TmdbTransport owner;
16. explicit retry classifier;
17. candidate-exact validateTmdbCredential();
18. remover TMDB validation de configApi.serviceRequest;
19. local bounded admission;
20. credentialScope HMAC + lifecycle/readiness;
21. shared 429 cooldown;
22. distributed credential admission quando topology exigir;
23. load/fairness tests;

Phase A3 — typed release identity
24. ReleaseVisibilityEntityKind;
25. dedicated authoritative movie-id resolver;
26. tratar legacy redis-id-cache como advisory para HIDE;
27. release-id-map v1 com origin provenance/freshness/stability;
28. remover tv_results fallback de movie;
29. preservar getSearch typed /find behavior;
30. positive + negative mapping stability;

Phase A4 — raw release factual owner
31. continuar a Phase A4 V14: canonical request profile/raw v2/generation/CAS/storage clock/stableUntil;

Phase A5 — evidence/policy
32. evidence V2 somente de ingress autoritativo;
33. Worldwide golden master;
34. Regional fail-open;
35. Series evaluator sem releaseRegion;
36. status normalizers separados por domínio;

Phase A6 — cache/search/pagination
37. neutral search/cache migration;
38. V7/V3 filtered cursors;
39. mapping + raw dependencies no cursor;
40. #579-class page-fill acceptance;
41. custom/merged/Jellyfin parity;

Phase A7 — config/UI/ops
42. global releaseRegion + provenance/round-trip;
43. countries selector failure-safe;
44. settingsRegistry/.env/docs para transport;
45. secret redaction/readiness;

Phase A8 — deploy
46. full closure gates;
47. 253+ test matrix + existing suites;
48. multi-replica/load/Redis suite;
49. dark deploy;
50. homogeneous fleet + scope-key consistency;
51. kill-switch drill;
52. UI enable;
53. rollback drill.
```

Não iniciar a parte visual regional antes de A0–A6 estarem verdes em CI/integration.

---

# 391. Definition of Done V15 — adições finais

Além de todo DoD V14:

```text
[ ] configApi.js não possui request TMDB direto fora do transport owner
[ ] TMDB /authentication (ou endpoint explicitamente justificado) valida a candidate exata
[ ] invalid candidate não é mascarada por built-in fallback
[ ] validation 429/5xx não vira "invalid key"
[ ] generic configApi retry loop não duplica retries TMDB
[ ] TMDB secret nunca aparece em URL/log/metric snapshot

[ ] credentialScope HMAC secret possui configuração/lifecycle documentados
[ ] distributed-required não gera HMAC secret aleatório por replica
[ ] rolling fleet detecta/evita scope-key mismatch
[ ] shared 429 cooldown funciona cross-replica para a mesma credential
[ ] local limiter não é descrito como fleet-safe quando não é

[ ] legacy redis-id-cache NÃO é authority por storage location
[ ] origin provenance sobrevive cache round-trip
[ ] legacy mapping candidate sem provenance não autoriza HIDE
[ ] positive mapping tem freshness + stability boundary
[ ] mapping correction invalida/limita cursor corretamente
[ ] generic 90-day id cache TTL não vira release-identity freshness

[ ] cold-store stability golden master = zero regressions
[ ] visibility status normalization não muda classifyMetaStability
[ ] recommendations/rank release date occurrence classificada source-only/no-op

[ ] issue #579 regression fixture passa em Worldwide e BR regional
[ ] page fill só fica curta por factual exhaustion ou budget/transient explicitamente sinalizado

[ ] settingsRegistry contém novos knobs com sensitive/restart corretos
[ ] .env.example atualizado
[ ] docs/ENVIRONMENT_VARIABLES.md atualizado
[ ] dashboard/settings API não revela HMAC secret

[ ] Direct-Network Closure = zero unclassified
[ ] Credential-Validation Closure = zero unclassified
[ ] Mapping-Provenance Closure = zero unclassified
[ ] Mapping-Stability Closure = zero unclassified
[ ] Stability-Domain Closure = zero unclassified
[ ] Fleet Admission Closure = zero unclassified
[ ] todos os gates V14 continuam zero unclassified
```

---

# 392. Final Pre-Merge Checklist V15

```text
[ ] dev ainda é 6e83e22ab9de5093f9918a1871157f401feebb03
    OU Rebase/Delta/Occurrence/Caller/Evidence/Retry/Transport/Identity gates foram rerodados

[ ] issue #742 continua compatível com o escopo implementado
[ ] TMDB /movie/{id}/release_dates docs revalidadas
[ ] TMDB /authentication docs revalidadas
[ ] TMDB application auth docs revalidadas
[ ] TMDB /find external-id matrix revalidada
[ ] TMDB Discover region/with_release_type docs revalidadas
[ ] TMDB rate-limit docs revalidadas

[ ] direct TMDB host allowlist passa
[ ] candidate credential isolation passa
[ ] secret redaction snapshot passa
[ ] local + distributed admission suites passam
[ ] scope key consistency/rotation fixture passa

[ ] legacy id_map provenance fixture passa
[ ] positive/negative mapping stability fixtures passam
[ ] getSearch typed /find regression fixture passa
[ ] cold-store stability golden master passa

[ ] raw owner/generation/CAS/storage clock/stableUntil suites passam
[ ] Worldwide golden-master passa
[ ] Regional BR/US/GB matrix passa
[ ] Series golden/matrix passa
[ ] response hygiene passa
[ ] filtered page-fill #579-class passa
[ ] search/custom/merged/Jellyfin pagination passa

[ ] config migration/round-trip/share/rollback passa
[ ] frontend build
[ ] backend build
[ ] lint
[ ] full node:test harness
[ ] Redis multi-replica suite
[ ] load P95/P99 benchmark
[ ] dark deploy metrics gate
[ ] homogeneous fleet + credential-scope gate
[ ] UI enable
[ ] kill switch drill
[ ] rollback drill
```

---

# 393. Evidência revalidada e resultado final V15

## 393.1. Evidência de código/snapshot

Revalidado contra `dev@6e83e22ab9de5093f9918a1871157f401feebb03`:

```text
- HEAD atual continua 6e83e22;
- issue #742 está OPEN e possui 0 comments;
- configApi.js possui serviceRequest próprio e TMDB validation direta;
- getTmdb.ts continua sendo o cliente TMDB de data-plane principal;
- getSearch.ts já seleciona movie_results/tv_results de acordo com o type no seu IMDb-id search path;
- id-resolver.ts generic path ainda seleciona movie_results[0] || tv_results[0] sem expected-kind guard;
- redis-id-cache.ts é type-scoped, TTL 90d, mas não persiste origin provenance;
- metaColdStore/stability.ts usa normalização trim+lowercase própria;
- package.json continua sem test script e Node requerido é >=24 <25.
```

## 393.2. Evidência TMDB atual

Documentação revalidada em 2026-09-24:

```text
Release dates:
https://developer.themoviedb.org/reference/movie-release-dates
→ 4 Digital, 5 Physical, 6 TV.

Application authentication:
https://developer.themoviedb.org/docs/authentication-application
→ v3 aceita api_key query ou Bearer application token.

Validate Key:
https://developer.themoviedb.org/reference/authentication-validate-key
→ GET /authentication é endpoint dedicado para testar API key.

Find By ID:
https://developer.themoviedb.org/reference/find-by-id
→ uma resposta pode conter movie/tv/person/etc.; IMDb suporta movie e TV;
→ TheTVDB na matriz atual suporta TV/season/episode, não movie.

Discover Movie:
https://developer.themoviedb.org/reference/discover-movie
→ region altera release date usada;
→ ordem de with_release_type é semanticamente relevante.

Rate limiting:
https://developer.themoviedb.org/docs/rate-limiting
→ antigo 40/10s foi removido;
→ existe upper limit aproximado/mutável e 429 deve ser respeitado.
```

## 393.3. O que continua sendo gate, não alegação estática

```text
- comportamento live do TMDB para payloads/correções futuras;
- distribuição real de 429 por credential/egress;
- escolha/tuning final de soft fleet admission ceiling;
- Redis distributed admission sob failover/partição;
- HMAC secret consistency em deployment real;
- mapping corrections reais em datasets/upstreams;
- P95/P99 e fanout sob carga;
- comportamento de todos os clientes durante transients;
- rollback real de config/cache em frota.
```

## 393.4. Resultado final

```text
V15 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,
      preservando a arquitetura V14 e fechando:

      - direct/control-plane TMDB transport bypass;
      - candidate credential exactness;
      - credentialScope HMAC lifecycle/rotation;
      - process-vs-fleet admission semantics;
      - origin provenance do TMDB movie mapping;
      - positive mapping freshness/stability;
      - cold-store status-normalization isolation;
      - #579-class page-fill regression acceptance;
      - operational settings/redaction closure.
```

Definição precisa de cobertura:

> **A V15 classifica a superfície estática localizada no snapshot por domínio/authority e adiciona
> closure gates que falham quando surge caller/network ingress/mapping origin/retry/status-domain novo.
> As propriedades que dependem de runtime, upstream, Redis distribuído, carga ou deployment só são
> consideradas provadas quando os testes/gates correspondentes passam.**

Nenhuma auditoria estática pode prometer que dados externos futuros serão infalíveis. O objetivo desta
V15 é mais forte e verificável: **não deixar uma incerteza externa, um cache legado, um bypass de
transporte ou uma mudança de domínio virar silenciosamente uma decisão HIDE ou um cursor estável.**

Checklist ultra-curto V15:

```text
1. fixe HEAD/tree;
2. feche Direct-Network + control-plane TMDB;
3. feche HMAC lifecycle + fleet admission;
4. feche entity kind + authoritative movie mapping provenance;
5. trate legacy id_map como advisory para HIDE;
6. feche positive/negative mapping stability;
7. preserve cold-store stability por golden master;
8. implemente raw owner/evidence/policy V14;
9. preserve Worldwide e Series por golden master;
10. neutralize search/cache policy;
11. implemente V7/V3 cursors com raw + mapping dependencies;
12. rode #579-class page-fill acceptance;
13. feche config/provenance/settings/secrets;
14. rode 253+ testes + Redis multi-replica/load;
15. dark deploy + homogeneous fleet;
16. só então exponha Release Region;
17. kill-switch + rollback drill antes de considerar concluído.
```
---

# 394. Reauditoria V16 — Setup/Template/Provenance Closure sobre a V15

A V15 fechou os domínios de transporte TMDB, admission/fleet, mapping provenance, stability e
page-fill, mas a reauditoria final do mesmo snapshot encontrou **seis classes adicionais** na
fronteira de criação/edição/importação de catálogos pelo frontend/setup. Elas não alteram o objetivo
da #742; fecham drift de semântica entre um catálogo recém-criado, o mesmo catálogo após edit/save e
um catálogo reconstruído/importado.

```text
CR. configure/src/components/setup/SetupPage.tsx, configure/src/lib/setup/applyTemplate.ts,
    configure/src/components/setup/ImportTemplateDialog.tsx e configure/src/lib/setup/types.ts
    participam do call graph de streaming/setup templates, mas não estavam no mandatory file map.
    O Occurrence Gate por termos não basta porque esses wrappers podem transportar/perder semântica
    sem conter literalmente releaseRegion/with_release_type.

CS. configure/src/lib/setup/streaming.ts cria movie Discover com releasedOnly=true usando
    watch_region=<provider region> + with_release_type=4|5|6 + release_date.lte, porém não materializa
    params.region. Já o DiscoverBuilderDialog deriva params.region quando release type está ativo.
    Assim, create-by-setup e edit/save podem produzir source semantics diferentes para o mesmo catálogo.

CT. A V15 define region provenance, mas faltava a máquina de estados exata do editor/reconstructor.
    Um params.region derivado de watch_region/language não pode voltar do round-trip como se o usuário
    tivesse escolhido explicitamente Release Region; isso muda precedência da policy e signatures.

CU. Setup Template não é Full Config Backup. templateShare.ts usa SHARED_SETTING_KEYS e applySetup()
    aplica um subconjunto deliberado de settings. Faltava decidir normativamente se config.releaseRegion
    viaja nesse formato. Sem decisão, uma implementação pode propagar policy global por acidente ou
    fazer um template alterar a região do usuário silenciosamente.

CV. O endpoint /api/tmdb/discover/reference já devolve dois universos distintos: countries vindo de
    /configuration/countries e watchRegions vindo de /watch/providers/regions. Global Release Region
    deve usar countries; StreamingPicker deve usar watchRegions. Um não é fallback/validator do outro.

CW. Faltava um Semantic No-op Edit/Save Gate: abrir e salvar sem alteração um catálogo Discover
    gerado pelo setup/import/AI precisa preservar source membership, effective release region,
    provenance, date-token semantics, filterSignature e pagination identity.
```

Snapshot V16 continua:

```text
repository: cedya77/aiometadata
branch: dev
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue #742: OPEN, 0 comments no snapshot revalidado
entries: 583
blobs: 544
directories: 39
```

A V16 mantém a definição honesta de cobertura: a superfície estática localizada é fechada por
occurrence/caller/authority gates; comportamento de upstream, concorrência distribuída, carga e rollout
continua sendo provado somente pelos testes/gates correspondentes.

---

# 395. Regra de precedência V16

As seções 1–393 permanecem como rationale, inventário histórico e contratos acumulados. As seções
**394+** são a camada normativa mais recente quando houver conflito.

A V16 prevalece especificamente sobre:

```text
- qualquer interpretação de Setup Streaming releasedOnly=true que deixe params.region implícita;
- qualquer reconstrução que converta região derivada em discover-explicit por perda de provenance;
- qualquer regra que use watchRegions como lista/validação de Release Region global;
- qualquer regra que trate Setup Template como Full Config Backup;
- qualquer edit/save que possa alterar silenciosamente source/filter/paging semantics;
- mandatory file maps anteriores que não incluam os callers de setup adicionados nesta V16.
```

Nenhum schema/cursor publicado precisa ser renumerado por esta V16: os campos novos devem entrar no
primeiro formato ainda não publicado já definido pela V14/V15.

---

# 396. Setup Orchestration Closure Gate V16

## 396.1. Call graph concreto

No snapshot auditado:

```text
SetupPage.tsx
  ├─ buildStreamingServiceCatalogs(...)
  │    └─ configure/src/lib/setup/streaming.ts
  └─ applySetup(previous, selection)
       └─ configure/src/lib/setup/applyTemplate.ts

ImportTemplateDialog.tsx
  ├─ buildTemplateFromConfig(config, ...)
  ├─ parseTemplate(...)
  └─ fetchTemplate(...)
       └─ configure/src/lib/setup/templateShare.ts
```

Esses arquivos precisam entrar no Caller-Closure Gate mesmo quando não contêm os termos da feature.

## 396.2. Regra de closure

Para qualquer helper que cria, aplica, importa, exporta ou reconstrói catálogos/configuração:

```text
helper changed
→ enumerate all direct callers at merge HEAD
→ classify each:
   changed
   covered-by-helper
   explicit-no-op
   regression-test
→ zero unclassified
```

Adicionar explicitamente:

```text
configure/src/components/setup/SetupPage.tsx
configure/src/lib/setup/applyTemplate.ts
configure/src/components/setup/ImportTemplateDialog.tsx
configure/src/lib/setup/types.ts
```

## 396.3. Invariantes de orchestration

```text
1. SetupPage não reimplementa region derivation.
2. applySetup não transforma template settings em release policy implicitamente.
3. ImportTemplateDialog não é caminho de full-config restore.
4. buildStreamingServiceCatalogs é a authority de source params para os rows que ele cria.
5. Canonical runtime resolver continua authority da policy Hide Unreleased.
```

---

# 397. Setup Streaming V16 — materialização obrigatória de `params.region`

## 397.1. Evidência do snapshot

Hoje `configure/src/lib/setup/streaming.ts` cria movie row com:

```text
watch_region = provider.region
with_watch_providers = ...
```

E, quando `releasedOnly=true`:

```text
with_release_type = 4|5|6
release_date.lte = <dynamic today token>
```

mas não inclui `region`.

Em contraste, `DiscoverBuilderDialog.tsx` já trata release-aware movie Discover desta forma conceitual:

```text
explicit releaseRegion
  || watchRegion
  || language-derived fallback
→ params.region
```

quando release type está ativo.

## 397.2. Contrato final para Setup Streaming

Para movie:

```text
releasedOnly=false
→ watch_region=provider.region
→ NÃO criar params.region por causa da #742
→ NÃO criar release provenance

releasedOnly=true
→ watch_region=provider.region
→ with_release_type=4|5|6
→ release_date.lte=<dynamic today token>
→ params.region=provider.region
→ metadata.discover.regionProvenance = {
     source: 'watch-region-derived',
     code: provider.region
   }
```

Para series:

```text
releasedOnly=true/false
→ manter semântica atual de watch providers/status
→ NÃO criar movie releaseRegion
→ NÃO criar movie release provenance
```

A regra vale também se o setup ganhar futuramente seleção customizada de movie release types: se a
query usar `with_release_type` e a região vier do provider selector, `params.region` deve ser
materializada com provenance `watch-region-derived`.

## 397.3. Por que `watch_region` sozinho não basta

São parâmetros TMDB diferentes:

```text
region
→ seleciona contexto regional de release date no Discover

watch_region
→ restringe contexto dos watch-provider filters
```

Logo:

```text
watch_region=BR + with_release_type=4|5|6
```

não deve ser tratado como representação canônica final quando a intenção do catálogo é release-aware.
A derivação pode existir como migration de legado, mas **config nova deve materializar a intenção**.

## 397.4. Source identity

Como `params.region` muda a sequência upstream, ele participa de:

```text
canonical Discover params
sourceMembershipSignature
source page-cache identity
sourceRevision/stability
merged source identity quando o row for usado dentro de merged
```

Ele não é adicionado ao `filterSignature` apenas por existir como source param. A policy final continua
usando o CanonicalFilterContext.

---

# 398. Discover Region Provenance V16 — máquina de estados do editor

A V13 definiu os enums; a V16 define as transições para impedir privilege escalation semântica de uma
região derivada para uma região explicitamente escolhida.

## 398.1. Derivação ao criar/salvar no Discover Builder

Para movie Discover com release-type semantics:

```text
if user selected releaseRegion explicitly:
  params.region = releaseRegion
  provenance.source = discover-explicit
  provenance.code = releaseRegion

else if watchRegion exists:
  params.region = watchRegion
  provenance.source = watch-region-derived
  provenance.code = watchRegion

else if valid defaultRegionFromLanguage exists:
  params.region = defaultRegionFromLanguage
  provenance.source = language-derived
  provenance.code = defaultRegionFromLanguage

else:
  params.region absent
  provenance absent
```

Sem release-type semantics:

```text
watchRegion continua watch/provider context;
não criar movie release provenance apenas por watch_region existir.
```

## 398.2. Reconstrução para form state

Regra obrigatória:

```text
provenance=discover-explicit
→ formState.releaseRegion = code

provenance=watch-region-derived
→ formState.releaseRegion NÃO é promovido a explicit
→ restaurar watchRegion normalmente
→ manter provenance persistida

provenance=language-derived
→ formState.releaseRegion NÃO é promovido a explicit
→ manter provenance persistida

provenance=legacy-normalized
→ restaurar de modo que save sem edição não eleve authority
```

Portanto é proibido implementar genericamente:

```text
if (params.region) formState.releaseRegion = params.region
```

sem consultar provenance.

Esse cuidado vale especialmente para:

```text
addon/lib/collectionBuilder/catalogReconstruction.ts
addon/utils/ai-catalog-config-builder.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
```

## 398.3. Transições por ação explícita do usuário

```text
derived → usuário escolhe Release Region US
→ discover-explicit/US

discover-explicit → usuário limpa Release Region, watchRegion=BR e release-aware=true
→ watch-region-derived/BR

discover-explicit → usuário limpa Release Region, sem watchRegion, language fallback válido
→ language-derived/<code>

discover-explicit → usuário limpa Release Region, sem derivação válida
→ params.region/provenance removidos
```

Uma simples abertura/fechamento/save sem edição **não conta** como escolha explícita.

## 398.4. Policy authority continua restrita

```text
discover-explicit
→ pode sobrescrever global

watch-region-derived
→ pode sobrescrever global somente no Discover release-aware conforme contrato da feature

language-derived
→ NÃO transforma global Hide Unreleased em regional por acidente

invalid/mismatched provenance
→ fallback seguro global/Worldwide + metric/warning
```

---

# 399. Setup Template V16 — fronteira com Full Config Backup

## 399.1. Decisão normativa

`aiometadata.setupTemplate` continua sendo template de setup, não backup integral de preferências do
usuário. Portanto, nesta feature:

```text
config.releaseRegion global
→ NÃO é exportada/importada por Setup Template v1 por padrão
→ NÃO é adicionada a SHARED_SETTING_KEYS apenas para #742
→ applySetup preserva previous.releaseRegion
```

Isto é coerente com o formato atual, que já não transporta genericamente todas as flags pessoais de
filtro.

O owner do round-trip de `config.releaseRegion` global continua sendo:

```text
Full Config export/import
SaveContext/config API/database
configuration backup/restore
```

já cobertos pelas seções V11/V12.

## 399.2. O que o Setup Template DEVE transportar

Catálogos portáveis carregados pelo template devem preservar a semântica **do próprio catálogo**:

```text
metadata.discover.params.region
metadata.discover.regionProvenance
with_release_type
release_date.*
watch_region
formState necessário para edição idempotente
```

Assim:

```text
global policy do receptor
→ permanece do receptor

source semantics explícitas/derivadas do catálogo compartilhado
→ permanecem no catálogo
```

## 399.3. Se o produto quiser compartilhar releaseRegion global no futuro

Isso exige decisão separada:

```text
TEMPLATE_VERSION bump ou regra backward-compatible explicitamente documentada
+ UI copy dizendo que preferências de filtro serão importadas
+ applySetup support
+ export/import fixtures
+ precedence entre previous config e template setting
```

Não adicionar silenciosamente ao formato v1.

---

# 400. Country Authority Split V16 — `countries` ≠ `watchRegions`

O endpoint existente `/api/tmdb/discover/reference` já agrega:

```text
countries
← TMDB /configuration/countries

watchRegions
← TMDB /watch/providers/regions
```

São datasets com responsabilidades diferentes.

## 400.1. Global Release Region picker

Deve usar:

```text
countries
```

porque o TMDB define `/configuration/countries` como a lista ISO 3166-1 usada no serviço.

Nunca validar `config.releaseRegion` pela existência em `watchRegions`.
Um país pode ser válido para release metadata mesmo sem possuir cobertura de watch providers equivalente.

## 400.2. Streaming Picker

Continua usando:

```text
watchRegions
```

pois a pergunta desse selector é disponibilidade/contexto de providers, não validade de release country.

## 400.3. Failure isolation

```text
countries falhou
→ Worldwide continua selecionável
→ releaseRegion persistida continua visível/preservada
→ save não apaga o valor

watchRegions falhou
→ streaming picker mostra erro/fallback próprio
→ NÃO altera config.releaseRegion

countries carregou e watchRegions falhou
→ global release picker continua funcional

watchRegions carregou e countries falhou
→ NÃO usar watchRegions como substituto silencioso do global picker
```

Backend permanece authority final de normalização/validação; a UI list não é proof de validade.

---

# 401. Semantic No-op Edit/Save Gate V16

Round-trip sintático não basta. O projeto precisa provar **equivalência semântica**.

Para cada fixture Discover relevante:

```text
create/import/reconstruct
→ capture CanonicalSourceDefinition
→ capture sourceMembershipSignature
→ capture CanonicalFilterContext/effective release region
→ capture filterSignature
→ capture paginationContractSignature
→ open editor
→ save sem alteração
→ recompute
```

Critério:

```text
source definition equivalente
sourceMembershipSignature idêntica
release provenance idêntica
EffectiveReleaseRegion idêntica
filterSignature idêntica
paginationContractSignature idêntica
```

Exceto quando ocorrer uma migration canônica intencional e versionada; nesse caso o teste deve provar
que a primeira normalização é idempotente:

```text
legacy → canonical1 → save → canonical2
canonical1 == canonical2
```

Fixtures mínimas:

```text
1. explicit region BR + 4|5|6
2. watch-derived BR + releasedOnly
3. language-derived region + release type
4. legacy watch_region + 4|5|6 sem region
5. no region / Worldwide
6. setup-generated streaming movie row
7. AI-generated Discover row
8. shared/imported catalog
```

---

# 402. Mandatory File/Occurrence Map V16 — adições finais

Somar aos mapas V15:

## Must-audit / regression fixture obrigatório

```text
configure/src/components/setup/SetupPage.tsx
configure/src/lib/setup/applyTemplate.ts
configure/src/components/setup/ImportTemplateDialog.tsx
configure/src/lib/setup/types.ts
```

## Must-change ou strongly expected

```text
configure/src/lib/setup/streaming.ts
addon/lib/collectionBuilder/catalogReconstruction.ts
addon/utils/ai-catalog-config-builder.ts
configure/src/components/sections/DiscoverBuilderDialog.tsx
```

Os três últimos já estavam em mapas anteriores; a V16 acrescenta o requisito específico da máquina
de estados de provenance/idempotência.

## Occurrence/caller terms adicionais

```text
buildStreamingServiceCatalogs
applySetup
buildSetupCatalogs
buildTemplateFromConfig
parseTemplate
fetchTemplate
SHARED_SETTING_KEYS
TEMPLATE_VERSION
ConfigTemplate
SetupSelection
watchRegions
countries
regionProvenance
releaseRegion
releasedOnly
with_release_type
```

Gate final:

```text
Setup-Orchestration Closure = zero unclassified callers
Template-Policy Closure = zero ambiguous propagation of global release policy
Region-Domain Closure = zero countries/watchRegions semantic substitution
Edit-Save Idempotence Closure = zero unexplained signature/provenance drift
```

---

# 403. Test Matrix V16 — casos 254–277

Adicionar aos 253 casos acumulados:

```text
254. buildStreamingServiceCatalogs possui somente SetupPage como caller direto no snapshot e todos
     os callers futuros precisam ser classificados pelo Setup-Orchestration Gate;

255. streaming movie BR + releasedOnly=false → watch_region=BR; params.region ausente;
256. streaming movie BR + releasedOnly=true → region=BR + with_release_type=4|5|6 +
     watch-region-derived provenance;
257. streaming series BR + releasedOnly=true → nenhuma movie releaseRegion/provenance;
258. streaming movie com custom home release types + watch region → materializa region/provenance;

259. Discover explicit US + watch BR + release-aware → region=US/discover-explicit;
260. Discover sem explicit + watch BR + release-aware → region=BR/watch-region-derived;
261. Discover sem explicit/watch + pt-BR fallback + release-aware → region=BR/language-derived;
262. derived watch-region open/save no-op → continua watch-region-derived, não discover-explicit;
263. language-derived open/save no-op → continua language-derived;
264. derived → usuário escolhe US → discover-explicit/US;
265. explicit US → usuário limpa, watch BR presente → watch-region-derived/BR;
266. provenance.code != params.region → provenance rejeitada + safe fallback;

267. Setup Template export com global releaseRegion=BR → v1 não exporta global releaseRegion;
268. Setup Template import sobre previous.releaseRegion=US → permanece US;
269. setup apply/replace sem template policy → previous.releaseRegion preservada;
270. Full Config export/import com releaseRegion=BR → continua BR;
271. shared Discover catalog preserva params.region + regionProvenance independentemente da policy global;

272. Global Release Region options vêm de reference.countries, não reference.watchRegions;
273. StreamingPicker options continuam vindo de watchRegions;
274. countries fetch failure não apaga releaseRegion persistida;
275. watchRegions failure não altera global releaseRegion;

276. setup-generated release-aware row: create → open → save no-op mantém source/filter/paging signatures;
277. issue #742 end-to-end: filme com home release fora de BR, sem 4/5/6 BR fresh-confirmed,
     em catálogo setup streaming BR → HIDE; Worldwide golden-master permanece inalterado.
```

A suite acumulada passa a ser descrita como **277+ casos**, sem contar parametrizações internas,
property/fuzz cases, multi-replica/load e suites preexistentes do projeto.

---

# 404. Definition of Done V16 — adições finais

Além de todo DoD V15:

```text
[ ] Setup-Orchestration Closure = zero unclassified
[ ] SetupPage/applyTemplate/ImportTemplateDialog/setup types classificados

[ ] setup streaming movie releasedOnly=true materializa params.region
[ ] setup streaming provenance = watch-region-derived
[ ] releasedOnly=false não promove watch_region para release region
[ ] series setup nunca recebe movie releaseRegion

[ ] Discover Builder escreve provenance conforme origem real
[ ] reconstruction não converte derived region em discover-explicit
[ ] AI config builder é provenance-aware ao reconstruir formState.releaseRegion
[ ] derived → explicit e explicit → derived possuem testes de transição

[ ] Setup Template v1 não altera config.releaseRegion global
[ ] Full Config backup/import continua preservando config.releaseRegion
[ ] shared catalog preserva sua própria discover region/provenance

[ ] global Release Region picker usa countries
[ ] StreamingPicker usa watchRegions
[ ] falha de um dataset não faz fallback silencioso para o outro

[ ] Semantic No-op Edit/Save Gate passa para setup/AI/import/legacy fixtures
[ ] sourceMembershipSignature permanece idêntica em no-op edit/save
[ ] filterSignature permanece idêntica em no-op edit/save
[ ] paginationContractSignature permanece idêntica em no-op edit/save
[ ] provenance/effective region permanecem idênticas em no-op edit/save

[ ] 277+ test matrix passa
[ ] todos os gates V15 continuam zero unclassified
```

---

# 405. Final Pre-Merge Checklist V16

```text
[ ] dev ainda é 6e83e22ab9de5093f9918a1871157f401feebb03
    OU todos os closure gates V15 + V16 foram rerodados no novo merge HEAD

[ ] issue #742 ainda é compatível com o escopo
[ ] TMDB release-dates/discover/countries/watch-regions docs revalidadas

[ ] buildStreamingServiceCatalogs materializa region somente no caso release-aware correto
[ ] provenance source calculada pela origem real, não inferida após perda de contexto
[ ] create-by-setup == edit/save semântico
[ ] create-by-AI/import == edit/save semântico

[ ] Setup Template v1 policy boundary passa
[ ] Full Config round-trip passa
[ ] country/watch-region domain isolation passa

[ ] V15 transport/admission/mapping/stability/page-fill gates passam
[ ] Worldwide golden-master passa
[ ] Regional BR/US/GB passa
[ ] Search/custom/merged/Jellyfin pagination passa
[ ] response hygiene passa
[ ] Redis multi-replica/load passa
[ ] dark deploy/homogeneous fleet/kill switch/rollback drill passam
```

---

# 406. Evidência revalidada e resultado final V16

## 406.1. Evidência adicional de código

Revalidado no snapshot `dev@6e83e22ab9de5093f9918a1871157f401feebb03`:

```text
- configure/src/lib/setup/streaming.ts:
  releasedOnly movie escreve with_release_type=4|5|6 + release_date.lte,
  mas não escreve params.region;

- configure/src/components/sections/DiscoverBuilderDialog.tsx:
  quando movie usa release type, deriva effective region de explicit releaseRegion,
  depois watchRegion, depois language fallback, e materializa params.region;

- configure/src/components/setup/SetupPage.tsx:
  é o caller de buildStreamingServiceCatalogs e applySetup;

- configure/src/lib/setup/applyTemplate.ts:
  começa com next={...previous}, aplica settings selecionados e substitui catalogs;
  portanto global releaseRegion pode e deve permanecer do receptor no Setup Template v1;

- configure/src/lib/setup/templateShare.ts:
  usa SHARED_SETTING_KEYS explícita e releaseRegion não faz parte dela no snapshot;

- configure/src/components/setup/ImportTemplateDialog.tsx:
  é o caller de buildTemplateFromConfig/parseTemplate/fetchTemplate;

- addon/index.ts /api/tmdb/discover/reference:
  retorna countries de /configuration/countries e watchRegions de /watch/providers/regions;
  os dois datasets já existem separadamente no mesmo endpoint.
```

## 406.2. Evidência TMDB que fundamenta a correção

```text
/movie/{id}/release_dates
→ tipos 4 Digital, 5 Physical, 6 TV.

/discover/movie
→ region faz a query usar release date regional;
→ with_release_type pode ser usado em conjunto com region;
→ a ordem dos release types é semanticamente relevante;
→ watch_region é documentado para filtros de watch providers, não como sinônimo de region.

/configuration/countries
→ lista de países ISO 3166-1 usada pelo TMDB.

/watch/providers/regions
→ lista de países onde o TMDB possui dados de watch providers.
```

## 406.3. Resultado final

```text
V16 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,
      preservando todo o fechamento V15 e acrescentando:

      - Setup-Orchestration Caller Closure;
      - materialização determinística de params.region no Setup Streaming release-aware;
      - provenance state machine explícita no editor/reconstruction;
      - fronteira Setup Template × Full Config Backup;
      - separação countries × watchRegions;
      - Semantic No-op Edit/Save Gate;
      - 277+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V16:

> **A V16 cobre estaticamente o snapshot por authority, occurrence e caller closure e fecha também os
> caminhos de criação/aplicação/importação de setup que podem transportar semântica sem conter os termos
> centrais da feature. Nenhuma afirmação sobre upstream/runtime/distributed behavior é promovida a fato
> sem o gate executável correspondente.**

Checklist ultra-curto V16:

```text
1. fixe HEAD/tree;
2. execute todos os gates V15;
3. feche Setup-Orchestration callers;
4. materialize setup movie release-aware region + provenance;
5. implemente provenance state machine no builder/reconstruction/AI;
6. mantenha Setup Template v1 livre de policy global implícita;
7. separe countries de watchRegions;
8. prove no-op edit/save por signatures e effective context;
9. rode 277+ casos + golden masters + Redis/load;
10. dark deploy + homogeneous fleet;
11. só então habilite UI regional;
12. execute kill-switch e rollback drill.
```
---

# 407. Reauditoria V17 — Effective TMDB Discover Source Context Closure sobre a V16

A V16 fechou setup/template/provenance, mas a reauditoria do mesmo snapshot encontrou uma classe
adicional **concreta no runtime do TMDB Discover**: o conjunto de parâmetros usado para assinatura/cache
é resolvido em um momento diferente do conjunto de parâmetros efetivamente enviado ao TMDB.

Isso não invalida a arquitetura anterior; pelo contrário, confirma o invariante V9 de que
`sourceMembershipSignature` deve representar os parâmetros efetivos da fonte. A V17 transforma esse
invariante, que antes estava genérico, em **closure executável do pipeline real**.

Novos blockers cumulativos:

```text
CX. addon/lib/discoverCatalogSignature.ts calcula discoverSig somente sobre
    metadata.discover.params/discoverParams persistidos e o aplica antes da execução do provider.
    Em seguida, addon/lib/getCatalog.ts resolve date tokens e sanitizeTmdbDiscoverParams() pode
    adicionar, remover ou reescrever parâmetros. Logo o objeto assinado no cache legado não é,
    necessariamente, o request semanticamente efetivo.

CY. sanitizeTmdbDiscoverParams() possui dependências implícitas não materializadas no objeto persistido:
    - page;
    - request language;
    - config.includeAdult fallback;
    - sort_by default;
    - remoção de parâmetros inválidos/incompatíveis;
    - remoção de with_watch_providers quando watch_region falta;
    - conversão primary_release_date.* → release_date.* quando with_release_type está ativo;
    - derivação de region a partir do sufixo de language quando with_release_type existe e region falta.
    Qualquer dependência que possa alterar membership/order/payload não pode ficar invisível à
    source/cache/paging identity.

CZ. A derivação runtime `with_release_type + region ausente → region = language country` ocorre hoje
    dentro do sanitizer, depois que a provenance já foi perdida. Isso permite uma região efetiva de
    source sem `regionProvenance`, impedindo distinguir explicit/watch/language/legacy na camada de
    policy e nos logs. Sanitizer não pode criar authority sem provenance.

DA. A V16 materializa region para configs novas do Setup/Builder, mas legacy/imported configs ainda
    podem chegar ao runtime com `with_release_type` e sem `region`. Portanto a correção não pode depender
    de "todo config novo já vem materializado"; precisa existir runtime normalization idempotente,
    provenance-aware e sem side-effect de write.

DB. Route, merged-catalog source reads e comprehensive warmer constroem/consomem cache identity em
    caminhos diferentes. O mesmo TMDB Discover precisa resolver o MESMO Effective Source Context em
    todos eles. Um helper exclusivo da route não fecha caller parity.

DC. Dynamic date tokens possuem deliberadamente identidade persistida diferente do valor resolvido.
    A V17 preserva isso, mas exige que o valor resolvido gere uma revision/boundary de snapshot
    observável. Um cache/cursor não pode atravessar a mudança do request efetivo apenas porque
    `discoverSig` continuou igual.

DD. O contrato de cache precisa proibir under-partitioning:
    se duas execuções podem enviar requests semanticamente diferentes capazes de alterar
    membership/order/payload, elas não podem compartilhar uma identidade correctness-critical sem
    uma boundary/revision que prove equivalência temporal.
```

O snapshot auditado continua:

```text
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
tree: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
entries: 583
blobs: 544
directories: 39
issue #742: open / 0 comments no snapshot revalidado
```

Não houve drift de `dev` entre V16 e V17. A V17 é, portanto, uma reauditoria sem rebase delta.

---

# 408. Regra de precedência V17

As seções 1–406 permanecem como trilha acumulada V8→V16.

Para qualquer conflito relacionado a:

```text
TMDB Discover effective params
stored params × effective params
runtime region derivation
legacy region migration
hidden provider fallbacks
source request identity
discoverSig compatibility
sourceMembershipSignature
page-cache identity
sourceSnapshotRevision
dynamic date token revision
route/merged/warmer parity
```

**as seções 407+ prevalecem**.

A V17 NÃO revoga:

```text
- Worldwide golden-master;
- tri-state release evidence;
- regional CalendarDate semantics;
- evidence freshness/CAS/generation;
- Search neutralization;
- filtered pagination contracts;
- provenance V13/V16;
- setup materialization V16;
- transport/fleet/mapping/stability V15;
- todos os rollout/rollback gates anteriores.
```

---

# 409. Effective TMDB Discover Source Context — authority única

Criar uma authority única, conceitualmente:

```ts
interface EffectiveTmdbDiscoverSourceContext {
  catalogType: 'movie' | 'series';

  /**
   * Configuração persistida/canônica. Date tokens continuam tokens.
   * Nunca é mutada in-place.
   */
  storedParams: Readonly<Record<string, unknown>>;

  /**
   * Definição efetiva da fonte depois de defaults/migration/sanitization
   * semanticamente relevantes, mas preservando a identidade dos date tokens.
   * É a base da strong source identity.
   */
  definitionParams: Readonly<Record<string, unknown>>;

  /**
   * Request exato a ser enviado neste sample/request.
   * Date tokens já resolvidos; page já aplicada.
   */
  requestParams: Readonly<Record<string, unknown>>;

  /**
   * Provenance da region quando existir.
   */
  releaseRegionProvenance?: DiscoverRegionProvenance | null;

  /**
   * Revision concreta do request temporal atual.
   * Ex.: valores resolvidos de __tmdb_date__.
   */
  sourceSnapshotRevision?: string | null;

  /**
   * Primeira boundary em que requestParams pode mudar só pela passagem do tempo.
   */
  stableUntil: Date | null;

  /**
   * Dependências não persistidas que foram materializadas.
   * Somente ids/valores não-secretos.
   */
  materializedDependencies: Readonly<{
    language?: string;
    includeAdult?: boolean;
    genre?: string | null;
    legacyRegionSource?: DiscoverRegionProvenanceSource | null;
  }>;
}
```

Nome recomendado:

```text
resolveEffectiveTmdbDiscoverSourceContext(...)
```

ou equivalente.

O nome é menos importante que a regra:

> **nenhum caller pode reconstruir sozinho a semântica efetiva do TMDB Discover.**

---

# 410. Ordem canônica do pipeline TMDB Discover

A ordem precisa ser única e testada:

```text
1. clone stored params
2. normalize legacy shape
3. resolve/validate persisted region provenance
4. aplicar migration runtime de legacy release-aware region, sem write lateral
5. materializar defaults externos que alteram request/source semantics
6. canonicalizar tipos/arrays/order-sensitive fields
7. validar allowed params por media type
8. aplicar transforms determinísticos do TMDB Discover
9. construir definitionParams
10. calcular strong sourceMembershipSignature
11. resolver dynamic date tokens com RequestEvaluationClock
12. construir sourceSnapshotRevision + stableUntil
13. adicionar page
14. construir requestParams
15. usar requestParams no network call
16. usar a MESMA authority no route cache, merged source, warmer, logs e metrics
```

Importante:

```text
discoverSig legado
→ pode continuar como compatibility/debug migration key

discoverSig legado
→ NÃO é authority correctness-critical

sourceMembershipSignature
→ deriva do contexto canônico V17

requestParams
→ não pode sofrer nova mutation semanticamente relevante depois da signature/context resolution
```

Se algum adapter precisar remover um parâmetro por limitação específica do endpoint, essa transformação
deve acontecer **antes** de congelar o contexto ou produzir uma sub-revision explicitamente versionada.

---

# 411. Hidden Dependency Closure — matriz normativa

Toda dependência abaixo precisa estar explícita:

| Dependência | Pode alterar | Tratamento V17 |
|---|---|---|
| `params.region` | membership/release-date semantics | definition identity + provenance |
| `watch_region` | provider membership | definition identity; nunca policy por si |
| `with_release_type` | membership/order/release date | order-sensitive canonical identity |
| `language` | payload e, em legado, region derivada | definition identity quando efetivo |
| `config.includeAdult` fallback | membership | materializar antes da source identity |
| `genre` injetado pela route | membership | source variant/identity |
| `sort_by` rewrite | order | canonical effective definition |
| `with_watch_providers` removido sem `watch_region` | membership | identity reflete o request efetivo |
| dynamic date token | membership com tempo | token na definition + revision/boundary do valor resolvido |
| `page` | posição, não definição global | page-cache coordinate; não policy |
| media type | endpoint/semantics | source identity |
| API key/secret | transporte, não semântica | NUNCA em identity/log |

Invariante de não-under-partitioning:

```text
Se A e B podem produzir request/source semanticamente diferente
capaz de alterar membership, order ou cached payload:

  correctnessIdentity(A) != correctnessIdentity(B)

OU

  a diferença é representada por sourceSnapshotRevision/stableUntil
  e o read-time validator impede reutilização fora da equivalência.
```

Over-partitioning temporário pode ser aceito como custo de performance; under-partitioning não.

---

# 412. Runtime Region Derivation Closure — retirar authority do sanitizer

O comportamento atual:

```text
with_release_type presente
+
params.region ausente
+
language=pt-BR
→ sanitizer cria region=BR
```

não deve continuar como regra implícita solta.

A V17 exige:

```text
resolveLegacyDiscoverReleaseRegion(...)
```

ou a mesma lógica dentro da authority da seção 409.

Precedência para movie Discover release-aware:

```text
1. params.region + provenance válida
   → preservar provenance

2. params.region sem provenance em config legado
   → validar
   → source='legacy-normalized'
   → sem write lateral

3. region ausente + watch_region válido + release-aware inequívoco
   → runtime effective region = watch_region
   → source='legacy-normalized' para config antigo
   → configs novos do Setup continuam source='watch-region-derived'

4. region/watch ausentes + language possui country válido + legacy behavior exige fallback
   → runtime effective region = language country
   → source='language-derived'

5. restante
   → region ausente
```

Separar duas perguntas:

```text
A. qual region o SOURCE TMDB Discover efetivamente usa?
B. qual releaseRegion a POLICY Hide Unreleased está autorizada a usar?
```

Elas podem diferir.

`language-derived` continua sem autoridade automática para transformar a policy global Worldwide em
regional. A fonte pode ter um legacy regional prefilter sem conceder override de policy.

O sanitizer passa a ser uma função mecânica:

```text
validate/coerce/remove unsupported params
```

e não um local que inventa provenance/authority.

---

# 413. Definition Params × Request Params × Temporal Revision

A V17 formaliza três objetos diferentes.

## 413.1. `storedParams`

Exemplo:

```json
{
  "with_release_type": "4|5|6",
  "watch_region": "BR",
  "release_date.lte": "__tmdb_date__:today:to"
}
```

É configuração; não é request final.

## 413.2. `definitionParams`

Após normalização/migration:

```json
{
  "with_release_type": "4|5|6",
  "watch_region": "BR",
  "region": "BR",
  "release_date.lte": "__tmdb_date__:today:to",
  "include_adult": false,
  "language": "pt-BR",
  "sort_by": "popularity.desc"
}
```

Pode manter token temporal não resolvido.

É material para:

```text
sourceMembershipSignature
diagnostic source context
merged source identity
```

## 413.3. `requestParams`

No dia 2026-09-24, page 2:

```json
{
  "with_release_type": "4|5|6",
  "watch_region": "BR",
  "region": "BR",
  "release_date.lte": "2026-09-24",
  "include_adult": false,
  "language": "pt-BR",
  "sort_by": "popularity.desc",
  "page": 2
}
```

É o objeto efetivamente enviado ao TMDB.

## 413.4. `sourceSnapshotRevision`

Para dynamic token:

```text
sha256(canonical({
  release_date.lte: "2026-09-24",
  ...
}))
```

ou outra revision forte equivalente.

Não precisa virar parte permanente da source-definition signature se o design usar stability boundary,
mas precisa impedir que página/cursor produzidos sob `2026-09-23` sejam tratados como o mesmo snapshot
válido após a boundary de `2026-09-24`.

---

# 414. Date-token contract V17 — preservar a intenção correta do código atual

`discoverCatalogSignature.ts` deixa date tokens sem resolver de propósito.

Essa decisão continua válida **somente** se:

```text
- RequestEvaluationClock é único por request;
- token resolution usa timezone canônico;
- sourceSnapshotRevision identifica o valor resolvido OU
  page cache stableUntil/PTTL é clampado à boundary;
- cursor.validUntil <= dynamic-token boundary;
- comprehensive warmer usa o mesmo logical clock/context;
- read-time validation rejeita artifact além da boundary;
- rollback não interpreta revision V17 como snapshot antigo.
```

Nunca:

```text
stored token está igual
→ request efetivo está necessariamente igual
```

Testar DST e offsets não inteiros conforme gates anteriores.

---

# 415. Route × Merged × Warmer parity

A mesma fonte TMDB Discover pode ser lida por superfícies diferentes.

Obrigatório:

```text
addon/index.ts
  route page cache

addon/lib/getCatalog.ts
  direct provider execution
  merged source fetches

addon/lib/comprehensiveCatalogWarmer.js
  warmed page writes

addon/lib/cacheWarmer.js
  synthetic/base warm behavior quando aplicável
```

Todos precisam convergir para:

```text
mesmo definitionParams
mesmo sourceMembershipSignature
mesmo temporal revision/boundary
mesma page coordinate
mesmo effective region/provenance
```

O warmer não pode escrever:

```text
key baseada em stored discoverSig
+
payload obtido com hidden effective params diferentes
```

que depois seja consumida por uma route com outro hidden context.

Gate:

```text
Effective-TMDB-Discover-Source-Context Closure
= zero TMDB Discover caller correctness-critical que construa effective params fora da authority comum
```

---

# 416. Cache-key compatibility e rollout

Durante migration:

```text
legacy discoverSig
→ dual-read somente se artifact puder ser provado semanticamente compatível

V17 strong identity
→ single-write

artifact legado sem informação suficiente para provar hidden dependencies
→ MISS conservador
```

Não tentar "adivinhar" compatibilidade de:

```text
region ausente
with_release_type presente
language/includeAdult externos desconhecidos
```

Rollout recomendado:

```text
Phase A
→ calcular context/signatures em shadow mode
→ comparar legacy cache key × V17 effective context
→ métricas de mismatch sem alterar resposta

Phase B
→ V17 single-write
→ optional safe dual-read apenas para classes provadamente equivalentes

Phase C
→ parar legacy reads após TTL máximo/cleanup window
```

Métricas:

```text
tmdb_discover_context_hidden_dependency_total{dependency}
tmdb_discover_signature_mismatch_total{reason}
tmdb_discover_legacy_region_normalized_total{source}
tmdb_discover_post_context_mutation_total{field}
tmdb_discover_temporal_revision_change_total
tmdb_discover_cache_legacy_bypass_total{reason}
```

`post_context_mutation_total` deve permanecer zero em steady state.

---

# 417. Post-Context Mutation Guard

Depois de construir `EffectiveTmdbDiscoverSourceContext`, qualquer mutation dos campos que influenciam
o request é suspeita.

Em desenvolvimento/test:

```text
Object.freeze(context.definitionParams)
Object.freeze(context.requestParams)
```

ou clone/freeze equivalente.

No boundary de network:

```text
canonical(requestParamsBeforeSend)
===
canonical(paramsActuallySent)
```

ignorando apenas campos de transporte explicitamente permitidos, como credential/header.

Se houver diferença:

```text
test → fail
debug/dev → assertion
production → metric + conservative cache bypass/log redacted
```

Nunca recalcular region/includeAdult/language dentro de `getTmdb.ts`.

---

# 418. Mandatory File/Occurrence Map V17

Somar aos mapas V16:

## Must-change / authority

```text
addon/lib/getCatalog.ts
  sanitizeTmdbDiscoverParams
  resolveDynamicTmdbDiscoverParams caller
  region fallback from language
  includeAdultFallback
  primary_release_date → release_date rewrite
  watch provider removal

addon/lib/discoverCatalogSignature.ts
  getDiscoverParams
  computeDiscoverSignature
  applyDiscoverSignature
  legacy-only status

addon/lib/tmdbDiscoverDateTokens.ts
  resolveDynamicTmdbDiscoverParams
  parseDateToken
  temporal boundary/revision contract
```

## Must-audit parity

```text
addon/index.ts
  applyDiscoverSignature
  route page-cache key
  filtered page fill

addon/lib/getCatalog.ts
  buildCatalogCacheArgs
  merged source catalogKey

addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
```

## Regression/no-op classification

```text
configure/src/lib/setup/previewParams.ts
configure/src/components/setup/StickyApplyBar.tsx
configure/src/components/setup/AppliedNext.tsx
configure/src/lib/setup/templates.ts
configure/src/lib/collectionBuilder/importModes.ts
configure/src/lib/collectionBuilder/manifestSources.ts
```

Esses arquivos não precisam necessariamente mudar; precisam ser classificados para provar que não
reconstroem hidden source semantics nem alteram provenance.

Novos Occurrence Gate terms:

```text
sanitizeTmdbDiscoverParams
resolveDynamicTmdbDiscoverParams
includeAdultFallback
sanitized.region
sanitized.language
sanitized.include_adult
sanitized.with_release_type
primary_release_date.
release_date.
applyDiscoverSignature
computeDiscoverSignature
buildCatalogCacheArgs
sourceSnapshotRevision
definitionParams
requestParams
materializedDependencies
```

Closure final:

```text
Post-Signature Mutation Closure = zero hidden semantic mutation after correctness identity
Hidden Dependency Closure = zero effective request dependency absent from identity/revision
Discover Context Caller Closure = zero independent resolver
Legacy Region Normalization Closure = zero provenance-less authority creation
```

---

# 419. Version Registry V17

O registry V15/V16 permanece.

Nenhum schema já publicado pela feature existe no snapshot; portanto a V17 **refina a primeira definição**
de `CATALOG_SOURCE_SIGNATURE_VERSION = 1` em vez de criar um bump artificial.

Registry relevante:

```ts
export const RAW_RELEASE_DATES_CACHE_SCHEMA = 2;
export const RAW_RELEASE_DATES_REQUEST_PROFILE_VERSION = 1;
export const RELEASE_EVIDENCE_SCHEMA = 2;
export const RELEASE_VISIBILITY_POLICY_VERSION = 1;
export const RELEASE_ENTITY_KIND_CONTRACT_VERSION = 1;
export const TMDB_ID_RESOLUTION_CONTRACT_VERSION = 1;
export const TMDB_CREDENTIAL_SCOPE_VERSION = 1;
export const TMDB_RELEASE_ID_MAP_CACHE_SCHEMA = 1;
export const SEARCH_RESULT_CACHE_SCHEMA_VERSION = 2;
export const CATALOG_SOURCE_SIGNATURE_VERSION = 1; // V17 semantics included pre-first-deploy
export const CATALOG_FILTER_SIGNATURE_VERSION = 1;
export const PAGINATION_CONTRACT_SIGNATURE_VERSION = 1;
export const CATALOG_CURSOR_SCHEMA_VERSION = 7;
export const SEARCH_CURSOR_SCHEMA_VERSION = 3;
```

Se uma implementação intermediária de source signature v1 for publicada antes deste contrato:

```text
→ bump CATALOG_SOURCE_SIGNATURE_VERSION para 2
→ não reinterpretar v1 deployed
```

---

# 420. Test Matrix V17 — casos 278–300

Adicionar aos 277 casos acumulados:

```text
278. stored with_release_type=4|5|6, region ausente, watch ausente, language=pt-BR
     → source effective region BR/language-derived; nenhuma provenance explicit inventada;

279. mesmo stored params do caso 278, language=en-US
     → source effective region US e correctness identity/revision não compartilha artifact incompatível;

280. legacy stored watch_region=BR + with_release_type=4|5|6 + region ausente + language=en-US
     → effective source region BR pela migration release-aware, não US pelo sanitizer escondido;

281. watch_region=BR sem release-aware semantics
     → region não é promovida;

282. explicit/provenance US + watch BR + language pt-BR
     → effective source region US/discover-explicit;

283. include_adult ausente + config.includeAdult=false versus true
     → request efetivo e correctness source identity distinguem os dois universos;

284. include_adult persistido=false + config.includeAdult=true
     → persisted false vence fallback;

285. with_release_type + sort_by=primary_release_date.desc
     → request efetivo usa release_date.desc e canonical context registra a transformação;

286. with_watch_providers presente sem watch_region
     → provider filter removido antes de congelar effective context; nenhum post-signature drift;

287. params.language ausente + duas request languages diferentes
     → nenhum payload cache correctness-critical é compartilhado sem identidade compatível;

288. dynamic `today` token: dois requests no mesmo logical day
     → mesma definition identity e temporal revision compatível;

289. dynamic `today` token cruzando local midnight
     → revision/stableUntil invalida page/cursor antes de reutilização;

290. legacy discoverSig idêntico + hidden effective region diferente
     → V17 strong identity/validator impede collision correctness-critical;

291. route e merged source para o mesmo catálogo/context
     → definitionParams/sourceMembershipSignature iguais;

292. route e comprehensive warmer para o mesmo catálogo/context/clock
     → page key/revision compatíveis;

293. setup-generated movie releasedOnly BR novo
     → chega ao runtime já materializado region=BR/watch-region-derived; legacy fallback não dispara;

294. runtime legacy normalization
     → não persiste config durante read;

295. sanitizer não pode criar regionProvenance;
     provenance só nasce na authority de normalization/builder/reconstruction;

296. config.includeAdult muda entre requests com cache antigo presente
     → cache miss/invalidation segura; nunca retorna source membership antigo;

297. effective region muda por edit/save
     → cursor anterior inválido por sourceMembershipSignature;

298. property test: qualquer diferença em effective request field classificado como
     membership/order/payload-critical causa identity/revision incompatível;

299. post-context mutation assertion:
     params entregues ao TMDB == canonical requestParams, exceto credential/header;

300. #742 legacy end-to-end:
     catálogo release-aware legado com watch_region=BR, language=en-US, region ausente,
     filme com home release US e sem 4/5/6 BR fresh-confirmed
     → source usa BR após normalization, policy regional autorizada apenas conforme provenance/context,
     HIDE quando o CanonicalFilterContext efetivo for BR; Worldwide golden-master permanece idêntico.
```

A suite acumulada passa a ser descrita como **300+ casos**, além de parametrizações, property/fuzz,
concurrency, multi-replica, fault-injection e suites preexistentes.

---

# 421. Definition of Done V17

Além de todo DoD V16:

```text
[ ] EffectiveTmdbDiscoverSourceContext possui uma única authority
[ ] storedParams/definitionParams/requestParams são conceitos separados
[ ] runtime normalization não muta config compartilhada

[ ] region derivada de language não nasce dentro do sanitizer
[ ] legacy watch_region + release-aware recebe migration explícita/provenance
[ ] language-derived source não ganha authority de policy automaticamente
[ ] config nova Setup/Builder continua materializando region/provenance

[ ] includeAdult fallback entra no effective source context
[ ] effective language entra na cache/source identity quando relevante
[ ] sort rewrite ocorre antes da identity congelada
[ ] provider-param removal ocorre antes da identity congelada
[ ] genre/type/page possuem coordinate/identity explícita

[ ] discoverSig é compatibility/debug, não correctness authority
[ ] sourceMembershipSignature reflete o contexto efetivo
[ ] dynamic token tem sourceSnapshotRevision/stableUntil
[ ] cursor.validUntil respeita temporal source boundary

[ ] addon/index.ts route usa authority comum
[ ] getCatalog.ts direct/merged usa authority comum
[ ] comprehensiveCatalogWarmer usa authority comum
[ ] cacheWarmer classificado/parity-safe

[ ] zero semantic mutation após context freeze
[ ] zero hidden dependency sem identity/revision
[ ] zero legacy region authority sem provenance

[ ] migration de cache é rollback-safe
[ ] shadow mismatch metrics avaliadas antes de cutover
[ ] 300+ test matrix passa
[ ] todos os gates V16 continuam passando
```

---

# 422. Final Pre-Merge Checklist V17

```text
[ ] dev ainda é 6e83e22ab9de5093f9918a1871157f401feebb03
    OU Rebase/Delta/Occurrence/Caller + todos os gates V15–V17 foram rerodados

[ ] issue #742 permanece compatível com o escopo
[ ] TMDB release_dates/discover docs foram revalidadas

[ ] nenhuma source signature é calculada antes de uma hidden semantic dependency ser resolvida
[ ] nenhum request TMDB Discover recebe mutation correctness-critical após context freeze
[ ] legacy language/watch region migration está explícita e testada
[ ] includeAdult/language hidden fallbacks estão fechados

[ ] route == merged == warmer para effective source context
[ ] source definition == page-cache identity contract
[ ] temporal revision invalida dynamic token artifact na boundary
[ ] no-op edit/save V16 continua estável

[ ] Worldwide golden-master
[ ] BR/US/GB regional
[ ] Search/custom/merged/Jellyfin
[ ] Redis multi-replica/load/fault injection
[ ] dark deploy/homogeneous fleet
[ ] cache migration + kill switch + rollback drill
[ ] 300+ tests/gates aprovados
```

---

# 423. Evidência revalidada e resultado final V17

## 423.1. Evidência concreta adicional do snapshot

Revalidado em `dev@6e83e22ab9de5093f9918a1871157f401feebb03`:

```text
addon/lib/discoverCatalogSignature.ts
→ computeDiscoverSignature() lê params persistidos;
→ usa MD5 truncado de 8 hex no legado;
→ date tokens permanecem unresolved por design.

addon/index.ts
→ applyDiscoverSignature() entra no extraArgs/cache identity antes da execução do catálogo.

addon/lib/getCatalog.ts
→ raw stored params são clonados;
→ resolveDynamicTmdbDiscoverParams() resolve date tokens;
→ sanitizeTmdbDiscoverParams() depois:
   * injeta page;
   * injeta language fallback;
   * injeta include_adult fallback;
   * injeta sort_by default;
   * valida/remove params;
   * converte primary_release_date sort para release_date com with_release_type;
   * se with_release_type e region ausente, deriva region do country de language.

addon/lib/getCatalog.ts / merged source
→ buildCatalogCacheArgs() também usa discover signature persistida como parte do catalogKey.

package.json
→ continua sem script/test runner dedicado no snapshot; o harness exigido pelo plano ainda é
  deliverable obrigatório, não uma capacidade que já exista upstream.
```

Consequência:

```text
V16 estava correta no princípio "params canônicos/effective → strong source identity",
mas faltava fechar concretamente a ordem do pipeline que hoje produz o request.
A V17 elimina essa lacuna.
```

## 423.2. Evidência externa revalidada

TMDB permanece documentando:

```text
/movie/{id}/release_dates
→ 4 Digital / 5 Physical / 6 TV;

/discover/movie
→ region seleciona contexto regional de release date;
→ with_release_type trabalha com region;
→ ordem de release types é relevante;
→ watch_region pertence aos filtros de watch providers;
→ include_adult e language são query params do request.
```

## 423.3. Resultado final

```text
V17 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,

      preservando V16 e acrescentando:

      - Effective TMDB Discover Source Context único;
      - Post-Signature Mutation Closure;
      - Hidden Dependency Closure;
      - runtime legacy region normalization provenance-aware;
      - definitionParams × requestParams × sourceSnapshotRevision;
      - route/merged/warmer source-context parity;
      - explicit includeAdult/language/source-param identity;
      - dynamic token revision/boundary contract;
      - cache migration/shadow mismatch observability;
      - 300+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V17:

> **A V17 cobre estaticamente o snapshot auditado até o boundary do request efetivamente enviado ao
> TMDB Discover e transforma toda dependência dinâmica não provada por static analysis em gate
> executável, temporal ou distribuído. “100%” aqui significa zero ocorrência/caller/authority sem
> classificação no snapshot e zero comportamento runtime/upstream assumido sem teste/gate; não significa
> afirmar infalibilidade de um sistema externo.**

Checklist ultra-curto V17:

```text
1. fixe HEAD/tree;
2. rerode todos os gates V16;
3. centralize EffectiveTmdbDiscoverSourceContext;
4. materialize hidden defaults/migrations antes da correctness identity;
5. congele definition/request params;
6. derive strong source identity + temporal revision/boundary;
7. faça route/merged/warmer compartilhar a mesma authority;
8. migre cache em shadow → single-write;
9. rode 300+ casos + golden/property/concurrency/load;
10. dark deploy + homogeneous fleet;
11. habilite a UI regional;
12. kill-switch + rollback drill.
```

---

# 424. Reauditoria V18 — Local Membership Projection + Preview/Caller Closure sobre a V17

A V17 fechou corretamente a diferença entre `storedParams`, `definitionParams`, parâmetros efetivos,
revision temporal e request do TMDB Discover **até o ponto em que se assumia que a membership da fonte
era inteiramente definida pelo request upstream + filtros de Release Visibility posteriores**.

A reauditoria integral do mesmo snapshot encontrou duas classes adicionais concretas no código atual e
uma consequência temporal associada:

```text
DE. addon/lib/getCatalog.ts trata with_runtime.gte/lte de séries de forma especial:
    - os campos passam pelo sanitizer;
    - depois são removidos de `parameters` antes de /discover/tv;
    - cada item retornado é consultado por moviedb.tvInfo();
    - runtime é inferido de episode_run_time[0], last_episode_to_air.runtime ou
      next_episode_to_air.runtime;
    - runtime desconhecido/erro é fail-open (item mantido);
    - somente então o conjunto segue para hidratação de meta.

    Logo a definição lógica da fonte possui uma LOCAL MEMBERSHIP PROJECTION que não é igual ao
    request realmente enviado ao TMDB. O modelo V17 `definitionParams → requestParams` não é suficiente
    se `requestParams` for a única representação da source membership.

DF. O filtro local de runtime depende de TMDB TV detail cache/fetch e pode mudar membership sem que a
    página bruta de /discover/tv mude. Falha temporária de tvInfo() também mantém o item. Portanto
    projection freshness/revision, WorkBudget e estados `unknown/failure` não podem ser confundidos com
    upstream exhaustion nem ficar invisíveis ao page-set stability contract.

DG. addon/index.ts possui um segundo caller direto de TMDB Discover:
    GET /api/tmdb/discover/preview.
    Esse endpoint monta params diretamente de req.query, resolve apenas dynamic date tokens e chama
    moviedb.discoverMovie()/discoverTv(). Ele não executa a mesma sanitização/normalização/provenance
    nem a projeção local de runtime usada pelo catálogo real. Assim o Preview pode representar uma
    fonte semanticamente diferente daquela salva/executada.

DH. configure/src/components/sections/DiscoverBuilderDialog.tsx calcula o Preview a partir de
    buildDiscoverParams(), cujas datas relativas são inicialmente materializadas com `new Date()` no
    navegador. No save, relative presets são convertidos para `__tmdb_date__:*` e depois resolvidos no
    backend com o timezone efetivo. Perto da virada de dia, ou quando browser timezone != config.timezone,
    Preview e runtime podem divergir mesmo sem qualquer edição de configuração.

DI. A ocorrência de `moviedb.discoverMovie()` / `moviedb.discoverTv()` no snapshot está concentrada em:
    - addon/lib/getCatalog.ts: execução de catálogo;
    - addon/index.ts: preview;
    - addon/lib/getTmdb.ts: wrappers de transporte.
    A V17 fechava route/merged/warmer, mas não classificava explicitamente o caller Preview. O
    Direct-Discover-Caller Gate precisa incluir qualquer caller futuro desses wrappers/endpoints.

DJ. configure/src/components/sections/CatalogsSettings.tsx materializa o template de customização
    `tmdb.airing_today` com datas concretas derivadas de `new Date().toISOString().split('T')[0]` e sem
    `airDatePreset='today'`. Ao converter esse catálogo built-in em Discover customizado, o save pode
    persistir um dia fixo em vez de preservar a semântica dinâmica "today". Isso precisa ser uma decisão
    explícita de produto: preservar dinâmica via token/preset, ou declarar o customize como snapshot.
    Não pode permanecer como drift temporal acidental.
```

O snapshot auditado continua, sem rebase delta:

```text
HEAD: 6e83e22ab9de5093f9918a1871157f401feebb03
tree: 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
entries: 583
blobs: 544
direct Discover execution callers: getCatalog + /api/tmdb/discover/preview
issue #742: open / 0 comments no snapshot revalidado
```

A V18 não descarta nenhuma exigência V17. Ela corrige o último modelo incompleto: **nem toda source
membership efetiva é necessariamente expressável apenas pelos query params enviados ao upstream**.

---

# 425. Regra de precedência V18

As seções 1–423 permanecem como trilha acumulada V8→V17.

Para qualquer conflito relacionado a:

```text
TMDB Discover source definition
upstream request params
local membership projection
with_runtime.gte/lte em TV
TV detail membership evidence
preview parity
preview clock/timezone
direct Discover callers
source projection revision
source/page stability
runtime template temporal semantics
```

**as seções 424+ prevalecem**.

A V18 preserva integralmente:

```text
- V17 EffectiveTmdbDiscoverSourceContext;
- V17 hidden dependency/post-signature closure;
- V16 setup/template/provenance contracts;
- V15 transport/fleet/mapping/stability contracts;
- V14 semantic entity kind + mapping provenance;
- V13 WorkBudget/retry/evidence ingress;
- V10–V12 cursor/cache/raw/freshness/page-set stability;
- Worldwide golden-master e Regional CalendarDate semantics;
- todos os rollback/kill-switch/CI/occurrence gates anteriores.
```

---

# 426. Effective TMDB Discover Source Context V18 — três domínios, não dois

A authority V17 deve ser refinada para representar três coisas diferentes:

```text
1. LOGICAL SOURCE DEFINITION
   o conjunto/order que o catálogo promete produzir;

2. UPSTREAM REQUEST
   o request que de fato sai para /discover/movie ou /discover/tv;

3. LOCAL MEMBERSHIP PROJECTION
   transformação determinística/fail-open aplicada ao resultado upstream
   antes de considerar a página como a source page observável pelo restante do sistema.
```

Modelo conceitual V18:

```ts
interface EffectiveTmdbDiscoverSourceContextV18 {
  catalogType: 'movie' | 'series';

  storedParams: Readonly<Record<string, unknown>>;

  /**
   * Definição semântica completa da fonte.
   * Inclui constraints que podem ser executadas localmente.
   * Date tokens continuam canônicos/unresolved aqui.
   */
  logicalDefinition: Readonly<{
    params: Readonly<Record<string, unknown>>;
    localProjection: TmdbDiscoverLocalMembershipProjection;
  }>;

  /**
   * Params exatos enviados ao endpoint Discover neste request/page.
   * NÃO contém constraints executadas apenas localmente.
   */
  upstreamRequestParams: Readonly<Record<string, unknown>>;

  releaseRegionProvenance?: DiscoverRegionProvenance | null;
  sourceSnapshotRevision?: string | null;
  localProjectionRevision?: string | null;
  stableUntil: Date | null;

  materializedDependencies: Readonly<{
    language?: string;
    includeAdult?: boolean;
    genre?: string | null;
    legacyRegionSource?: DiscoverRegionProvenanceSource | null;
  }>;
}
```

Tipo recomendado:

```ts
type TmdbDiscoverLocalMembershipProjection =
  | { kind: 'none'; version: 1 }
  | {
      kind: 'tv-runtime-range';
      version: 1;
      gteMinutes: number | null;
      lteMinutes: number | null;
      runtimeResolution: [
        'episode_run_time[0]',
        'last_episode_to_air.runtime',
        'next_episode_to_air.runtime'
      ];
      unknownPolicy: 'keep';
      errorPolicy: 'keep';
    };
```

Regra fundamental:

> `sourceMembershipSignature` representa a **logicalDefinition completa**, não somente
> `upstreamRequestParams`.

Assim:

```text
mesmo /discover/tv request upstream
+ runtime 20–30 min
!=
mesmo /discover/tv request upstream
+ runtime 45–90 min
```

mesmo que os query params enviados ao TMDB sejam idênticos após remover `with_runtime.*`.

---

# 427. Pipeline TMDB Discover V18 — ordem normativa final

Substituir a leitura simplificada V17 por esta ordem:

```text
1. clone stored params
2. normalize legacy shape
3. resolve/validate region provenance
4. runtime migration idempotente de legacy release-aware region
5. materializar defaults externos semanticamente relevantes
6. canonicalizar tipos e operadores
7. validar allowed params por media type
8. aplicar transforms determinísticos de source definition
9. EXTRair constraints local-only para LocalMembershipProjection
10. construir logicalDefinition = canonical params + local projection
11. calcular strong sourceMembershipSignature(logicalDefinition)
12. resolver dynamic date tokens com RequestEvaluationClock
13. construir sourceSnapshotRevision + temporal stableUntil
14. adicionar page
15. construir upstreamRequestParams removendo APENAS constraints local-only já materializadas
16. congelar context
17. executar /discover/movie ou /discover/tv via transport compartilhado
18. aplicar LocalMembershipProjection sobre a página upstream
19. registrar projection outcome/revision/stability
20. hidratar metas
21. aplicar Release Visibility / demais membership filters no chokepoint
22. page-fill/dedupe/cursor usam o conjunto pós-source-projection e pós-policy conforme contratos V10+
```

Proibições:

```text
- não remover with_runtime.* depois de assinar sem materializar a projeção;
- não hashear somente upstreamRequestParams quando existe local projection;
- não deixar Preview executar uma versão paralela dessa ordem;
- não transformar erro de projection em upstream exhausted;
- não deixar local projection iniciar network calls fora do WorkBudget/admission/transport policy.
```

---

# 428. TV Runtime Local Membership Projection — contrato exato

O comportamento atual deve ser preservado inicialmente como golden-master, salvo decisão explícita de produto:

```text
mediaType != tv
→ projection none

sem with_runtime.gte/lte efetivo
→ projection none

TV + runtime range
→ remover with_runtime.* do upstream request
→ para cada item upstream, consultar detail necessário
→ runtime = primeiro valor numérico > 0 de:
   1. episode_run_time[0]
   2. last_episode_to_air.runtime
   3. next_episode_to_air.runtime

runtime unknown
→ KEEP

detail fetch error
→ KEEP

runtime < gte
→ DROP

runtime > lte
→ DROP

caso contrário
→ KEEP
```

Essa regra deve sair do corpo monolítico de `getCatalog.ts` para helper testável, por exemplo:

```text
resolveTmdbDiscoverLocalProjection(...)
applyTmdbDiscoverLocalProjection(...)
```

Não duplicar a resolução em Preview, merged ou warmer.

O helper deve retornar estrutura observável:

```ts
interface LocalProjectionResult<T> {
  items: T[];
  evaluated: number;
  kept: number;
  dropped: number;
  unknown: number;
  failures: number;
  budgetExhausted: boolean;
  nextStabilityBoundary?: Date | null;
  revision?: string | null;
}
```

`unknown` e `failures` não são erros fatais no contrato legado; são motivo de observabilidade e
possível future-policy version bump.

---

# 429. Projection Stability, cache e cursor — não confundir página bruta com página lógica

Quando existe local membership projection, há dois page sets conceituais:

```text
RAW UPSTREAM PAGE
/discover/tv response

LOGICAL SOURCE PAGE
raw page após LocalMembershipProjection
```

O restante do pipeline de catalog/filter/pagination deve operar sobre **LOGICAL SOURCE PAGE**.

Regras:

```text
A. page-cache que armazena o resultado já projetado precisa ter identidade contendo
   sourceMembershipSignature(logicalDefinition).

B. se existir/futuramente existir cache neutro da página upstream, ele pode ser compartilhado entre
   runtime ranges somente se a projection for aplicada depois e tiver namespace próprio.

C. cursor/page-set revision não pode assumir que raw page revision == logical page revision.

D. refresh de tvInfo/detail que muda keep/drop precisa produzir uma nova logical page revision ou
   ficar protegido pelo mesmo page-cache stability deadline já contratado.

E. cursor.validUntil/stableUntil = min(
     temporal source boundary,
     neutral page stability,
     logical projection stability,
     filter/evidence boundaries,
     dynamic source/filter-state boundaries
   ).

F. projection failure/budget exhaustion não autoriza marcar source como exhausted.

G. uma página que fica vazia apenas por projection local precisa continuar page-fill conforme os
   mesmos contratos zero-visible/budgetExhausted/upstreamExhausted já definidos.
```

Se o storage/cache atual não expõe freshness suficiente do `tmdb:tv:detail:*` para construir uma
boundary exata, usar a estabilidade da **página lógica cacheada** como authority e transformar a
falta de uma boundary mais fina em gate explícito; não inventar freshness pela hora de leitura.

---

# 430. Projection WorkBudget + TMDB admission

O filtro de runtime atual pode multiplicar chamadas de detalhe por página e, sob filtered page-fill,
por várias páginas.

Exemplo:

```text
20 itens/page
× N páginas lidas para preencher uma página visível
× 1 tvInfo potencial por item
```

Isso precisa entrar no mesmo modelo de recursos V13/V15.

Contrato:

```text
- cache hit de tvInfo não consome network-attempt budget;
- miss/fetch consome TMDB detail attempt budget;
- retry consome attempt novamente;
- deadline global do request continua soberana;
- local projection recebe budget restante, não cria contador próprio ilimitado;
- admission/rate-limit/circuit-breaker do TMDB Direct-Network Gate continua obrigatório;
- budgetExhausted é distinto de upstreamExhausted;
- em budgetExhausted, preservar checkpoint de progresso seguro e fail-open conforme policy versionada.
```

Adicionar métricas:

```text
tmdb_discover_projection_total{kind,result}
tmdb_discover_runtime_projection_items_total{result=kept|dropped|unknown|failure}
tmdb_discover_runtime_detail_total{result=cache_hit|fetched|error|budget_exhausted}
tmdb_discover_projection_latency_seconds{kind}
tmdb_discover_projection_budget_exhausted_total{surface}
```

Nunca logar credentials.

---

# 431. TMDB Discover Preview Parity Gate — preview é caller de source semantics

`GET /api/tmdb/discover/preview` deixa de ser um caller independente de semântica.

Ele deve usar a mesma authority V18 em modo ephemeral/preview:

```text
UI form state
  ↓
build semantic candidate params
  ↓
resolveEffectiveTmdbDiscoverSourceContextV18(..., surface='preview')
  ↓
upstreamRequestParams page=1
  ↓
shared TMDB transport
  ↓
applyTmdbDiscoverLocalProjection()
  ↓
preview DTO
```

Paridade obrigatória:

```text
mesmos params semânticos
+ mesmo RequestEvaluationClock
+ mesmo timezone
+ mesmo provider fixtures
=
mesmo ordered logical source id set de page 1
entre Preview e execução normal antes da hidratação/policy específica de Release Visibility.
```

Não exigir que o Preview hidrate toda a `Meta` final se isso destruir latência. A paridade exigida é da
**source semantics**: params, local membership projection e ordered IDs.

`total_results` merece contrato explícito:

```text
raw upstream total_results
!= necessariamente total lógico após local projection
```

Portanto a UI deve:

```text
- ou rotular/usar total upstream como aproximado;
- ou omitir total exato quando projection local estiver ativa;
- nunca apresentar raw total como contagem exata do conjunto projetado.
```

---

# 432. Preview Clock/Timezone Authority — navegador não decide a data efetiva do catálogo

Para presets relativos (`today`, `this_week`, `this_month`, etc.), a UI pode exibir datas humanas,
mas não deve ser a authority correctness-critical do Preview.

Problema atual:

```text
buildDiscoverParams()
→ getTodayLocalDateString()/getDateRangeFromPreset()
→ browser Date/local timezone

save
→ applyDynamicTmdbDateTokens()
→ token persistido
→ backend resolve com config.timezone
```

Contrato V18:

```text
Preview de preset relativo
→ enviar o token/preset semântico ao backend
→ backend usa o MESMO RequestEvaluationClock + effective timezone do runtime
→ preview requestParams e sourceSnapshotRevision vêm da mesma authority
```

A UI pode continuar mostrando a data calculada localmente apenas como apresentação, mas:

```text
browser rendered date
→ não entra em correctness identity
→ não substitui backend resolved date
→ discrepância browser/config timezone pode gerar hint visual, não mudança silenciosa de semantics
```

Teste obrigatório com:

```text
browser timezone = America/Los_Angeles
config.timezone = America/Fortaleza
clock próximo da meia-noite em um deles
→ Preview e saved runtime usam America/Fortaleza para a source semantics.
```

---

# 433. Direct Discover Caller Gate V18

Adicionar occurrence/caller gate específico:

```bash
rg -n "discoverMovie\(|discoverTv\(|/discover/movie|/discover/tv|tmdb/discover/preview" addon configure
```

Cada ocorrência precisa ser classificada como:

```text
A. transport wrapper;
B. canonical executor usando EffectiveTmdbDiscoverSourceContextV18;
C. preview adapter usando a mesma authority;
D. test/fixture/documentation;
E. forbidden direct caller.
```

Snapshot V18 conhecido:

```text
addon/lib/getTmdb.ts
→ wrapper de transporte

addon/lib/getCatalog.ts
→ executor de catálogo

addon/index.ts
→ preview caller + route orchestration
```

DoD:

```text
zero ocorrência E;
zero caller de Discover que monte params semanticamente relevantes à mão depois da refatoração;
zero caller que aplique local runtime semantics fora do helper central.
```

O gate deve ser rerodado em qualquer rebase porque um novo endpoint de preview/debug/admin pode
reintroduzir bypass silencioso.

---

# 434. Template Temporal Semantics Gate — `tmdb.airing_today` customize

O snapshot contém:

```text
configure/src/components/sections/CatalogsSettings.tsx
DEFAULT_CATALOG_TEMPLATES['tmdb.airing_today']
→ airDateFrom = new Date().toISOString().split('T')[0]
→ airDateTo   = new Date().toISOString().split('T')[0]
→ não materializa airDatePreset='today'
```

E o save de Discover só converte datas relativas para tokens quando o preset relativo está presente.

A implementação precisa escolher e testar uma das duas políticas:

## Política recomendada: preserve-dynamic

```text
Customize "Airing Today"
→ formState.airDatePreset = 'today'
→ datas visuais podem ser derivadas para UI
→ persisted params usam __tmdb_date__:today:from/to
→ catálogo continua dinamicamente "today" após amanhã.
```

## Alternativa permitida: explicit-snapshot

```text
Customize "Airing Today"
→ UI informa explicitamente que será criado um snapshot da data atual
→ ID/nome/metadata deixam isso inequívoco
→ teste garante que o freeze é intencional
```

Não aceitar o estado intermediário atual em que a semântica dinâmica pode virar estática sem contract.

Esse gate é maior que #742, mas pertence à mesma authority temporal de TMDB Discover introduzida pela
V17/V18 e evita um segundo tipo de source drift temporal.

---

# 435. Discover Form Hydration Parity — prevenção de drift entre edit/customize/reconstruct

A reauditoria também classificou dois branches de hidratação em `DiscoverBuilderDialog.tsx`:

```text
editingCatalog
→ carrega formState amplo, incluindo watchRegion, watchProviders, runtimeRange e releaseRegion;

customizeTemplate
→ carrega um subconjunto diferente de campos.
```

No snapshot atual, os `DEFAULT_CATALOG_TEMPLATES` não carregam `releaseRegion`, portanto isso não é
blocker factual da #742 hoje. Porém a duplicação é um vetor direto de regressão quando um template
release-aware/dynamic for adicionado.

Melhoria arquitetural V18:

```text
hydrateDiscoverFormState(formState, mode)
```

com tabela explícita de campos por source e testes de round-trip.

Regra:

```text
se um campo é semanticamente suportado no formState de um source,
nenhum branch edit/customize/import/reconstruct pode simplesmente esquecê-lo sem policy explícita.
```

Campos prioritários no regression fixture:

```text
releaseRegion
regionProvenance
watchRegion
watchProviders
providerJoinMode
releasedOnly
tmdbMovieReleaseTypes
runtimeRange
movieDatePreset
seriesDatePreset
airDatePreset
```

Isso complementa, sem substituir, o Template-Policy Closure Gate V16.

---

# 436. Param Operator Semantics — concretização do canonicalization gate já exigido

A V10/V14/V17 já exigiam canonical serialization consciente de ordem. A V18 torna o caso TMDB Discover
executável porque o próprio sanitizer aceita arrays e atualmente os converte genericamente para string.

TMDB documenta filtros em que:

```text
comma `,` = AND
pipe  `|` = OR
```

E `with_release_type` também possui ordem relevante para a release date retornada.

Logo não usar genericamente:

```text
array
→ join(',')
```

como se toda lista tivesse a mesma álgebra.

Criar schema por campo, conceitualmente:

```ts
interface TmdbDiscoverParamSemantics {
  key: string;
  valueKind: 'scalar' | 'ordered-or-list' | 'and-or-expression' | 'set-like';
  allowedOperators?: Array<'and' | 'or'>;
  orderSensitive?: boolean;
}
```

Regras:

```text
- string persistida com `|` preserva OR e ordem quando order-sensitive;
- string com `,` preserva AND;
- arrays só são aceitos quando a origem define qual operador representam;
- origem ambígua → rejeitar/normalizar com warning, nunca escolher AND silenciosamente;
- canonicalization de signature acontece DEPOIS de preservar a álgebra do filtro;
- parser/serializer/edit/save/import/export precisam round-trip sem trocar AND↔OR.
```

Esse refinamento não revoga os gates V10/V14; ele os torna específicos para o único sanitizer que hoje
faz `arrayValues.join(',')` de forma genérica.

---

# 437. Version Registry V18

Não reutilizar version numbers anteriores para os contratos novos.

Adicionar conceitualmente:

```ts
export const TMDB_DISCOVER_EFFECTIVE_CONTEXT_VERSION = 2;
export const TMDB_DISCOVER_LOCAL_PROJECTION_CONTRACT_VERSION = 1;
export const TMDB_DISCOVER_PREVIEW_CONTRACT_VERSION = 1;
export const TMDB_DISCOVER_PARAM_OPERATOR_CONTRACT_VERSION = 1;
export const DISCOVER_FORM_HYDRATION_CONTRACT_VERSION = 1;
```

Observação:

```text
CATALOG_SOURCE_SIGNATURE_VERSION
PAGINATION_CONTRACT_SIGNATURE_VERSION
```

só precisam de bump de valor concreto quando a implementação alterar o formato/semântica deployed.
O plano não deve inventar o número final antes de conhecer o branch de implementação, mas o PR precisa
provar que artefatos V17/pre-V18 não são lidos como equivalentes se a nova projection mudar a identity.

Namespaces/cursors continuam sujeitos aos gates rollback-safe e homogeneous-fleet anteriores.

---

# 438. Mandatory File/Occurrence Map V18

Além de todos os mandatory maps anteriores, classificar explicitamente:

| Arquivo | Motivo V18 | Ação esperada |
|---|---|---|
| `addon/lib/getCatalog.ts` | extrai/remove runtime params e filtra TV localmente | changed: delegar para context/projection authority |
| `addon/lib/getTmdb.ts` | wrappers Discover + `tvInfo` cache/transport | covered/changed conforme admission hooks |
| `addon/index.ts` | `/api/tmdb/discover/preview` + catalog route | changed: preview usa authority comum |
| `addon/lib/discoverCatalogSignature.ts` | legado signature | covered: compatibility/debug somente |
| `addon/lib/tmdbDiscoverDateTokens.ts` | dynamic token resolution | changed/covered: RequestClock comum ao preview/runtime |
| `addon/lib/catalogPagination.ts` | page-fill/cursor | covered/changed: projection empty/budget semantics |
| `addon/lib/comprehensiveCatalogWarmer.js` | caller warm | covered: mesma logical source authority |
| `addon/lib/cacheWarmer.js` | synthetic configs/warm | classified/parity-safe |
| `addon/utils/mergedCatalog.ts` + merged path em `getCatalog.ts` | source composition | covered: projected source identity |
| `configure/src/components/sections/DiscoverBuilderDialog.tsx` | preview + save + duplicated hydration | changed |
| `configure/src/components/sections/CatalogsSettings.tsx` | `tmdb.airing_today` customize template | changed ou explicit-snapshot policy |
| `addon/lib/collectionBuilder/catalogReconstruction.ts` | form/params round-trip | covered + hydration fixtures |
| `addon/utils/ai-catalog-schema.ts` | runtime/release param schema | covered |
| `addon/utils/ai-catalog-generation.ts` | AI can emit runtime/release params | covered |
| `addon/utils/ai-catalog-sanitizer.ts` | AI canonicalization | covered/operator parity |
| `addon/utils/ai-catalog-config-builder.ts` | params→formState | covered/hydration parity |
| `configure/src/lib/setup/streaming.ts` | release-aware Discover generation | covered V16/V18 parity |
| `configure/src/lib/setup/previewParams.ts` | setup preview params | classify no-op/covered; não confundir com Discover Preview |
| `public/featured/callandt95.json` | runtime/date/release-aware fixtures | fixture round-trip |

Occurrence gates mínimos adicionais:

```text
rg -n "with_runtime\.gte|with_runtime\.lte|runtimeRange|episode_run_time" addon configure public
rg -n "discoverMovie\(|discoverTv\(|/discover/movie|/discover/tv" addon configure
rg -n "tmdb/discover/preview|handlePreview|buildDiscoverParams" addon configure
rg -n "getTodayLocalDateString|getDateRangeFromPreset|__tmdb_date__|airDatePreset|movieDatePreset|seriesDatePreset" addon configure public
rg -n "customizeTemplate|DEFAULT_CATALOG_TEMPLATES|hydrate.*FormState" configure/src
rg -n "join\(','\)|join\('\|'\)|with_release_type|with_genres|with_people|with_companies|with_keywords|with_status|with_type" addon configure
```

Para cada match:

```text
changed
covered by shared authority
intentional no-op
fixture/test/documentation
forbidden/unclassified
```

DoD: zero `forbidden/unclassified`.

---

# 439. Test Matrix V18 — casos 301–336

Adicionar aos 300 casos acumulados:

```text
301. TV Discover sem with_runtime.*
     → localProjection=none; upstream params preservados.

302. TV Discover with_runtime.gte=20/lte=30
     → logicalDefinition contém runtime projection; upstream request NÃO contém with_runtime.*.

303. mesmo upstream request, runtime 20–30 versus 45–90
     → sourceMembershipSignature incompatível.

304. runtime conhecido dentro da faixa
     → KEEP.

305. runtime conhecido abaixo de gte
     → DROP.

306. runtime conhecido acima de lte
     → DROP.

307. episode_run_time ausente + last_episode_to_air.runtime válido
     → usar fallback 2.

308. primeiros dois ausentes + next_episode_to_air.runtime válido
     → usar fallback 3.

309. runtime completamente desconhecido
     → KEEP + metric unknown.

310. tvInfo error
     → KEEP + metric failure; nunca upstreamExhausted.

311. projection remove todos os itens da page 1, page 2 possui candidatos
     → page-fill continua até alvo/exhaustion/budget.

312. projection budget esgota antes da fonte
     → budgetExhausted=true, upstreamExhausted=false, checkpoint preservado.

313. cache hit de tvInfo
     → zero network-attempt budget consumido.

314. tvInfo retry
     → cada tentativa contabilizada no WorkBudget/admission.

315. refresh de detail muda keep→drop
     → logical page revision/stability impede cursor stale de atravessar mudança incompatível.

316. route versus merged com runtime range e fixtures idênticas
     → mesmo logical ordered id set.

317. route versus comprehensive warmer com runtime range
     → mesma source identity/page semantics.

318. Preview TV com runtime range
     → ordered ids da source page 1 == runtime source page 1 antes da meta/policy.

319. Preview sem runtime range
     → zero detail projection fan-out.

320. Preview with_release_type + region ausente em legacy input
     → mesma runtime normalization/provenance que execução real.

321. Preview with_watch_providers sem watch_region
     → mesma canonical removal que execução real.

322. Preview primary_release_date.desc + with_release_type
     → mesma rewrite para release_date.desc.

323. Preview include_adult ausente
     → mesmo fallback efetivo que runtime.

324. Preview media type movie recebe somente movie-allowed params;
     Preview TV recebe somente tv-allowed params.

325. relative preset `today`, browser timezone != config.timezone
     → source semantics do Preview usa config.timezone/backend clock.

326. relative preset cruza meia-noite no config.timezone
     → Preview e runtime mudam sourceSnapshotRevision juntos.

327. Preview raw total_results com projection ativa
     → não é exposto/rotulado como total lógico exato.

328. Direct Discover occurrence gate
     → somente wrapper + canonical executor + preview adapter classificados.

329. nenhuma chamada moviedb.discoverMovie/discoverTv recebe params mutados depois do context freeze.

330. `tmdb.airing_today` Customize em policy preserve-dynamic
     → persisted airDatePreset=today + dynamic tokens; amanhã continua today.

331. se produto escolher explicit-snapshot no caso 330
     → UI/metadata/test deixam freeze explícito; nenhuma ambiguidade.

332. edit/customize hydration property fixture com releaseRegion/watchRegion/runtimeRange/presets
     → nenhum campo semanticamente suportado some silenciosamente.

333. params string `with_release_type=4|5|6`
     → OR/order preservados em save/import/runtime/signature.

334. params string com comma em campo AND-capable
     → AND preservado; não normalizar para pipe.

335. array input em campo cujo operador é ambíguo
     → reject/warn ou origem explícita; nunca `join(',')` silencioso.

336. full #742 + runtime projection + filtered pagination:
     movie regional continua obey Release Visibility; series runtime projection permanece source-level;
     nenhuma policy regional é aplicada a series e nenhum cursor cruza source/projection boundary inválida.
```

A suite acumulada passa a ser descrita como **336+ casos**, além de parametrizações, golden-master,
property/fuzz, concurrency, multi-replica, load, fault-injection e suites preexistentes.

---

# 440. Definition of Done V18

Além de todo DoD V17:

```text
[ ] EffectiveTmdbDiscoverSourceContext V18 separa logicalDefinition/upstreamRequest/localProjection
[ ] sourceMembershipSignature cobre localProjection semanticamente relevante
[ ] upstreamRequestParams contém exatamente o que vai ao TMDB, sem local-only fields
[ ] zero semantic mutation após context freeze

[ ] with_runtime.* TV possui helper central de local projection
[ ] runtime resolution order está versionada/testada
[ ] unknown/error policy está explícita e golden-mastered
[ ] projection failure/budget exhaustion != upstream exhaustion
[ ] projection participa de page-set stability/revision
[ ] filtered page-fill funciona quando projection zera páginas
[ ] detail fan-out usa WorkBudget/admission/transport compartilhados

[ ] /api/tmdb/discover/preview usa a mesma source authority
[ ] Preview aplica a mesma local projection
[ ] Preview não mantém sanitizer paralelo
[ ] Preview relative-date semantics usa backend RequestClock/effective timezone
[ ] Preview total_results não finge ser projected exact count

[ ] Direct Discover Caller Gate = zero bypass
[ ] novos callers de discover entram automaticamente no occurrence gate

[ ] tmdb.airing_today customize possui policy temporal explícita
[ ] preserve-dynamic usa preset/token; snapshot, se escolhido, é explicitamente rotulado
[ ] edit/customize/reconstruct hydration possui parity fixtures

[ ] operator semantics comma/pipe/order são preservadas
[ ] array ambíguo não vira AND silenciosamente

[ ] mandatory file map V18 classificado integralmente
[ ] 336+ test matrix passa
[ ] todos os gates V17 continuam passando
```

---

# 441. Final Pre-Merge Checklist V18

```text
[ ] dev ainda é 6e83e22ab9de5093f9918a1871157f401feebb03
    OU Rebase/Delta/Occurrence/Caller + todos os gates V15–V18 foram rerodados

[ ] issue #742 continua compatível com o escopo
[ ] TMDB release_dates/discover docs revalidadas

[ ] logical source definition inclui local membership projection
[ ] upstream request e local projection não são confundidos
[ ] runtime TV range não desaparece da correctness identity
[ ] projection WorkBudget/failure/stability testados

[ ] preview == runtime source semantics para page 1 sob fixed fixtures/clock
[ ] preview usa effective timezone do backend para presets relativos
[ ] direct Discover callers = zero bypass

[ ] route == merged == warmer para logical source context
[ ] source page revision inclui/encapsula projection stability
[ ] cursor.validUntil respeita source + projection + filter boundaries

[ ] setup/builder/import/export/reconstruct continuam region/provenance-safe
[ ] dynamic template semantics não congela silenciosamente
[ ] no-op edit/save V16 continua estável
[ ] operator semantics preservadas

[ ] Worldwide golden-master
[ ] BR/US/GB regional
[ ] Search/custom/merged/Jellyfin
[ ] Redis multi-replica/load/fault injection
[ ] dark deploy/homogeneous fleet
[ ] cache migration + kill switch + rollback drill
[ ] 336+ tests/gates aprovados
```

---

# 442. Evidência revalidada e resultado final V18

## 442.1. Evidência concreta adicional do snapshot

Revalidado em `dev@6e83e22ab9de5093f9918a1871157f401feebb03`:

```text
addon/lib/getCatalog.ts
→ sanitizeTmdbDiscoverParams() aceita with_runtime.gte/lte;
→ para mediaType=tv, o código lê esses valores e os remove de `parameters`;
→ /discover/tv recebe o request sem os dois runtime params;
→ response.results é pós-filtrado localmente;
→ cada item usa moviedb.tvInfo({ id, language });
→ runtime fallback = episode_run_time[0] / last_episode_to_air.runtime /
  next_episode_to_air.runtime;
→ runtime desconhecido ou fetch exception mantém o item.

addon/lib/getTmdb.ts
→ tvInfo() é cacheado em `tmdb:tv:detail:<id><query-suffix>` por 24h;
→ discoverMovie()/discoverTv() são wrappers diretos de /discover/movie e /discover/tv.

addon/index.ts
→ GET /api/tmdb/discover/preview coleta req.query quase diretamente;
→ resolveDynamicTmdbDiscoverParams() é aplicado;
→ page=1 é forçado;
→ moviedb.discoverMovie()/discoverTv() é chamado sem compartilhar o sanitizer/projection
  de getCatalog.ts.

configure/src/components/sections/DiscoverBuilderDialog.tsx
→ handlePreview() chama buildDiscoverParams() e envia esses params ao endpoint Preview;
→ getTodayLocalDateString()/getDateRangeFromPreset() usam Date do navegador;
→ no save, applyDynamicTmdbDateTokens() converte relative presets para tokens persistidos;
→ edit path carrega releaseRegion/watchRegion/runtimeRange;
→ customizeTemplate path é uma hidratação separada/subset.

configure/src/components/sections/CatalogsSettings.tsx
→ DEFAULT_CATALOG_TEMPLATES['tmdb.airing_today'] materializa a data corrente concreta
  sem airDatePreset='today'.
```

Occurrence audit adicional do snapshot:

```text
with_runtime
→ 7 arquivos

runtimeRange
→ 4 arquivos

episode_run_time
→ 4 arquivos

customizeTemplate
→ 2 arquivos

discoverMovie()/discoverTv()
→ execução em getCatalog + preview em addon/index + wrappers em getTmdb
```

## 442.2. Evidência externa revalidada

TMDB continua documentando:

```text
/discover/movie
→ region altera a release-date semantics;
→ with_release_type aceita 1–6 e pode trabalhar com region;
→ ordem de release types é relevante;
→ comma = AND e pipe = OR em filtros suportados;
→ with_runtime.gte/lte são filtros documentados.

/discover/tv
→ with_runtime.gte/lte são query params documentados;
→ filtros AND/OR por comma/pipe também existem para vários campos.

/movie/{id}/release_dates
→ 4 Digital / 5 Physical / 6 TV.
```

A decisão de AIOmetadata de remover runtime filters do Discover TV e reaplicá-los localmente é uma
**semântica própria do projeto**; por isso ela precisa estar modelada como local source projection e não
pode ser inferida apenas da documentação upstream.

## 442.3. Resultado final

```text
V18 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,

      preservando V17 e acrescentando:

      - Logical Source Definition × Upstream Request × Local Membership Projection;
      - TV runtime local-projection contract;
      - projection WorkBudget/freshness/page-stability closure;
      - TMDB Discover Preview Parity Gate;
      - backend RequestClock/timezone authority para Preview;
      - Direct Discover Caller Gate;
      - dynamic-template temporal semantics closure;
      - edit/customize form hydration parity guard;
      - concrete TMDB operator-semantics contract;
      - 336+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V18:

> **A V18 cobre estaticamente o snapshot auditado até os callers diretos de TMDB Discover, distingue
> explicitamente membership produzida pelo upstream de membership projetada localmente e transforma
> todo comportamento dinâmico restante em gate executável, temporal, distribuído ou de integração.
> “100%” significa zero ocorrência/caller/authority conhecida sem classificação no snapshot e zero
> comportamento runtime/upstream assumido sem teste/gate; não significa afirmar infalibilidade do TMDB,
> da rede, do relógio distribuído ou de qualquer sistema externo.**

Checklist ultra-curto V18:

```text
1. fixe HEAD/tree;
2. rerode todos os gates V17;
3. modele logicalDefinition + upstreamRequest + localProjection;
4. centralize TV runtime projection;
5. inclua projection em source identity/stability/WorkBudget;
6. faça Preview usar a mesma source authority e backend clock;
7. feche todos os direct Discover callers;
8. resolva dynamic template semantics;
9. preserve operator semantics + hydration parity;
10. rode 336+ casos + golden/property/concurrency/load/fault;
11. dark deploy + homogeneous fleet;
12. kill-switch + rollback drill.
```
---

# 443. Reauditoria V19 — Request Context / In-Process / Transport-Freshness Closure

Esta V19 é uma **reauditoria final adicional sobre a V18 inteira**, contra o mesmo snapshot de código.
Ela não remove nenhuma exigência das seções 1–442. O objetivo desta camada é fechar superfícies que
não estavam modeladas explicitamente como parte da prova de correção da #742: a coerência da configuração
consumida dentro de uma request, o caminho interno usado pelo Jellyfin para chamar as rotas Stremio sem
middleware/fila, o cancelamento de trabalho após timeout, o cache transitório de páginas que falharam e a
validade de respostas depois que elas saem do pipeline interno.

> **Precedência V19:** em qualquer conflito com as seções 1–442, esta camada V19 prevalece.

## 443.1. Snapshot revalidado

```text
repo                       cedya77/aiometadata
branch                     dev
HEAD                       6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA                   00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release correspondente     v3.1.0
blobs                      544
issue #742                 aberta / 0 comentários no snapshot revalidado
```

Não houve drift de código após o HEAD já fixado pela V18 no momento desta reauditoria.
Logo o Rebase Gate continua satisfeito **somente para esse snapshot exato**.

## 443.2. Evidência estática nova que motivou a V19

No snapshot auditado:

```text
addon/lib/getCache.ts
→ resolveConfigForCache(userUUID, options) reutiliza options.config quando fornecido;
→ se options.config existe e não possui userUUID, o helper adiciona userUUID por mutação;
→ sem options.config, o wrapper chama loadConfigFromDatabase(userUUID);
→ o helper é consumido por cacheWrapCatalog/search/meta/meta-components/reconstruct/meta-smart.

addon/index.ts
→ catalogRoute carrega config, aplica overrides e depois anota o próprio objeto runtime com:
   config.userUUID
   config._currentCatalogConfig
   config._currentSearchType
   config._currentSearchCatalogId
   config._searchLight
→ cacheOptions normalmente recebe { config }, o que é bom para a rota principal;
→ essas anotações continuam sendo estado contextual mutável misturado ao objeto de configuração.

addon/lib/inProcessRoutes.ts
→ invokeRoute() chama handlers registrados diretamente;
→ o próprio arquivo documenta que isso ocorre sem socket, sem middleware e sem queue;
→ o timeout é implementado com Promise.race();
→ quando o timeout vence, não existe AbortController/AbortSignal cancelando o handler subjacente.

addon/lib/jellyfin/items.ts
→ fetchCatalogPage()/fetchMeta() usam invokeRoute();
→ JELLYFIN_ROUTE_TIMEOUT_MS controla apenas o timeout do chamador;
→ failedPages é um LRU local que suprime nova tentativa do mesmo URL por JELLYFIN_CATALOG_RETRY;
→ a key de failedPages é a URL, não o JellyfinPagingScope/filter/source signature da V18.

addon/index.ts / respond()
→ catalog/meta usam atualmente Cache-Control: no-cache, must-revalidate, max-age=0;
→ essa política é hoje segura contra retenção longa de resposta policy-specific;
→ a V18, porém, não transformava transport/HTTP response freshness em invariante do projeto.
```

Esses facts não invalidam a arquitetura central da V18. Eles mostram que a prova de correção ainda
precisava atravessar **um boundary anterior ao filtro** (config/request context), **um boundary paralelo
à rota HTTP** (in-process Jellyfin) e **um boundary posterior ao filtro** (response/client/proxy cache).

---

# 444. Blockers novos V19

Adicionar cumulativamente aos blockers históricos:

```text
DK. Uma única request ainda não possui contrato formal de RequestConfigSnapshot. Recarregar config ou
    mutar o mesmo objeto em wrappers distintos pode fazer source identity, cache identity, evaluator,
    filter signature e cursor observarem estados diferentes durante save/replicação concorrente.

DL. resolveConfigForCache() ainda pode mutar options.config ao materializar userUUID, enquanto
    addon/index.ts usa _currentCatalogConfig/_currentSearch* como scratch state dentro da própria config.
    Correctness-critical context não pode depender de mutação incidental desse objeto.

DM. addon/lib/inProcessRoutes.ts executa catalog/meta handlers sem middleware e sem queue. Qualquer
    WorkBudget/admission/request-clock/config-snapshot instalado apenas na pilha HTTP pode ser bypassado
    pelo Jellyfin, criando uma segunda semântica operacional para a mesma source/filter pipeline.

DN. invokeRoute() usa Promise.race para timeout sem abortar o trabalho subjacente. Após o Jellyfin
    abandonar a chamada, provider fetch, revalidation, cursor write ou cache write ainda pode continuar,
    consumindo budget e produzindo efeitos tardios fora do lifecycle que originou a request.

DO. jellyfin/items.ts possui failedPages como estado transitório real que influencia se uma source page
    será sequer consultada. A V18 modelava pageLengths/catalogLengths/walkCursors/memberCursors, mas não
    esse negative/backoff state. Failure suppression não pode virar source exhaustion implícita nem cruzar
    um paging/filter/source scope incompatível.

DP. A validade temporal termina hoje no cursor/cache interno. Uma resposta policy-specific também pode
    ser retida por browser/player/reverse proxy/CDN. O contrato de response caching precisa garantir que
    nenhum response continue reutilizável além de config/source/filter/nextTransitionAt aplicáveis.

DQ. O request context precisa permanecer coerente também em chamadas internas, warmers e nested catalog
    execution. "A rota principal passa { config }" não é prova suficiente; cada caller de wrappers que
    podem resolver config precisa ser classificado como snapshot-bound ou explicitamente independente.

DR. Timeout, 429, budget exhaustion, Redis/transient failure e abort do in-process route precisam continuar
    pertencendo à taxonomia transient failure, nunca a upstreamExhausted. failedPages/backoff não pode
    escrever end-of-source/cursor/catalogLength como se a origem tivesse terminado.
```

---

# 445. RequestConfigSnapshot — nova autoridade única por request

Criar um conceito explícito, mesmo que a implementação use nomes diferentes:

```ts
interface RequestConfigSnapshot {
  readonly userUUID: string;
  readonly config: Readonly<UserConfig>;

  /**
   * Revisão user-scoped para detectar mudança de configuração quando útil.
   * Não substitui source/filter signatures e não entra genericamente em shared neutral caches.
   */
  readonly configRevision: string | number | null;

  readonly evaluationClock: RequestEvaluationClock;
  readonly effectiveTimezone: string;
}
```

O snapshot deve nascer uma única vez no boundary da request lógica:

```text
load stored/shared config
        ↓
request-owned clone / profile scope / install overrides
        ↓
runtime normalization idempotente
        ↓
materializar userUUID + configRevision
        ↓
capturar RequestEvaluationClock/effectiveTimezone
        ↓
freeze/immutability guard dos campos correctness-critical
        ↓
RequestConfigSnapshot
```

Todos os consumers abaixo devem derivar do **mesmo snapshot**:

```text
catalog/source execution
search execution
cache wrapper config projection
EffectiveSearchSourceContext
EffectiveTmdbDiscoverSourceContext
CanonicalFilterContext
release-region resolution
RequestEvaluationClock
evidence completion
sourceMembershipSignature
filterSignature
paginationContractSignature
JellyfinPagingScope
logs/metrics/reason codes
```

## 445.1. O que o snapshot NÃO significa

Não usar `configRevision` como atalho para tudo:

```text
shared neutral catalog/search cache
→ continua keyed por source semantics reais, não por configVersion inteiro.

filterSignature
→ continua descrevendo membership pós-cache.

configRevision
→ somente safety invalidator user-scoped quando necessário.
```

Uma alteração irrelevante como cor/arte/label não deve invalidar shared neutral payload por acidente.

## 445.2. Cross-region config cache

O snapshot garante **coerência intra-request**, não linearizabilidade global da configuração.
Se a arquitetura existente aceita Redis de config regional com invalidação limitada por TTL:

```text
replica A pode observar config nova
replica B pode observar config anterior por janela bounded
```

isso deve ser tratado como consistency contract existente, não escondido.

Obrigatório:

```text
- dentro de cada request, todos os componentes usam uma única revisão observada;
- filter/source signatures impedem cursor/cache incompatível mesmo se duas replicas observarem revisões diferentes;
- nenhuma request mistura metade da revisão A com metade da revisão B;
- observabilidade registra configRevision sem incluir secrets;
- se o produto exigir read-after-write global imediato para releaseRegion, isso é feature de config
  invalidation/replication separada e precisa de mecanismo explícito, não suposição.
```

---

# 446. RequestExecutionContext — scratch state não pertence ao config persistido

Os campos atuais:

```text
_currentCatalogConfig
_currentSearchType
_currentSearchCatalogId
_searchLight
```

são request execution state, não user configuration.

V19 recomenda separar:

```ts
interface RequestExecutionContext {
  readonly configSnapshot: RequestConfigSnapshot;
  readonly surface: 'catalog' | 'search' | 'meta' | 'preview' | 'warmer' | 'jellyfin';
  readonly catalogConfig?: Readonly<CatalogConfig> | null;
  readonly searchCatalogId?: string | null;
  readonly searchType?: string | null;
  readonly searchLight?: boolean;
  readonly workBudget: WorkBudget;
  readonly signal: AbortSignal;
}
```

Alternativa aceitável para migração incremental:

```text
request-owned overlay object
= { ...snapshot.config, _current... }
```

contanto que:

```text
- snapshot original nunca seja mutado;
- overlay não volte para configCache/database;
- overlay não seja compartilhado entre requests;
- nested/parallel source execution não escreva scratch fields concorrentes no mesmo objeto;
- signatures recebam inputs explícitos e nunca leiam _current* implicitamente.
```

## 446.1. resolveConfigForCache

`resolveConfigForCache()` deve obedecer:

```text
options.configSnapshot presente
→ usar snapshot.config sem mutá-lo.

options.config presente durante migração
→ tratar como request-owned; userUUID precisa já vir materializado OU criar overlay, não mutar
  um objeto que possa ser considerado immutable/shared.

nenhuma config fornecida
→ loadConfigFromDatabase permitido apenas para callers classificados como request boundary
  ou background job que deliberadamente cria seu próprio snapshot.
```

Proibido em correctness-critical path:

```text
wrapper A carrega config A
provider method usa config B já capturada
filter usa config B
cursor usa config A
```

## 446.2. Parallel/nested catalog safety

Merged/warmer/Jellyfin podem executar múltiplas sources em paralelo.
Teste obrigatório:

```text
source A + source B compartilham RequestConfigSnapshot
→ cada source possui RequestExecutionContext próprio
→ nenhuma escreve _currentCatalogConfig no objeto comum
→ cache/source/filter signatures permanecem determinísticas independentemente da ordem de completion.
```

---

# 447. In-Process Route Parity Gate

`addon/lib/inProcessRoutes.ts` entra agora como arquivo obrigatório da #742.

A propriedade desejada é:

```text
HTTP catalog request
≡
Jellyfin in-process catalog invocation
```

para todos os aspectos correctness-critical, exceto transporte HTTP que não existe no caminho interno.

Paridade mínima:

```text
same config snapshot semantics
same profile/install overrides aplicáveis
same RequestEvaluationClock/effective timezone
same source context
same release evidence authority
same filter context
same paging/source/filter signatures
same release visibility decision
same response hygiene
same WorkBudget/provider budgets
same retry classifier
same admission/backpressure policy
same cancellation semantics
same cursor write rules
same observability dimensions sem secrets
```

## 447.1. Arquitetura preferida

Preferir extração de core compartilhado:

```text
HTTP adapter ─────────┐
                      ▼
              executeCatalogRequest(ctx)
                      ▲
Jellyfin adapter ─────┘
```

E analogamente para meta quando necessário.

Assim `invokeRoute()` deixa de simular partes do Express para conseguir paridade e passa a ser, no máximo,
um adapter fino sobre o mesmo core.

## 447.2. Se invokeRoute permanecer

Então ele precisa construir/receber explicitamente:

```text
RequestConfigSnapshot
RequestExecutionContext
RequestEvaluationClock
AbortSignal
WorkBudget
admission lease
profile/install scope
```

Nenhuma dessas garantias pode depender de middleware que o próprio `invokeRoute()` não executa.

## 447.3. Request-auth

O caminho in-process atualmente usa `runWithRequestAuth(false, ...)`.
Isso não deve ser reinterpretado como autorização para remover user/profile semantics do catálogo.

Separar:

```text
request transport auth/session
≠
user config/profile/filter scope
```

O Jellyfin adapter continua responsável por fornecer o user/profile scope que a operação precisa.

---

# 448. Abort Propagation Gate — timeout precisa cancelar trabalho

Um `Promise.race()` que rejeita após `JELLYFIN_ROUTE_TIMEOUT_MS` não encerra o handler que perdeu a corrida.
V19 torna isso correctness/operational-critical.

Contrato:

```ts
const controller = new AbortController();

invoke(..., {
  signal: controller.signal,
  workBudget,
});

on timeout/client abort:
controller.abort(reason);
```

O signal precisa alcançar, quando tecnicamente possível:

```text
provider fetch / HTTP request
release evidence revalidation
TMDB detail projection
retry/backoff sleep
meta hydration fan-out
filtered page fill loop
merged source loops
warmer/internal nested execution quando request-owned
```

## 448.1. Efeitos tardios

Depois do abort:

```text
não criar cursor novo para a request abortada;
não avançar walk cursor como se resposta tivesse sido entregue;
não marcar source exhausted por trabalho interrompido;
não registrar success/failure metric como request concluída normalmente;
não manter admission lease ocupado;
```

Raw factual write iniciado antes do abort só pode completar se:

```text
- write é monotonic/CAS;
- fato é user/policy-neutral;
- lifecycle está explicitamente classificado como detachable safe work;
```

Caso contrário, aborta junto.

## 448.2. Retry/backoff

Backoff deve ser abort-aware:

```text
sleep(delay, signal)
```

não:

```text
await new Promise(resolve => setTimeout(resolve, delay))
```

quando aquele retry pertence ao budget da request.

## 448.3. Leak test

Teste de fault injection:

```text
Jellyfin route timeout em T
→ caller recebe timeout
→ active request/provider/admission gauges retornam ao baseline
→ nenhum retry inicia depois de T
→ nenhum cursor/end-of-source é persistido
→ nenhuma fila continua crescendo por requests já abandonadas.
```

---

# 449. Jellyfin Failure-State Closure

`failedPages` é um estado operacional que altera comportamento futuro e, portanto, entra no ledger.

## 449.1. Classificação semântica

```text
failedPages hit
→ transient source backoff
→ NÃO upstreamExhausted
→ NÃO empty source
→ NÃO source page length = 0 factual
→ NÃO catalog length final
```

## 449.2. Scope

Não usar URL nua como única correctness identity se o conteúdo daquela URL pode mudar pela configuração
sem mudar a URL externa.

Derivar a key do mesmo escopo conceitual usado pelo Jellyfin paging:

```text
JellyfinFailureScope = strongHash({
  userScope,
  catalog/source identity,
  sourceMembershipSignature,
  filterSignature,
  paginationContractSignature,
  profile/install tags,
  relevant extras,
});
```

`configRevision` pode entrar apenas como safety invalidator user-scoped quando necessário; preferir as
assinaturas semânticas.

## 449.3. Failure classes

Distinguir no mínimo:

```text
timeout / abort
budget exhausted
provider 429 / Retry-After
provider 5xx / network
Redis transient
invalid response / corruption
permanent invalid catalog/source
```

Somente uma classe realmente permanente e provada pode evitar retry de forma equivalente a source-invalid.
Nenhuma classe transitória vira source exhaustion.

## 449.4. TTL/backoff

`JELLYFIN_CATALOG_RETRY` continua podendo limitar churn, mas:

```text
- respeita Retry-After quando aplicável;
- é bounded pelo lifecycle da config/source scope;
- mudança de filter/source signature não herda o backoff anterior;
- não sobrevive rollback/schema incompatível;
- possui reason metric agregada.
```

## 449.5. Interação com length/walk state

Se `fetchCatalogPage()` falhar:

```text
Window.failed=true
ou estado equivalente
```

e o caller deve propagar failure separadamente de:

```text
items=[] + exhausted=true
```

Nunca persistir `catalogLengths`, `pageLengths` ou `walkCursors` como conclusão factual derivada apenas de
um failedPages hit/timeout/budget failure.

---

# 450. Response Freshness / Transport Cache Contract

A V18 calcula `nextTransitionAt`, source stability e cursor validity, mas a decisão também precisa sobreviver
ao boundary de transporte.

## 450.1. Regra geral

Para resposta que contém membership policy-specific:

```text
responseReuseUntil <= min(
  config validity quando aplicável,
  source page stability,
  evidence freshness boundary,
  nextTransitionAt,
  runtime dynamic-state boundary
)
```

A estratégia mais simples e atualmente compatível para catálogo/meta policy-sensitive é:

```text
Cache-Control: no-cache, must-revalidate, max-age=0
```

ou `no-store` quando apropriado.

A V19 não exige adicionar cache HTTP agressivo; exige **não enfraquecer** a garantia existente sem tornar
essa nova camada temporalmente correta.

## 450.2. Se no futuro houver max-age > 0

Obrigatório:

```text
maxAgeSeconds = floor(max(0, responseReuseUntil - now))
```

com ceiling operacional menor se desejado.

Além disso:

```text
- shared proxy cache não pode misturar users/configs;
- Vary/cache key deve carregar toda dimensão necessária OU a resposta deve ser private/no-store;
- 304/ETag/Last-Modified não pode validar uma resposta além de responseReuseUntil;
- response cache não substitui read-time cursor/evidence validation.
```

## 450.3. Search

Search entregue pela rota de catálogo herda a mesma regra.
Neutral Search Cache interno pode ser longo; **a resposta filtrada ao usuário não pode** ser retida como se
fosse neutral.

## 450.4. Discover Preview

Preview é dynamic source projection e pode depender de relative-date tokens/clock.
Então:

```text
preview response
→ no-store/no-cache
```

é o baseline recomendado.

Se houver caching:

```text
previewTemporalRevision
+ effective timezone
+ logical source signature
+ projection revision
```

precisam participar da identity e a TTL nunca cruza a próxima transition boundary.

## 450.5. Jellyfin

As rotas Jellyfin que retornam listas policy/user-specific devem continuar não compartilháveis entre users.
O In-Process path não possui cache HTTP, mas seus `pageLengths/catalogLengths/walkCursors/failedPages`
constituem o equivalente interno e continuam sujeitos aos gates anteriores.

---

# 451. Mandatory File / Caller / Occurrence Map V19

Somar ao mapa V18:

```text
addon/lib/inProcessRoutes.ts                         # NOVO obrigatório
addon/lib/requestSession.ts                          # audit: auth/context propagation
addon/index.ts                                       # catalogRoute/respond/cacheOptions/request annotations
addon/lib/getCache.ts                                # resolveConfigForCache + all wrapper consumers
addon/lib/configApi.js                               # snapshot load boundary
addon/lib/configCache.ts                             # shared-readonly semantics
addon/lib/configAccess.ts                            # config access helpers
addon/lib/jellyfin/items.ts                          # invokeRoute/failedPages/routeTimeout/paging state
addon/lib/jellyfin/context.ts                        # profile-scoped config boundary
addon/lib/jellyfin/profiles.ts                       # scopeConfigToProfile
addon/lib/jellyfin/index.ts                          # HTTP no-store/admission boundary
addon/lib/jellyfin/collections.ts                    # member paging/failure propagation
addon/lib/comprehensiveCatalogWarmer.js              # background snapshot/admission parity
addon/lib/malCatalogWarmer.js                        # background config snapshot parity
addon/lib/cacheWarmer.js                             # synthetic snapshot/defaults
```

## 451.1. Occurrence terms adicionais

```text
resolveConfigForCache
loadConfigFromDatabase
loadSharedConfig
options.config
_currentCatalogConfig
_currentSearchCatalogId
_currentSearchType
_searchLight
registerInProcessRoute
invokeRoute
Promise.race
JELLYFIN_ROUTE_TIMEOUT_MS
failedPages
JELLYFIN_CATALOG_RETRY
pageLengths
catalogLengths
walkCursors
Cache-Control
Last-Modified
ETag
AbortController
AbortSignal
signal
```

## 451.2. Classification rule

Toda ocorrência deve terminar em exatamente uma classe:

```text
A = changed by #742/V19
B = covered by shared abstraction and fixture
C = deliberate no-op with written rationale
D = test-only / generated / documentation occurrence
```

Zero ocorrência correctness-relevant sem classificação.

## 451.3. Wrapper caller closure

Para cada caller de:

```text
cacheWrapCatalog
cacheWrapSearch
cacheWrapMeta
cacheWrapMetaComponents
reconstructMetaFromComponents
cacheWrapMetaSmart
```

provar uma das duas condições:

```text
1. recebe o RequestConfigSnapshot/request-owned config do operation boundary;
OU
2. é background/request boundary deliberado e cria exatamente um snapshot antes de continuar.
```

Nenhum caller pode recarregar config no meio da mesma operação lógica sem design explícito.

---

# 452. Test Matrix V19

Adicionar aos 336+ casos V18:

```text
337. request carrega config BR; save muda para US no meio da execução
     → source/cache/filter/cursor da request inteira continuam BR.

338. request seguinte após observar config US
     → source/filter signatures US; nenhum cursor BR é reutilizado.

339. duas replicas observam config revisions diferentes dentro da janela de cache
     → cada request é internamente coerente; signatures distintas impedem cross-reuse incorreto.

340. resolveConfigForCache(options.configSnapshot)
     → zero mutation do snapshot.

341. config snapshot deep-freeze + cacheWrapCatalog/search/meta-smart
     → zero write em userUUID/_current*/campos persistidos.

342. userUUID ausente no config de entrada
     → overlay/context materializa userUUID sem mutar shared snapshot.

343. merged parallel source A/B
     → contexts independentes; completion order não altera signatures/output membership.

344. search + catalog concorrentes para mesmo usuário
     → _currentSearch* não contamina catalog context e vice-versa.

345. warmer cria snapshot uma vez por config/run
     → wrappers internos não recarregam revisão diferente no meio da operação.

346. HTTP catalog vs Jellyfin in-process com fixed config/clock/source fixtures
     → mesma lista/ordem antes da conversão Jellyfin.

347. HTTP search vs Jellyfin Search/Hints equivalente
     → mesma release visibility membership.

348. HTTP e in-process recebem o mesmo RequestEvaluationClock fixture
     → midnight/365d/release-day decision idêntica.

349. in-process path usa o mesmo WorkBudget/provider budget
     → detail/revalidation fan-out não excede cap HTTP.

350. admission saturated
     → HTTP e in-process obedecem a mesma policy de reject/queue/degrade.

351. invokeRoute timeout
     → AbortSignal dispara e provider request é cancelada quando suportado.

352. timeout durante retry backoff
     → nenhum retry posterior inicia.

353. timeout durante filtered page fill
     → nenhum cursor de progresso é gravado para resposta não entregue.

354. timeout durante local TV runtime projection
     → projection para, budget é liberado, source não vira exhausted.

355. timeout durante raw release revalidation
     → stale-negative nunca autoriza HIDE; detached write só ocorre se monotonic/neutral-safe.

356. 100 timeouts concorrentes
     → active gauges/semaphores retornam ao baseline; zero leak de admission lease.

357. failedPages timeout entry
     → classificado transient, não upstreamExhausted.

358. failedPages 429
     → Retry-After/backoff respeitado, sem catalogLength final.

359. failedPages Redis/network 5xx
     → retry scope transient, sem end-of-source.

360. config BR falha e entra failedPages; config muda para US antes do TTL
     → US scope não herda failure suppression BR.

361. filterSignature muda por hide flag
     → novo JellyfinFailureScope não herda failedPages antigo.

362. sourceMembershipSignature muda por Discover params
     → failure scope antigo não bloqueia nova source.

363. failedPages hit em first page
     → Window.failed equivalente; não grava catalog length=0.

364. failedPages hit em middle page
     → walk cursor anterior preservado; não avança para fim.

365. request abortada antes de responder
     → response metrics distinguem aborted de empty/exhausted.

366. catalog response atual
     → Cache-Control continua no-cache/must-revalidate/max-age=0 ou policy mais estrita.

367. search response filtrada
     → não recebe shared/public max-age que possa sobreviver à transition boundary.

368. release date cruza nextTransitionAt enquanto client revalida
     → nova membership é observada; resposta anterior não recebe 304 indevido.

369. config releaseRegion muda BR→US
     → response validator/cache policy não mantém resposta BR reutilizável como US.

370. Preview relative token perto da meia-noite
     → response não permanece fresh além da próxima revision boundary.

371. reverse-proxy simulation com public cache habilitado por engano
     → integration gate falha se duas configs/users compartilharem response policy-specific.

372. in-process response hygiene
     → _releaseAvailability/internal reason/provenance não vaza ao Jellyfin body.

373. background warmer sem request socket
     → cria background OperationContext próprio com clock/budget/snapshot explícitos.

374. wrapper caller closure
     → todos os resolveConfigForCache consumers classificados; zero implicit mid-operation reload.

375. abort após upstream success mas antes de raw CAS
     → somente monotonic neutral-safe write pode completar; nenhum policy/cursor effect tardio.

376. abort após filter computation mas antes de response
     → nenhum delivered-cursor/walk-state é confirmado como se cliente tivesse recebido a página.

377. HTTP adapter e in-process adapter property test
     → para inputs semanticamente iguais, core request result possui mesmo semantic digest.

378. occurrence gate V19
     → zero ocorrência não classificada para config/context/in-process/failure/transport terms.
```

A suite acumulada passa a ser descrita como **378+ casos**, além de parametrizações, golden-master,
property/fuzz, concurrency, multi-replica, load, fault-injection e suites preexistentes.

---

# 453. Definition of Done V19

Além de todo DoD V18:

```text
[ ] RequestConfigSnapshot existe conceitualmente e é único por operação lógica
[ ] configRevision não substitui source/filter/pagination signatures
[ ] resolveConfigForCache não muta snapshot correctness-critical
[ ] _currentCatalogConfig/_currentSearch* não são hidden authority de signatures
[ ] parallel/nested source execution não compartilha scratch mutation

[ ] addon/lib/inProcessRoutes.ts classificado no mandatory map
[ ] HTTP × in-process semantic parity test passa
[ ] in-process recebe RequestClock/config snapshot/WorkBudget/admission explícitos
[ ] middleware-only guarantees não são necessárias à correctness do core

[ ] invokeRoute timeout propaga AbortSignal
[ ] retry/backoff/provider/detail fan-out respeita abort
[ ] request abortada libera admission/semaphore/budget leases
[ ] late work não grava cursor/exhaustion/delivered state indevido

[ ] failedPages faz parte do Jellyfin failure-state ledger
[ ] failedPages key/scope inclui semantic paging identity suficiente
[ ] failedPages transient != exhausted
[ ] failure não fabrica catalogLength/pageLength/end-of-source
[ ] config/filter/source change não herda failure suppression incompatível

[ ] response transport freshness está explicitamente coberta
[ ] catalog/search policy-specific response não é public-cacheable além de validUntil
[ ] Preview dynamic response não cruza temporal revision boundary
[ ] HTTP validators não podem produzir 304 além da validade semântica

[ ] wrapper caller closure V19 = zero implicit mid-operation config reload
[ ] occurrence gate V19 = zero unclassified
[ ] 378+ accumulated test matrix passa
[ ] todos os gates V18 continuam passando
```

---

# 454. Final Pre-Merge Checklist V19

```text
[ ] dev ainda é 6e83e22ab9de5093f9918a1871157f401feebb03
    OU Rebase + Delta + Occurrence + Caller-Closure + todos os gates V15–V19 rerodados

[ ] issue #742 continua compatível com escopo
[ ] TMDB release_dates/discover docs revalidadas

[ ] uma request = um RequestConfigSnapshot
[ ] um RequestEvaluationClock compartilhado pelo snapshot/context
[ ] nenhum correctness path re-resolve config no meio da operação
[ ] nenhuma mutação _current* contamina contexto paralelo

[ ] HTTP adapter == in-process adapter no semantic core
[ ] WorkBudget/admission/retry/cancel parity confirmada
[ ] JELLYFIN_ROUTE_TIMEOUT_MS cancela trabalho, não apenas o waiter
[ ] abort leak/fault tests passam

[ ] failedPages é transient scoped state
[ ] failedPages nunca é source exhaustion
[ ] catalogLengths/pageLengths/walkCursors não são concluídos a partir de failure
[ ] config/filter/source revision quebra failure scope incompatível

[ ] response Cache-Control/validators respeitam temporal/config validity
[ ] search filtrada não vira shared public response cache
[ ] Discover Preview não fica stale através de midnight/source revision

[ ] Worldwide golden-master
[ ] BR/US/GB regional
[ ] Search/custom/merged/Jellyfin/in-process
[ ] Redis multi-replica/load/fault injection
[ ] dark deploy/homogeneous fleet
[ ] cache migration + kill switch + rollback drill
[ ] 378+ tests/gates aprovados
```

---

# 455. Resultado final da auditoria V19

## 455.1. O que mudou de verdade em relação à V18

A V18 já fechava o domínio funcional e distribuído central da #742 em nível muito alto. A V19 não
reformula release evidence, region semantics ou TMDB Discover. Ela fecha **boundaries de execução** que
podiam escapar da arquitetura mesmo com os evaluators corretos:

```text
1. config observada pela operação;
2. request-local scratch context;
3. adapter HTTP vs adapter in-process;
4. lifecycle/cancelamento após timeout;
5. negative/backoff state específico do Jellyfin;
6. lifetime da resposta depois que ela sai do backend.
```

## 455.2. Estado final

```text
V19 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,

      preservando integralmente V18 e acrescentando:

      - RequestConfigSnapshot / intra-request config coherence;
      - RequestExecutionContext sem hidden mutable config authority;
      - resolveConfigForCache caller closure;
      - HTTP × Jellyfin in-process semantic parity;
      - admission/WorkBudget parity fora do middleware;
      - AbortSignal/timeout lifecycle closure;
      - Jellyfin failedPages transient-state closure;
      - response transport/cache temporal validity;
      - 378+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V19:

> **A V19 cobre estaticamente o snapshot auditado até os boundaries de configuração, adapters HTTP e
> in-process, estado transitório de paginação Jellyfin e transporte da resposta, além de todas as closures
> acumuladas V8→V18. “100%” continua significando zero ocorrência/caller/authority conhecida sem
> classificação no snapshot e zero comportamento runtime/upstream/distribuído assumido sem gate executável;
> não significa afirmar infalibilidade de TMDB, rede, Redis, clock, clientes ou sistemas externos antes da
> execução dos testes definidos.**

Checklist ultra-curto V19:

```text
1. fixe HEAD/tree;
2. rerode todos os gates V18;
3. crie um RequestConfigSnapshot por operação;
4. remova scratch authority do config compartilhado;
5. faça HTTP/in-process chamar o mesmo semantic core;
6. propague admission/WorkBudget/clock/signal aos dois adapters;
7. transforme timeout em cancelamento real;
8. modele failedPages como transient scoped state;
9. feche response transport freshness/validators;
10. rode 378+ casos + golden/property/concurrency/load/fault;
11. dark deploy + homogeneous fleet;
12. kill-switch + rollback drill.
```
---

# 456. Reauditoria V20 — Conditional HTTP / Context Carrier / Shared-Work Lifecycle Closure

A V19 fechou corretamente os boundaries de config snapshot, scratch context, paridade in-process,
abort, `failedPages` e transport freshness em nível arquitetural. A reauditoria V20 do **mesmo snapshot**
`dev@6e83e22ab9de5093f9918a1871157f401feebb03` encontrou quatro classes adicionais que precisam ser
normativas antes da implementação:

```text
1. comportamento real de conditional requests do Express 5.2.1;
2. autoridade/propagação concreta do RequestExecutionContext;
3. ownership de cancelamento quando o trabalho é compartilhado por single-flight;
4. interação entre abort, error-cache, refresh-ahead e WorkBudget/admission.
```

A V20 **não muda** a semântica funcional da #742:

```text
Worldwide continua legado;
Regional continua CalendarDate + TMDB types 4/5/6;
UNKNOWN continua fail-open;
releaseRegion continua separado de watch_region;
series continua sem releaseRegion;
neutral cache continua antes de policy;
filtered paging continua dependente de source/filter/stability identity.
```

Ela fecha o lifecycle entre request, shared work, cache e transporte que ainda podia invalidar uma
implementação funcionalmente correta.

## 456.1. Snapshot revalidado

No momento desta V20:

```text
dev HEAD = 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA = 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
Tree = 583 entries / 544 blobs / 39 directories
Release = v3.1.0
Issue #742 = open / 0 comments
```

O `compare 6e83e22..dev` foi revalidado como idêntico. Portanto os findings abaixo não são drift:
são closure adicional do mesmo código auditado.

---

# 457. Blockers novos V20

Adicionar cumulativamente aos blockers históricos:

```text
DS. O código de `respond()` evita o ETag manual para catalog/meta, mas Express 5.2.1 habilita weak ETag
    por default e `res.send()` gera validator automaticamente. Logo "não setamos ETag" não é uma
    descrição correta do comportamento efetivo.

DT. `respond()` define `Last-Modified` de catalog/meta usando somente `configVersion`. Esse timestamp
    não muda quando membership muda por midnight, release evidence, source refresh, watched state ou
    outra boundary dinâmica. Além disso HTTP-date possui resolução de segundos. Conditional request
    baseada somente em `If-Modified-Since` pode validar uma representação semanticamente velha.

DU. V19 define `RequestExecutionContext`, mas não fixa o carrier/ownership contract. O snapshot possui
    `AsyncLocalStorage` em `requestSession.ts` apenas para auth. Uma implementação que passe parte do
    contexto por parâmetro e parte por hidden ALS/fallback pode reintroduzir mid-operation drift.

DV. O `singleFlight()` atual compartilha uma única Promise entre leader/waiters. Propagar o AbortSignal
    do primeiro caller diretamente ao shared factory faria o cancelamento de uma request derrubar
    trabalho ainda necessário por outras requests saudáveis. O lifecycle do waiter e do shared work
    precisa ser separado.

DW. O generic cache classifier atual classifica erros desconhecidos como `PERMANENT_ERROR`. Um
    `AbortError` de client/request abort cuja mensagem não contenha "timeout" pode portanto virar
    error-cache compartilhado se `enableErrorCaching` estiver ativo. Cancelamento request-owned nunca
    pode envenenar cache/source state para outro caller.

DX. `runRefreshAhead()` e qualquer trabalho detached/background podem sobreviver à request. Se V20 usar
    ALS para operation context, Node pode propagar contexto automaticamente para async resources filhos.
    Detached work não pode herdar silenciosamente signal, scratch, profile/filter policy ou lease da
    request que o disparou.

DY. WorkBudget/admission accounting precisa distinguir waiter cost de shared-work cost. Um provider call
    deduplicado por single-flight não deve consumir N vezes o mesmo provider budget, mas cada waiter
    continua sujeito ao seu próprio deadline/cancelamento. Release de admission lease também não pode
    acontecer enquanto o shared work real continua vivo.

DZ. O Response-Freshness Gate V19 precisa testar o stack HTTP real, não apenas headers calculados. A
    suíte deve atravessar `res.json/res.send -> ETag generation -> req.fresh -> 304`, inclusive requests
    com apenas `If-Modified-Since`, apenas `If-None-Match`, ambos, HEAD e dois config saves no mesmo segundo.
```

Esses blockers são de implementação/execução; não alteram os facts/evaluator definidos nas camadas anteriores.

---

# 458. Express Conditional Validator Gate — comportamento efetivo, não intenção do helper

## 458.1. Fatos do snapshot/dependency

O snapshot fixa:

```text
package.json: express ^5.2.1
package-lock.json: express 5.2.1
```

No Express 5.2.1:

```text
defaultConfiguration()
→ etag = weak

res.send(body)
→ gera ETag quando nenhum foi definido e etag fn está habilitado
→ depois avalia req.fresh
→ se fresh, transforma status em 304

req.fresh
→ considera ETag e Last-Modified para GET/HEAD
```

No AIOmetadata atual:

```text
respond()
→ não cria o ETag manual customizado para catalog/meta
→ MAS chama res.send(data)
→ portanto o ETag automático do Express continua possível

catalog/meta
→ Last-Modified = new Date(configVersion).toUTCString()
→ Cache-Control = no-cache, must-revalidate, max-age=0
```

Conclusão normativa:

> `no-cache` não elimina validators; ele exige revalidation. A correção depende de o validator representar
> a representação efetiva, não apenas a revisão da configuração.

## 458.2. Contrato para catalog/search policy-specific response

A opção de menor risco para esta feature é:

```text
1. executar o semantic core completo antes de qualquer decisão 304;
2. NÃO usar configVersion sozinho como Last-Modified de catálogo filtrado;
3. remover Last-Modified desse response OU derivá-lo de revision semanticamente completa;
4. permitir body-derived ETag somente se ele for calculado do body final já filtrado/sanitizado;
5. nunca reutilizar ETag de neutral/raw/source payload para response policy-specific;
6. manter Cache-Control que force revalidation; `private` é recomendado para response user-specific.
```

Baseline recomendado:

```http
Cache-Control: private, no-cache, must-revalidate, max-age=0
```

com:

```text
Last-Modified ausente para catalog/search policy-specific
OU semanticamente correto;
ETag opcional/body-derived após o filtro final.
```

`no-store` continua aceitável quando o produto preferir simplicidade máxima sobre conditional reuse.

## 458.3. Por que `configVersion` não basta

Membership pode mudar sem save de config:

```text
regional CalendarDate cruza meia-noite;
Worldwide cruza future-primary/365-day transition;
series premiere cruza timestamp;
release evidence revalida;
source page é refreshada/substituída;
watched/filter state muda;
provider fallback/source context muda;
cursor/source stability expira.
```

Logo:

```text
configVersion unchanged
≠
representation unchanged
```

## 458.4. Resolução de segundos

HTTP `Last-Modified` não carrega milissegundos.

O snapshot grava `configVersion` em ms, mas:

```ts
new Date(configVersion).toUTCString()
```

trunca efetivamente para resolução HTTP de segundos.

Dois saves no mesmo segundo não podem depender exclusivamente desse header para invalidação.

## 458.5. ETag automático não é necessariamente ruim

Se o ETag for calculado do **body final** depois de:

```text
source execution
filtered pagination
release visibility
watched/other filters
request-local projection
response hygiene
```

então uma mudança real de body produz validator diferente.

V20 não exige desligar o ETag global do Express. Exige que:

```text
- não exista early 304 antes do semantic core;
- o validator seja do response final daquela request;
- Last-Modified não forneça um atalho incorreto;
- nenhuma camada proxy/CDN use validator de neutral payload para response user-specific.
```

## 458.6. Manifest/meta/rotas não relacionadas

Não alterar indiscriminadamente o comportamento de todas as rotas nesta feature.

Classificar:

```text
catalog/search response afetada pela #742 → MUST satisfy V20 validator contract
TMDB Discover Preview                 → no-store/no-cache baseline V19
meta                                  → classificar separadamente; não herdar mudança por acidente
manifest/debug                        → manter contrato existente salvo finding independente
poster/art proxy                      → OUT OF SCOPE; possui validator contract próprio
```

---

# 459. Operation Context Carrier Gate

V19 definiu corretamente `RequestConfigSnapshot` + `RequestExecutionContext`. V20 torna obrigatória a
forma de propagação.

## 459.1. Regra de autoridade

Durante uma operação correctness-critical deve existir **um único root context**:

```ts
interface OperationContext {
  readonly requestId: string;
  readonly configSnapshot: RequestConfigSnapshot;
  readonly evaluationClock: RequestEvaluationClock;
  readonly signal: AbortSignal;
  readonly workBudget: WorkBudget;
  readonly profileScope: ProfileScope | null;
  readonly surface: SurfaceKind;
}
```

Child/source contexts derivam dele sem recarregar config:

```ts
child = deriveOperationContext(parent, {
  catalogConfig,
  searchSource,
  sourceIdentity,
});
```

## 459.2. Estratégia preferida

Preferência V20:

```text
adapter HTTP/Jellyfin/warmer
→ cria OperationContext
→ executeCatalogRequest(ctx, input)
→ helpers correctness-critical recebem ctx/context-derived args explicitamente
```

`AsyncLocalStorage` pode ser usado para cross-cutting concerns, mas não deve ser a única forma de um helper
obter config/filter/source identity quando a assinatura explícita puder carregar essa autoridade.

## 459.3. Se usar AsyncLocalStorage

O snapshot já possui ALS em `requestSession.ts` para auth. Existem duas opções aceitáveis:

```text
A. estender deliberadamente para um typed OperationContextStore;
B. criar store separado para execution context e manter auth store independente.
```

Requisitos:

```text
- nested invocation deriva/empilha contexto, não sobrescreve parent globalmente;
- nenhum fallback chama loadConfigFromDatabase dentro de active operation;
- ausência de context em helper que exige context é erro de programação/teste, não fallback silencioso;
- logs nunca serializam configSnapshot/secrets;
- context não é guardado em singleton/global mutable object;
- request end não deixa referência forte desnecessária a config/signal/payload.
```

## 459.4. Auth context não é semantic context

Continuar separando:

```text
runWithRequestAuth(false)
≠
sem user config
≠
sem profile scope
≠
sem releaseRegion
```

O child context do Jellyfin in-process deve carregar a semântica do usuário/profile mesmo quando transport auth
for deliberadamente `false`.

## 459.5. Background boundary

Quando uma operação realmente background/detached começar:

```text
não reutilizar implicitamente o ALS da request;
criar BackgroundExecutionContext explícito;
```

Isso é detalhado no Gate 462.

---

# 460. Shared Single-Flight Cancellation Gate

## 460.1. Problema

O snapshot possui:

```ts
singleFlight(key, factory, cloneResult = identity)
```

Todos os callers concorrentes da mesma key aguardam a mesma Promise/factory.

Depois que AbortSignal for propagado, isto seria incorreto:

```text
factory(signalDoLeader)
```

porque:

```text
leader cancela
→ shared fetch aborta
→ waiter B saudável perde trabalho que ainda precisava
```

## 460.2. Modelo correto

Separar:

```text
WaiterLifecycle
SharedFlightLifecycle
```

Conceitualmente:

```ts
interface SharedFlight<T> {
  promise: Promise<T>;
  controller: AbortController;
  activeWaiters: number;
  state: 'running' | 'settled';
}
```

Cada request:

```text
- registra um waiter;
- pode parar de esperar quando seu signal/deadline aborta;
- decrementa activeWaiters exatamente uma vez;
- NÃO aborta shared factory enquanto existir outro waiter vivo.
```

Underlying shared work:

```text
activeWaiters > 0
→ continua

activeWaiters == 0
→ aborta, salvo quando classificado explicitamente como detachable-safe background work
```

## 460.3. Leader não é especial

O caller que criou o flight é somente o primeiro waiter.

Teste obrigatório:

```text
leader aborta
waiter B continua vivo
→ factory continua
→ B recebe sucesso
→ leader recebe abort
```

## 460.4. Request-owned policy fica fora do shared factory

Sempre que possível:

```text
shared single-flight
→ raw/neutral/source work

request-owned stage
→ evidence policy completion quando user-specific
→ filter
→ pagination checkpoint
→ response projection
```

Não compartilhar uma factory cuja saída já dependa de:

```text
releaseRegion do caller
watched state do caller
profile/install filter
request clock específico não incluído na identity
request-local cursor state
```

## 460.5. Flight identity

A key do flight precisa usar a mesma strong source identity do cache/source operation.

Proibido:

```text
flight key mais fraca que cache key/sourceMembershipSignature
```

porque dois logical sources diferentes poderiam deduplicar o mesmo trabalho.

## 460.6. Shutdown

Process shutdown/drain:

```text
→ aborta shared flights em execução por shutdown signal
→ não espera eternamente por waiter count
→ métricas/leases fecham deterministicamente
```

---

# 461. Abort / Error-Cache Poisoning Gate

## 461.1. Finding concreto

O generic classifier atual diferencia:

```text
404
429
5xx/timeout/connection
restante → PERMANENT_ERROR
```

Um client/request `AbortError` típico pode possuir:

```text
name = AbortError
message = "This operation was aborted"
code = ABORT_ERR
```

sem conter `timeout`.

Se chegar a um wrapper com `enableErrorCaching=true`, não pode cair em:

```text
PERMANENT_ERROR → shared error TTL
```

## 461.2. Typed cancellation reason

Não inferir toda semântica por substring de mensagem.

Normalizar error/cancellation:

```ts
type FailureClass =
  | 'client-abort'
  | 'request-deadline'
  | 'attempt-timeout'
  | 'upstream-network'
  | 'upstream-429'
  | 'upstream-5xx'
  | 'redis-transient'
  | 'invalid-response'
  | 'permanent-request-error';
```

## 461.3. Cacheability da falha

```text
client-abort
request-deadline
→ SKIP_CACHE
→ nenhum error envelope compartilhado
→ nenhum source exhausted
→ nenhum negative release evidence
→ nenhum global failed/backoff state derivado apenas disso
```

`attempt-timeout`, `429`, `5xx`, network podem usar backoff/error-cache **somente** sob o contract já definido
para transient source failure, com scope correto e sem virar negative release evidence.

## 461.4. Outer cache poisoning

Mesmo quando o primitive TMDB classifica corretamente o abort, o outer wrapper também precisa preservar
essa classificação.

Exemplo:

```text
catalog cache miss
→ getCatalog
→ evidence/provider call recebe request abort
→ throw ClientAbortError
→ cacheWrapCatalog
```

Resultado obrigatório:

```text
request termina abortada
catalog:<neutral-key> não recebe PERMANENT_ERROR/TEMPORARY_ERROR por causa do caller abortado
```

## 461.5. Error envelope schema

Se error caching continuar:

```text
error envelope deve guardar failureClass versionada
```

não apenas `message/type/timestamp`, para read path não reclassificar contexto perdido.

Não guardar:

```text
raw secret
token
URL com API key
client abort reason com PII
```

---

# 462. Detached Work / Refresh-Ahead Context Gate

## 462.1. Categorias

Classificar async work em duas famílias:

```text
REQUEST_OWNED
DETACHED_BACKGROUND
```

### REQUEST_OWNED

```text
filtered page fill
release evidence completion necessária à resposta
mapping necessário à decisão
Jellyfin in-process request
request retry/backoff
cursor/checkpoint derivado da resposta
```

Herda:

```text
request deadline
request signal
request WorkBudget
request config snapshot
```

### DETACHED_BACKGROUND

Exemplos possíveis:

```text
refresh-ahead deliberado
warmer
maintenance
safe neutral refresh
```

Possui:

```text
próprio AbortController
próprio deadline
próprio WorkBudget/admission
source-safe snapshot
shutdown signal
```

## 462.2. ALS inheritance hazard

Se OperationContext usar AsyncLocalStorage, async work iniciado dentro da request pode herdar o store
automaticamente.

Portanto `runRefreshAhead()`/equivalente precisa entrar em boundary explícito:

```text
exit/clear request ALS
→ createBackgroundExecutionContext(...)
→ run detached work
```

Nunca herdar implicitamente:

```text
request.signal
request cursor
request scratch catalogConfig
request filterSignature
request response validator state
```

## 462.3. Config/source snapshot para refresh-ahead

Refresh-ahead pode capturar apenas o que a **source key** representa.

Se a source for global/neutral:

```text
não capturar releaseRegion/watch filter/profile policy
```

Se for legitimamente user/account scoped:

```text
capturar somente o account/source scope exigido
+ sourceMembershipSignature
+ credential reference/fingerprint seguro
```

Config nova salva depois não muda retroativamente a identity da refresh já iniciada; o resultado só pode
escrever na key cujo source snapshot originou aquele trabalho.

## 462.4. Parent abort

```text
request abort
→ REQUEST_OWNED work cancela
→ DETACHED_BACKGROUND não cancela automaticamente apenas por parent request abort
```

mas:

```text
process shutdown
kill switch relevante
source epoch invalidation quando exigido
→ detached work pode/deve abortar.
```

---

# 463. Shared WorkBudget / Admission Accounting Gate

V19 exige o mesmo WorkBudget/admission em HTTP e in-process. V20 fecha a interação com deduplicação.

## 463.1. Dois budgets

Modelar conceitualmente:

```text
RequestBudget
SharedFlightBudget
```

RequestBudget limita quanto tempo/trabalho aquele caller aceita esperar/consumir.

SharedFlightBudget limita o trabalho físico único executado para uma source key.

## 463.2. Regra de charging

```text
2 requests → mesma source flight → 1 provider call físico
```

Então:

```text
provider-call concurrency/admission
→ cobra 1 shared work unit

waiters
→ cada um cobra sua espera/request deadline
→ não duplica provider-call count físico
```

Não permitir o inverso:

```text
1 flight real ocupa slot
caller aborta e libera admission global
mas factory continua executando sem lease
```

Lease do underlying work pertence ao flight e só é liberado quando o flight termina/aborta de verdade.

## 463.3. Fanout

Para evidence completion de N metas:

```text
RequestBudget
→ limita quantos itens a request pode exigir

single-flight/source dedupe
→ reduz chamadas duplicadas entre requests

FleetBudget
→ limita total físico global
```

Os três níveis precisam ser observáveis separadamente.

## 463.4. Métricas

Adicionar no mínimo:

```text
shared_flight_active{kind}
shared_flight_waiters{kind}
shared_flight_join_total{kind}
shared_flight_abort_total{reason}
shared_flight_orphan_abort_total
request_waiter_abort_total{reason}
cache_error_skip_total{reason=client_abort|request_deadline}
background_context_start_total{kind}
background_context_abort_total{reason}
http_conditional_304_total{surface,validator}
http_conditional_forced_200_total{surface,reason}
```

Sem userUUID/token/region arbitrária de alta cardinalidade.

---

# 464. Dependency-Semantics Gate — Express é parte do correctness contract

O comportamento de conditional response usado pela #742 não está apenas no código do repositório; parte dele
vem de Express.

## 464.1. Lock-aware gate

Antes do merge e a cada mudança relevante de dependency lock:

```text
package-lock express version
Express default etag setting
res.send ETag generation
req.fresh semantics
304 conversion timing
```

precisam ser revalidados.

Não assumir que:

```text
"nosso helper não define ETag"
→ "nenhum ETag existe"
```

## 464.2. Rebase trigger

Adicionar ao snapshot invalidation:

```text
mudança de express/fresh/etag dependency
→ rerun Conditional-HTTP Gate
```

mesmo se nenhum arquivo da release visibility tiver mudado.

## 464.3. Teste black-box > implementação interna

A suíte principal deve provar comportamento via request HTTP real:

```text
GET catalog
→ captura validators
→ altera clock/evidence/config/source state
→ GET condicional
→ valida status/body
```

Testes unitários da função `respond()` sozinhos não fecham esse gate.

---

# 465. Mandatory File / Caller / Occurrence Map V20

Além de todos os maps V8→V19, classificar explicitamente:

```text
package.json
package-lock.json
addon/index.ts
addon/server.ts
addon/lib/requestSession.ts
addon/lib/inProcessRoutes.ts
addon/lib/getCache.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/cacheSourceRefetch.ts
addon/lib/getCatalog.ts
addon/lib/getSearch.ts
addon/lib/getMeta.js
addon/lib/getTmdb.ts
addon/lib/jellyfin/items.ts
addon/lib/jellyfin/context.ts
addon/lib/jellyfin/profiles.ts
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/cacheWarmer.js
addon/lib/malCatalogWarmer.js
```

External locked dependency behavior auditado:

```text
express@5.2.1/lib/application.js
express@5.2.1/lib/request.js
express@5.2.1/lib/response.js
```

Isso é evidence de dependency contract, não arquivo a ser modificado no PR.

## 465.1. Occurrence terms V20

```text
ETag
Last-Modified
If-None-Match
If-Modified-Since
req.fresh
res.send
res.json
app.set('etag'
app.disable('etag'

AsyncLocalStorage
runWithRequestAuth
RequestExecutionContext
RequestConfigSnapshot
loadConfigFromDatabase
loadSharedConfig

singleFlight
inFlightRequests
cloneJsonCompatibleResult
AbortController
AbortSignal
AbortError
TimeoutError
ABORT_ERR
Promise.race

classifyResult
enableErrorCaching
TEMPORARY_ERROR
PERMANENT_ERROR
SKIP_CACHE

runRefreshAhead
refreshAhead
setTimeout
WorkBudget
admission
```

Cada ocorrência/caller recebe:

```text
changed
covered-by-central-helper
explicit-no-op
out-of-scope-with-reason
test-only
```

Zero unclassified.

## 465.2. Direct conditional-response callers

Se outro helper além de `respond()` puder enviar catalog/search body diretamente, ele entra no mesmo gate.

Occurrence closure deve procurar:

```text
res.send(
res.json(
res.end(
writeHead(
status(304)
```

nas rotas relevantes.

---

# 466. Test Matrix V20 — casos acumulados 379–420

Adicionar aos 378+ casos V19:

```text
379. catalog response sem ETag manual → Express auto ETag é detectado/documentado pelo teste black-box.

380. mesmo body + If-None-Match correto
     → 304 permitido somente depois de semantic core/revalidation executar conforme contrato.

381. release regional cruza midnight; client envia ETag da resposta anterior
     → body muda → ETag muda → 200 com membership nova.

382. release regional cruza midnight; client envia SOMENTE If-Modified-Since da resposta anterior
     → não recebe 304 por configVersion estático.

383. evidence raw é revalidada e muda membership sem config save; If-Modified-Since-only
     → 200 com resposta nova.

384. source page refresh muda membership sem config save; If-Modified-Since-only
     → 200 com resposta nova.

385. dois saves de config dentro do mesmo segundo HTTP
     → validator não confunde as revisões.

386. If-None-Match + If-Modified-Since presentes e body mudou
     → nenhuma combinação produz 304 incorreto.

387. HEAD condicionado atravessa transition boundary
     → status/validators coerentes com GET equivalente.

388. Discover Preview dynamic token
     → no-store/no-cache conforme contrato; midnight não reutiliza preview velho.

389. leader e waiter B entram no mesmo single-flight; leader aborta
     → leader termina abortado; shared work continua; B recebe sucesso.

390. waiter B aborta; leader continua
     → factory não é cancelada; leader recebe sucesso.

391. único waiter aborta
     → underlying request-owned/shared flight sem consumidores é cancelado dentro do bound definido.

392. três waiters; dois abortam, um permanece
     → apenas o waiter restante recebe sucesso; provider call físico = 1.

393. last waiter aborta durante retry backoff
     → backoff aborta; nenhum novo attempt inicia.

394. last waiter aborta durante provider fetch
     → shared controller cancela fetch; lease fecha; gauges retornam ao baseline.

395. leader abort não transfere ownership incorreto de clone/request payload
     → waiter recebe RequestOwned independente.

396. client AbortError alcança cacheWrapCatalog com enableErrorCaching
     → SKIP_CACHE; zero error envelope Redis.

397. client AbortError alcança cacheWrapSearch
     → SKIP_CACHE; segunda request saudável executa normalmente.

398. request deadline alcança cacheWrapMeta/meta-smart
     → não grava PERMANENT_ERROR compartilhado.

399. per-attempt TMDB timeout com request viva
     → retry classifier transient conforme V14; não confundido com client abort.

400. client abort vence simultaneamente a per-attempt timeout
     → reason determinístico `client-abort`/request cancel; zero retry posterior.

401. cached error envelope antigo sem failureClass durante migration
     → tratado pela compatibility policy, nunca reinterpretado como release negative evidence.

402. refresh-ahead iniciado dentro de HTTP request usando ALS
     → background context não contém request.signal/cursor/filter scratch.

403. parent request aborta depois que detachable refresh foi legitimamente criado
     → refresh segue somente com seu próprio background budget/signal.

404. process shutdown
     → detached refresh/shared flights são abortados e leases fechados.

405. config é salva enquanto refresh-ahead antigo executa
     → resultado só escreve na source key antiga correspondente ao snapshot que iniciou o trabalho.

406. global neutral refresh
     → releaseRegion/profile/watch filter não aparece em background source context/key.

407. user-scoped refresh
     → somente source/account dimensions necessárias são preservadas; sem request policy acidental.

408. duas requests joinam um shared flight
     → provider admission physical charge = 1, não 2.

409. waiter aborta
     → waiter/request budget fecha; shared provider lease continua enquanto outro waiter existe.

410. shared flight termina
     → provider lease libera exatamente uma vez; sem negative active gauge.

411. nested Jellyfin in-process operation dentro de active request context
     → child context deriva snapshot/clock/profile sem sobrescrever parent.

412. helper correctness-critical chamado em active operation sem ctx explícito quando exigido
     → teste falha; não reload silencioso de config.

413. detached background work tenta ler request-local scratch via ALS
     → store ausente/isolado; teste detecta vazamento se houver.

414. HTTP request salva config no meio da operação
     → operation mantém snapshot antigo do início; próxima request vê config nova.

415. HTTP catalog e Jellyfin in-process joinam a mesma neutral source flight quando identities equivalem
     → source work pode deduplicar, policy stage permanece request-owned e sem cross-surface contamination.

416. HTTP BR/hide ON e HTTP US/hide ON compartilham mesma neutral source flight
     → cada request filtra com sua região; zero cache/error/abort cross-talk.

417. BR request aborta; US request permanece no mesmo flight
     → US não é cancelada e não herda error-cache/backoff do abort BR.

418. conditional-response occurrence test
     → nenhuma rota relevante envia 304 por validator que não represente o response final.

419. package-lock muda Express/fresh/etag dependency
     → CI/rebase gate exige rerun do Conditional-HTTP suite antes de aceitar coverage claim.

420. full fault test: shared flight + one abort + one waiter + Redis transient + midnight transition
     → nenhuma stale HIDE, nenhum poisoned error cache, nenhum cursor falso, waiter saudável obtém
       resultado coerente ou fail-open não-checkpointable segundo os contracts anteriores.
```

A suíte acumulada passa a ser:

```text
420+ casos determinísticos/golden/integration/concurrency/fault/load
+
property tests já definidos
+
black-box conditional HTTP tests V20.
```

---

# 467. Definition of Done V20

Além de todo DoD V8→V19:

```text
[ ] dev/HEAD/tree continuam exatamente no snapshot OU todos os gates reexecutados
[ ] issue #742 continua compatível com o escopo

[ ] comportamento Express conditional HTTP foi validado na versão lockada
[ ] catalog/search policy response não usa configVersion-only Last-Modified
[ ] nenhum If-Modified-Since-only produz stale 304 após temporal/evidence/source/config transition
[ ] body-derived ETag, se mantido, é do response final e só pode validar body equivalente
[ ] nenhuma early conditional shortcut pula semantic core necessário
[ ] Preview dynamic response possui no-store/no-cache baseline

[ ] existe um único OperationContext root por operação
[ ] configSnapshot/evaluationClock/signal/workBudget/profileScope possuem authority explícita
[ ] helper correctness-critical não reabre config por fallback durante active operation
[ ] auth ALS não é confundido com semantic/profile context
[ ] nested contexts são derivados, não globais/mutáveis

[ ] shared single-flight separa waiter lifecycle de underlying work lifecycle
[ ] abort de um waiter não cancela waiters saudáveis
[ ] last-waiter abort cancela underlying work salvo detached-safe classification explícita
[ ] leader não recebe tratamento privilegiado
[ ] shared flight key é tão forte quanto logical source identity

[ ] client-abort/request-deadline = SKIP_CACHE
[ ] AbortError não vira PERMANENT_ERROR/TEMPORARY_ERROR compartilhado por acidente
[ ] outer catalog/search/meta cache não é envenenado por cancellation do caller
[ ] error envelope/cache failure reason é typed/versioned quando persistido

[ ] refresh-ahead/background possui BackgroundExecutionContext próprio
[ ] detached work não herda request signal/filter/cursor scratch via ALS
[ ] detached work possui deadline/budget/admission/shutdown semantics próprias
[ ] config save durante background work não muda a key/authority daquele trabalho em voo

[ ] provider admission accounting cobra physical shared work uma vez
[ ] waiter/request accounting permanece individual
[ ] lease de shared work só libera quando underlying work realmente encerra

[ ] occurrence/caller gate V20 = zero unclassified
[ ] 420+ test matrix passa
[ ] todos os gates V19 continuam passando
[ ] dark deploy + homogeneous fleet + kill switch + rollback drill continuam válidos
```

---

# 468. Resultado final da auditoria V20

## 468.1. O que mudou de verdade em relação à V19

A V19 já era um plano muito forte e havia identificado corretamente que transport freshness, timeout e
in-process parity eram boundaries reais. A V20 encontrou três detalhes de execução que precisam ser
explicitados para que esses contracts sejam realmente implementáveis sem armadilha:

```text
1. Express adiciona conditional-validator behavior além do ETag manual do helper;
2. abort em trabalho single-flight não pode usar ownership do primeiro waiter;
3. cancellation não pode cair no generic error-cache como falha compartilhável;
4. context/background/admission precisam ter lifecycle próprio e explícito.
```

## 468.2. Estado final V20

```text
V20 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,

      preservando integralmente V19 e acrescentando:

      - Express 5.2.1 conditional-response reality closure;
      - configVersion-only Last-Modified prohibition for policy-specific responses;
      - explicit OperationContext carrier/ownership contract;
      - shared single-flight waiter-vs-work cancellation semantics;
      - abort/error-cache poisoning prevention;
      - detached refresh/background context isolation;
      - shared WorkBudget/admission accounting;
      - dependency-lock correctness gate;
      - 420+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V20:

> **A V20 cobre estaticamente o snapshot auditado até o comportamento efetivo do framework HTTP lockado,
> o carrier do contexto de execução, ownership de cancellation em trabalho compartilhado, error-cache,
> detached background work e accounting de admission, além de todas as closures V8→V19. “100%” significa
> zero ocorrência/caller/authority/dependency behavior conhecido sem classificação no snapshot e zero
> comportamento runtime/upstream/distribuído assumido sem gate executável. Não significa afirmar
> infalibilidade externa antes da execução dos 420+ testes/gates definidos.**

Checklist ultra-curto V20:

```text
1. fixe HEAD/tree + dependency lock;
2. rerode todos os gates V19;
3. implemente RequestConfigSnapshot + OperationContext root;
4. faça HTTP/Jellyfin/warmer derivarem contextos explícitos;
5. corrija Last-Modified/conditional-validator semantics de catalog/search;
6. mantenha body validator apenas no response final;
7. separe waiter abort de shared-flight abort;
8. torne client-abort/request-deadline não-cacheáveis;
9. isole refresh-ahead/background do request ALS/signal/policy;
10. cobre provider admission por physical work, não por waiter;
11. rode 420+ casos + property/concurrency/load/fault + conditional HTTP black-box;
12. dark deploy + homogeneous fleet + kill-switch + rollback drill.
```

---

# 469. Reauditoria V21 — HTTP Disconnect / Runtime / Loser-Lifecycle / Shutdown & Lease Closure

A V20 já era arquiteturalmente forte, mas a inspeção final do mesmo snapshot encontrou uma diferença
fundamental entre **cancelar a espera** e **encerrar o trabalho que ainda pode produzir efeitos**.
Essa diferença aparece em quatro lugares concretos do código atual:

```text
HTTP transport
→ ainda não existe uma authority única que converta disconnect real em AbortSignal da operação;

Promise.race timeouts
→ o caller deixa de esperar, mas o loser continua vivo se não receber/obedecer cancelamento;

refresh-ahead
→ o timeout local coincide com a expiração do lock distribuído e o lock não possui ownership/fencing;

shutdown/background
→ o processo pode avançar para flush/close de recursos enquanto work/timers anteriores ainda existem.
```

A V21 não altera a semântica funcional de release visibility definida anteriormente. Ela fecha o
**termination contract** que torna essa semântica confiável sob disconnect, timeout, concorrência,
rolling runtime e shutdown.

## 469.1. Snapshot de código permanece idêntico

```text
dev HEAD = 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA = 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
Release = v3.1.0
Issue #742 = open / 0 comments
```

Não houve drift de source code desde V20.

## 469.2. Snapshot de runtime NÃO é equivalente a snapshot Git

O repositório fixa apenas:

```text
package.json engines.node = >=24.0.0 <25
.nvmrc = 24
Dockerfile = FROM node:24-alpine
GitHub Actions = node-version: 24
```

Isso significa que o Git SHA não congela sozinho:

```text
Node patch version
Node core HTTP semantics
base-image digest
bundled runtime behavior
```

Além disso, o lock atual contém `@types/node` 25.x enquanto o runtime declarado é Node 24.
Type-check success, portanto, não é prova de disponibilidade do mesmo API no runtime mínimo.

A V21 transforma esse fato em Runtime-Semantics Gate executável.

---

# 470. Blockers novos V21

Adicionar cumulativamente a DS–DZ e a todos os blockers históricos:

```text
EA. O plano V20 exige `OperationContext.signal`, mas ainda não define de onde o signal HTTP nasce.
    Em Node moderno, `IncomingMessage`/`ServerResponse` possuem eventos `close` com semânticas distintas;
    usar `req.on('close')` ingenuamente pode interpretar request normalmente concluída como client abort.

EB. `IncomingMessage.signal` não pode ser assumido apenas porque o projeto aceita Node 24: ele foi
    introduzido durante a linha 24.x e sua semântica de conclusão normal foi corrigida posteriormente.
    O baseline `>=24.0.0 <25`, `node:24-alpine` e `node-version: 24` não congela essa capability.

EC. `@types/node` está em major 25 enquanto o runtime suportado é major 24. O compilador pode aceitar
    superfície que não exista no runtime mínimo; compile-time typing não pode ser runtime authority.

ED. `Promise.race()` não cancela automaticamente a Promise perdedora. Esse padrão existe em paths
    correctness/operational-critical (`inProcessRoutes`, `cacheRefreshAhead`, `lifecycle/shutdown`).
    Timeout de wait sem loser lifecycle explícito permite late write, late retry ou resource use após teardown.

EE. O modelo V20 de `SharedFlight` possui `running|settled`, mas não fecha a janela entre
    last-waiter abort e settlement. Um caller novo pode encontrar a entrada antiga e juntar-se a um flight
    que já está sendo abortado. A entrada precisa de estado `cancelling/non-joinable` e proteção ABA.

EF. `SharedFlightBudget` não pode ser herdado do primeiro waiter. Se o primeiro caller tem deadline curto
    e um segundo caller saudável tem deadline maior, usar o budget do leader recria leader privilege por
    outra via. O budget físico precisa ser source/fleet-owned e determinístico.

EG. `cacheRefreshAhead.ts` define `REBUILD_TIMEOUT_MS = LOCK_SECONDS * 1000`. Quando o wait local expira,
    o Redis lock pode expirar no mesmo instante e outro replica adquirir a mesma key, enquanto o rebuild
    antigo continua vivo porque `Promise.race` não o cancela.

EH. O refresh lock atual armazena valor constante `1`. Sem owner token, um worker atrasado não consegue
    provar que ainda possui o lock. Um `EXPIRE`/renew/release tardio pode atingir o lock já readquirido por
    outro worker; e um write tardio não possui fence contra a nova geração.

EI. `runRefreshAhead()` remove `inFlight`/decrementa `activeCount` quando o race termina, não quando o loser
    necessariamente morreu. Isso pode liberar admission/local dedupe enquanto trabalho físico ainda roda.

EJ. `shutdown.ts::closeOne()` usa `Promise.race` com timeout e, ao vencer o timeout, continua a sequência
    sem cancelar/joinar o closer perdedor. O shutdown atual possui apenas fases `traffic|resource`; por LIFO,
    flushers `metrics/jellyfin artwork` registrados depois do HTTP server executam antes do `server.close()`.
    Recursos podem ser fechados enquanto work ainda está vivo.

EK. Warmers/schedulers relevantes não possuem um contrato comum de quiescência. `cacheWarmer` não guarda
    o interval handle criado por `scheduleEssentialWarming`; `comprehensiveCatalogWarmer` agenda recursão
    por `setTimeout` sem ownership de shutdown; `malCatalogWarmer` guarda o interval mas não o initial timeout.
    Um shutdown pode impedir o work atual e ainda permitir que timer já armado inicie novo work.

EL. `requestTracker.middleware()` chama `trackOnce()` antes do `originalSend`. Em Express, `res.send()` pode
    avaliar freshness e transformar status 200 em 304 depois desse ponto. Logo telemetry/status pode registrar
    200 quando o wire response efetivo foi 304, justamente no gate de conditional HTTP introduzido pela V20.

EM. Provider metrics atuais podem registrar client/request abort como provider failure antes da taxonomy
    final de cancellation. Cancelamento owned pelo caller não deve degradar métricas de upstream nem alimentar
    health/backoff como se fosse falha factual do provider.

EN. O snapshot invalidation V20 observa source/dependency lock, mas não runtime flutuante. Mudança do Node
    patch/base-image efetivo pode alterar transport semantics sem qualquer commit no repositório.
```

---

# 471. HTTP Disconnect Signal Gate — uma única autoridade de client cancellation

## 471.1. Não usar `req.close` como sinônimo de client abort

Para request HTTP longa, a authority precisa representar:

```text
cliente/transport deixou de precisar da resposta
```

não:

```text
a mensagem de request terminou de ser lida normalmente
```

No Node moderno, `IncomingMessage` é separado do lifecycle da resposta. Em GET, o request pode estar
completamente recebido muito antes de catalog/search terminar.

Portanto é proibido implementar:

```ts
req.once('close', () => controller.abort());
```

como regra universal.

## 471.2. Baseline V21 compatível com todo `engines.node`

A #742 não precisa elevar a versão mínima do Node apenas para obter client cancellation.
Criar um adapter central, conceitualmente:

```ts
interface HttpCancellationBinding {
  signal: AbortSignal;
  dispose(): void;
}

bindHttpCancellation(req, res, shutdownSignal): HttpCancellationBinding
```

Contrato recomendado para o baseline atual:

```text
1. criar controller request-owned;
2. compor com global shutdown signal;
3. observar `res.finish` como conclusão normal do response;
4. observar `res.close`;
5. se `close` ocorrer antes de `finish`, classificar client-abort;
6. após finish/abort, remover listeners exatamente uma vez;
7. normal finish nunca aborta a operação retroativamente.
```

`res.writableFinished`/estado equivalente pode ser usado como safety check, mas o teste black-box de
socket disconnect é a authority final.

## 471.3. `IncomingMessage.signal` nativo

Pode ser usado somente se uma destas condições for verdadeira:

```text
A. engines/runtime mínimo for elevado para versão cuja semântica necessária esteja garantida;
OU
B. runtime feature/version gate provar a versão segura e houver fallback para versões anteriores.
```

No baseline V21, **presença da propriedade sozinha não basta**.

O motivo é histórico dentro do próprio Node 24:

```text
message.signal foi adicionado em 24.16.x;
a semântica foi ajustada em 24.20.x para não abortar após conclusão normal da mensagem.
```

Logo:

```text
Node 24.0–24.15 → API ausente;
Node 24.16–24.19 → API existe, mas não possui a semântica final assumida;
Node 24.20+       → pode ser usada se os testes do runtime passarem.
```

## 471.4. Composição de sinais

Não espalhar `AbortSignal.any()` ad hoc.
Criar helper único:

```ts
composeOperationSignal({
  clientSignal,
  requestDeadlineSignal,
  shutdownSignal,
}): AbortSignal
```

Para attempt de provider:

```ts
composeAttemptSignal({
  operationSignal,
  attemptTimeoutMs,
}): AbortSignal
```

A composição precisa preservar `signal.reason`/causa tipada.

## 471.5. In-process/Jellyfin

`invokeRoute()` constrói um objeto `req` sintético, não um `http.IncomingMessage` real.
Logo semantic core nunca pode depender de `req.signal` magicamente existir.

Regra:

```text
HTTP adapter     → bindHttpCancellation(...) → OperationContext.signal
Jellyfin adapter → controller/deadline próprio → OperationContext.signal
warmer           → BackgroundExecutionContext.signal
semantic core    → recebe somente ctx.signal
```

---

# 472. Runtime-Semantics / Type-Surface Gate

## 472.1. Runtime fingerprint obrigatório

Cada execução da suíte correctness-critical registra:

```text
process.version
process.versions
package-lock hash
express resolved version
undici resolved version
base-image ref/digest quando disponível
```

Esse fingerprint acompanha o evidence bundle do PR.

## 472.2. Matriz mínima

Enquanto `engines.node` permanecer:

```text
>=24.0.0 <25
```

a suíte precisa provar pelo menos:

```text
minimum supported Node 24.x relevante
+
runtime Node 24.x usado no container/CI de release
```

Se uma capability só existe em patch posterior, existem apenas duas soluções válidas:

```text
feature-detect + fallback coberto por teste
OU
raise engines.node e alinhar Docker/CI/docs.
```

## 472.3. Docker/CI floating tags

`node:24-alpine` e `node-version: 24` são selectors móveis.
Não tratá-los como runtime congelado.

Para esta feature, escolher um dos contracts:

```text
preferred/minimal-impact:
→ manter selectors atuais
→ usar adapter compatível com min engine
→ executar runtime-semantic tests a cada build relevante
→ registrar process.version no artifact/evidence

hardening opcional:
→ pin de patch/digest
→ política explícita de atualização periódica
```

## 472.4. `@types/node`

O lock atual resolve major 25 enquanto runtime é 24.
Recomendação de higiene:

```text
alinhar @types/node ao major 24
```

Mas mesmo isso não substitui teste no runtime mínimo, pois type packages representam uma linha de APIs e
não necessariamente a menor patch declarada em `engines`.

## 472.5. Rebase/runtime trigger

Rerun deste gate quando mudar:

```text
Dockerfile
.nvmrc
package.json engines.node
package-lock @types/node
package-lock undici
workflow node-version
base image efetiva
Node patch efetivamente usado na release
```

---

# 473. Promise-Race Loser Lifecycle Gate

## 473.1. Regra geral

Para todo `Promise.race()` em path que pode afetar catalog/search/release evidence/paging/cache/shutdown,
classificar a Promise perdedora em exatamente uma categoria:

```text
CANCEL_AND_JOIN
DETACH_EXPLICITLY
SIDE_EFFECT_FREE_OBSERVE
OUT_OF_SCOPE_WITH_REASON
```

Proibido:

```text
timeout venceu
→ caller segue
→ loser side-effecting fica sem owner
```

## 473.2. `CANCEL_AND_JOIN`

Usar quando o loser pertence à operação:

```text
abort loser
→ impedir novos retries/work
→ esperar quiescência/settlement dentro de drain grace
→ somente então liberar lease/admission/ownership
```

Exemplos:

```text
Jellyfin in-process handler request-owned
refresh rebuild que não foi promovido a background independente
shutdown closer antes de dependências serem fechadas
```

## 473.3. `DETACH_EXPLICITLY`

Só é válido se o loser:

```text
receber BackgroundExecutionContext novo
possuir budget/deadline próprio
estar registrado no BackgroundTaskRegistry
possuir commit authority/fence explícita
não herdar request ALS/signal/policy
ser abortável por shutdown
```

Não basta deixar a Promise rodando.

## 473.4. `SIDE_EFFECT_FREE_OBSERVE`

Só para work cuja continuação tardia não pode:

```text
escrever cache/state
consumir lease correctness-critical
iniciar retry encadeado
mudar source stability
usar recurso que o shutdown pode fechar
```

A classificação precisa estar documentada no occurrence ledger.

## 473.5. Timer cleanup não é work cancellation

Isto:

```ts
clearTimeout(timer)
```

limpa apenas o timer da race.
Não cancela a Promise adversária.

O gate testa o underlying work, não apenas ausência de timer.

---

# 474. Shared-Flight Rejoin / Budget Authority Gate

## 474.1. Estado do flight

Substituir o modelo mínimo:

```text
running | settled
```

por estado capaz de fechar cancellation ABA:

```ts
type FlightState = 'running' | 'cancelling' | 'settled';

interface SharedFlight<T> {
  readonly generation: string;
  readonly key: string;
  readonly controller: AbortController;
  readonly promise: Promise<T>;
  state: FlightState;
  joinable: boolean;
  activeWaiters: number;
  readonly budget: SharedFlightBudget;
}
```

## 474.2. Last waiter abort

Transição atômica conceitual:

```text
activeWaiters 1 → 0
→ mark joinable=false / state=cancelling
→ detach/remove entry da lookup de novos joiners
→ controller.abort(orphan-reason)
```

A ordem importa.

Não fazer:

```text
controller.abort()
→ esperar factory assentar
→ só então impedir novos joiners
```

## 474.3. Rejoin durante cancellation

Caller que chega depois de `joinable=false`:

```text
NÃO junta flight moribundo
→ cria/entra em nova generation para a mesma logical source key
```

O finalizer do flight antigo usa compare-by-identity/generation:

```text
old finally
→ nunca apaga a entry nova
```

Preservar a proteção já existente no `singleFlight()` atual contra finalizer antigo apagar Promise substituta.

## 474.4. Waiter registration

```text
signal já abortado antes do join
→ não incrementa activeWaiters
→ retorna cancellation imediatamente

join bem-sucedido
→ increment exatamente uma vez
→ decrement exatamente uma vez em success/error/abort
```

Contagem nunca fica negativa.

## 474.5. Budget físico não pertence ao leader

`SharedFlightBudget` é derivado de:

```text
source kind
provider policy
fleet admission
source-level attempt/deadline ceiling
```

Não de:

```text
deadline do primeiro request
região do primeiro request
profile do primeiro request
cursor do primeiro request
```

Cada waiter continua tendo seu próprio deadline.

Exemplo obrigatório:

```text
A cria flight, deadline 1s
B junta, deadline 5s
source budget permite 4s
A aborta em 1s
B continua
physical flight não morre por herdar deadline de A
```

## 474.6. Listener lifecycle

Todo listener adicionado a waiter signal deve ser removido no settlement/abort.
Stress test precisa provar:

```text
milhares de joins/aborts
→ zero listener leak
→ zero duplicate decrement
→ zero retained request context após settle
```

---

# 475. Refresh-Ahead Lease Ownership / Fencing Gate

## 475.1. Finding concreto do snapshot

Hoje:

```text
LOCK_SECONDS = 300
REBUILD_TIMEOUT_MS = LOCK_SECONDS * 1000
Redis lock value = '1'
withRebuildTimeout = Promise.race(rebuild, timeout)
```

Portanto existe uma janela real:

```text
T = 300s
→ Redis lock expira
→ timeout local rejeita
→ runRefreshAhead finally limpa inFlight/activeCount
→ rebuild antigo pode continuar
→ outro replica/worker pode adquirir a mesma key
→ dois writers físicos podem coexistir
```

## 475.2. Separar lease, deadline e cooldown

Não usar uma única key/TTL para três conceitos diferentes:

```text
execution lease
operation deadline
post-success/backoff cooldown
```

Modelo recomendado:

```text
refresh lease
→ ownership do work ativo
→ owner token aleatório/opaco
→ TTL > deadline + abort/drain safety margin OU renovação controlada

refresh deadline
→ AbortSignal do BackgroundExecutionContext

cooldown/backoff
→ key/state separado quando o produto quiser impedir novo refresh por período
```

## 475.3. Owner token

Acquire:

```text
SET refresh-lock:<key> <opaqueOwnerToken> NX PX <leaseMs>
```

Toda operação sobre lease precisa comparar owner:

```text
renew
release
expire/backoff mutation
```

Nunca executar `EXPIRE` cego em key que pode ter sido readquirida por outro worker.

## 475.4. Fencing de write

Owner token sozinho impede mexer no lock alheio, mas não impede um worker antigo que perdeu o lease de
escrever na cache depois.

Logo qualquer refresh que possa sobreviver à perda de lease precisa de um dos contracts:

```text
A. cancellation-confirmed:
   downstream honra signal;
   nenhuma write ocorre depois do abort;
   underlying work assenta antes de lease/admission ser liberado;

OU

B. fenced commit:
   cada lease recebe monotonic fence/generation;
   write final valida atomicamente que ainda possui generation/authority atual;
   stale worker perde o commit mesmo que termine depois.
```

Para cache compartilhada/distribuída, B é o hardening preferido quando não é possível provar cancelabilidade
end-to-end de todos os providers.

## 475.5. `inFlight` local

`inFlight.delete()` e `activeCount--` significam:

```text
physical work encerrou ou foi explicitamente detached/re-owned
```

não apenas:

```text
wait local terminou
```

## 475.6. Source/page stability

Refresh commit continua obrigado a obedecer todos os gates anteriores:

```text
source snapshot antigo escreve somente key antiga
page revision/stability contract
raw fetchGeneration monotônica
no policy-specific cache contamination
```

Fencing V21 não substitui generation/stability V13–V20; é a camada de ownership concorrente acima delas.

---

# 476. Shutdown Drain Ordering / Scheduler Quiescence Gate

## 476.1. Finding concreto

`addon/lib/lifecycle/shutdown.ts` aceita apenas:

```text
traffic
resource
```

executando cada grupo em ordem reversa de registro.

No `server.ts` atual, `http server` é registrado como traffic antes de `metrics` e `jellyfin artwork`.
Como traffic é revertido, flushers posteriores podem executar antes de `server.close()`.

Além disso:

```text
closeOne()
→ Promise.race(close(), timeout)
→ timeout marca failed
→ closer perdedor continua potencialmente vivo
→ sequência segue para outros resources
```

Isso não é suficiente para o lifecycle prometido pela V20.

## 476.2. Fases normativas V21

A implementação da #742 deve introduzir ordem semântica explícita, mesmo que os nomes internos sejam outros:

```text
1. ADMISSION_FREEZE
   - marcar shuttingDown
   - impedir novos detached/background jobs
   - cancelar timers/schedulers relevantes
   - iniciar stop de novas conexões/requests

2. EXECUTION_CANCEL_AND_DRAIN
   - abortar global shutdown signal
   - abortar request/shared/background work registrado
   - aguardar task registry/shared flights
   - force-close transport se grace expirar

3. FLUSH
   - metrics
   - jellyfin remembered artwork
   - meta cold-store pending buffers
   - outros buffers que dependem de storage vivo

4. RESOURCE_CLOSE
   - Redis
   - database
   - demais recursos base
```

Não depender de ordem acidental de `register()` para expressar dependency graph.

## 476.3. HTTP server stop vs abort de work

`server.close()` sozinho pode esperar requests ativas.
O drain não pode esperar indefinidamente por work que só termina quando recebe shutdown abort.

Contrato:

```text
freeze admission
+
iniciar server.close
+
abort global operation signal
+
await execution drain dentro da mesma grace window
```

Se grace expirar:

```text
force transport close quando apropriado
marcar forced shutdown
não continuar uma longa teardown assíncrona fingindo que work já morreu
```

## 476.4. BackgroundTaskRegistry

Criar registry único para work relevante à feature:

```ts
interface BackgroundTaskHandle {
  kind: string;
  promise: Promise<unknown>;
  controller: AbortController;
  sourceKey?: string;
}
```

O registry precisa:

```text
freeze()            → rejeita novos tasks
drain(signal/deadline)
abortAll(reason)
activeCount()
```

Refresh-ahead/warmers relevantes entram nele.

## 476.5. Scheduler handles

Requisitos específicos do snapshot:

```text
cacheWarmer.scheduleEssentialWarming
→ guardar interval handle
→ clear no stop/shutdown
→ stop flag não pode ser resetado por callback já enfileirado após shutdown

comprehensiveCatalogWarmer.scheduleNextWarmup
→ guardar recursive timeout handle
→ clear no stop/shutdown
→ stop quando idle também impede futuro timer

malCatalogWarmer
→ guardar/clear initial delay timeout além do intervalHandle
```

Warmers fora do escopo da #742 recebem classificação explícita, não reforma indiscriminada.

## 476.6. Resource safety invariant

```text
Redis/database close
→ só depois que nenhum release/catalog/search work registrado puder iniciar nova operação nesses recursos
```

Se o drain falhar, o shutdown reporta isso como **forced termination**, não como graceful close bem-sucedido.

---

# 477. Cancellation Commit Authority / Provenance Gate

## 477.1. Typed reason é authority

Adicionar reason de baixa cardinalidade, por exemplo:

```ts
type CancellationReason =
  | 'client-abort'
  | 'request-deadline'
  | 'attempt-timeout'
  | 'last-waiter'
  | 'background-deadline'
  | 'shutdown'
  | 'kill-switch'
  | 'source-invalidated';
```

`AbortController.abort(reason)`/`signal.reason` deve carregar a authority quando possível.

Fallback por `name/code/message` existe apenas para erros de libs externas que perderam provenance.
Não classificar cancellation por substring genérica `abort` se a operação possui signal autoritativo.

## 477.2. Commit depois do cancelamento

Todo estágio side-effecting define seu commit contract:

```text
request-local response/cursor/checkpoint
→ nunca commit depois de request cancellation

shared neutral factual write
→ só pode commit se detachable-safe + monotonic/CAS/fence + source identity ainda válida

background refresh
→ commit somente enquanto background authority/fence válida

error-cache/backoff
→ nunca derivado de client-abort/request-deadline
```

## 477.3. Abort entre compute e write

Teste obrigatório para a janela:

```text
provider retorna sucesso
→ signal aborta
→ antes do SET/checkpoint
```

A decisão deve ser explícita por stage.
Não aceitar comportamento acidental dependente de microtask timing.

## 477.4. Provider health/metrics

Separar:

```text
upstream failed
caller cancelled
```

Client/request abort:

```text
não incrementa provider failure health counter
não cria rate/backoff penalty
incrementa cancellation metric apropriada
```

Attempt timeout com request ainda viva continua upstream/transport transient conforme V14/V20.

---

# 478. Response Finalization / RequestTracker Gate

## 478.1. Finding concreto

O middleware atual faz:

```text
res.on('finish', trackOnce)
+
res.send = function(data) {
  trackOnce();
  return originalSend(data);
}
```

Para response que Express converte condicionalmente:

```text
status antes de originalSend = 200
originalSend/res.send
→ calcula validator/freshness
→ pode mudar status para 304
```

Como `trackOnce()` já marcou a response, o `finish` posterior não corrige o status.

## 478.2. Regra V21

Telemetry que afirma status final deve observar **finalized response**.

Preferred:

```text
res.once('finish', trackFinalResponse)
```

Se um monkey patch de `send` continuar por safety net:

```text
chamar originalSend primeiro
→ só então fallback track
```

sem impedir o `finish` path de possuir a status authority.

## 478.3. Abort/close telemetry

Adicionar `res.close` apenas para classificar response abortada quando `finish` não ocorreu.
Não registrar como 200/success normal.

## 478.4. Conditional metrics

Os counters V20:

```text
http_conditional_304_total
http_conditional_forced_200_total
```

precisam ser derivados após finalização real, ou instrumentados diretamente no response policy helper,
sem dupla contagem.

## 478.5. Search-success metrics

`resultCount` pode continuar em `res.locals`, mas status/termination class precisa distinguir:

```text
200 body delivered
304 conditional response
client-aborted before finish
5xx
```

Isso evita usar telemetria incorreta como rollout gate.

---

# 479. Mandatory File / Caller / Occurrence Map V21

Além de todos os mapas V8→V20, classificar explicitamente:

```text
RUNTIME / BUILD
Dockerfile
.nvmrc
package.json
package-lock.json
.github/workflows/env-registry-check.yml
.github/workflows/docker-publish-preview.yml
.github/workflows/docker-publish-testing.yml

HTTP / FINALIZATION / METRICS
addon/index.ts
addon/server.ts
addon/lib/requestTracker.js
addon/lib/inProcessRoutes.ts
addon/lib/requestSession.ts

EXECUTION LIFECYCLE
addon/lib/lifecycle/runtime.ts
addon/lib/lifecycle/shutdown.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/cacheSourceRefetch.ts
addon/lib/getCache.ts

BACKGROUND / WARMERS IN RELEASE-CORRECTNESS CLOSURE
addon/lib/cacheWarmer.js
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/malCatalogWarmer.js

TRANSPORT / PROVIDER
addon/lib/getTmdb.ts
```

Arquivos com `Promise.race`, timers ou schedulers fora desse domínio continuam obrigados a receber
`explicit-no-op`/`out-of-scope-with-reason` no occurrence ledger quando encontrados pelo grep global.

## 479.1. Occurrence terms adicionais V21

```text
req.on('close'
req.once('close'
res.on('close'
res.once('close'
res.on('finish'
res.once('finish'
writableFinished
writableEnded
message.signal
req.signal
signal.reason
throwIfAborted
AbortSignal.any
AbortSignal.timeout

Promise.race
setInterval
setTimeout
clearInterval
clearTimeout
unref

shutdownSequence
createShutdownSequence
closeOne
server.close
closeAllConnections
closeIdleConnections

refresh-lock
LOCK_SECONDS
REBUILD_TIMEOUT_MS
redis.set(...NX
expire(lock
activeCount
inFlight

res.send =
originalSend
trackOnce
statusCode
```

## 479.2. Caller closure de shutdown/background

Enumerar todo caller que:

```text
inicia refresh/warmup timer
registra closer
fecha Redis/database
cria shared flight
cria detached background task
pode iniciar work depois de shutdown flag
```

Zero caller sem owner/stop/drain classification.

## 479.3. Runtime evidence closure

O evidence bundle do PR inclui:

```text
node --version
npm ls express undici @types/node
Docker/base ref usado no integration test
package-lock hash
resultado da HTTP disconnect suite
resultado da conditional HTTP suite
```

---

# 480. Test Matrix V21 — casos acumulados 421–465

Adicionar aos 420+ casos V20:

```text
421. HTTP GET normal com fallback de disconnect signal
     → request body termina normalmente; operation NÃO aborta; catálogo conclui 200.

422. client fecha socket antes de response finish
     → OperationContext.signal aborta exatamente uma vez como client-abort.

423. response emite finish e depois close normal
     → nenhum abort retroativo; listeners são removidos.

424. runtime Node 24 abaixo da capability nativa de message.signal
     → fallback funciona; nenhuma leitura obrigatória de req.signal.

425. runtime Node 24.20+ com native signal path habilitado
     → comportamento equivalente ao fallback para normal finish e premature disconnect.

426. Jellyfin in-process req sintética sem message.signal
     → ctx.signal explícito continua funcionando; semantic core não lê transport magic.

427. waiter chega com signal já abortado
     → não incrementa activeWaiters; zero shared-work side effect por esse waiter.

428. último waiter aborta
     → flight torna-se non-joinable antes de controller.abort().

429. novo caller chega enquanto flight antigo está cancelling
     → cria/junta nova generation; não recebe cancellation do flight antigo.

430. finally do flight antigo executa depois de nova generation criada
     → não remove/substitui entry nova.

431. leader deadline=1s, waiter B=5s, source budget=4s
     → leader sai em 1s; physical flight continua; B recebe resultado se source completa em 4s.

432. background waiter legítimo mantém neutral source flight vivo após request waiter abortar
     → work usa shared/background authority, nunca deadline do request líder.

433. waiter abort e flight settle no mesmo tick
     → outcome determinístico; decrement exatamente uma vez; activeWaiters nunca negativo.

434. stress 10k join/abort cycles
     → zero listener/context leak e counters voltam ao baseline.

435. inProcessRoutes timeout
     → race loser recebe abort; nenhum cursor/cache/request metric tardio após timeout.

436. refresh-ahead excede background deadline
     → underlying rebuild recebe abort; `runRefreshAhead` não considera work encerrado apenas porque timeout venceu.

437. provider ignora abort e retorna depois
     → commit guard/fence rejeita late correctness write quando authority expirou.

438. refresh lease A possui token A
     → renew/expire/release só funciona enquanto stored token == A.

439. lease A expira; B adquire token B; A termina atrasado e tenta `EXPIRE`
     → operação de A não altera TTL/ownership de B.

440. A perde lease/fence; B completa generation nova; A tenta cache write tardio
     → A não sobrescreve B.

441. refresh deadline e lease TTL
     → existe safety margin/renewal/fence; nunca dependem do mesmo instante de expiração.

442. Redis lock acquisition fica pendente além do background deadline
     → task cancela/draina e não ocupa activeCount indefinidamente.

443. shutdown inicia enquanto nenhum warmer roda, mas timers estão armados
     → admission freeze cancela timers; nenhum novo warmer começa.

444. shutdown inicia durante refresh-ahead
     → global shutdown signal aborta task; registry drena antes de Redis close.

445. cacheWarmer interval já agendado
     → stop/shutdown limpa handle; callback não reseta stop flag e reinicia work.

446. comprehensive warmer possui recursive setTimeout futuro
     → stop/shutdown cancela handle mesmo quando `isRunning=false`.

447. MAL warmer está antes do initial delay
     → shutdown cancela initial timeout e interval; zero run posterior.

448. graceful shutdown com requests ativas
     → admission fecha primeiro; flush de metrics/art não ocorre antes do traffic/work drain.

449. active request espera TMDB quando SIGTERM chega
     → shutdown signal chega ao ctx/provider/backoff; request/shared work encerra dentro do grace.

450. Redis/database close ordering
     → zero registered release/catalog/search task vivo quando resource close começa.

451. work não obedece abort dentro do grace
     → shutdown reporta forced/non-graceful path; não declara drain bem-sucedido.

452. shutdown closer excede timeout
     → loser não fica usando recurso enquanto teardown dependente prossegue sem owner.

453. shutdown chamado duas vezes
     → sequence idempotente; signals/closers/metrics não duplicam.

454. conditional catalog 304
     → requestTracker observa status final 304, não pre-send 200.

455. conditional request resulta 200 por body novo
     → telemetry observa 200 final e validator novo.

456. client abort antes de finish
     → request telemetry registra cancellation/aborted class, não success normal.

457. client abort durante TMDB fetch
     → cancellation counter incrementa; provider failure health counter não incrementa.

458. per-attempt timeout sem client abort
     → provider transient metric/retry permanece válido e distinguível.

459. config save ocorre durante background refresh e shutdown logo depois
     → old source snapshot nunca escreve key da config nova; shutdown não cria late cross-snapshot commit.

460. duas replicas atingem refresh deadline/lease boundary
     → fence garante no máximo uma generation autoritativa de write.

461. minimum supported Node integration run
     → HTTP disconnect adapter/AbortSignal composition/conditional suite passam.

462. current container Node integration run
     → mesmo semantic result da matriz mínima.

463. compile passa com @types/node mas runtime API foi deliberadamente removida/feature-disabled no teste
     → fallback cobre; type surface não é authority.

464. runtime/base-image fingerprint muda sem source diff
     → CI exige rerun Runtime-Semantics + Abort/Conditional gates antes da coverage claim.

465. full fault: BR filtered page + shared flight + client disconnect + refresh lease rollover + SIGTERM
     → nenhum stale HIDE, nenhum cursor falso, nenhum poisoned error-cache, nenhum late stale write,
       nenhum recurso fechado sob task registrada viva e telemetry reflete termination real.
```

A suíte acumulada passa a ser:

```text
465+ casos determinísticos/golden/integration/concurrency/fault/load
+
property tests V8→V20
+
black-box conditional HTTP V20
+
black-box disconnect/runtime/shutdown/distributed-refresh V21.
```

---

# 481. Definition of Done V21

Além de todo DoD V8→V20:

```text
[ ] dev HEAD/tree continuam exatamente no snapshot ou todos os gates foram reexecutados
[ ] issue #742 continua aberta/compatível com a semântica implementada

[ ] existe uma única authority de HTTP client disconnect
[ ] normal request completion não é confundida com disconnect
[ ] HTTP adapter não depende de req.signal em runtime onde a semântica não é garantida
[ ] HTTP/Jellyfin/warmer entregam OperationContext.signal explícito ao mesmo semantic core
[ ] abort listeners são descartados após settle/finish

[ ] Runtime-Semantics Gate passa no mínimo suportado e no runtime de release
[ ] process.version/base-image/dependency fingerprint acompanha evidence do PR
[ ] @types/node não é usado como prova de runtime capability
[ ] Docker/CI/runtime drift dispara rerun dos gates apropriados

[ ] toda Promise.race correctness-critical possui loser classification explícita
[ ] timeout não libera ownership/admission enquanto side-effecting loser continua sem owner
[ ] detached loser, quando permitido, recebe BackgroundExecutionContext/registry próprios

[ ] shared flight possui cancelling/non-joinable state
[ ] last-waiter abort impede novos joiners antes de abortar underlying work
[ ] novo caller durante cancellation cria/junta nova generation
[ ] old finalizer não apaga new generation
[ ] SharedFlightBudget é source/fleet-owned, nunca leader-request-owned
[ ] waiter counts/listeners fecham exatamente uma vez

[ ] refresh lease possui owner token
[ ] lease mutation usa compare-owner
[ ] lease deadline possui safety margin/renewal/fence
[ ] stale worker não consegue commit depois de perder authority
[ ] local inFlight/admission só libera quando physical work encerra ou é explicitamente re-owned
[ ] cooldown/backoff não é confundido com execution lease

[ ] shutdown congela admission/schedulers antes do drain
[ ] active execution recebe shutdown signal
[ ] work drain ocorre antes de flush/resource close
[ ] Redis/database não fecham sob task release/catalog/search registrada viva
[ ] timeout de closer não abandona loser side-effecting sem owner
[ ] cacheWarmer/comprehensive/MAL relevant timers possuem stop handles/quiescence
[ ] forced shutdown é distinguido de graceful shutdown

[ ] post-cancel commit authority está definida por stage
[ ] client-abort/request-deadline não produz error cache/backoff/provider failure health
[ ] signal.reason/typed cancellation preserva provenance de baixa cardinalidade

[ ] requestTracker/status telemetry ocorre após response finalization
[ ] Express-generated 304 é medido como 304
[ ] aborted response é distinguido de 200 normal
[ ] rollout gates não dependem de telemetry pre-send incorreta

[ ] occurrence/caller/runtime gate V21 = zero unclassified
[ ] 465+ test matrix passa
[ ] todos os gates V20 continuam passando
[ ] dark deploy + homogeneous fleet + kill switch + rollback drill continuam válidos
```

---

# 482. Resultado final da auditoria V21

## 482.1. O que a V21 encontrou que o V20 ainda deixava implícito

O V20 estava correto no **que** deveria ser cancelado/isolado, mas ainda não fechava integralmente **como o
sistema sabe que o trabalho realmente terminou**.

A V21 fecha essa última classe de ambiguity:

```text
transport disconnect authority
runtime Node capability drift
Promise.race loser ownership
shared-flight cancellation/rejoin ABA
source-owned physical work budget
refresh distributed lease ownership + fencing
post-abort commit authority
shutdown dependency ordering
scheduler quiescence
response-finalization telemetry
```

## 482.2. Estado final V21

```text
V21 = implementation-ready engineering design
      para dev@6e83e22ab9de5093f9918a1871157f401feebb03
      / tree 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d,

      preservando integralmente V20 e acrescentando:

      - HTTP disconnect signal authority compatível com o range Node declarado;
      - runtime/type-surface evidence e drift gate;
      - loser lifecycle obrigatório para Promise.race;
      - shared-flight non-joinable cancelling generation;
      - source-owned SharedFlightBudget;
      - refresh lease owner token + commit fence;
      - shutdown admission-freeze → drain → flush → resource-close;
      - quiescência de timers/warmers relevantes;
      - typed cancellation/commit authority;
      - request telemetry somente após final response status;
      - 465+ regression/acceptance cases acumulados.
```

Definição precisa de cobertura V21:

> **A V21 cobre estaticamente o snapshot auditado e fecha os boundaries conhecidos de facts, policy,
> cache, paging, source identity, temporal validity, config snapshot, transport freshness, cancellation,
> shared work, distributed refresh ownership e shutdown. “100%” neste documento significa zero ocorrência,
> caller, authority, state transition ou runtime dependency conhecido sem classificação no snapshot, e zero
> comportamento externo/distribuído assumido sem gate executável. Não significa afirmar infalibilidade de
> TMDB/Redis/rede/Node antes da execução dos 465+ testes e fault gates definidos.**

Checklist ultra-curto V21:

```text
1. fixe HEAD/tree + dependency/runtime fingerprint;
2. rerode todos os gates V20;
3. implemente HTTP disconnect binding seguro + OperationContext explícito;
4. componha client/deadline/shutdown/attempt signals com reason tipada;
5. transforme Promise.race timeout em cancel-and-join ou detach explícito;
6. torne shared flights non-joinable antes do last-waiter abort e use source-owned budget;
7. dê owner token/fence ao refresh distribuído e separe lease/deadline/cooldown;
8. congele schedulers, aborte/drain work, depois flush e só então feche Redis/database;
9. proíba late commit sem authority após cancel/lease loss;
10. mova response telemetry para o status final pós-Express;
11. rode 465+ casos + property/concurrency/load/fault + HTTP disconnect/runtime/shutdown suites;
12. dark deploy + homogeneous fleet + kill-switch + rollback drill.
```
---

# 483. Reauditoria normativa V22 — Async Work / Transport / Scheduler Closure

> **Camada normativa V22.** Esta seção e todas as seções 483+ prevalecem sobre V8→V21 em qualquer conflito relacionado a inventário de trabalho assíncrono, timers, schedulers, startup losers, HTTP transport compartilhado, retry/backoff cancellation, processos de manutenção destacados, ownership de sockets atualizados, disposer contracts e shutdown quiescence. A arquitetura de release evidence/policy/paging das versões anteriores permanece preservada.

## 483.1. Snapshot revalidado

```text
dev HEAD = 6e83e22ab9de5093f9918a1871157f401feebb03
Tree SHA = 00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
Release = v3.1.0
Data da reauditoria V22 = 2026-09-24
```

O source snapshot continua idêntico ao V21. Portanto os gaps abaixo são gaps de **cobertura do plano**, não drift de implementação.

## 483.2. Evidência nova: o Occurrence Gate V21 ainda não estava materializado como ledger completo

A V21 exigia classificar todos os `Promise.race`, timers e schedulers relevantes, mas o documento não enumerava todas as ocorrências do próprio snapshot.

Na reauditoria do commit fixado, a busca de source encontrou:

```text
Promise.race(        → 14 arquivos backend
setInterval(         → 19 arquivos backend
setTimeout(          → 46 arquivos backend
new AbortController( → 4 arquivos backend
AbortSignal          → 7 arquivos backend
```

Comparando essas ocorrências com o texto V21, ainda não apareciam explicitamente no plano:

```text
Promise.race:
- addon/lib/deviceAuthSessions.ts
- addon/lib/jellyfin/dashboard.ts
- addon/lib/jellyfin/resume.ts
- addon/lib/lifecycle/deepHealth.ts
- addon/lib/tmdb-keyword-index.ts
- addon/lib/tmdb-network-index.ts

setInterval:
- addon/lib/anime-list-mapper.js
- addon/lib/cacheCleanupScheduler.ts
- addon/lib/eventLoopLag.ts
- addon/lib/id-mapper.js
- addon/lib/imdbRatings.ts
- addon/lib/jellyfin/playstateSync.ts
- addon/lib/mal.ts
- addon/lib/posterCache/handler.ts
- addon/lib/posterCache/store.ts
- addon/lib/posterCache/warmQueue.ts
- addon/lib/wiki-mapper.ts
- addon/utils/recommendations/refresh.ts

Abort/retry transport relevantes que também não estavam no file map V21:
- addon/utils/httpClient.ts
- addon/utils/retry.ts
- addon/lib/kitsu.ts
- addon/lib/movielens.ts
- addon/lib/simkl.ts
- addon/lib/jellyfin/streams.ts
- addon/lib/jellyfin/subtitles.ts
```

Esses números são **evidência de auditoria do snapshot**, não a authority final do merge. O PR deve gerar o ledger outra vez a partir do checkout fixado por `rg`/AST, porque nenhum índice de busca externo substitui a árvore local do CI.

## 483.3. Consequência sobre a claim de cobertura

A frase V21:

```text
zero occurrence ... conhecido sem classificação
```

não pode ser tratada como provada apenas pela redação V21.

A V22 substitui a claim por:

```text
zero ocorrência somente quando o Async-Occurrence Ledger gerado do checkout
for reconciliado contra a allowlist/classification ledger e o CI retornar zero drift.
```

---

# 484. Blockers novos V22

Adicionar cumulativamente a EA–EN e a todos os blockers históricos:

```text
EO. O mandatory map V21 não lista 6 dos 14 arquivos com Promise.race encontrados no snapshot.
    Logo o loser-lifecycle gate ainda não possui caller closure comprovável.

EP. O mandatory map V21 não lista 12 dos 19 arquivos backend com setInterval encontrados no snapshot.
    Parar somente essential/comprehensive/MAL warmers não congela toda a produção de background work.

EQ. `addon/utils/httpClient.ts` não aceita `AbortSignal` em HttpRequestOptions e não passa signal para
    `undici.request`. Qualquer provider que use esse transport pode continuar rede/body/retry após caller abort.

ER. `addon/utils/retry.ts::withRetries()` possui sleep baseado em setTimeout sem signal. Mesmo quando o
    request físico puder ser abortado, o retry backoff pode continuar mantendo a operação viva.

ES. Redirect/retry em `httpClient.ts` não possui deadline absoluto compartilhado. Reiniciar timeout por
    redirect/attempt pode exceder o budget físico da OperationContext.

ET. `server.ts::withTimeout()` faz Promise.race entre initializer e deadline. O loser não é cancelado nem
    registrado. Initializers mutam memória/cache e alguns armam intervalos após sucesso tardio.

EU. A mensagem "will retry on first use" não é suficiente enquanto o initializer original pode terminar
    depois do timeout. Late initializer + first-use retry podem executar duas gerações concorrentes.

EV. `performEpochCleanup()` e `sweepLegacyMetaComponentKeys()` são disparados com `.catch(...)` sem await,
    ownership ou registry, apesar de usarem Redis. Shutdown pode fechar Redis enquanto esses sweeps continuam.

EW. `startRecommendationRefresh()` mantém interval handle, mas não exporta stop/drain. O sweep pode tocar Redis
    depois do início do shutdown e o callback ativo não é joinado.

EX. `startPlaystateSync()` não guarda initial timeout nem interval handle e não possui stop. O sync realiza
    reads/writes de database e chamadas a trackers, portanto é side-effecting background work.

EY. `CacheCleanupScheduler.stop()` limpa apenas intervalId. O initial setTimeout de 30 s não é guardado e
    `stop()` não espera um `runCleanup()` já ativo terminar.

EZ. `startMovieLensSyncSchedule()` e o popular-warming interval em `addon/index.ts` não guardam handles nem
    expõem disposer. Um SIGTERM não impede callback já armado de iniciar novo work.

FA. `eventLoopLag.stopEventLoopMonitor()` já existe, porém o server não o registra no shutdown sequence.

FB. `metaColdStore` cria sweep interval anônimo no server. O resource closer faz flush/close do store, mas o
    timer não é limpo explicitamente antes do close.

FC. `initializeMapper`, `initializeAnimeListMapper`, `initializeRatings` e `initializeMappings` armam periodic
    refresh timers como efeito colateral de readiness initialization. Lifecycle de bootstrap e lifecycle de
    scheduler estão acoplados.

FD. `id-mapper.js` possui cleanup próprio via process SIGINT/SIGTERM além do shutdown authority central.
    Signal handlers paralelos quebram ordering explícito e tornam testes de drain menos determinísticos.

FE. `anime-list-mapper`, IMDb ratings e wiki mapper não expõem no snapshot um disposer simétrico equivalente
    ao cleanup exportado por id-mapper. Seus intervals não entram no shutdown central.

FF. `DashboardAPI` pode iniciar `_heapLogTimer`, `posterCache/store.ts` inicia sweepTimer e
    `posterCache/handler.ts` inicia summaryTimer; esses owners não possuem dispose central documentado na V21.

FG. `posterCache/warmQueue.ts` possui timers e physical work próprios. Parar o warmer de catálogos não prova
    que image warm tasks/timers já terminaram antes do teardown.

FH. `mal.ts` possui interval de limpeza de ETag cache e `traktUtils.ts` cria interval de limpeza de request
    queues sem owner explícito de shutdown. Mesmo sendo majoritariamente memory-only, precisam classificação
    explícita para satisfazer a claim global, não silêncio.

FI. `server.close()`/`closeIdleConnections()` não resolve sozinho sockets que passaram por protocol upgrade.
    `jellyfin/socket.ts` mantém keepalive interval por socket; shutdown precisa registrar e encerrar upgrades.

FJ. `jellyfin/socket.ts` limpa o keepalive apenas em close/error do próprio socket. Sem socket registry de
    shutdown, um client WebSocket persistente pode sobreviver ao início do drain.

FK. `deepHealth`, device-auth Redis reads, TMDB keyword/network index, Jellyfin dashboard/resume e outros
    Promise.race precisam classificação específica: CANCEL_AND_JOIN, DETACH_EXPLICITLY ou SAFE_IGNORE.

FL. `jellyfin/resume.ts::memoNextUp()` intencionalmente deixa o build continuar após deadline para atualizar
    `lastNextUp`. Isso é detached side-effecting work por design e precisa BackgroundExecutionContext/registry.

FM. `tmdb-keyword-index.ts` e `tmdb-network-index.ts` usam timeout também em Redis SETEX. Se o race perde,
    o Redis command continua; timeout de espera não é cancelamento do write.

FN. `getManifest.ts` e `traktUtils.ts` possuem timeout races cujo underlying fetch/rate-limited work continua.
    Eles precisam signal real ou classificação detached explícita; fallback não mata o loser.

FO. `unref()` não equivale a cancelamento, quiescência, join nem ownership. Ele apenas não mantém o event loop
    vivo sozinho e não pode ser usado como justificativa de graceful shutdown.

FP. Parar um interval/timeout futuro não basta: callback já iniciado precisa entrar no ActiveWorkRegistry e
    ser cancelado/joinado antes de fechar Redis/database/filesystem-dependent resources.

FQ. O V21 não contém `addon/utils/httpClient.ts`/`addon/utils/retry.ts` no transport closure. Portanto abort
    propagation não está caller-closed para todos os providers que compartilham esse HTTP client.

FR. Startup task timeout, scheduler admission freeze e shutdown signal precisam compartilhar uma única
    lifecycle authority; caso contrário um late bootstrap worker pode criar scheduler depois do freeze.

FS. Occurrence discovery baseado somente em Promise.race/setTimeout/setInterval ainda perde detached work
    iniciado por `void promise`, `.catch(...)` sem await, `setImmediate`, queue/task objects, process signal
    listeners e protocol-upgrade sockets. O gate precisa ser semântico + sintático.

FT. O response/server drain V21 não define explicitamente o lifecycle dos upgraded Jellyfin sockets.
    HTTP drain só pode ser declarado completo quando request sockets e upgrade sockets forem classificados.

FU. Background producer iniciado por dashboard/manual endpoint durante a janela de shutdown precisa falhar
    admission antes de criar work; fechar o listener não basta para requests admin que já estavam em voo.
```

---

# 485. Async-Occurrence Ledger Gate — authority gerada do checkout

## 485.1. Objetivo

Criar um gate reproduzível que responda:

> Todo mecanismo capaz de manter ou iniciar trabalho assíncrono no backend foi classificado por owner, cancellation, join e resource dependencies?

Não manter esse inventário apenas em prosa manual.

## 485.2. Scanner mínimo

No CI/PR Guard, gerar ledger para o source backend com pelo menos:

```text
Promise.race
Promise.any
setTimeout
setInterval
setImmediate
queueMicrotask
.unref()
new AbortController
AbortSignal
process.on('SIGINT'/'SIGTERM')
server.on('upgrade') / upgrade handlers
.catch(...) em Promise iniciada sem await/return
detached `void <promise>`
recurring/self-rescheduling setTimeout
queue/worker start functions
functions start*/schedule*/initialize* que criem timer/work owner
```

Preferência:

```text
AST scanner versionado
+
rg fallback legível para reviewers
```

## 485.3. Ledger schema

Cada ocorrência não trivial recebe entrada machine-readable:

```ts
interface AsyncOccurrenceRecord {
  id: string;
  file: string;
  symbol: string;
  occurrenceKind:
    | 'promise-race'
    | 'timeout'
    | 'interval'
    | 'detached-promise'
    | 'retry-backoff'
    | 'scheduler'
    | 'signal-handler'
    | 'upgrade-socket'
    | 'queue-worker';

  owner: string;
  startsWork: boolean;
  mayOutliveCaller: boolean;
  sideEffects: 'none' | 'memory' | 'cache' | 'database' | 'network' | 'filesystem' | 'mixed';
  resources: string[];

  policy:
    | 'CANCEL_AND_JOIN'
    | 'DETACH_EXPLICITLY'
    | 'DRAIN_ON_SHUTDOWN'
    | 'CONNECTION_OWNED'
    | 'SAFE_IGNORE';

  stopAuthority?: string;
  joinAuthority?: string;
  rationale: string;
}
```

## 485.4. CI invariant

```text
actual occurrence set
-
classified occurrence set
=
∅
```

E também:

```text
classified occurrence aponta para linha/symbol inexistente
→ CI fail (stale allowlist)
```

Não aceitar wildcard do tipo:

```text
addon/lib/** = SAFE_IGNORE
```

Cada owner precisa ser explícito.

---

# 486. BackgroundWorkRegistry — owner único para lifecycle físico

## 486.1. Criar registry central

Conceitualmente:

```ts
interface BackgroundTaskHandle {
  id: string;
  kind: string;
  signal: AbortSignal;
  promise: Promise<void>;
}

interface SchedulerHandle {
  name: string;
  stopAdmission(): void | Promise<void>;
  abortActive(reason: unknown): void;
  drain(deadline: Date): Promise<DrainResult>;
  dispose(): void | Promise<void>;
}

interface BackgroundWorkRegistry {
  registerScheduler(handle: SchedulerHandle): () => void;
  runOwned<T>(spec: OwnedWorkSpec<T>): Promise<T>;
  freezeAdmission(reason: unknown): void;
  abortActive(reason: unknown): void;
  drain(deadline: Date): Promise<DrainReport>;
}
```

## 486.2. Invariante

Todo callback que possa tocar:

```text
Redis
DB
provider/network
filesystem cache
shared in-memory index correctness-critical
```

após seu scheduler disparar entra no registry **antes** de iniciar side effect.

## 486.3. Estado mínimo

```text
ACCEPTING
→ FROZEN
→ ABORTING
→ DRAINING
→ DRAINED
→ DISPOSED
```

Depois de `FROZEN`:

```text
nenhum scheduler/manual admin trigger/bootstrap loser
pode criar novo task handle.
```

## 486.4. Stop de timer não é drain

Obrigatório diferenciar:

```text
stopAdmission()
→ limpa interval/timeout/recursive schedule futuro

abortActive()
→ sinaliza callbacks já iniciados

drain()
→ espera callbacks físicos settle

dispose()
→ remove listeners/handles/resources locais
```

---

# 487. Scheduler/Timer Closure — file-by-file obrigatório

Esta seção fecha o gap concreto do snapshot.

## 487.1. `addon/lib/cacheWarmer.js`

Já identificado na V21, agora normatizado pelo registry:

```text
- armazenar handle de scheduleEssentialWarming;
- stopAdmission limpa handle;
- warmEssentialContent/warmPopularContent entram no BackgroundWorkRegistry;
- callback iniciado respeita shutdown signal;
- stop não pode ser revertido por callback/tarefa tardia.
```

## 487.2. `addon/lib/comprehensiveCatalogWarmer.js`

```text
- armazenar recursive setTimeout handle;
- impedir scheduleNextWarmup() depois de FROZEN;
- `stopComprehensiveWarming()` precisa também cancelar future schedule;
- current run entra no registry e possui drain Promise;
- image warm work delegado também precisa ownership.
```

## 487.3. `addon/lib/malCatalogWarmer.js`

```text
- armazenar initialDelayHandle além de intervalHandle;
- stop limpa ambos;
- current run entra no registry;
- callback de initial delay revalida admission antes de runWarmup().
```

## 487.4. `addon/utils/recommendations/refresh.ts`

Adicionar:

```ts
stopRecommendationRefresh(): void
awaitRecommendationRefreshIdle(): Promise<void>
```

Ou retornar `SchedulerHandle` de `startRecommendationRefresh()`.

Regras:

```text
- clearInterval(timer);
- impedir novo sweep quando frozen;
- `sweeping=true` corresponde a Promise registrada, não apenas boolean;
- active sweep recebe signal;
- Redis work settle antes de redis.quit().
```

## 487.5. `addon/lib/jellyfin/playstateSync.ts`

Refatorar para guardar:

```text
initialDelayHandle
intervalHandle
activeSyncPromise
```

Adicionar stop/drain.

`syncAllPlaystate()` precisa verificar signal entre users e antes de writes.

## 487.6. `addon/lib/cacheCleanupScheduler.ts`

Adicionar:

```text
initialTimeoutId
activeCleanupPromise
stopped/frozen state
```

`stop()` passa a:

```text
clearTimeout(initialTimeoutId)
clearInterval(intervalId)
impedir callback já enfileirado de iniciar
```

`drain()` espera `activeCleanupPromise`.

## 487.7. `addon/index.ts` schedules

`startEssentialWarmingSchedules()` e `startMovieLensSyncSchedule()` devem retornar disposer/handle.

Guardar explicitamente:

```text
popularWarmInterval
movieLensSyncInterval
```

Não deixar `setInterval(...)` anônimo.

## 487.8. `addon/lib/eventLoopLag.ts`

Já existe `stopEventLoopMonitor()`.

Ajuste necessário:

```text
registrar no shutdown central na fase scheduler/dispose.
```

Não criar novo mecanismo.

## 487.9. `metaColdStore` sweep no `server.ts`

Guardar:

```text
coldStoreSweepInterval
```

Ordenação:

```text
clear interval
→ drain eventual sweep ativo
→ flushNow
→ close
```

## 487.10. Initializer-owned periodic refreshes

### `addon/lib/id-mapper.js`

O `cleanup()` já existe e é exportado.

```text
- remover/evitar depender de process SIGINT/SIGTERM local para ordering;
- registrar cleanup no scheduler registry;
- scheduled update ativo precisa Promise/drain, não só clearInterval.
```

### `addon/lib/anime-list-mapper.js`

Adicionar disposer equivalente:

```text
stopAnimeListMapperUpdates()
+
active update drain
```

### `addon/lib/imdbRatings.ts`

Adicionar:

```text
stopImdbRatingsUpdates()
+
active update drain
```

### `addon/lib/wiki-mapper.ts`

Adicionar:

```text
stopWikiMapperUpdates()
+
active refresh drain
```

## 487.11. Poster cache lifecycle

### `addon/lib/posterCache/store.ts`

Adicionar `dispose()/stopSweep()`:

```text
clearInterval(sweepTimer)
await active sweep if any
```

O `indexed = scan()` inicial também precisa ser owner-classified se puder continuar durante shutdown.

### `addon/lib/posterCache/handler.ts`

`summaryTimer` é observability-only, mas ainda precisa disposer explícito para a claim global:

```text
clearInterval(summaryTimer)
```

### `addon/lib/posterCache/warmQueue.ts`

```text
- stopLagProbe();
- clear idleTimer;
- freeze queue admission;
- abort/drain active workers;
- impedir pump() depois de frozen;
```

## 487.12. Memory-only maintenance timers

### `addon/lib/mal.ts`
### `addon/utils/traktUtils.ts`

Podem ser classificados como low-risk/memory-only, mas ainda devem possuir uma decisão explícita:

```text
preferred: disposer central
acceptable se provado: SAFE_IGNORE no process-exit final,
mas nunca usar SAFE_IGNORE se callback puder iniciar network work ou tocar resource externo.
```

## 487.13. Connection-owned interval

`addon/lib/jellyfin/socket.ts` keepalive é legitimamente `CONNECTION_OWNED` durante operação normal porque
`close/error` limpa o timer. Porém shutdown precisa fechar o socket owner explicitamente; somente assim o timer
fica transitivamente encerrado.

---

# 488. Startup Task Timeout / Late-Loser Gate

## 488.1. Problema concreto

`server.ts` possui:

```text
withTimeout(task.key, task.timeoutMs, Promise.resolve().then(task.run))
```

`Promise.race` limita o wait de readiness, mas não o trabalho.

Alguns initializers:

```text
baixam arquivos
escrevem Redis/cache
mutam indexes em memória
armam intervals após concluir
```

Logo timeout != cancellation.

## 488.2. Novo contrato

Substituir o modelo `run(): Promise<unknown>` por algo como:

```ts
interface InitTask {
  key: string;
  timeoutMs: number;
  run(ctx: InitializationContext): Promise<InitResult>;
}

interface InitializationContext {
  signal: AbortSignal;
  generation: string;
  workRegistry: BackgroundWorkRegistry;
  schedulerRegistry: BackgroundWorkRegistry;
}
```

## 488.3. Política por initializer

Cada initializer é classificado em uma destas classes:

```text
A. CANCEL_ON_TIMEOUT
   → timeout aborta e join obrigatório antes de retry.

B. DETACH_TO_BACKGROUND
   → readiness deixa de esperar, mas ownership é transferido explicitamente ao registry;
     first-use não inicia segunda generation concorrente.

C. NON_CANCELLABLE_SINGLETON
   → loser pode continuar, mas há generation/singleflight única e shutdown drain obrigatório.
```

`SAFE_IGNORE` não é válido para initializer que muta correctness state.

## 488.4. Late scheduler creation fence

Antes de qualquer initializer armar timer periódico:

```text
schedulerRegistry.assertAccepting(generation)
```

Se shutdown já congelou admission:

```text
não instalar interval
não iniciar follow-up work
settle como cancelled/shutdown
```

## 488.5. First-use retry

A frase "retry on first use" só é verdadeira se:

```text
late generation antiga não está mais autoritativa
OU
first-use junta a mesma generation ainda viva.
```

Nunca:

```text
timeout da generation A
→ first-use cria B
→ A termina depois e publica estado/timer concorrente
```

---

# 489. Shared HTTP Transport / Retry Cancellation Gate

## 489.1. `addon/utils/httpClient.ts` entra no core mandatory map

Adicionar ao `HttpRequestOptions`:

```ts
signal?: AbortSignal;
deadlineAt?: number;
```

O mesmo signal/deadline acompanha:

```text
httpGet/httpPost/httpHead
requestFollowingRedirects
every redirect
withTransportRetries
every attempt
body consumption
```

## 489.2. Undici

`requestOptions` precisa receber:

```ts
signal: attemptSignal
```

Não usar apenas:

```text
bodyTimeout
headersTimeout
```

porque esses são transport timeouts e não representam caller/shutdown cancellation.

## 489.3. Retry helper

`addon/utils/retry.ts` passa a aceitar:

```ts
interface RetryOptions {
  ...
  signal?: AbortSignal;
  deadlineAt?: number;
}
```

Sleep deve ser abortável.

Conceitualmente:

```ts
abortableSleep(delayMs, signal)
```

Antes de cada attempt:

```text
throwIfAborted(signal)
remaining = deadlineAt - now
se remaining <= 0 → typed deadline cancellation
```

## 489.4. Redirect não reinicia budget

Um request com budget 8 s que recebe 3 redirects não recebe 8 s novos por hop.

```text
operation deadline absoluto
→ remaining budget calculado a cada redirect/attempt
```

## 489.5. Taxonomy

Separar:

```text
client_abort
request_deadline
shutdown_abort
attempt_timeout
provider_network_error
provider_http_error
```

Somente as classes realmente retryable passam por retry.

```text
client_abort       → never retry
shutdown_abort     → never retry
request_deadline   → never retry
attempt_timeout    → retry somente se operation budget permitir
```

## 489.6. Caller closure

Depois de adicionar signal ao transport, classificar todos os callers de `httpGet/httpPost/httpHead` em:

```text
request-owned
background-owned
bootstrap-owned
connection/auth-owned
```

Request-owned paths devem receber OperationContext.signal; background/bootstrap paths recebem context próprio.

---

# 490. Detached Startup Maintenance Gate

## 490.1. Paths concretos

No snapshot:

```text
performEpochCleanup().catch(...)
sweepLegacyMetaComponentKeys().catch(...)
```

são iniciados no boot sem await.

## 490.2. Regra

Registrar ambos como bootstrap background work:

```text
owner = startup-maintenance
resources = [redis]
shutdownPolicy = CANCEL_AND_JOIN ou DRAIN_ON_SHUTDOWN
```

## 490.3. Commit semantics

Se um sweep é abortado:

```text
não marcar migration/sweep como concluído
```

para que o próximo boot possa retomar/reexecutar idempotentemente.

## 490.4. Resource ordering

```text
startup maintenance drain
→ redis.quit
```

Nunca o contrário.

---

# 491. Upgraded-Socket Shutdown Gate — Jellyfin

## 491.1. Problema

`addon/lib/jellyfin/socket.ts` aceita protocol upgrade e mantém socket + keepalive interval.

O HTTP server closer atual não possui registry desses sockets.

## 491.2. Criar socket registry

Conceitualmente:

```ts
interface UpgradedSocketRegistry {
  register(socket): () => void;
  freeze(): void;
  closeGracefully(deadline): Promise<void>;
  destroyRemaining(): void;
  activeCount(): number;
}
```

## 491.3. Admission

Depois de shutdown freeze:

```text
new upgrade request
→ reject/close
→ não incrementar perUser
→ não criar keepalive timer
```

## 491.4. Drain

Ordem:

```text
freeze HTTP/upgrade admission
→ server.close() para requests normais
→ enviar close aos upgraded Jellyfin sockets
→ aguardar grace
→ destroyRemaining somente no forced path
→ validar activeCount == 0
```

## 491.5. Keepalive

Fechar socket precisa acionar exatamente uma vez o disposer que:

```text
clearInterval(timer)
remove registry entry
ajusta perUser
```

`close` e `error` concorrentes não podem decrementar duas vezes.

---

# 492. Promise.race Classification Ledger V22

Todos os 14 arquivos do snapshot recebem classificação explícita.

```text
addon/lib/lifecycle/shutdown.ts
→ CANCEL_AND_JOIN / forced-shutdown escalation; loser não pode ficar sem owner.

addon/lib/inProcessRoutes.ts
→ request-owned deadline; responder cedo só é permitido se underlying work aborta ou é re-owned.

addon/lib/cacheRefreshAhead.ts
→ CANCEL_AND_JOIN + lease/fence authority; V21 permanece normativo.

addon/server.ts
→ INIT_TASK policy A/B/C da seção 488; nunca implicit loser.

addon/index.ts
→ Redis limiter race: classificar Redis INCR loser como bounded detached I/O ou substituir por cancellable command path;
  não contaminar request accounting depois de cancellation.

addon/lib/requestTracker.js
→ stats read race é observability; SAFE_IGNORE somente se loser não fizer write e Redis lifecycle estiver protegido.

addon/lib/deviceAuthSessions.ts
→ Redis GET loser = detached read; não pode escrever session state após caller path; precisa resource ownership até settle.

addon/lib/lifecycle/deepHealth.ts
→ probe loser = observational read; classificar SAFE_IGNORE/DETACH apenas se nenhuma probe fizer side effect e resource close esperar/abortar.

addon/lib/tmdb-keyword-index.ts
→ cache read pode ser detached read; cache SETEX loser é side-effecting e precisa DRAIN_ON_SHUTDOWN ou cancellable Redis primitive.

addon/lib/tmdb-network-index.ts
→ mesmo contrato do keyword index.

addon/lib/jellyfin/resume.ts
→ DETACH_EXPLICITLY por design: Next Up continua buildando para preencher lastNextUp; registrar generation/background owner.

addon/lib/jellyfin/dashboard.ts
→ deadline de describe pode abandonar read/meta work; classificar request-owned cancel ou detached read com bounded owner.

addon/lib/getManifest.ts
→ studio fetch timeout: propagar signal/attempt timeout ao underlying Jikan transport; não deixar fetch/rate-limit loser órfão.

addon/utils/traktUtils.ts
→ genres fallback timeout: abortar queued/network operation ou transferir explicitamente ownership; fallback sozinho não resolve loser.
```

---

# 493. Resource Disposer Contracts

Cada resource/scheduler singleton que inicia timer/listener deve ter simetria:

```text
init/start
↕
dispose/stop
```

Mandatory disposer review no snapshot:

```text
addon/lib/id-mapper.js                    → cleanup já existe; centralizar ownership
addon/lib/anime-list-mapper.js            → adicionar disposer
addon/lib/imdbRatings.ts                   → adicionar disposer
addon/lib/wiki-mapper.ts                   → adicionar disposer
addon/lib/cacheWarmer.js                   → guardar/limpar interval
addon/lib/comprehensiveCatalogWarmer.js    → guardar/limpar recursive timeout
addon/lib/malCatalogWarmer.js              → guardar/limpar initial timeout + interval
addon/lib/cacheCleanupScheduler.ts         → initial timeout + interval + active job
addon/utils/recommendations/refresh.ts      → stop + active job drain
addon/lib/jellyfin/playstateSync.ts         → stop + active job drain
addon/lib/eventLoopLag.ts                  → registrar disposer existente
addon/lib/posterCache/store.ts             → stop sweep + active sweep
addon/lib/posterCache/handler.ts           → stop summary timer
addon/lib/posterCache/warmQueue.ts         → freeze/abort/drain timers/workers
addon/lib/dashboardApi.js                  → clear _heapLogTimer
addon/index.ts                              → popular/MovieLens interval disposers
addon/server.ts                             → cold-store sweep handle
addon/lib/mal.ts                            → classify/dispose memory cleanup interval
addon/utils/traktUtils.ts                   → classify/dispose queue cleanup interval
addon/lib/jellyfin/socket.ts                → connection disposer + global socket registry
```

## 493.1. Idempotence

Todo disposer deve aceitar:

```text
stop duas vezes
stop antes de start
stop depois de natural completion
close + error simultâneos
```

sem double decrement/double resolve.

---

# 494. Shutdown V22 — ordem final autoritativa

Substituir qualquer ordering anterior conflitante por:

```text
PHASE 0 — mark shutdown / freeze global admission
  - HTTP business admission
  - protocol upgrade admission
  - manual maintenance/restart admission
  - scheduler/bootstrap admission

PHASE 1 — stop future producers
  - clear timers/intervals/recursive timeouts
  - stop scheduler callbacks futuros
  - prevent late initializer from installing scheduler

PHASE 2 — abort request-owned work
  - client/server shutdown signal
  - in-process/Jellyfin request contexts

PHASE 3 — abort cancellable background work
  - warmers
  - refresh-ahead
  - recommendation/playstate/cache-cleanup/mapping refreshes
  - startup maintenance

PHASE 4 — drain physical work registry
  - active requests/shared flights
  - active scheduler callbacks
  - detached-but-owned tasks
  - startup losers
  - image warm workers

PHASE 5 — drain HTTP + upgraded sockets
  - normal HTTP connections
  - Jellyfin upgraded sockets

PHASE 6 — finalize telemetry/flushers
  - request metrics already finalized
  - metricsBatch flush
  - remembered Jellyfin artwork
  - store flushes

PHASE 7 — close resources
  - cold store
  - database
  - Redis
  - dispatchers/agents se explicitamente owned

PHASE 8 — dispose observability/memory-only owners
  - event loop histogram
  - summary/heap timers
  - remaining safe local timers

PHASE 9 — forced escalation only if grace expired
  - destroy remaining sockets/tasks where safe
  - emit non-graceful report
  - never report graceful=true when registry nonzero
```

A implementação pode fundir fases adjacentes internamente, mas os happens-before acima são normativos.

---

# 495. Mandatory File / Caller / Occurrence Map V22

Adicionar ao mapa acumulado V8→V21:

## 495.1. Core lifecycle / transport — CHANGE REQUIRED

```text
addon/server.ts
addon/lib/lifecycle/runtime.ts
addon/lib/lifecycle/shutdown.ts
addon/utils/httpClient.ts
addon/utils/retry.ts
addon/lib/inProcessRoutes.ts
addon/lib/requestTracker.js
addon/lib/cacheRefreshAhead.ts
addon/lib/cacheSourceRefetch.ts
addon/lib/getCache.ts
```

## 495.2. Startup / detached maintenance — CHANGE OR EXPLICIT CLASSIFICATION

```text
addon/lib/epochCleanup.ts
addon/lib/metaHashMigration.ts
addon/lib/id-mapper.js
addon/lib/anime-list-mapper.js
addon/lib/imdbRatings.ts
addon/lib/wiki-mapper.ts
addon/lib/tmdb-keyword-index.ts
addon/lib/tmdb-network-index.ts
```

## 495.3. Schedulers / background producers — CHANGE REQUIRED

```text
addon/lib/cacheWarmer.js
addon/lib/comprehensiveCatalogWarmer.js
addon/lib/malCatalogWarmer.js
addon/lib/cacheCleanupScheduler.ts
addon/utils/recommendations/refresh.ts
addon/lib/jellyfin/playstateSync.ts
addon/lib/eventLoopLag.ts
addon/lib/posterCache/warmQueue.ts
addon/index.ts
```

## 495.4. Resource-local timers/disposers — CHANGE OR EXPLICIT SAFE CLASSIFICATION

```text
addon/lib/posterCache/store.ts
addon/lib/posterCache/handler.ts
addon/lib/dashboardApi.js
addon/lib/mal.ts
addon/utils/traktUtils.ts
addon/lib/jellyfin/socket.ts
```

## 495.5. Promise.race loser classification — OCCURRENCE REQUIRED

```text
addon/lib/deviceAuthSessions.ts
addon/lib/jellyfin/dashboard.ts
addon/lib/jellyfin/resume.ts
addon/lib/lifecycle/deepHealth.ts
addon/lib/getManifest.ts
addon/lib/tmdb-keyword-index.ts
addon/lib/tmdb-network-index.ts
addon/utils/traktUtils.ts
addon/index.ts
addon/server.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/inProcessRoutes.ts
addon/lib/lifecycle/shutdown.ts
addon/lib/requestTracker.js
```

## 495.6. Abort surface review — OCCURRENCE REQUIRED

```text
addon/lib/getTmdb.ts
addon/lib/kitsu.ts
addon/lib/movielens.ts
addon/lib/simkl.ts
addon/utils/mdbList.ts
addon/lib/configApi.js
addon/lib/redisReady.ts
addon/lib/jellyfin/streams.ts
addon/lib/jellyfin/subtitles.ts
addon/lib/posterCache/warmQueue.ts
addon/server.ts
```

## 495.7. No-op classification admissível

Frontend timers em `configure/` e callback-local heartbeat de uma conexão podem permanecer sem entrar no
BackgroundWorkRegistry somente quando seu lifetime owner já for a própria component/connection e o disposer for
provável por teste. Eles ainda aparecem no occurrence ledger com classificação, não são ignorados pelo scanner.

---

# 496. Test Matrix V22 — casos 466–520

Adicionar aos 465+ casos V8→V21:

```text
466. gerar Async-Occurrence Ledger no snapshot fixado
     → todas as ocorrências atuais possuem classification record; zero unmatched.

467. remover artificialmente uma entrada do ledger para arquivo com Promise.race
     → CI falha.

468. manter entrada apontando para occurrence removida
     → CI falha por stale classification.

469. adicionar novo setInterval em backend sem registro
     → CI falha.

470. adicionar detached `void someAsyncWrite()` sem classificação
     → CI falha.

471. HTTP request é abortado durante `httpClient.ts` undici request
     → physical request aborta; zero retry posterior.

472. shutdown signal chega durante `httpClient.ts` body consumption
     → body read encerra; task registry settle.

473. request_deadline expira durante retry backoff
     → abortableSleep termina imediatamente; nenhuma nova attempt.

474. client_abort acontece durante retry backoff
     → nenhuma nova attempt; provider failure metric não incrementa.

475. attempt_timeout com operation budget restante
     → retry permitido conforme policy.

476. attempt_timeout sem operation budget restante
     → zero retry.

477. redirect 1 consome metade do budget
     → redirect 2 recebe apenas remaining budget, não budget novo.

478. três redirects + retry
     → deadline absoluto nunca é excedido por reset de timeout.

479. initializer termina antes do deadline
     → readiness ready; scheduler registrado uma vez.

480. initializer CANCEL_ON_TIMEOUT excede deadline
     → signal aborta, join conclui e nenhum timer é instalado.

481. initializer DETACH_TO_BACKGROUND excede readiness deadline
     → ownership transfere ao registry; first-use junta a mesma generation.

482. initializer antigo A fica lento; first-use tenta iniciar B
     → generation/singleflight impede duas authoritative generations concorrentes.

483. shutdown começa enquanto late initializer tenta instalar interval
     → registry frozen rejeita scheduler install.

484. `performEpochCleanup` ativo durante SIGTERM
     → registry drena/cancela antes de redis.quit.

485. `sweepLegacyMetaComponentKeys` abortado no meio
     → completion marker não é gravado; próximo boot pode retomar.

486. recommendation interval armado, sem sweep ativo, SIGTERM
     → interval é limpo; zero sweep posterior.

487. recommendation sweep ativo, SIGTERM
     → task aborta/join antes de Redis close.

488. playstate initial delay ainda não venceu, SIGTERM
     → timeout limpo; zero sync iniciado.

489. playstate sync ativo escrevendo DB, SIGTERM
     → loop observa signal; drain termina antes de database.close.

490. cache cleanup initial 30s timeout armado, stop chamado
     → timeout não dispara cleanup.

491. cache cleanup callback já ativo, stop chamado
     → stopAdmission imediato + drain aguarda callback.

492. MovieLens interval armado, SIGTERM
     → handle limpo; zero sync novo.

493. popular warming interval armado, SIGTERM
     → handle limpo; zero warm novo.

494. id-mapper scheduled update ativo, shutdown
     → cleanup impede próximos ticks e active update entra no drain.

495. anime-list mapper scheduled update ativo, shutdown
     → disposer + drain antes de resource close.

496. IMDb ratings scheduled update ativo, shutdown
     → disposer + drain antes de Redis close.

497. wiki mapper scheduled update ativo, shutdown
     → disposer + drain antes de Redis close.

498. eventLoop monitor iniciado
     → shutdown chama stopEventLoopMonitor exatamente uma vez.

499. cold-store sweep timer armado
     → clear timer precede flushNow/close.

500. cold-store sweep já ativo
     → active sweep settle precede close.

501. poster store sweep timer armado
     → disposer limpa timer.

502. poster warm queue possui workers ativos
     → admission freeze impede novos; active workers abort/drain.

503. DashboardAPI heap timer habilitado
     → dispose limpa timer.

504. MAL memory cleanup interval e Trakt queue cleanup interval
     → classification ledger contém owner/disposer ou SAFE_IGNORE justificado.

505. Jellyfin upgraded socket conectado no SIGTERM
     → upgrade registry envia close e keepalive timer é limpo.

506. Jellyfin socket não fecha dentro do grace
     → forced path destrói socket; shutdown reporta forced, não graceful.

507. novo upgrade chega depois de freeze
     → rejeitado sem criar perUser/timer.

508. socket emite close e error em sequência
     → disposer/perUser decrementa uma vez.

509. deepHealth probe excede deadline
     → loser classification não produz late mutation; resource lifecycle seguro.

510. deviceAuth Redis GET excede deadline
     → caller recebe miss; late read não altera session result e Redis close não ocorre antes de settle/ownership.

511. TMDB keyword Redis SETEX excede timeout race
     → command não fica órfão sem owner; shutdown sabe esperar/cancelar.

512. TMDB network Redis SETEX idem
     → mesmo invariant.

513. Jellyfin Next Up build excede response deadline
     → response usa previous/empty; detached build aparece no background registry.

514. Next Up detached build + invalidateResume generation change
     → late result não publica cache incompatível.

515. Next Up detached build + shutdown
     → abort/drain conforme BackgroundExecutionContext; zero late resource access.

516. manifest studio fetch timeout
     → underlying provider/queue work aborta ou possui explicit detached owner.

517. Trakt genres timeout com fallback
     → fallback retorna, mas underlying work não fica órfão.

518. full graceful shutdown com todos schedulers habilitados
     → registry final = 0 antes de DB/Redis close; graceful=true.

519. full forced shutdown com um task deliberadamente non-cooperative
     → task/sockets remanescentes aparecem no report; graceful=false; nenhuma falsa declaração de drain.

520. fault composto: BR filtered catalog + TMDB request via cancellable transport + refresh-ahead +
     recommendation sweep + Jellyfin upgraded socket + late initializer + SIGTERM
     → nenhum stale HIDE, nenhum cursor inválido, zero orphan write, zero scheduler novo após freeze,
       upgraded socket encerrado, resources fechados somente após registered work drain e telemetry final correta.
```

A suíte acumulada passa a ser:

```text
520+ casos determinísticos/golden/integration/concurrency/fault/load
+
property tests históricos
+
conditional HTTP / disconnect / runtime / distributed refresh V20–V21
+
Async-Occurrence / transport retry / scheduler / startup-loser / upgraded-socket V22.
```

---

# 497. Definition of Done V22

Além de todo DoD V8→V21:

```text
[ ] checkout HEAD/tree corresponde ao snapshot ou Rebase/Delta gates foram rerodados
[ ] Async-Occurrence Ledger é gerado do checkout, não copiado de busca externa
[ ] zero Promise.race/timer/scheduler/detached-work occurrence sem classification
[ ] stale classification também falha CI

[ ] addon/utils/httpClient.ts aceita OperationContext signal/deadline
[ ] undici request recebe signal efetivo
[ ] redirect preserva signal/deadline absoluto
[ ] addon/utils/retry.ts possui abortable backoff
[ ] client/shutdown/deadline cancellation nunca inicia retry novo
[ ] attempt timeout continua distinguível de operation cancellation

[ ] startup initializer timeout possui loser policy A/B/C explícita
[ ] late initializer não cria scheduler após shutdown freeze
[ ] first-use retry não compete com initializer generation antiga
[ ] initializer side effects/intervals possuem ownership depois de readiness timeout

[ ] performEpochCleanup e metaHashMigration sweep são registered background work
[ ] nenhum completion marker é gravado após cancel parcial
[ ] startup maintenance drena antes de Redis close

[ ] BackgroundWorkRegistry possui freeze/abort/drain report
[ ] timer stop e active-work drain são estados distintos
[ ] registry admission é consultada também por manual/admin triggers

[ ] recommendations refresh possui stop + active sweep drain
[ ] Jellyfin playstate sync guarda/limpa initial timeout + interval e drena active sync
[ ] cacheCleanupScheduler guarda/limpa initial timeout e drena active cleanup
[ ] essential/popular/MovieLens schedules possuem handles/disposers
[ ] eventLoopLag disposer existente é registrado
[ ] cold-store sweep handle é limpo antes do store close
[ ] id/anime-list/IMDb/wiki periodic updates possuem lifecycle central
[ ] id-mapper não depende de signal handler paralelo para correctness ordering
[ ] poster store/handler/warmQueue lifecycle está explicitamente fechado
[ ] DashboardAPI heap timer possui dispose
[ ] MAL/Trakt memory timers possuem explicit classification

[ ] Jellyfin upgraded sockets possuem registry global de shutdown
[ ] upgrade admission congela junto com HTTP business admission
[ ] socket keepalive timer é limpo exatamente uma vez
[ ] forced socket destroy é distinguido de graceful socket close

[ ] todos os 14 Promise.race files do snapshot possuem loser policy explícita
[ ] Jellyfin Next Up detached work possui BackgroundExecutionContext + generation guard
[ ] Redis read/write losers não ficam usando resource fechado sem owner

[ ] shutdown final segue freeze → stop producers → abort → drain work → drain sockets → flush → close resources
[ ] graceful=true somente quando work/socket registries chegaram a zero dentro do grace
[ ] forced/non-cooperative leftovers aparecem em telemetry/report

[ ] 520+ matrix V8→V22 passa
[ ] dark deploy + homogeneous fleet + kill switch + rollback drill permanecem válidos
```

---

# 498. Resultado final da auditoria V22

## 498.1. O que a V22 corrige na V21

A V21 acertou os boundaries difíceis de HTTP disconnect, Node runtime, shared-flight cancellation, refresh fencing,
shutdown ordering e response finalization. O gap residual não era a arquitetura de release visibility; era a
**closure do inventário físico de trabalho assíncrono**.

A V22 fecha:

```text
- occurrence ledger realmente reconciliável com o checkout;
- shared HTTP transport cancellation;
- retry/backoff cancellation;
- startup Promise.race loser ownership;
- detached startup maintenance;
- scheduler registry global;
- initial-delay/interval/recursive-timeout ownership;
- active callback drain, não só timer clear;
- initializer-owned periodic refreshes;
- poster/background resource disposers;
- Jellyfin upgraded socket lifecycle;
- explicit classification dos 14 Promise.race encontrados no snapshot.
```

## 498.2. Estado de engenharia

```text
V22 = implementation-ready design para o snapshot fixado,
      condicionado aos gates executáveis definidos no documento.

Não existe justificativa técnica para chamar a V21 de inválida:
ela continua sendo a base arquitetural correta.

Mas a claim máxima de "zero occurrence conhecido sem classificação"
só fica defensável depois da camada V22 e do ledger gerado em CI.
```

## 498.3. Definição precisa de “100%” nesta versão

> **“100%” significa cobertura rastreável do snapshot fixado por source occurrence + caller closure + state/resource ownership + testes/gates executáveis. Não significa prometer ausência metafísica de bugs nem correção de upstreams externos. A claim só é válida enquanto HEAD/tree/dependencies/runtime permanecem dentro do fingerprint auditado e enquanto o Async-Occurrence Ledger, Rebase/Delta/Caller gates e a matriz V8→V22 passam.**

## 498.4. Checklist executivo V22

```text
1. fixe HEAD/tree/runtime/dependency fingerprint;
2. gere o Async-Occurrence Ledger do checkout;
3. implemente BackgroundWorkRegistry + SchedulerHandle lifecycle;
4. torne httpClient/retry signal/deadline-aware;
5. feche startup timeout losers/generations;
6. registre startup maintenance detached;
7. dê stop + drain a todos os schedulers/resource timers listados;
8. registre/feche Jellyfin upgraded sockets;
9. execute shutdown freeze→drain→flush→resource-close;
10. prove zero orphan/detached-unowned work;
11. rode os 520+ casos acumulados + static occurrence gate;
12. dark deploy + homogeneous fleet + kill switch + rollback drill.
```

---

# 499. Reauditoria normativa V23 — Deferred Work / Flush / Bespoke Retry Closure

## 499.1. Snapshot revalidado

A V23 foi reaudita sobre o mesmo snapshot da V22:

```text
branch: dev
HEAD:   6e83e22ab9de5093f9918a1871157f401feebb03
Tree:   00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue #742: open
```

O compare `6e83e22... → dev` está `identical` no momento desta reauditoria.
Logo os achados V23 não são consequência de drift; são **gaps residuais de classificação/ownership dentro do mesmo snapshot**.

## 499.2. O que foi rechecado

Além dos gates V8→V22, a V23 executa uma reconciliação específica de:

```text
setTimeout
setInterval
setImmediate
.unref()
Promise.race
explicit detached void promises
unawaited .catch(...) side effects
write-behind / coalesced flush
manual background jobs
stale-while-revalidate rebuilds
startup fire-and-forget maintenance
provider-local retry/backoff sleeps
resource-owned keep-alive agents
```

## 499.3. Resultado funcional da #742

A rechecagem dos pontos diretamente relacionados a release visibility não encontrou uma nova classe funcional que invalide a arquitetura acumulada:

```text
hideUnreleased / catalogFiltersActive / applyCatalogFilters
isReleasedDigitally / releaseAvailability
TMDB release_dates ingress
watch_region / with_release_type / params.region
Discover Builder / Collection reconstruction
catalog/search/warmer callers
```

continuam cobertos pelo mapa V8→V22.

O delta V23 é predominantemente de **lifecycle correctness**: impedir que operações já inventariadas como “background” ou “best effort” atravessem cancellation/shutdown e mutem DB/Redis/filesystem/cache após o owner ter sido fechado.

## 499.4. Regra de prova V23

A V23 separa três níveis que não podem mais ser confundidos:

```text
SOURCE OCCURRENCE
→ algo existe fisicamente no checkout.

CLASSIFICATION
→ sabemos se é request-owned, background-owned, resource-owned, embedded-client-only ou safe-detach.

LIFECYCLE CLOSURE
→ existe owner + stop/freeze + abort/drain/flush/dispose + teste de late completion.
```

Encontrar uma string e mencioná-la no plano **não** prova closure.

---

# 500. Novos blockers objetivos V23

Os blockers residuais encontrados no snapshot são:

```text
FV.  O V22 registra 46 arquivos backend com setTimeout, mas 9 desses arquivos não apareciam
     em nenhuma seção do documento; a claim de ledger materializado não fechava fisicamente.

FW.  addon/lib/metricsBatch.ts arma timer unref para flush Redis; shutdown chama flushMetrics(),
     porém não cancela o timer nem prova join de um flush já ativo antes de redis.quit.

FX.  addon/lib/jellyfin/ids.ts faz delayed DB write e exporta flushPendingJellyfinIds(), mas o
     snapshot não possui caller de shutdown para essa função; pending IDs podem ser perdidos ou
     um callback pode competir com database.close().

FY.  addon/lib/metaColdStore/store.ts usa setImmediate para flush e flushNow() pode aguardar
     encoding antes de tocar SQLite; shutdown pode executar outro flush/close enquanto um flush
     anterior ainda está vivo.

FZ.  addon/lib/posterCache/upstream.ts mantém hostCache/resolving + HTTP/HTTPS keep-alive agents
     e destroy timer unref; não existe disposer operacional que congele admission e feche tudo.

GA.  addon/lib/posterCache/store.ts possui setImmediate de eviction além do sweep/index scan já
     mapeados; limpar apenas sweepTimer não fecha active/scheduled eviction.

GB.  configApi.js inicia warmRecommendations() por setImmediate depois do save e responde sem
     registrar ownership; shutdown/config-resave pode deixar uma geração antiga trabalhando.

GC.  configApi.js também dispara syncCollectionImages(...).catch(...) sem await/registry;
     pins/warmQueue podem ser alterados depois de nova config ou durante shutdown.

GD.  addon/utils/recommendations/jobs.ts inicia void async IIFE para jobs manuais; o trabalho
     pode ler histórico, chamar modelo, gravar picks e hidratar art sem BackgroundWorkRegistry.

GE.  addon/utils/recommendations/catalog.ts chama void markSeen(userUUID); é uma escrita Redis
     barata que hoje não possui owner e não há razão para deixá-la órfã.

GF.  addon/lib/jellyfin/watched.ts inicia stale-while-revalidate com void rebuild(); a snapshot
     antiga é devolvida corretamente, mas o rebuild precisa generation/commit guard + lifecycle owner.

GG.  addon/lib/jellyfin/items.ts limpa o imageFlushTimer no flush de shutdown, mas um flush já
     iniciado pode continuar em Redis; timer ownership e active-work ownership são estados distintos.

GH.  server.ts inicia runNginxImport() e authSession.backfillSessionIndex() sem await/registry;
     ambos fazem side effects reais em resources que também participam do shutdown.

GI.  episodeIndex.ts e jellyfin/playstate.ts possuem Redis writes fire-and-forget; precisam de
     classificação explícita de bounded best-effort I/O ou tracking até Redis close.

GJ.  addon/utils/concurrency.ts fornece sleep(ms) não abortável e vários providers mantêm sleeps
     próprios; o Shared HTTP/Retry Gate do V22 não caller-fecha esses backoffs bespoke.

GK.  addon/lib/anilist.ts, addon/lib/tvdb.ts, addon/lib/tvmaze.ts e addon/lib/anilistTracker.js
     podem continuar aguardando rate-limit/retry depois do request deadline ou shutdown signal.

GL.  oauthPage.ts aparece no setTimeout scan, mas seus timers são window.setTimeout dentro de HTML
     entregue ao browser; sem classificação EMBEDDED_CLIENT_ONLY o ledger produz falso blocker.

GM.  A execução do occurrence gate precisa ser separada do workflow pull_request_target do PR Guard;
     qualquer checkout/teste de código de fork em contexto privilegiado seria regressão de segurança.

GN.  A prova de 'zero occurrence sem classificação' precisa de artifact/manifest versionado com
     HEAD/tree/scanner-version + counts + file:line:kind:owner:policy, não apenas texto de busca.

GO.  O shutdown normativo precisa incluir write-behind/deferred-flush e upstream agents na ordem
     de recursos; freeze de schedulers sozinho não impede late Redis/DB/filesystem access.
```

---

# 501. Snapshot Occurrence Reconciliation Gate V23

## 501.1. Nove arquivos `setTimeout` ausentes do V22

O ledger V23 deve materializar pelo menos estes paths, ausentes do texto V22 apesar de pertencerem ao conjunto backend de `setTimeout`:

| Arquivo | Ocorrência / papel | Classificação normativa V23 |
|---|---|---|
| `addon/lib/metricsBatch.ts` | coalesced Redis flush timer | `RESOURCE_WRITE_BEHIND / REDIS` |
| `addon/lib/oauthPage.ts` | `window.setTimeout` no HTML gerado | `EMBEDDED_CLIENT_ONLY / NO_BACKEND_LIFECYCLE` |
| `addon/lib/posterCache/upstream.ts` | delayed keep-alive agent destroy | `RESOURCE_OWNED / HTTP_AGENT` |
| `addon/utils/concurrency.ts` | generic sleep | `OPERATION_OR_BACKGROUND_DELAY` |
| `addon/lib/jellyfin/ids.ts` | delayed DB persistence | `RESOURCE_WRITE_BEHIND / DATABASE` |
| `addon/lib/anilist.ts` | rate-limit/retry waits | `REQUEST_OR_BACKGROUND_BACKOFF` |
| `addon/lib/tvmaze.ts` | retry sleep | `REQUEST_OR_BACKGROUND_BACKOFF` |
| `addon/lib/tvdb.ts` | 429 exponential backoff | `REQUEST_OR_BACKGROUND_BACKOFF` |
| `addon/lib/anilistTracker.js` | tracker retry delays | `REQUEST_OR_BACKGROUND_BACKOFF` |

## 501.2. `setImmediate` ledger

No snapshot atual, o backend possui pelo menos estes cinco arquivos com `setImmediate`:

```text
addon/lib/configApi.js
addon/lib/metaColdStore/store.ts
addon/lib/posterCache/store.ts
addon/utils/recommendations/refresh.ts
addon/lib/jellyfin/playstateSync.ts
```

A V22 já possuía arquitetura para refresh/playstate scheduler, mas não fechava fisicamente:

```text
configApi recommendation warm
metaColdStore deferred flush
posterCache deferred eviction
```

Esses três passam a ser mandatory occurrences.

## 501.3. `.unref()` ledger

No snapshot, os paths localizados com `.unref()`/`.unref?.()` incluem:

```text
addon/index.ts
addon/lib/cacheRefreshAhead.ts
addon/lib/dashboardApi.js
addon/lib/posterCache/upstream.ts
```

`unref()` apenas permite o processo sair; **não** cancela callback, I/O ou side effect.
Logo nunca conta como disposer.

## 501.4. Zero-occurrence cases

No snapshot revalidado, buscas de backend por:

```text
Promise.any(
queueMicrotask(
process.nextTick(
```

não produziram ocorrências relevantes no mesmo audit pass.
O manifest deve registrar count `0`, pois um zero explícito protege contra drift futuro.

## 501.5. Authority

Busca externa/manual é ferramenta de auditoria, não authority final.
O gate de merge gera o manifest a partir do checkout e exige:

```text
manifest.headSha == git rev-parse HEAD
manifest.treeSha == git rev-parse HEAD^{tree}
manifest.scannerVersion == expected
manifest.unclassified == 0
manifest.staleClassifications == 0
```

---

# 502. Deferred Flush / Write-Behind Closure Gate

Delayed writes precisam de protocolo diferente de scheduler periódico.
O owner correto possui quatro estados:

```text
accepting
scheduled
active
closed
```

## 502.1. Contrato comum

Criar primitive compartilhada ou seguir contrato equivalente:

```ts
interface DeferredFlushController {
  schedule(): void;
  freeze(): void;
  flush(): Promise<void>;
  dispose(): Promise<void>;
  isScheduled(): boolean;
  isActive(): boolean;
}
```

Invariantes:

```text
freeze impede nova admissão;
dispose cancela timer/immediate ainda não executado;
dispose aguarda active flight;
final flush acontece depois de freeze e antes do resource close;
nenhum callback antigo rearma novo trabalho;
dispose é idempotente.
```

## 502.2. `addon/lib/metricsBatch.ts`

Problema atual:

```text
schedule()
→ setTimeout(... flushMetrics().catch(...)).unref()

shutdown
→ chama flushMetrics()
→ não limpa timer
→ não sabe se outro flush já está ativo
```

Alteração obrigatória:

```text
- guardar timer;
- guardar activeFlush Promise;
- freeze antes do traffic drain;
- clearTimeout(timer);
- serializar flushMetrics por single active flight;
- mover counters para batch local atomicamente;
- em falha durante shutdown, reportar dropped/failed counters;
- await active + final batch;
- só então redis.quit.
```

Preferir API:

```ts
stopAndFlushMetrics(): Promise<FlushReport>
```

em vez de registrar `flushMetrics()` diretamente no shutdown.

## 502.3. `addon/lib/jellyfin/ids.ts`

O arquivo já possui uma boa base:

```text
flushPendingJellyfinIds()
→ clearTimeout(flushTimer)
→ persiste pending batch
```

O gap é ownership global e active-flight join.

Obrigatório:

```text
- registrar disposer no shutdown antes de database.close;
- adicionar accepting=false no freeze;
- não aceitar novo pending row depois do freeze sem política explícita;
- guardar activePersist Promise;
- join de callback que já retirou batch de pending;
- final flush do pending remanescente;
- database.close somente depois.
```

A falha deve remover `persisted` como hoje e aparecer em shutdown telemetry.

## 502.4. `addon/lib/jellyfin/items.ts`

`scheduleImageFlush()` já possui timer handle e `flushRememberedImages()` limpa timer.
Isso fecha apenas `scheduled`, não `active`.

Adicionar:

```text
activeImageFlush
freezeImageWrites()
disposeImageWrites()
```

Shutdown:

```text
freeze
→ clear timer
→ join active flush
→ final pendingImages flush
→ Redis close
```

## 502.5. `addon/lib/metaColdStore/store.ts`

`put()` usa:

```text
setImmediate(() => flushNow())
```

`flushNow()` pode:

```text
splice queue
→ await encodeCachePayload(...)
→ depois acessar db.prepare(...)
```

Logo `await flushNow(); close()` no shutdown não prova que **outro flush anterior** já terminou.

Alteração obrigatória:

```text
- guardar Immediate handle;
- clearImmediate durante dispose;
- activeFlush singleflight/mutex;
- freeze admission de put();
- nenhum flush paralelo toca SQLite;
- final drain/flush;
- close somente após activeFlush == null e queue vazia.
```

`close()` deve falhar em teste/debug se:

```text
writeQueue.length > 0 || activeFlush != null || flushImmediate != null
```

ou produzir report explícito no forced path.

---

# 503. Config-Save / Manual Background Work Closure Gate

## 503.1. `configApi.js` — recommendation warm

Após salvar configuração, o snapshot executa conceitualmente:

```text
setImmediate(() => warmRecommendations(config, userUUID))
→ response já pode ter sido enviado
```

Esse warm não é request-owned depois do save; é **CONFIG_GENERATION_BACKGROUND**.

Obrigatório:

```text
ownerKey = recommendation-warm:<userUUID>
generation = configVersion/configUpdatedAt forte
snapshot = immutable config clone
policy = LATEST_GENERATION_WINS
shutdown = CANCEL_AND_JOIN ou bounded DRAIN
```

Se nova config for salva:

```text
warm geração A não pode publicar artefato incompatível depois da geração B.
```

Se `warmRecommendations` não puder abortar imediatamente, todo publish final precisa generation-check.

## 503.2. `configApi.js` — collection image sync

O save também dispara `syncCollectionImages(...).catch(...)`.

Esse trabalho:

```text
setPins
→ pode alterar pin ownership
→ pode ofertar warmQueue work
```

Logo não é `SAFE_IGNORE`.

Registrar como:

```text
ownerKey = collection-image-sync:<userUUID>
generation = saved config revision
resources = poster store + warm queue
```

Late generation antiga não pode remover/adicionar pins da configuração mais nova.

## 503.3. `addon/utils/recommendations/jobs.ts`

`startJob()` cria um job em memória e inicia `void (async () => {...})()`.

Converter para owner explícito:

```ts
startJob(ctx, configSnapshot, userUUID, catalogId)
```

com:

```text
BackgroundExecutionContext.signal
config generation
job generation/id
registry registration
terminal states: done | error | cancelled | superseded
```

O endpoint manual/admin precisa consultar admission do registry.
Depois de freeze:

```text
startJob
→ não inicia novo modelo/network/meta warm
→ responde shutdown/unavailable de forma determinística.
```

## 503.4. `addon/utils/recommendations/catalog.ts`

`markSeen(userUUID)` já captura a própria falha e é uma escrita Redis curta.
A opção preferida é simples:

```text
await markSeen(userUUID)
```

porque deixar essa operação como `void` não entrega benefício relevante e aumenta a superfície de lifecycle.

Se o projeto insistir em detach:

```text
trackBestEffortRedisWrite(promise)
```

com drain antes de `redis.quit`.

---

# 504. SWR / Best-Effort Detached I/O Gate

## 504.1. `addon/lib/jellyfin/watched.ts`

O stale-while-revalidate atual:

```text
return stale snapshot imediatamente
+
void rebuild().catch(...).finally(...)
```

é válido como UX, mas precisa de owner.

Adicionar:

```text
ownerKey = jellyfin-watched-rebuild:<scopeHash>
generation = watched source/filter generation
signal = background registry signal
commit guard = generation ainda autoritativa
```

Invariantes:

```text
um rebuild por key/generation;
shutdown freeze impede novo rebuild;
late old rebuild não publica em hydrated/lastGood;
rebuild ativo entra no drain;
failed/retry state não é escrito depois de cancel.
```

## 504.2. `addon/lib/jellyfin/episodeIndex.ts`

O Redis `SET ... NX` fire-and-forget é cache write de baixo valor.
Classificar explicitamente como:

```text
BEST_EFFORT_CACHE_WRITE / REDIS
```

Mas `BEST_EFFORT` não significa resource-unowned.

Duas implementações aceitáveis:

```text
A. await write no producer se custo desprezível;
B. active Redis-write set limitado + drain antes de redis.quit.
```

Nunca manter promises ilimitadas em memória.

## 504.3. `addon/lib/jellyfin/playstate.ts`

Aplicar o mesmo contrato a pipelines Redis terminados em:

```text
.exec().catch(() => undefined)
```

Definir no ledger se a escrita é:

```text
correctness-relevant → await/mandatory drain
cache/index best-effort → bounded tracked write
```

Silenciar erro não substitui classification.

---

# 505. Poster Cache Deferred Work / Upstream Agent Disposal Gate

## 505.1. `addon/lib/posterCache/store.ts` eviction

Além do sweep já coberto pela V22, há:

```text
scheduleEviction()
→ setImmediate(... evict() ...)
```

Adicionar:

```text
evictionImmediate handle
activeEviction Promise
evictionAdmission flag
```

Disposer:

```text
freeze eviction admission
→ clearImmediate ainda pendente
→ await active eviction
→ impedir finally/callback de reagendar
```

O initial `indexed = scan()` permanece background-owned e também precisa settle/drain quando o store for descartado.

## 505.2. `addon/lib/posterCache/upstream.ts`

O host cache possui resources reais:

```text
http.Agent keepAlive
https.Agent keepAlive
TLS session cache
hostCache
resolving promise map
delayed destroy timer
```

Criar API operacional — não depender de helper `_resetConnectionCache()` de teste:

```ts
freezeUpstreamConnections(): void;
disposeUpstreamConnections(): Promise<void>;
```

## 505.3. Timer ownership

`scheduleDestroy(entry)` precisa guardar handles em um set.

No dispose:

```text
freeze
→ clear todos destroy timers
→ destroy cached agents agora
→ aguardar/cancelar resolving promises conforme capacidade do resolver
→ qualquer resolve que finalize após freeze NÃO chama storeHost
→ agents recém-criados após freeze são destruídos imediatamente
→ hostCache/resolving/timer sets terminam vazios.
```

## 505.4. Late DNS/connection result

Se DNS resolver não for cancelável:

```text
não fingir cancellation;
transferir ownership ao drain;
aplicar generation/frozen check antes de publish no cache.
```

## 505.5. Shutdown ordering

Poster upstream disposal acontece antes de declarar o poster subsystem fechado e antes do process exit report.

---

# 506. Startup Detached Maintenance Closure V23

A V22 cobriu `performEpochCleanup()` e legacy meta-key sweep, mas o boot atual possui outros dois side effects detached.

## 506.1. `runNginxImport()`

Esse path:

```text
varre filesystem recursivamente
lê cache nginx legado
shapePoster(...)
store.put(...)
grava completion marker
```

Portanto não é safe-ignore.

Classificar:

```text
owner = startup-poster-import
resources = filesystem + poster store
policy = DETACH_TO_BACKGROUND ou AWAIT_BOOT explicitamente escolhida
shutdown = CANCEL_AND_JOIN/DRAIN
```

Se mantido detached:

```text
- passa BackgroundExecutionContext;
- loop observa signal entre arquivos;
- marker .nginx-import-completed só é escrito após conclusão real;
- cancel parcial não escreve marker;
- poster store não é disposed antes do import settle.
```

## 506.2. `authSession.backfillSessionIndex()`

Esse path faz:

```text
Redis SCAN/GET-like reads
ZSET writes
TTL reads
index expiry writes
```

Registrar:

```text
owner = startup-auth-session-backfill
resource = redis
shutdown = CANCEL_AND_JOIN ou DRAIN
```

O scanner precisa aceitar signal entre páginas/items.

## 506.3. Readiness semantics

A decisão de deixar esses jobs fora do critical readiness path é válida somente se:

```text
readiness não depende do resultado
+
work possui owner
+
first-use correctness não exige completion
+
shutdown conhece o work.
```

---

# 507. Bespoke Retry / Sleep Closure Gate V23

## 507.1. Problema

A V22 tornou `addon/utils/retry.ts` signal/deadline-aware, mas o snapshot possui backoff fora desse helper.

Paths obrigatórios:

```text
addon/utils/concurrency.ts
addon/lib/anilist.ts
addon/lib/tvdb.ts
addon/lib/tvmaze.ts
addon/lib/anilistTracker.js
```

E callers já conhecidos do `sleep()` compartilhado em request/background paths precisam ser reclassificados.

## 507.2. Primitive única

Promover `sleep()` para:

```ts
sleep(ms: number, signal?: AbortSignal): Promise<void>
```

ou reutilizar `abortableSleep()` do retry core.

Requisitos:

```text
signal já aborted → rejeita imediatamente com typed cancellation;
abort durante wait → clearTimeout + remove listener + rejeita;
resolve normal → remove listener;
zero double-settle;
zero timer orphan;
```

## 507.3. Deadline absoluto

Backoff request-owned recebe também operation deadline.
Antes de dormir:

```text
remaining = deadlineAt - now
if remaining <= 0 → deadline cancellation
sleep(min(delay, remaining), signal)
```

Não iniciar novo attempt se o sleep terminou por deadline/abort.

## 507.4. AniList

Substituir inline waits de:

```text
rate limit reset
minimum interval
Retry-After
reset timestamp
```

por primitive cancelável.

Se a mesma classe é usada por warmer/background work:

```text
request caller → OperationContext.signal
background caller → BackgroundExecutionContext.signal
```

## 507.5. TVDB / TVMaze / AniListTracker

Aplicar o mesmo contrato aos exponential/network backoffs.

Cancellation taxonomy:

```text
client_abort
request_deadline
shutdown_abort
```

não conta como provider failure e não alimenta failure/backoff cache como erro upstream.

## 507.6. Legacy behavior

Caller que ainda não possui context pode omitir signal temporariamente para preservar comportamento,
mas precisa aparecer no Caller-Closure Gate com classificação e migration owner.

Nenhum caller fica invisível por usar helper genérico.

---

# 508. Snapshot Occurrence Manifest + CI / PR Security Gate

## 508.1. Manifest gerado

Adicionar script read-only, por exemplo:

```text
scripts/generate-async-occurrence-ledger.ts
```

Saída determinística:

```json
{
  "schema": 1,
  "headSha": "...",
  "treeSha": "...",
  "scannerVersion": "...",
  "counts": {},
  "occurrences": []
}
```

Cada occurrence contém no mínimo:

```text
path
line
kind
snippetHash
ownerClass
lifecyclePolicy
resourceClass
classificationVersion
```

Não armazenar source text sensível nem secrets.

## 508.2. Stable classification

Classification pode viver em arquivo versionado, por exemplo:

```text
scripts/async-occurrence-classifications.json
```

O checker falha se:

```text
occurrence nova sem classification
classification sem occurrence correspondente
snippet/path/line drift não reconciliado
unknown owner/policy
count inesperadamente zero para scanner obrigatório
```

Line number isolado não deve ser identidade única; usar semantic key + snippet hash para tolerar deslocamento benigno e exigir review real quando a ocorrência muda.

## 508.3. Workflow seguro

O **scanner/test runner que faz checkout do PR** deve executar em workflow `pull_request` com permissões mínimas, por exemplo:

```text
permissions:
  contents: read
```

O workflow `pull_request_target` existente do PR Guard:

```text
NÃO faz checkout do código do fork
NÃO executa npm script do PR
NÃO executa scanner carregado do PR
```

Ele pode permanecer apenas como intake metadata/API guard.

## 508.4. Artifact de auditoria

CI publica o JSON ledger e um summary:

```text
HEAD/tree
counts por primitive
unclassified count
stale classification count
changed occurrence list
```

O PR description pode anexar esse summary, mas a autoridade é o artifact produzido pelo checkout seguro.

---

# 509. Shutdown / Resource Ordering V23 — ordem normativa final

A ordem V22 é estendida para contemplar write-behind e resource-owned agents.

```text
0. capture shutdown generation/deadline; tornar transition idempotente.

1. freeze external admission:
   HTTP business routes
   in-process routes
   admin/manual job triggers
   Jellyfin upgrades
   config-save background producers
   refresh-ahead/revalidation admission

2. freeze internal producers:
   scheduler registry
   recommendation/playstate/cache cleanup warmers
   write-behind schedule()
   poster eviction/import/new upstream-host admission
   stale-while-revalidate rebuild creation

3. cancel pending delayed callbacks:
   timeouts
   intervals
   immediates
   recursive timers
   initial-delay timers
   delayed agent-destroy handles

4. abort request/background operations que suportam cancellation:
   provider HTTP
   retry/backoff sleeps
   startup maintenance
   recommendation jobs
   SWR rebuilds
   warm workers

5. drain active non-resource-final work:
   request/shared flights
   startup losers
   recommendation jobs
   warmers/workers
   poster import/index/eviction
   watched rebuilds
   tracked best-effort Redis writes

6. drain/flush resource write-behind while resources ainda estão vivos:
   metrics active + final batch
   Jellyfin pending ID mappings
   Jellyfin remembered images
   meta cold-store active + final queue
   any correctness-critical buffered write

7. drain/close connection-owned resources:
   Jellyfin upgraded sockets
   poster upstream keep-alive agents / resolving ownership
   transport-owned sockets conforme contrato

8. close persistent/shared resources:
   poster/cold-store handles conforme dependência
   database
   Redis
   remaining resources na ordem de dependency graph

9. final telemetry/report:
   registries == 0
   deferred controllers closed
   sockets == 0
   upstream agents/timers == 0
   pending write queues == 0
   forced leftovers explicitamente listados
```

## 509.1. Regra de dependency graph

Não confiar apenas em `phase: traffic/resource` textual.
Cada closer declara dependências:

```text
metrics dependsOn redis
jellyfinIds dependsOn database
jellyfinArtwork dependsOn redis
metaColdStore flush dependsOn sqlite store open
nginxImport dependsOn posterStore
posterUpstream disposal owns agents/timers
```

O shutdown executor valida que um resource não fecha enquanto existir registered work dependente.

---

# 510. Mandatory File / Caller / Occurrence Map V23

Além do mandatory map V8→V22, estes paths são obrigatórios no implementation PR e no review ledger.

```text
addon/lib/metricsBatch.ts
→ delayed Redis flush timer + active flush + stopAndFlush lifecycle.

addon/lib/jellyfin/ids.ts
→ delayed DB write + active persist + shutdown registration.

addon/lib/jellyfin/items.ts
→ delayed artwork Redis flush + active flush join.

addon/lib/metaColdStore/store.ts
→ setImmediate flush + single active flush + freeze/final flush/close.

addon/lib/posterCache/store.ts
→ initial scan + sweep + deferred eviction lifecycle.

addon/lib/posterCache/upstream.ts
→ hostCache/resolving/agent/destroy-timer disposer.

addon/lib/posterCache/nginxImport.ts
→ startup poster import background context + cancel/marker semantics.

addon/server.ts
→ register new startup/background/disposer owners in dependency-safe order.

addon/lib/authSession.ts
→ startup session backfill signal/ownership.

addon/lib/configApi.js
→ recommendation warm + collection image sync background generations.

addon/lib/collectionImageCacheSync.ts
→ generation-safe pin sync + warmQueue admission.

addon/utils/recommendations/jobs.ts
→ manual job BackgroundExecutionContext + terminal cancellation state.

addon/utils/recommendations/catalog.ts
→ markSeen awaited ou tracked.

addon/lib/jellyfin/watched.ts
→ SWR rebuild generation/commit guard + registry ownership.

addon/lib/jellyfin/episodeIndex.ts
→ fire-and-forget Redis cache write classification/tracking.

addon/lib/jellyfin/playstate.ts
→ detached Redis pipeline classification/tracking.

addon/utils/concurrency.ts
→ abort-aware sleep primitive.

addon/lib/anilist.ts
addon/lib/tvdb.ts
addon/lib/tvmaze.ts
addon/lib/anilistTracker.js
→ bespoke retry/rate-limit sleeps migrated para cancellation context.

addon/lib/oauthPage.ts
→ EMBEDDED_CLIENT_ONLY occurrence classification; nenhuma mudança de backend lifecycle exigida.
```

## 510.1. Caller-closure para novos owners

Para cada função alterada:

```text
quem inicia?
quem cancela?
quem espera?
qual resource usa?
qual generation autoriza publish?
o que acontece após freeze?
qual test prova late completion?
```

Nenhum `start*`, `schedule*`, `put*`, `mark*`, `rebuild*`, `sync*` ou fire-and-forget modificado entra no merge sem essas respostas.

---

# 511. Matriz de testes adicional V23 — casos 521–560

Adicionar cumulativamente:

```text
521. metrics timer armado + SIGTERM
     → timer é limpo; final batch executa uma vez; zero callback após redis.quit.

522. metrics flush já ativo + SIGTERM
     → shutdown junta active flush antes de final flush/redis.quit; zero double-exec.

523. metrics write chega depois de freeze
     → rejeitado/contabilizado pela política; não rearma timer.

524. Jellyfin ID flush timer armado + shutdown
     → clear timer + pending batch persistido antes de database.close.

525. Jellyfin ID DB write já ativo + shutdown
     → active persist settle antes de database.close.

526. Jellyfin ID persist falha no shutdown
     → report registra falha e persisted markers são revertidos; sem falso graceful silent success.

527. Jellyfin image timer armado + shutdown
     → clear timer + pending image hashes flushados antes de Redis close.

528. Jellyfin image flush já ativo + shutdown
     → active flush entra no drain; final pending batch não compete.

529. cold-store setImmediate armado + shutdown
     → immediate cancelado; queue final flushada uma vez antes de close.

530. cold-store flush ativo parado em encodeCachePayload + shutdown
     → shutdown aguarda active flight; db.close só ocorre depois.

531. cold-store put depois de freeze
     → não agenda Immediate nem adiciona write invisível.

532. poster eviction Immediate armado + dispose
     → clearImmediate; zero evict posterior.

533. poster eviction já ativa + dispose
     → disposer aguarda active eviction; estado termina quiescent.

534. poster upstream delayed destroy timer armado + dispose
     → timer limpo; agents destruídos imediatamente uma vez.

535. poster host resolve pendente + freeze + resolve tardio
     → não repopula hostCache; agents tardios são destruídos/owned.

536. poster upstream dispose repetido
     → idempotente; cache/timer/resolving registries terminam vazios.

537. nginx import ativo lendo milhares de arquivos + SIGTERM
     → cancel/drain antes de poster store disposal; marker não é escrito em conclusão parcial.

538. nginx import completa normalmente
     → marker é escrito somente depois de todos writes aceitos/settled pela política definida.

539. auth session backfill ativo + SIGTERM
     → scan para/junta antes de redis.quit; zero ZADD tardio.

540. config save agenda recommendation warm e shutdown congela admission antes do Immediate
     → warm não inicia.

541. recommendation warm geração A ativo, config geração B salva
     → A não publica resultado autoritativo sobre B.

542. collection image sync geração A termina depois da B
     → pins finais refletem B; A não desfaz/adiciona estado obsoleto.

543. collection image sync durante shutdown
     → trabalho entra no drain; warmQueue não aceita novos items após freeze.

544. recommendations startJob chamado após registry freeze
     → zero async IIFE/model/provider work iniciado; resposta terminal determinística.

545. recommendation job ativo + shutdown
     → terminal state cancelled/forced conforme caso; zero late cache/art publish.

546. recommendation job geração antiga termina após supersede
     → result não substitui geração nova.

547. markSeen no caminho normal
     → operação é awaited ou aparece em tracked Redis-write set; zero orphan promise.

548. watched stale rebuild ativo + shutdown
     → abort/drain; zero late lastGood/hydrated publish após freeze.

549. watched rebuild geração A + invalidation/generation B
     → late A é descartado no commit guard.

550. episodeIndex best-effort Redis SET ativo + redis shutdown
     → tracked write settle/cancel policy ocorre antes de redis.quit; registry não cresce sem bound.

551. playstate best-effort pipeline ativo + redis shutdown
     → mesma invariance de resource ownership.

552. oauthPage browser HTML contém window.setTimeout
     → scanner classifica EMBEDDED_CLIENT_ONLY; nenhuma falsa exigência de backend disposer.

553. concurrency.sleep(signal) recebe signal já aborted
     → rejeita imediatamente; nenhum timer/listener residual.

554. concurrency.sleep(signal) é abortado durante wait
     → clearTimeout + listener cleanup + typed cancellation.

555. concurrency.sleep termina normalmente
     → listener removido; zero double-settle em abort tardio.

556. AniList aguarda Retry-After e request é abortado
     → wait termina; nenhum attempt seguinte; cancellation não vira provider failure.

557. TVDB 429 exponential backoff + deadline
     → nenhum retry depois do deadline.

558. TVMaze/AniListTracker retry wait + shutdown
     → background/request signal termina sleep e nenhum novo transport attempt inicia.

559. occurrence manifest no snapshot atual
     → todos Promise.race/setInterval/setTimeout/setImmediate/.unref/detached-classified paths têm entry;
       os 9 arquivos setTimeout ausentes na V22 aparecem; unclassified=0; stale=0.

560. fault composto V23: regional BR filtered catalog + request cancellation + provider bespoke backoff +
     config-save warm + watched SWR rebuild + cold-store active flush + pending Jellyfin IDs + poster host resolve + SIGTERM
     → nenhum stale HIDE/cursor incompatível, nenhum retry pós-deadline, nenhum publish de geração antiga,
       nenhuma DB/Redis/filesystem write após close, nenhum agent/timer órfão e telemetry final distingue graceful/forced.
```

A suíte acumulada passa a ser:

```text
560+ casos determinísticos/golden/integration/concurrency/fault/load
+
property tests históricos
+
conditional HTTP / disconnect / runtime / distributed refresh V20–V21
+
Async-Occurrence / transport retry / scheduler / startup-loser / upgraded-socket V22
+
deferred flush / config-save background / bespoke retry / poster-agent / startup-maintenance V23.
```

---

# 512. Definition of Done V23

Além de todo DoD V8→V22:

```text
[ ] HEAD/tree continuam exatamente no fingerprint V23 ou todos Rebase/Delta/Occurrence gates foram rerodados
[ ] manifest de occurrences é gerado pelo checkout seguro e contém HEAD/tree/scannerVersion
[ ] zero occurrence sem classification e zero classification stale
[ ] os 9 setTimeout files ausentes na V22 estão presentes/classificados
[ ] setImmediate e .unref paths possuem ownership explícito
[ ] EMBEDDED_CLIENT_ONLY diferencia browser timers de backend timers

[ ] metricsBatch possui freeze + timer clear + active flush join + final flush
[ ] shutdown usa stopAndFlushMetrics (ou contrato equivalente) antes de redis.quit
[ ] Jellyfin ID write-behind possui shutdown registration e active persist join
[ ] Jellyfin artwork flush distingue scheduled timer de active flush
[ ] metaColdStore put/flush usa Immediate handle + serialized active flush + admission freeze
[ ] metaColdStore não fecha SQLite enquanto qualquer flush anterior pode retornar do encode e tocar DB

[ ] poster eviction setImmediate é cancelável/drainable
[ ] poster initial scan/sweep/eviction terminam quiescent no disposer
[ ] poster upstream host cache possui production disposer
[ ] delayed agent-destroy timers são tracked e limpos
[ ] late DNS/resolve não repopula cache depois de freeze
[ ] HTTP/HTTPS keep-alive agents e TLS session state são fechados no shutdown

[ ] config-save recommendation warm usa immutable config generation + registry owner
[ ] collection image sync é generation-safe e registry-owned
[ ] manual recommendation jobs consultam admission e suportam cancellation/supersede
[ ] recommendation markSeen não fica como orphan Redis write
[ ] watched SWR rebuild possui owner + generation commit guard
[ ] episodeIndex/playstate fire-and-forget Redis writes são awaited ou bounded+tracked

[ ] runNginxImport é awaited ou registered background work
[ ] partial nginx import não grava completion marker
[ ] authSession backfill é registered e termina antes de Redis close

[ ] shared sleep primitive aceita AbortSignal
[ ] AniList/TVDB/TVMaze/AniListTracker bespoke waits são canceláveis
[ ] request-owned backoff respeita deadline absoluto
[ ] cancellation não alimenta provider failure/error-cache como erro upstream
[ ] background-owned backoff usa BackgroundExecutionContext.signal

[ ] occurrence workflow que executa checkout roda em pull_request com permissions mínimas
[ ] pull_request_target PR Guard nunca executa código do fork
[ ] shutdown dependency graph impede resource close com dependents ativos
[ ] final report inclui timers/immediates/write queues/agents/background writes ativos
[ ] graceful=true somente com registries/queues/agents/sockets zerados

[ ] 560+ matrix V8→V23 passa
[ ] dark deploy + homogeneous fleet + kill switch + rollback drill continuam obrigatórios
```

---

# 513. Resultado final da auditoria V23

## 513.1. O que mudou em relação à V22

A V22 resolveu corretamente o grande problema de lifecycle: criou o conceito de occurrence ledger, registry, abortable transport, startup-loser policy, scheduler disposers e socket drain.

A V23 encontrou que a **implementação da prova ainda estava incompleta no próprio plano**.
A contagem dizia `46 setTimeout files`, mas nove arquivos não estavam materializados; e vários trabalhos side-effecting escapavam do mapa por não parecerem “scheduler” clássico.

A V23 fecha especificamente:

```text
- delayed Redis metrics flush;
- delayed Jellyfin ID DB persistence;
- active Jellyfin image flush;
- meta cold-store setImmediate/write-behind race;
- poster deferred eviction;
- poster upstream keep-alive agent/destroy lifecycle;
- nginx legacy cache import detached at startup;
- auth session backfill detached at startup;
- config-save recommendation warm;
- config-save collection image sync;
- manual recommendation async jobs;
- recommendation markSeen orphan write;
- watched stale-while-revalidate rebuild;
- Jellyfin best-effort Redis writes;
- generic + bespoke provider retry sleeps;
- browser-only timer classification;
- manifest/CI authority and pull_request_target safety boundary.
```

## 513.2. Estado de engenharia

```text
V23 = implementation-ready design para o snapshot fixado,
      com coverage claim mais defensável do que V22,
      condicionado à execução dos gates e testes definidos.
```

A arquitetura central da #742 **não precisou ser reescrita**.
O novo delta é uma extensão de lifecycle/operational correctness necessária para que a palavra “completo” seja coerente com o inventário físico real do snapshot.

## 513.3. Definição precisa de “100%” V23

> **“100%” significa que, para o HEAD/tree/dependency/runtime fingerprint fixado, todas as classes de source occurrence definidas pelo scanner possuem classificação, owner e lifecycle policy rastreáveis; todos os callers correctness-critical são fechados; e todo requisito não demonstrável estaticamente foi transformado em teste/gate executável. Não significa prometer ausência metafísica de bugs, comportamento infalível de upstreams ou resultado de testes que ainda não foram executados sobre a implementação futura.**

## 513.4. Checklist executivo V23

```text
1. fixe HEAD/tree/dependency/runtime fingerprint;
2. gere e versione o Snapshot Occurrence Manifest no checkout seguro;
3. implemente/complete BackgroundWorkRegistry + dependency-aware shutdown;
4. feche delayed flushes de metrics/Jellyfin IDs/images/cold-store;
5. feche poster eviction + upstream agents + resolving/timers;
6. registre nginx import + auth-session backfill startup work;
7. torne config-save background side effects generation-safe;
8. registre/cancele manual recommendation jobs e watched SWR rebuilds;
9. elimine/classifique best-effort Redis orphan writes;
10. migre generic/bespoke sleeps para cancellation/deadline context;
11. preserve toda a arquitetura release evidence/filter/paging V8→V22;
12. rode os 560+ casos + occurrence/caller/dependency gates;
13. faça dark deploy + homogeneous fleet + kill switch + rollback drill;
14. só então sustente a claim V23 para esse fingerprint.
```

## 513.5. Condição de reauditoria

Qualquer novo commit em `dev`, alteração de dependencies/runtime ou mudança nos files classificados neste delta exige, no mínimo:

```text
Rebase/Delta Gate
Snapshot Occurrence Manifest Gate
Caller-Closure Gate
Deferred-Flush Gate
Bespoke-Retry/Sleep Gate
Background-Work/Shutdown Dependency Gate
Release-Visibility gates afetados pelo delta
```

Se o delta tocar evidence/filter/paging/config/Discover, rerodar integralmente todos os gates definidos no cabeçalho deste documento.
---

# 514. Reauditoria normativa V24 — Outbound Transport / Dispatcher / Direct-Network Closure

## 514.1. Snapshot revalidado

Esta camada V24 foi reauditada contra o mesmo snapshot fixado pela V23:

```text
branch:  dev
HEAD:    6e83e22ab9de5093f9918a1871157f401feebb03
Tree:    00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue:   #742 open
```

A rechecagem do histórico de commits confirmou que `6e83e22ab9de5093f9918a1871157f401feebb03` continua sendo o commit mais recente de `dev` no momento desta auditoria. A V24, portanto, não é um rebase funcional: é uma extensão de **closure operacional e de prova** sobre a mesma árvore.

## 514.2. Resultado da nova auditoria

A arquitetura de Release Visibility V8→V23 permanece correta como direção de implementação. O novo gap está na própria definição física da prova de lifecycle:

```text
V22/V23 scanner
→ inventaria timers, Promise.race, detached promises, schedulers, signals e sockets.

snapshot real
→ também cria dispatchers/agents de rede process-lifetime, global dispatchers,
  SOCKS dispatchers e chamadas diretas de network que podem escapar do transport compartilhado.
```

Logo, `unclassified == 0` no `AsyncOccurrenceRecord` V23 ainda não implica:

```text
zero resource sem owner
zero outbound transport sem disposer
zero direct-network caller sem signal/deadline authority
zero socket pool vivo após shutdown
```

Essa diferença é material porque a própria V23 já exige `agents/timers == 0` no relatório final, mas não possuía um inventário exaustivo dos agents que tornasse essa afirmação demonstrável.

## 514.3. Escopo normativo V24

As seções 1–513 permanecem válidas, exceto quando esta camada V24 explicita um contrato mais forte para:

```text
resource occurrence scanning
outbound dispatcher ownership
global dispatcher ownership
SOCKS dispatcher ownership
direct-network caller closure
signal/deadline composition
response-body terminal disposition
transport drain/close ordering
transport shutdown telemetry
occurrence manifest authority
```

Em qualquer conflito nesses domínios, V24 prevalece.

---

# 515. Novos blockers objetivos V24

```text
GP. O Async-Occurrence scanner V23 não inclui constructors/registrations de recursos de transporte.
    Portanto o CI pode provar zero async occurrence não classificada e ainda deixar Agent/ProxyAgent
    process-lifetime fora do ledger.

GQ. addon/utils/httpClient.ts possui directDispatcher, bootstrapDispatcher e, com proxy global,
    cria ProxyAgent inline em setGlobalDispatcher(...). O handle do ProxyAgent global não é retido,
    logo não existe close authority explícita para esse recurso.

GR. Há dispatchers process-lifetime específicos de provider fora do poster cache, incluindo TMDB,
    TVMaze, MAL/Jikan, MDBList, Simkl, Trakt e Letterboxd, sem disposer/shutdown caller localizado
    no snapshot auditado.

GS. addon/utils/gemini-client.ts e addon/utils/openrouter-client.ts já exportam closeAgent(), mas
    não existe caller localizado. Ter um closer sem registration/owner não fecha lifecycle.

GT. addon/lib/configApi.js cria geminiDispatcher próprio para testes de API key e não possui closer
    localizado; esse recurso é distinto do client Gemini usado na execução normal.

GU. TMDB, MAL e MDBList podem criar fetch-socks socksDispatcher. O plano não pode presumir que esse
    objeto possui a mesma API de close/destroy do undici.Agent sem provar o contrato da versão fixada.

GV. O Caller Closure V22 fecha callers de httpGet/httpPost/httpHead, mas o backend também possui
    chamadas diretas via undici/global fetch/request, Axios e clients/SDKs. Esses caminhos não podem
    depender implicitamente do shared transport para receber OperationContext.signal/deadline.

GW. AbortSignal.timeout() é attempt timeout; sozinho não representa client abort, request deadline
    absoluto nem shutdown cancellation. Caminhos diretos que usam somente timeout continuam capazes
    de viver após o owner lógico ter terminado.

GX. A seção 501.3 V23 materializa somente um subconjunto dos paths com .unref(). O snapshot contém
    17 arquivos backend com .unref/.unref?.; a versão normativa do manifest precisa registrar os 17.

GY. O schema AsyncOccurrenceRecord não possui resourceKind, creationAuthority, closeAuthority,
    aliases ou network caller signal/retry authority. A invariância actual-classified=empty precisa
    ser estendida para resources e direct-network callers.

GZ. A ordem de shutdown V22/V23 diz 'dispatchers/agents se explicitamente owned', mas o mapa
    obrigatório não define owners para todos os dispatchers acima. A condição é circular: justamente
    os resources não inventariados nunca se tornam 'explicitamente owned'.

HA. Telemetry V23 exige upstream agents/timers == 0, mas sem registry completo essa métrica pode
    reportar zero observável enquanto agents não registrados continuam vivos.

HB. O teste composto 560 afirma 'nenhum agent/timer órfão', porém sua cobertura concreta V23 está
    concentrada no poster upstream. A V24 torna a afirmação testável para todo outbound transport.
```

Nenhum blocker GP–HB exige reescrever a policy regional. Eles fecham a infraestrutura que sustenta o significado operacional de “completo”.

---

# 516. Resource Occurrence Manifest Gate V24

## 516.1. O manifest deixa de ser apenas async

O artefato autoritativo passa a possuir três conjuntos disjuntos e reconciliáveis:

```text
asyncOccurrences
resourceOccurrences
networkCallerOccurrences
```

A condição de merge é:

```text
actualAsync       - classifiedAsync       = ∅
actualResources   - classifiedResources   = ∅
actualNetCallers  - classifiedNetCallers  = ∅

classified* apontando para symbol/AST node inexistente = CI fail
```

## 516.2. Scanner AST mínimo ampliado

Além do scanner V23, localizar semanticamente no backend:

```text
undici.Agent / new Agent
undici.ProxyAgent / new ProxyAgent
fetch-socks socksDispatcher
undici.setGlobalDispatcher
undici.request
undici.fetch
fetch/globalThis.fetch
axios.create + axios/instance request methods
node:http Agent
node:https Agent
AbortSignal.timeout
client/SDK singleton que encapsule transporte reutilizável
exports close*/destroy*/dispose* associados a network resources
```

Não depender apenas do nome textual `Agent`: aliases/import renames precisam ser resolvidos pelo AST quando possível.

## 516.3. Resource schema

Adicionar representação equivalente a:

```ts
interface ResourceOccurrenceRecord {
  id: string;
  file: string;
  symbol: string;
  resourceKind:
    | 'undici-agent'
    | 'undici-proxy-agent'
    | 'socks-dispatcher'
    | 'global-dispatcher'
    | 'node-http-agent'
    | 'node-https-agent'
    | 'network-client'
    | 'other-long-lived-resource';

  owner: string;
  lifetime: 'process' | 'startup' | 'background' | 'request' | 'connection';
  creationAuthority: string;
  aliases: string[];
  resources: string[];

  admissionAuthority?: string;
  drainAuthority?: string;
  closeAuthority?: string;
  forceCloseAuthority?: string;

  closePolicy:
    | 'DRAIN_THEN_CLOSE'
    | 'ABORT_DRAIN_CLOSE'
    | 'DESTROY_ON_FORCED_SHUTDOWN'
    | 'EXTERNAL_LIFETIME_PROVEN'
    | 'NO_CLOSE_REQUIRED_PROVEN';

  rationale: string;
}
```

`NO_CLOSE_REQUIRED_PROVEN` não é allowlist genérica: precisa documentar por que o objeto não possui sockets/listeners/timers próprios ou por que sua vida é estritamente menor que o owner.

## 516.4. Network caller schema

```ts
interface NetworkCallerOccurrenceRecord {
  id: string;
  file: string;
  symbol: string;
  api: 'shared-http' | 'undici-request' | 'undici-fetch' | 'fetch' | 'axios' | 'sdk' | 'other';
  ownerClass: 'request' | 'background' | 'startup' | 'connection' | 'resource-maintenance';

  signalAuthority: string | null;
  deadlineAuthority: string | null;
  retryAuthority: string | null;
  dispatcherResourceId: string | null;
  bodyDisposition: 'consume' | 'cancel' | 'stream-owned' | 'not-applicable';

  mayOutliveCaller: boolean;
  classification: 'CLOSED' | 'EXPLICIT_BOUNDED_EXCEPTION';
  rationale: string;
}
```

A exceção `EXPLICIT_BOUNDED_EXCEPTION` precisa possuir teste demonstrando que o work não faz publish/write após owner completion e não impede shutdown quiescence.

---

# 517. Inventário físico de outbound dispatchers do snapshot V24

A inspeção estática localizou pelo menos os seguintes owners concretos. Estes paths passam a ser mandatory no manifest; o scanner continua sendo a authority para detectar outros.

| Arquivo | Resource | Estado do snapshot | Contrato V24 |
|---|---|---|---|
| `addon/utils/httpClient.ts` | `directDispatcher` | `undici.Agent`, process-lifetime | registrar owner + close |
| `addon/utils/httpClient.ts` | global proxy dispatcher | `new ProxyAgent(...)` passado inline a `setGlobalDispatcher` | reter handle + owner + close |
| `addon/utils/httpClient.ts` | `bootstrapDispatcher` | `Agent/ProxyAgent`, process-lifetime | registrar owner + close |
| `addon/lib/getTmdb.ts` | `dispatcher` | SOCKS/ProxyAgent/Agent | disposer explícito por variante |
| `addon/lib/tvmaze.ts` | `tvmazeAgent` | ProxyAgent/Agent | disposer explícito |
| `addon/lib/mal.ts` | `malDispatcher` | SOCKS/ProxyAgent/Agent | disposer explícito por variante |
| `addon/utils/mdbList.ts` | `mdblistDispatcher` | SOCKS/ProxyAgent/Agent | disposer explícito por variante |
| `addon/utils/simklUtils.ts` | `simklDispatcher` | Agent | disposer explícito |
| `addon/utils/traktUtils.ts` | `traktDispatcher` | ProxyAgent/Agent | disposer explícito |
| `addon/utils/letterboxdUtils.ts` | `letterboxdDispatcher` | Agent | disposer explícito |
| `addon/utils/gemini-client.ts` | `geminiDispatcher` | ProxyAgent/Agent; `closeAgent()` existe | registrar closer no lifecycle |
| `addon/utils/openrouter-client.ts` | `openrouterDispatcher` | ProxyAgent/Agent; `closeAgent()` existe | registrar closer no lifecycle |
| `addon/lib/configApi.js` | `geminiDispatcher` | ProxyAgent/Agent para key test | disposer explícito |
| `addon/lib/posterCache/upstream.ts` | pinned `http.Agent` / `https.Agent` | já fechado normativamente pela V23 | preservar V23 + incluir no resource manifest |

Regra:

```text
manual table = review aid
AST Resource Occurrence Manifest = authority
```

Se o scanner achar um 15º resource, o PR falha até classificá-lo.

---

# 518. Shared HTTP Dispatcher Ownership Gate

## 518.1. `httpClient.ts` não cria resource sem handle

Proibir:

```ts
setGlobalDispatcher(new ProxyAgent(...));
```

quando esse objeto pertence ao processo e precisa participar do shutdown.

Modelo conceitual:

```ts
const globalDispatcher = proxyUrl
  ? new ProxyAgent(...)
  : directDispatcher;

setGlobalDispatcher(globalDispatcher);
```

O registry conhece identidade/alias:

```text
globalDispatcher === directDispatcher
→ um único physical resource
→ close exactly once
```

## 518.2. Bootstrap dispatcher

`bootstrapDispatcher` continua separado porque possui connect-timeout/configuração própria.
Seu lifecycle é process-owned mesmo que os requests sejam startup-owned.

Depois que bootstrap termina, duas estratégias são válidas:

```text
A. manter reutilizável até shutdown e fechar na fase de transport resources;
B. fechar imediatamente após o último bootstrap consumer, se caller closure provar que não haverá reuso.
```

Escolher uma e testar; não deixar lifetime emergir implicitamente do module cache.

## 518.3. Close semantics

Shutdown gracioso:

```text
freeze network admission
→ abort/drain request/background/startup work
→ nenhum novo request usa dispatcher
→ dispatcher.close() / API equivalente comprovada
→ assert resource registry vazio
```

Forced shutdown:

```text
grace deadline expirou
→ destroy/force-close somente onde API/semântica comprovarem segurança
→ report graceful=false
```

Não chamar `destroy()` como caminho normal apenas para encurtar shutdown.

---

# 519. Provider Dispatcher Closure Gate

Cada singleton de provider listado na seção 517 precisa exportar ou registrar um disposer idempotente.

Contrato mínimo:

```text
freeze admission
no new provider operation
abort/drain active operations do owner
close dispatcher
clear registry entry
```

### 519.1. TMDB

`addon/lib/getTmdb.ts` possui três famílias de dispatcher:

```text
SOCKS
HTTP(S) proxy
Direct Agent
```

As três precisam convergir para um `disposeTmdbTransport()` ou registry equivalente sem presumir interface comum que não foi validada.

### 519.2. TVMaze / MAL / MDBList / Simkl / Trakt / Letterboxd

Mesmo contrato. Um provider que usa o shared `httpClient` para parte das requests e dispatcher próprio em outra parte continua possuindo dois boundaries distintos; o manifest precisa refletir ambos.

### 519.3. Gemini / OpenRouter

Os `closeAgent()` já existentes deixam de ser dead lifecycle API:

```text
server/runtime registration
→ freeze AI admission
→ drain/abort active AI calls
→ closeAgent()
```

### 519.4. Config API Gemini dispatcher

O dispatcher de validação de API key não deve ser confundido com o dispatcher do Gemini runtime.
Ele precisa owner próprio ou precisa reutilizar explicitamente um transport compartilhado com identidade/lifetime compatíveis.

---

# 520. SOCKS Dispatcher Contract Gate

Antes de implementar disposer genérico, provar na versão lockada de `fetch-socks`:

```text
qual objeto socksDispatcher(...) retorna;
se expõe close/destroy;
se delega a Agent/dispatcher interno;
se mantém sockets/timers próprios;
como cancellation signal é propagado;
qual comportamento ocorre com request ativo durante teardown.
```

Resultado permitido:

```text
1. API possui disposer comprovado
   → registrar e testar.

2. API não possui disposer público, mas resource interno é acessível/owned de forma suportada
   → wrapper explícito + teste.

3. API não oferece lifecycle control seguro
   → classificar boundary como limitação e substituir por transport com ownership verificável
      antes de sustentar graceful=true sob uso SOCKS.
```

Nunca chamar `.close()`/`.destroy()` por adivinhação de shape.

---

# 521. Direct-Network Caller Closure Gate V24

## 521.1. O shared transport não é suficiente

A regra V22:

```text
classificar todos os callers de httpGet/httpPost/httpHead
```

é necessária, mas não suficiente.

A V24 exige classificar **todo outbound network call** detectado pelo AST, inclusive quando ele usa:

```text
undici.fetch
undici.request
global fetch
Axios
provider SDK/client
custom dispatcher
```

## 521.2. Operation context

Request-owned network call:

```text
OperationContext.signal
+
absolute deadline
+
per-attempt timeout
```

Background/startup call:

```text
BackgroundExecutionContext.signal
+
owner deadline/budget quando aplicável
```

Per-attempt timeout não substitui parent signal.

## 521.3. Signal composition

Criar primitive única, por exemplo:

```ts
createAttemptSignal({
  parentSignal,
  absoluteDeadlineAt,
  attemptTimeoutMs,
})
```

Ela deve:

```text
preservar reason/taxonomy do primeiro cancel authority efetivo;
remover listeners/timers ao settle;
não criar timer se parent já estiver aborted;
não estender deadline absoluto entre retry/redirect;
ser compatível com o runtime Node fixado/testado.
```

Taxonomy continua:

```text
client_abort
shutdown_abort
request_deadline
attempt_timeout
provider_network_error
provider_http_error
```

## 521.4. Retry authority

Uma direct-network call não pode implementar retries invisíveis fora do OperationContext budget.

Se SDK/library possui retry interno:

```text
desabilitar
OU
configurar dentro do mesmo budget
OU
classificar explicitamente e provar que parent cancellation interrompe o retry loop.
```

---

# 522. Response Body / Connection Reuse Closure Gate

Para callers baseados em `undici.request`/streams/response bodies:

```text
every acquired response body
→ consumed
OU cancelled/destroyed por caminho suportado
OU transferido explicitamente para stream owner que entra no registry.
```

Early return, HTTP error, parse failure, redirect, client abort e shutdown não podem deixar body sem terminal disposition quando isso retiver conexão/pool state.

Esse gate é especialmente importante depois de tornar os dispatchers explicitamente owned: um body órfão pode impedir `close()` de atingir quiescence dentro do grace period.

---

# 523. `.unref()` Reconciliation V24

A V23 estava correta ao afirmar que `unref()` não é disposer, mas sua subseção normativa listava apenas um subconjunto. No snapshot fixado, os 17 arquivos backend localizados com `.unref()`/`.unref?.()` são:

```text
addon/lib/cacheRefreshAhead.ts
addon/lib/jellyfin/playstateSync.ts
addon/server.ts
addon/lib/deviceAuthSessions.ts
addon/index.ts
addon/lib/posterCache/upstream.ts
addon/lib/eventLoopLag.ts
addon/lib/jellyfin/ids.ts
addon/lib/metricsBatch.ts
addon/lib/inProcessRoutes.ts
addon/utils/recommendations/refresh.ts
addon/lib/posterCache/warmQueue.ts
addon/lib/posterCache/handler.ts
addon/lib/jellyfin/resume.ts
addon/lib/jellyfin/items.ts
addon/lib/dashboardApi.js
addon/lib/posterCache/store.ts
```

O manifest versionado deve registrar a occurrence exata por AST node, não apenas o número de arquivos.

Regras:

```text
unref timer + side effect
→ continua precisando owner/stop/drain.

unref timer puramente local/observability
→ ainda precisa classificação e disposer ou SAFE_IGNORE provado.
```

---

# 524. Snapshot Reconciliation Matrix V24

Para o HEAD fixado, o audit pass localizou estes **contadores por arquivo backend contendo a primitive**:

```text
setTimeout(         → 46 arquivos backend
setInterval(        → 19 arquivos backend
setImmediate(       → 5 arquivos backend
.unref/.unref?.     → 17 arquivos backend
Promise.race(       → 14 arquivos backend
AbortSignal.timeout → 6 arquivos backend
```

Também foram localizados:

```text
new ProxyAgent(...) → 9 arquivos backend
socksDispatcher(...) → 3 arquivos backend
setGlobalDispatcher(...) → addon/utils/httpClient.ts
closeAgent() exportado → Gemini + OpenRouter, sem caller localizado no snapshot
```

Esses números são **reconciliation tripwires**, não substituem o manifest AST por occurrence. Se um refactor mantiver o mesmo número de arquivos e mover/adicionar occurrence, o manifest ainda precisa detectar o delta.

---

# 525. Shutdown V24 — transport phase autoritativa

A ordem acumulada V23 passa a explicitar transport resources:

```text
0. mark shutdown generation / freeze global admission

1. freeze external admission
   - HTTP business routes
   - in-process routes
   - admin/manual jobs
   - Jellyfin upgrade
   - config-save background producers
   - provider/AI/network admission

2. freeze internal producers/schedulers/write-behind admission

3. cancel delayed callbacks/timers/immediates

4. abort request/background/startup operations
   - parent OperationContext/BackgroundExecutionContext
   - retry/backoff
   - direct network callers

5. drain active logical work
   - requests/shared flights
   - background/startup work
   - active network operations
   - streams whose owner must finish gracefully

6. flush write-behind while DB/Redis/filesystem remain alive

7. close connection/transport resources
   - Jellyfin upgraded sockets
   - poster upstream agents
   - shared httpClient global/direct/bootstrap dispatchers
   - TMDB/TVMaze/MAL/MDBList/Simkl/Trakt/Letterboxd dispatchers
   - Gemini/OpenRouter/configApi Gemini dispatchers
   - SOCKS resources according to proven contract

8. close persistent resources
   - cold-store/store handles
   - database
   - Redis

9. dispose memory/observability-only owners

10. final assertion/report
   - async registry == 0
   - resource registry == 0
   - network caller active == 0
   - upgraded sockets == 0
   - pending write queues == 0
   - pending response bodies/streams == 0
   - forced leftovers explicitly enumerated
```

`graceful=true` somente quando todos os registries autoritativos estão zerados.

---

# 526. Mandatory File / Caller / Resource Map V24

Além de todo mandatory map V8→V23:

```text
addon/utils/httpClient.ts
→ retain global dispatcher handle; direct/bootstrap/global resource registration; disposer.

addon/lib/getTmdb.ts
→ dispatcher variant ownership (SOCKS/Proxy/Agent) + dispose + direct-call signal composition.

addon/lib/tvmaze.ts
→ tvmazeAgent disposer + retry/network context.

addon/lib/mal.ts
→ malDispatcher variant ownership + retry/network context.

addon/utils/mdbList.ts
→ mdblistDispatcher variant ownership + direct fetch/shared-call closure.

addon/utils/simklUtils.ts
→ simklDispatcher disposer + caller context.

addon/utils/traktUtils.ts
→ traktDispatcher disposer + existing queue/retry lifecycle integration.

addon/utils/letterboxdUtils.ts
→ letterboxdDispatcher disposer.

addon/utils/gemini-client.ts
→ register existing closeAgent + active-call drain/abort contract.

addon/utils/openrouter-client.ts
→ register existing closeAgent + active-call drain/abort contract.

addon/lib/configApi.js
→ config-test geminiDispatcher disposer + request signal/deadline authority.

addon/lib/posterCache/upstream.ts
→ preserve V23 node http/https agent disposer and include in generic Resource Manifest.

addon/server.ts
addon/lib/lifecycle/runtime.ts
addon/lib/lifecycle/shutdown.ts
→ ResourceRegistry registration + dependency/order enforcement + final transport telemetry.

scripts/async-occurrence-scanner.* / equivalent
→ evolve to lifecycle occurrence scanner covering async + resources + network callers.
```

## 526.1. Direct network closure is generated, not hand-maintained

O mandatory map acima destaca resources já provados. A lista completa de direct callers não deve ser copiada manualmente para sempre; o AST scanner gera o conjunto e o CI exige classificação sem wildcard.

---

# 527. Observabilidade V24

Adicionar métricas/logs sem secrets/URLs sensíveis:

```text
lifecycle_resource_active{kind,owner}
network_operation_active{owner_class,transport}
transport_close_total{owner,result}
transport_force_destroy_total{owner,reason}
transport_close_duration_ms{owner}
shutdown_unclosed_resources_total{kind}
shutdown_active_network_total{owner_class}
network_body_terminal_disposition_total{result}
```

Final shutdown report deve listar nomes de owners pendentes, não credenciais/endpoints completos.

Exemplo conceitual:

```json
{
  "graceful": false,
  "activeResources": ["tmdb-dispatcher"],
  "activeNetworkOperations": 1,
  "forced": ["tmdb-dispatcher"],
  "pendingWrites": 0
}
```

---

# 528. Matriz de testes adicional V24 — casos 561–600

Adicionar cumulativamente aos 560+ casos V8→V23:

```text
561. httpClient sem proxy + shutdown gracioso
     → directDispatcher fecha uma vez; ResourceRegistry termina vazio.

562. httpClient com HTTP_PROXY
     → ProxyAgent global possui handle retido e fecha; nenhum resource inline inacessível.

563. bootstrapDispatcher criado + bootstrap completo + shutdown
     → lifetime escolhido A/B é obedecido; zero double-close/reuse-after-close.

564. globalDispatcher === directDispatcher
     → alias registry fecha o physical resource exatamente uma vez.

565. shared http request ativo + SIGTERM
     → parent shutdown abort/drain ocorre antes de dispatcher close.

566. network admission depois do freeze
     → nenhum novo shared/direct request começa e nenhum dispatcher novo é alocado.

567. TMDB direct Agent + shutdown
     → request settle/abort; disposeTmdbTransport fecha resource.

568. TMDB ProxyAgent + shutdown
     → mesmo contract; zero proxy socket residual.

569. TMDB SOCKS + shutdown
     → comportamento segue contrato comprovado de fetch-socks; sem método inventado.

570. TVMaze request/retry ativo + shutdown
     → backoff/network para e tvmazeAgent fecha depois do drain.

571. MAL/Jikan dispatcher ativo + shutdown
     → zero request/retry após close.

572. MDBList dispatcher ativo + shutdown
     → shared/direct branches entram no mesmo parent lifecycle.

573. Simkl dispatcher ativo + shutdown
     → active operation termina/cancela antes do close.

574. Trakt queue + network ativo + shutdown
     → queue admission freeze + active retry/network drain + dispatcher close.

575. Letterboxd request ativo + shutdown
     → dispatcher close somente após terminal body disposition.

576. configApi API-key test ativo + shutdown
     → config-test geminiDispatcher possui owner e não sobrevive ao runtime.

577. Gemini runtime closeAgent registrado
     → shutdown chama exatamente uma vez após active AI calls drainarem/abortarem.

578. OpenRouter runtime closeAgent registrado
     → mesma invariância.

579. AI closeAgent chamado com request ainda ativo
     → lifecycle ordering impede close prematuro; forced path fica explícito.

580. dispatcher.close falha/rejeita
     → shutdown report lista owner e graceful=false; erro não é silenciado.

581. dispatcher não fecha antes do grace deadline
     → force policy executa somente API comprovada; graceful=false.

582. shutdown chamado duas vezes
     → todos transport disposers idempotentes; zero double-destroy/double metric.

583. initializer tardio tenta criar dispatcher após freeze
     → registration/admission rejeita ou resource é imediatamente disposed; zero leak.

584. direct undici/global fetch request-owned + client disconnect
     → parent client_abort cancela underlying I/O, não só a resposta HTTP local.

585. direct network request-owned + server shutdown
     → shutdown_abort propaga até transport.

586. direct network background-owned + registry cancel
     → BackgroundExecutionContext.signal interrompe I/O e publish tardio é proibido.

587. path com somente AbortSignal.timeout mas parent context disponível
     → AST/lint/gate falha até compor parent signal.

588. parent client_abort vence attempt timeout
     → taxonomy final = client_abort; retry=false.

589. attempt timeout vence com operation budget restante
     → taxonomy = attempt_timeout; retry somente conforme classifier/budget.

590. absolute deadline vence antes do attempt timeout
     → request_deadline; nenhum retry inicia.

591. composed signal settle normal
     → timers/listeners auxiliares removidos; zero listener leak em load test.

592. parent signal aborta durante retry sleep
     → sleep cancela imediatamente e nenhuma nova attempt começa.

593. redirect/retry em direct caller
     → remaining absolute budget diminui; nenhum hop renova budget.

594. Axios/IMDb outbound caller
     → manifest classifica signal/deadline/body lifecycle ou registra bounded exception testada.

595. SDK/client outbound caller (ex.: Kitsu)
     → retry/cancellation internos são conhecidos; nenhuma retry authority escondida.

596. response adquirida + early HTTP error/parse failure
     → body consumido/cancelado/owned; dispatcher.close não fica preso por body órfão.

597. global dispatcher proxy handle
     → final ResourceRegistry sabe exatamente qual objeto físico foi instalado globalmente.

598. `.unref()` snapshot reconciliation
     → os 17 arquivos backend estão representados; qualquer novo path sem classification falha CI.

599. Resource/Network Occurrence Manifest
     → new Agent/ProxyAgent/SOCKS/global dispatcher/direct-network occurrence não classificada falha CI;
       stale record também falha.

600. fault composto V24: catálogo BR filtrado + request abort + provider retry + config background work
     + active shared/direct network + SIGTERM
     → nenhuma stale HIDE/cursor incompatível, nenhum retry/I/O pós-deadline, nenhum late publish/write,
       todos dispatchers/agents/body owners terminam zerados ou aparecem explicitamente como forced,
       e graceful=true só ocorre com Async + Resource + Network registries em zero.
```

A suíte acumulada passa a ser:

```text
600+ casos determinísticos/golden/integration/concurrency/fault/load
+
property tests históricos
+
release/cache/pagination/config/Discover gates V8→V18
+
request/HTTP/shared-work/runtime/shutdown gates V19→V21
+
async occurrence/background/scheduler/socket gates V22
+
deferred flush/config-save/retry/poster/startup gates V23
+
resource occurrence/outbound dispatcher/direct-network closure gates V24.
```

---

# 529. Definition of Done V24

Além de todo DoD V8→V23:

```text
[ ] HEAD/tree/dependency/runtime fingerprint continua válido ou Rebase/Delta gates foram rerodados
[ ] lifecycle occurrence scanner cobre async + resource + direct-network callers
[ ] actualAsync-classifiedAsync = empty
[ ] actualResources-classifiedResources = empty
[ ] actualNetCallers-classifiedNetCallers = empty
[ ] stale classifications = 0

[ ] httpClient retém handle do global ProxyAgent em vez de criar resource inacessível inline
[ ] directDispatcher/globalDispatcher/bootstrapDispatcher têm owner/lifetime/disposer explícitos
[ ] aliases de um mesmo physical dispatcher fecham exactly once

[ ] getTmdb dispatcher variants têm disposer comprovado
[ ] tvmazeAgent tem disposer
[ ] malDispatcher variants têm disposer
[ ] mdblistDispatcher variants têm disposer
[ ] simklDispatcher tem disposer
[ ] traktDispatcher tem disposer
[ ] letterboxdDispatcher tem disposer
[ ] configApi geminiDispatcher tem disposer
[ ] Gemini closeAgent possui lifecycle caller real
[ ] OpenRouter closeAgent possui lifecycle caller real
[ ] poster upstream agents continuam cobertos e entram no Resource Manifest genérico

[ ] fetch-socks lifecycle é validado contra a versão lockada; nenhum close/destroy é inventado
[ ] todos direct-network callers têm ownerClass
[ ] request-owned direct calls recebem parent signal + absolute deadline + attempt timeout
[ ] background/startup direct calls recebem execution-context signal apropriado
[ ] AbortSignal.timeout não é aceito como única cancellation authority quando parent context existe
[ ] retries internos de SDK/library estão desabilitados, integrados ao budget ou explicitamente provados
[ ] response bodies/streams possuem terminal disposition/owner

[ ] `.unref()` manifest contém todas as 17 paths backend do snapshot e occurrences exatas
[ ] shutdown fecha transport resources somente depois de abort/drain dos work owners
[ ] late initializer não consegue registrar/alocar transport órfão após freeze
[ ] final report observa ResourceRegistry e NetworkOperationRegistry autoritativos
[ ] graceful=true exige async/resources/network/sockets/queues todos quiescent

[ ] 600+ matrix V8→V24 passa
[ ] dark deploy + homogeneous fleet + kill switch + rollback drill continuam obrigatórios
```

---

# 530. Resultado final da auditoria V24

## 530.1. O que a V24 corrige na V23

A V23 fechou corretamente delayed work, write-behind, retries bespoke, poster resources e manifest de async occurrences. A reauditoria V24 encontrou uma classe que o scanner não sabia enxergar: **outbound transport resources e direct-network callers**.

A V24 fecha:

```text
- Resource Occurrence Manifest;
- Network Caller Occurrence Manifest;
- global/direct/bootstrap dispatcher ownership do shared httpClient;
- provider-specific Agent/ProxyAgent/SOCKS lifecycle;
- Gemini/OpenRouter exported closers sem caller;
- configApi Gemini key-test dispatcher;
- direct fetch/request/Axios/SDK caller closure;
- parent signal + absolute deadline + attempt timeout composition;
- response body terminal disposition;
- full 17-file .unref reconciliation;
- transport-aware shutdown ordering/telemetry;
- 40 novos fault/integration tests, elevando a matriz para 600+.
```

## 530.2. Estado de engenharia

```text
V24 = implementation-ready design para o snapshot fixado,
      com uma claim de lifecycle closure mais forte que V23,
      condicionada à execução dos manifests/gates/testes definidos.
```

A arquitetura funcional de Release Visibility não foi reescrita porque a nova inspeção não encontrou um boundary funcional regional que invalide V8→V23. A mudança é uma extensão de **proof coverage** e **runtime resource ownership**.

## 530.3. Definição precisa de “100%” V24

> **“100%” nesta V24 significa: para o HEAD/tree/dependency/runtime fingerprint fixado, todas as classes de occurrence definidas pelo scanner — async, long-lived resource e outbound network caller — possuem classificação, owner e lifecycle policy rastreáveis; todos os callers correctness-critical permanecem fechados; e tudo que não pode ser demonstrado estaticamente virou gate/teste executável. Não significa garantir ausência metafísica de bugs, disponibilidade de upstreams ou resultados de testes ainda não executados sobre a implementação futura.**

## 530.4. Checklist executivo V24

```text
1. fixe HEAD/tree/dependency/runtime fingerprint;
2. implemente o lifecycle occurrence scanner AST (async + resources + network callers);
3. gere/versione o manifest no checkout seguro;
4. preserve BackgroundWorkRegistry/Scheduler/flush closure V22–V23;
5. crie ResourceRegistry + NetworkOperation ownership;
6. retenha/registre global/direct/bootstrap dispatchers do httpClient;
7. feche todos os provider dispatchers da seção 517;
8. registre os closeAgent de Gemini/OpenRouter e o dispatcher do configApi;
9. prove o lifecycle de fetch-socks antes de implementar teardown;
10. propague parent signal/deadline a todo direct-network caller;
11. prove terminal disposition de response bodies/streams;
12. execute os 600+ casos + static manifests + caller/dependency gates;
13. faça dark deploy + homogeneous fleet + kill switch + rollback drill;
14. só então sustente a claim V24 para esse fingerprint.
```

## 530.5. Condição de reauditoria

Qualquer commit posterior a `6e83e22ab9de5093f9918a1871157f401feebb03`, mudança no dependency lock ou alteração de runtime exige rerun dos gates históricos afetados e, no mínimo:

```text
Rebase/Delta Gate
Snapshot Occurrence Manifest Gate
Resource Occurrence Manifest Gate
Direct-Network Caller Closure Gate
Outbound Dispatcher Lifecycle Gate
Signal Composition Gate
Transport Drain/Close Gate
Caller-Closure Gate
Background-Work/Shutdown Dependency Gate
```

Se o delta tocar release evidence/filter/paging/config/Discover, rerodar integralmente também toda a cadeia funcional V8→V23 correspondente.

---

# 531. Reauditoria normativa V25 — Full Process Resource, Dependency-I/O & Config-Generation Closure

## 531.1. Snapshot revalidado

Esta camada V25 foi revalidada contra o **mesmo snapshot fixo** da V24:

```text
branch:  dev
HEAD:    6e83e22ab9de5093f9918a1871157f401feebb03
Tree:    00f13a1d87d769db5f6b2dbcf6f92b54eecaa80d
release: v3.1.0
issue:   #742 open, sem comentários no momento da reauditoria
```

Não houve drift de `dev`. A V25, portanto, não muda a arquitetura funcional de Release Visibility; ela fecha gaps residuais na **prova de cobertura física** e um race real de coerência de configuração que a V24 ainda deixava implícito.

## 531.2. Resultado da nova auditoria

A V24 tornou autoritativos três conjuntos:

```text
asyncOccurrences
resourceOccurrences
networkCallerOccurrences
```

A nova inspeção mostrou que o conjunto `resourceOccurrences` ainda estava semanticamente estreito demais. Seu scanner mínimo era orientado a outbound network transport, enquanto o processo real também possui:

```text
- Redis process-lifetime;
- PostgreSQL Pool primário;
- PostgreSQL Pool opcional de read replica;
- SQLite operacional;
- SQLite separado do meta cold store;
- HTTP listener/socket admission;
- FileHandle/Dir/ReadStream/WriteStream locais;
- streams de proxy cuja vida atravessa request/response;
- clients/SDKs de terceiros que encapsulam network I/O fora dos call-shapes conhecidos pelo AST.
```

Além disso, o snapshot possui uma corrida de configuração que precisa ser tratada como correctness blocker:

```text
configCache.getOrLoad(A) inicia um DB load antigo
→ usuário salva config B
→ save publica B no configCache
→ load A termina depois
→ getOrLoad pode publicar A novamente
```

Com `DATABASE_READ_URI`, uma replica atrasada pode fornecer A mesmo após B já estar confirmada no primary. `configVersion = Date.now()` não é uma authority correctness-critical suficiente para resolver isso: pode colidir no mesmo milissegundo, depende de wall clock e não é storage-monotonic entre writers.

## 531.3. Regra de precedência V25

As seções 1–530 preservam toda a arquitetura e trilha V8→V24. As seções 531+ prevalecem quando houver conflito sobre:

```text
process resource occurrence scope
persistent storage resource ownership
local stream/file-handle lifecycle
dependency-encapsulated network I/O
runtime dependency lifecycle fingerprint
config generation / cache publication fencing
read-replica stale overwrite
scanner runtime-root/reachability authority
frontend effect/resource closure
final shutdown resource accounting
```

Para evidence, release policy, pagination, TMDB Discover, search, response freshness e demais domínios não alterados aqui, permanece a cadeia de precedência anterior.

---

# 532. Novos blockers objetivos V25

```text
HC. O Resource Occurrence Manifest V24 possui `other-long-lived-resource`, mas o scanner mínimo
    materializado é orientado a network transports. No snapshot existem `new Redis(...)`,
    `new Pool(...)`, `new BetterSqlite3(...)`, HTTP listener e filesystem handles/streams que não
    são garantidamente descobertos pelo scanner descrito na V24.

HD. `addon/lib/database.ts` pode possuir dois Pools físicos em PostgreSQL: primary e read replica.
    O alias `readDb === db` ou `readDb !== db` altera a cardinalidade real de resources. A prova de
    close-exactly-once precisa representar essa aliasing; contar apenas "database" como um owner
    lógico pode esconder um Pool residual ou provocar double-close.

HE. `addon/lib/metaColdStore/store.ts` abre um BetterSqlite3 independente do DB operacional.
    Ele depende de flush de write-behind antes de close e deve ser resource occurrence físico,
    não somente uma linha manual na ordem de shutdown.

HF. `addon/server.ts` cria o HTTP listener com `addon.listen(...)`. O listener, conexões HTTP e
    upgraded sockets possuem lifecycles distintos. O listener atual é fechado manualmente, mas não
    faz parte do Resource Manifest genérico exigido pelo DoD V24.

HG. `addon/lib/posterCache/store.ts` cria ReadStream/WriteStream e FileHandle; `nginxImport.ts`
    cria `fs.Dir`; caminhos de proxy transferem ownership de upstream streams para a resposta.
    O gate V24 de response body cobre o conceito, mas o scanner não reconcilia esses recursos locais.

HH. AST de `fetch`/Axios/undici não descobre sozinho I/O escondido em dependências. O snapshot usa
    pelo menos o client dinâmico `kitsu`, `@fanart-tv/api` e `name-to-imdb`. Um manifest de callers
    pode ficar falsamente vazio para esses requests se não existir capability registry de dependências.

HI. `addon/lib/kitsu.ts` usa dynamic import via `Function('return import("kitsu")')()` e mantém
    `kitsuClientPromise` singleton. Esse boundary é deliberadamente opaco ao import graph estático
    comum e precisa de registro explícito de network/retry/timeout/cancellation/lifecycle.

HJ. `addon/utils/fanart.ts` mantém até milhares de FanartTvApi clients em LRU. Se o package lockado
    possuir agent/timer/socket/client state persistente, eviction precisa disposer; se não possuir,
    isso precisa ser provado e registrado como NO_CLOSE_REQUIRED_PROVEN.

HK. `name-to-imdb` é uma dependência que pode executar network I/O fora do shared HTTP transport.
    O caller precisa de deadline/cancellation authority comprovada ou wrapper/replacement que forneça.

HL. A regra de rerun V24 monitora principalmente Node/undici e Express para semântica de lifecycle.
    A closure agora também depende das versões lockadas de Axios, fetch-socks, Kitsu, Fanart API,
    name-to-imdb, ioredis, pg, better-sqlite3 e qualquer adapter transitivo que implemente I/O/lifecycle.

HM. O global undici dispatcher não governa automaticamente todo stack de rede. Axios/SDKs podem
    possuir proxy, redirect, timeout, DNS, connection reuse e cancellation semantics diferentes.
    "usa o mesmo HTTP_PROXY" não pode ser presumido sem teste da versão lockada.

HN. `configCache.getOrLoad()` publica o valor carregado sem generation fence. Um load antigo que
    começou antes de um save pode terminar depois e sobrescrever a configuração nova em Redis/memória.

HO. `DATABASE_READ_URI` serve reads de uma replica local. Após um save no primary, uma cache miss
    pode observar replica lag e repopular config antiga. A seção 445.2 reconhece consistência bounded,
    mas não impede regressão monotônica da revisão observada.

HP. `configVersion = Date.now()` é útil como timestamp/compatibilidade, mas não é uma generation
    correctness-critical: duas gravações podem ocorrer no mesmo ms e clocks de writers diferentes
    não fornecem ordem storage-monotonic.

HQ. A claim "completo do AIOmetadata" continua mais ampla que o scanner backend. O frontend possui
    timers, listeners, fetches, AbortControllers e object URLs com lifecycle de mount/unmount.
    Eles precisam de um manifest separado ou a claim deve ser explicitamente limitada ao processo backend.

HR. O scanner "backend" não possui definição formal de runtime roots/reachability. Dynamic require/import,
    entrypoints auxiliares e wrappers podem escapar; docs/build/generated code podem criar falsos positivos.

HS. `ResourceRegistry == 0` só é demonstrável se cada recurso detectável possuir ownership class:
    APP_OWNED, REQUEST_OWNED, BACKGROUND_OWNED, EXTERNAL_RUNTIME_OWNED ou NO_CLOSE_REQUIRED_PROVEN.
    Sem essa taxonomia, ampliar o scanner pode tornar o DoD impossível ou levar a allowlists vagas.

HT. O pass-through de imagem usa stream ownership (`upstream.data.pipe(res)`) e precisa provar que
    client disconnect/response close destrói/cancela a origem. Apenas transferir a referência para
    `stream-owned` sem terminal callback não fecha connection reuse.
```

---

# 533. Process Resource Occurrence Manifest V25

## 533.1. Quatro universos autoritativos

A reconciliação passa a possuir quatro famílias, não três:

```text
asyncOccurrences
processResourceOccurrences
networkCallerOccurrences
frontendEffectOccurrences
```

`processResourceOccurrences` é superset conceitual do `resourceOccurrences` V24. O artefato pode manter o nome antigo por compatibilidade, mas sua semântica V25 é **todo recurso process-owned ou operation-owned capaz de manter handle, socket, fd, listener, stream ou native/client state relevante ao lifecycle**.

Merge invariant:

```text
actualAsync          - classifiedAsync          = ∅
actualProcessResource- classifiedProcessResource= ∅
actualNetCaller      - classifiedNetCaller      = ∅
actualFrontendEffect - classifiedFrontendEffect = ∅

classified occurrence apontando para AST node/symbol inexistente = CI fail
wildcard/path-prefix allowlist sem occurrence id = proibida
```

## 533.2. Scanner mínimo V25

Adicionar ao scanner V24, por binding/import resolution quando possível:

```text
# storage / connection pools
new Redis / ioredis constructor
new Pool / pg.Pool
new BetterSqlite3 / Database

# inbound servers/connections
.listen(...)
http.createServer / https.createServer / net.createServer
server.close / closeIdleConnections / closeAllConnections
socket/server connection registries

# filesystem/local streams
fs.createReadStream
fs.createWriteStream
fs.promises.open / fsp.open
fs.opendir / fs.promises.opendir / fsp.opendir
FileHandle.close
Dir.close
stream.pipeline / pipeline
.pipe(...)

# process/native boundaries futuros
worker_threads.Worker
child_process.spawn / exec / execFile / fork
fs.watch / watchFile
net.Socket / tls.connect

# existing network families V24
undici Agent/ProxyAgent/request/fetch/global dispatcher
node:http/node:https Agent
fetch-socks dispatcher
Axios instance/calls
AbortSignal timeout/any
```

`execSync`/sync one-shot work é classificado, mas normalmente não cria resource persistente depois do retorno. A classificação precisa registrar isso; não ignorar apenas porque o método é síncrono.

## 533.3. Taxonomia de ownership

```ts
interface ProcessResourceOccurrenceRecord {
  id: string;
  file: string;
  symbol: string;
  astFingerprint: string;

  kind:
    | 'redis-client'
    | 'pg-pool'
    | 'sqlite-database'
    | 'http-listener'
    | 'http-connection'
    | 'upgraded-socket'
    | 'file-handle'
    | 'directory-handle'
    | 'read-stream'
    | 'write-stream'
    | 'network-dispatcher'
    | 'sdk-client'
    | 'worker'
    | 'child-process'
    | 'watcher'
    | 'other';

  ownership:
    | 'APP_OWNED'
    | 'REQUEST_OWNED'
    | 'BACKGROUND_OWNED'
    | 'STARTUP_OWNED'
    | 'EXTERNAL_RUNTIME_OWNED'
    | 'NO_CLOSE_REQUIRED_PROVEN';

  physicalResourceKey: string;
  aliases: string[];
  dependsOn: string[];
  closeAuthority: string | null;
  forceCloseAuthority: string | null;
  terminalProof: string;
}
```

`physicalResourceKey` impede double-close quando dois símbolos apontam para o mesmo objeto físico.

## 533.4. Runtime-owned não significa "ignorar"

Exemplos aceitáveis:

```text
process.stdout / process.stderr
libuv/native pools geridos integralmente pelo runtime
biblioteca stateless sem handle persistente próprio
```

A classificação `EXTERNAL_RUNTIME_OWNED` exige rationale e, para dependências, evidence da versão lockada. Ela não é um escape para resources cuja API de teardown simplesmente não foi investigada.

---

# 534. Persistent Storage Resource Closure Gate

## 534.1. Redis

Snapshot:

```text
addon/lib/redisClient.ts
→ new Redis(...)
→ process-lifetime singleton
→ server.ts registra redis.quit()
```

V25 exige:

```text
- resource manifest contém o client físico;
- admission de writes/background producers congela antes do quit;
- active operations drenam antes do close;
- quit é idempotente no lifecycle owner;
- comportamento de forced shutdown é validado contra ioredis lockado;
- `disconnect()` só é usado como force path se a semântica lockada for comprovada;
- zero reconnect após shutdown generation.
```

Event listeners (`error/connect/ready/close/reconnecting`) pertencem ao Redis owner e não podem reacender trabalho depois de shutdown.

## 534.2. PostgreSQL primary + read replica

`addon/lib/database.ts` pode possuir:

```text
this.db     = primary Pool
this.readDb = this.db
```

ou:

```text
this.db     = primary Pool
this.readDb = separate replica Pool
```

Manifest obrigatório:

```text
physicalResourceKey=pg-primary
physicalResourceKey=pg-read-replica   # somente quando distinto
```

Invariantes:

```text
readDb === db
→ um Pool físico
→ close uma vez.

readDb !== db
→ dois Pools físicos
→ ambos end() exatamente uma vez.

nenhum query admission novo após storage-freeze.
pool.end() somente depois de request/background DB users drenados.
```

Não inventar force-destroy de internals de `pg`. Se a versão lockada não oferece force close seguro, forced shutdown reporta `NO_SAFE_FORCE_CLOSE` e o processo termina após o deadline sem fingir graceful closure.

## 534.3. SQLite operacional

`new BetterSqlite3(...)` do database operacional é um recurso físico síncrono.

```text
all background/write-behind users settled
→ db.close()
→ initialized/readDb/db aliases limpos
```

`close()` durante callback que ainda pretende usar o DB é lifecycle violation testável.

## 534.4. Meta cold store SQLite

O cold store é recurso independente:

```text
flush admission freeze
→ cancelar pending immediate
→ await active flush
→ queue == 0
→ db.close()
```

O resource manifest precisa apontar dependency edges entre `meta-cold-store-db` e seu write queue/background flush owner.

---

# 535. Inbound HTTP Listener / Connection Gate

O HTTP server deixa de ser apenas closer manual e entra no process resource graph.

```text
listener owner = http-server
request connections = connection children
Jellyfin upgraded sockets = upgraded-socket children já cobertos por V22
```

Shutdown:

```text
freeze route/in-process admission
→ server.close() inicia stop de novas conexões
→ closeIdleConnections() quando suportado
→ abort/drain request contexts
→ upgraded sockets usam registry próprio
→ grace expirou: closeAllConnections() somente para HTTP normal, conforme runtime lockado
→ listener settle
```

Não contar upgraded sockets duas vezes: Node `closeAllConnections()` não substitui o registry de upgrades.

Testar explicitamente keep-alive, request em streaming e request parado após headers.

---

# 536. Local Stream / FileHandle Closure Gate

## 536.1. Poster store

`addon/lib/posterCache/store.ts` precisa ter cada stream/handle em um terminal path demonstrável:

```text
createReadStream
createWriteStream
fsp.open/FileHandle
rewrite stream
openStream() transferido ao request
```

Preferir `stream.pipeline()`/`pipeline()` quando o path conecta source→destination e a propagação de erro/cancel precisa ser bidirecional.

## 536.2. Client disconnect no art proxy

Para pass-through normal:

```text
upstream stream acquired
→ response owns stream
→ res finish = completed
→ res close/client abort antes do finish = destroy/cancel upstream
→ listener cleanup
→ network body terminal disposition registrado
```

`upstream.data.pipe(res)` sem owner cleanup explícito não é prova suficiente.

## 536.3. Directory handles no nginx import

`fsp.opendir()` occurrences entram no manifest.

Quando `for await ... of dir` for usado como authority de auto-close:

```text
Node runtime lockado
+ teste early-return
+ teste throw
+ teste shutdown abort
→ handle fecha
```

Se o runtime não garantir um caminho, usar `finally { await dir.close() }` idempotente conforme API.

## 536.4. FileHandle rules

Todo `fsp.open()`:

```text
close in finally
OU
ownership transfer explícito para helper que fecha
```

Nenhum `FileHandle` pode depender de GC para terminal disposition.

---

# 537. Dependency-Encapsulated I/O Capability Gate

## 537.1. Por que AST de callers não basta

Um call como:

```ts
client.getMovieImages(...)
client.fetch(...)
nameToImdb(...)
```

não revela por sintaxe se há:

```text
HTTP
retry
redirect
socket pooling
timeout
background timer
agent próprio
signal support
close/dispose
```

Criar `lifecycle-dependency-capabilities.json` (ou TS equivalente), gerado/validado contra `package-lock.json`.

## 537.2. Schema mínimo

```ts
interface DependencyCapabilityRecord {
  package: string;
  lockedVersion: string;
  callSites: string[];
  capabilities: Array<'network'|'pool'|'timer'|'filesystem'|'native-worker'|'none'>;

  signalSupport: 'native'|'wrapper'|'none'|'unknown';
  timeoutAuthority: string;
  retryBehavior: string;
  proxyBehavior: string;
  redirectBehavior: string;
  bodyLifecycle: string;
  disposeBehavior: string;

  verification:
    | 'LOCKED_SOURCE_INSPECTED'
    | 'RUNTIME_CONTRACT_TESTED'
    | 'BOTH';
}
```

`unknown` não é merge-ready para pacote que participa de request-owned network I/O.

## 537.3. Seeds obrigatórios do snapshot

Pelo menos:

```text
kitsu
@fanart-tv/api
name-to-imdb
axios
fetch-socks
ioredis
pg
better-sqlite3
```

Adicionar `sharp` e qualquer outro native/client package se o scanner de import-capability mostrar lifecycle relevante.

## 537.4. Kitsu

`addon/lib/kitsu.ts` possui dynamic import e singleton promise.

Obrigatório provar na versão lockada:

```text
- transport real usado pelo package;
- suporte a AbortSignal ou ausência dele;
- timeout/retry internos;
- pooling/resource lifetime;
- disposer, se existir;
- comportamento quando parent request/shutdown aborta.
```

Se não houver parent cancellation suportada, envolver/substituir o client ou classificar o call como bounded exception **somente** se o publish final for cancel-authority fenced e o work tiver prazo absoluto curto comprovado.

## 537.5. Fanart client cache

`clientCache` não pode manter clients resource-owning depois da eviction.

```text
package client stateless/no persistent resources
→ NO_CLOSE_REQUIRED_PROVEN.

package client possui agent/timer/socket
→ LRU dispose hook + shutdown clear/dispose + tests.
```

## 537.6. name-to-imdb

Toda chamada request-owned precisa de um bound explícito. Se a dependency não aceita signal/deadline:

```text
preferir wrapper/implementation com cancellation
OU
executar como bounded dependency call com absolute deadline e late-result publish fence
```

Não transformar `Promise.race(timeout, dependency)` em "cancelamento" se o loser continua executando.

---

# 538. Outbound Network Policy Parity + Lifecycle Dependency Fingerprint

## 538.1. Policy parity por transport

Cada `NetworkCallerOccurrenceRecord` passa a declarar:

```ts
transportPolicy: {
  proxyAuthority: string;
  tlsAuthority: string;
  redirectLimit: number | 'library-default-proven';
  dnsPrivateAddressPolicy: string | 'not-applicable-fixed-provider';
  signalAuthority: string;
  absoluteDeadlineAuthority: string;
  attemptTimeoutAuthority: string;
}
```

Não exigir SSRF DNS pinning de providers fixos sem motivo; exigir nos boundaries que aceitam URL/host não confiável.

## 538.2. Global dispatcher não significa global policy

Testar separadamente:

```text
undici shared/global transport
Axios
Kitsu SDK
Fanart SDK
name-to-imdb
fetch-socks variant
node:http/node:https poster transport
```

Se dois stacks devem obedecer `HTTP_PROXY/HTTPS_PROXY/NO_PROXY`, provar com integration test da versão lockada. Se a intenção do produto for diferente, registrar explicitamente a divergência.

## 538.3. Dependency fingerprint

Gerar artifact estável do lockfile para packages lifecycle-critical, por exemplo:

```text
node effective runtime
undici
axios
fetch-socks
kitsu
@fanart-tv/api
name-to-imdb
ioredis
pg
better-sqlite3
express
fresh
etag
```

Mudança de versão/resolution/transitive adapter relevante:

```text
→ CI marca lifecycle-contract-drift
→ rerun do capability gate + transport/storage/runtime tests afetados
```

O trigger não depende de alteração em source file do wrapper; mudança só no `package-lock.json` já basta.

---

# 539. Config Generation Authority / Replica-Fencing Gate

## 539.1. `configVersion` deixa de ser correctness generation

Preservar `configVersion` para compatibilidade/telemetria se necessário, mas formalizar:

```text
configVersion (Date.now)
→ timestamp/legacy hint
→ NÃO ordena writes correctness-critical.
```

Criar revision storage-monotonic por usuário, por exemplo coluna:

```text
user_configs.revision BIGINT NOT NULL
```

Cada write confirmado no primary:

```text
revision := previous revision + 1
```

A operação de upsert precisa retornar a revisão realmente commitada.

## 539.2. ConfigEnvelope

Internamente:

```ts
interface ConfigEnvelope {
  schema: 1;
  revision: string; // bigint decimal canônico
  config: AppConfig;
}
```

`loadSharedConfig()` pode continuar entregando o config read-only ao caller, mas `RequestConfigSnapshot` carrega a revision do envelope separadamente.

## 539.3. Config cache publication fence

`getOrLoad` captura uma generation local antes do loader e só publica se ainda for current.

Além disso, o Redis write precisa ser revision-aware:

```text
incoming.revision > cached.revision
→ replace

incoming.revision == cached.revision
→ idempotent only if canonical config digest equal

incoming.revision < cached.revision
→ reject stale publication
```

Não comparar BIGINT via JS Number/Lua floating point de forma que perca precisão. Usar decimal-string comparison segura, fixed-width canonical decimal, ou primitive storage que preserve inteiro exato.

## 539.4. Save ordering

```text
1. freeze/fence pending loader generation local para userUUID
2. write config no primary e obter revision commitada
3. publicar ConfigEnvelope por CAS/revision no Redis
4. atualizar memory cache com a mesma revision
5. somente então disparar background work generation-scoped
6. response pode concluir
```

Um loader iniciado antes do passo 1 pode terminar, mas não pode publicar valor mais antigo.

## 539.5. Read replica policy

Preferência V25 para correctness e simplicidade:

```text
config cache MISS de user config correctness-critical
→ ler do primary
```

O volume é amortizado pelo Redis/memory cache e elimina replica-lag como authority do config.

Se o projeto insistir em `DATABASE_READ_URI` para user config:

```text
replica envelope revision < last-known/Redis revision
→ rejeitar
→ retry primary
```

Nunca permitir que cache TTL expiry faça a aplicação "voltar" de revision N para N-1.

## 539.6. Todos os config writers convergem

Gerar caller ledger de:

```text
database.saveUserConfig(...)
configCache.set/del(...)
manager/account mutations
OAuth token mutations que reescrevem config
system/cache-warmer config writes
imports/syncs que salvam config
```

Todos usam a mesma `saveAndPublishConfigRevision(...)` authority ou equivalente. Um writer lateral não pode bypassar o fence.

## 539.7. Rollout / migration

Migration em duas fases:

```text
A. adicionar revision com default/migration, readers aceitam row antiga;
B. todos writers começam a incrementar/retornar revision;
C. cache passa dual-read old/raw + envelope, single-write envelope;
D. observação de fleet homogênea;
E. remover old cache shape somente após rollback window.
```

Rollback para baseline que ignora a coluna extra deve continuar possível; não remover/renomear campos que a versão antiga exige durante a janela.

---

# 540. Scanner Runtime-Root / Dynamic Boundary Closure

## 540.1. Runtime roots explícitos

O scanner versionado declara seus roots, no mínimo:

```text
backend service source root: addon/server.ts
backend reachable modules: addon/** + runtime helpers efetivamente importados
frontend application root: configure/src/main.tsx (ou entrypoint real do Vite)
production scripts/CLIs: somente os que são executados pelo runtime/deploy
```

`dist/**`, docs, changelog e fixtures geradas não são segunda cópia autoritativa do source.

## 540.2. Reachability não substitui broad scan

Executar dois passes:

```text
A. broad source scan
B. runtime reachability/import graph
```

Classificar diferença:

```text
broad-only
→ dead/build/test code comprovado OU forgotten runtime root.

reachable-only impossível
→ scanner bug.
```

## 540.3. Dynamic require/import

Ocorrências de:

```text
require(expr não literal)
import(expr não literal)
Function(... import(...))
module loader wrappers
```

entram em `dynamicBoundaryOccurrences`.

Cada uma precisa:

```text
resolved package/module set
capability record
reason
```

Kitsu é mandatory fixture desse gate.

## 540.4. Package capability import guard

Se runtime source importar package classificado como network/storage/native-lifecycle e não houver `DependencyCapabilityRecord`, CI falha.

Isso fecha a classe de bug "novo SDK introduziu I/O sem aparecer no NetworkCallerManifest".

---

# 541. Frontend Effect / Abort / Unmount Closure

## 541.1. Escopo

A V25 separa explicitamente:

```text
backend process lifecycle
≠
browser component lifecycle
```

Para sustentar a claim de projeto completo, criar `FrontendEffectOccurrenceManifest`.

Scanner mínimo em `configure/src/**`:

```text
setInterval / window.setInterval
setTimeout / window.setTimeout
addEventListener / removeEventListener
fetch / AbortController
WebSocket / EventSource
URL.createObjectURL / URL.revokeObjectURL
ResizeObserver / IntersectionObserver / MutationObserver
worker creation
subscriptions com disposer
```

## 541.2. React ownership

Effects/subscriptions devem classificar:

```text
MOUNT_OWNED
USER_ACTION_OWNED
ROUTE_OWNED
GLOBAL_APP_OWNED
ONE_SHOT_BOUNDED
```

Para mount/route owners:

```text
unmount/route change
→ clear timer
→ remove listener
→ abort request quando relevante
→ revoke object URL
→ ignore late result by generation/identity when network abort is not sufficient.
```

## 541.3. Seed snapshot

Code search da reauditoria localizou, entre outros:

```text
setInterval no frontend:
- configure/src/hooks/useDeviceAuth.ts
- configure/src/components/dashboard/RestartManager.tsx
- configure/src/components/sections/RecommendationsIntegration.tsx

AbortController explícito:
- configure/src/hooks/useDashboardQueries.ts
- configure/src/components/sections/IntegrationsSettings.tsx

múltiplos addEventListener/fetch/createObjectURL em configure/src/**
```

Essas listas são seed de review; o AST manifest é a authority.

## 541.4. Relação com a #742

A feature regional não deve transformar este gate em refactor indiscriminado de UI não relacionada. Porém:

```text
- todo effect existente precisa ser classificado;
- qualquer occurrence insegura em arquivo tocado pela #742 é blocker do PR;
- occurrence preexistente fora do patch só pode permanecer se SAFE/BOUNDED for provado;
- leak real encontrado não pode ser escondido com grandfather wildcard.
```

---

# 542. Shutdown V25 — ordem final com process resources

A ordem acumulada passa a ser:

```text
0. freeze shutdown generation / config generation publication

1. freeze inbound admission
   - HTTP business/admin
   - in-process
   - Jellyfin upgrade
   - config writes/manual jobs

2. freeze background producers/schedulers/network/storage admission

3. cancel timers/immediates/deferred callbacks

4. abort logical operations
   - request contexts
   - startup/background contexts
   - retry/backoff
   - direct + SDK network calls
   - stream owners

5. drain active logical work
   - requests/shared flights
   - config pending loads/writers
   - background/startup jobs
   - active network operations
   - active local/proxy streams

6. flush write-behind
   - metrics
   - Jellyfin remembered artwork
   - cold store
   - poster/config-related pending writes

7. close inbound/transport resources
   - HTTP listener/normal connections
   - upgraded sockets
   - outbound agents/dispatchers/SDK-owned transports

8. close persistent storage resources
   - meta cold-store SQLite
   - operational SQLite OR pg read replica + pg primary
   - Redis

9. dispose memory/client registries that own resources
   - SDK client caches with disposer
   - memory-only owners clear after dependencies close as appropriate

10. final assertion
   async == 0
   processResource == 0 (excluding explicitly external-runtime-owned)
   activeNetwork == 0
   activeStreams == 0
   activeFileHandles == 0
   upgradedSockets == 0
   pendingConfigLoads == 0
   pendingWrites == 0
```

`graceful=true` é proibido quando qualquer registry autoritativo possui leftover não-external.

---

# 543. Mandatory File / Caller / Resource Map V25

Além de todo mandatory map V8→V24:

```text
addon/lib/redisClient.ts
→ Redis physical resource + reconnect/quit/forced policy.

addon/lib/database.ts
→ SQLite OR pg-primary + optional pg-read-replica alias-aware resource ownership;
  primary-read primitive para correctness-critical config misses;
  revision-monotonic config persistence.

addon/lib/configCache.ts
→ ConfigEnvelope; local pending-load generation fence; revision-aware Redis CAS;
  stale loader cannot overwrite newer save.

addon/lib/configApi.js
→ configVersion remains legacy timestamp; all saves publish storage revision;
  background work uses revision generation.

addon/lib/metaColdStore/store.ts
→ SQLite resource + flush dependency + File/Immediate closure.

addon/server.ts
→ HTTP listener resource registration + normal connection force-close path after grace.

addon/lib/posterCache/store.ts
→ ReadStream/WriteStream/FileHandle occurrence registration/terminal proof.

addon/lib/posterCache/nginxImport.ts
→ fs.Dir lifetime + abort/early-return close proof.

addon/lib/posterCache/artProxyServe.ts
→ pass-through stream ownership; client disconnect destroys/cancels upstream.

addon/lib/kitsu.ts
→ dynamic dependency boundary + SDK capability/cancellation contract.

addon/utils/fanart.ts
→ Fanart SDK capability + LRU client disposal/no-close proof.

addon/lib/getTmdb.ts
addon/lib/getMeta.js
→ name-to-imdb dependency caller classification where used.

package-lock.json
package.json
Dockerfile / .nvmrc / workflows selecting Node
→ lifecycle dependency fingerprint authority.

configure/src/**
→ frontend effect occurrence manifest; cleanup/abort/object URL closure.

scripts/lifecycle-occurrence-scanner.* / equivalent
→ runtime-root + dynamic-boundary + process-resource + dependency capability + frontend effects.
```

## 543.1. Config writer caller closure

Gerar por AST/search authority todo caller de:

```text
saveUserConfig
configCache.set
configCache.del
loadSharedConfig/getOrLoad
```

Nenhum caller manual fica fora do revision/fence contract.

---

# 544. Observabilidade V25

Adicionar, sem user secrets/URLs completas:

```text
process_resource_active{kind,owner}
process_resource_close_total{kind,owner,result}
stream_active{kind,owner}
file_handle_active{kind,owner}
dependency_io_active{package,owner_class}
dependency_contract_version{package,version_fingerprint}
config_cache_publish_total{result}
config_cache_stale_publish_rejected_total
config_revision_observed{source}
config_replica_stale_read_total
config_primary_fallback_total
frontend_effect_manifest_unclassified_total   # CI/test metric, não produção obrigatória
```

Config logs podem registrar:

```text
user fingerprint opaco
revision
source = memory | redis | primary | replica
```

Nunca config body, UUID completo, token ou API key.

Shutdown report V25 exemplo:

```json
{
  "graceful": false,
  "activeResources": ["pg-read-replica"],
  "activeStreams": 0,
  "activeFileHandles": 0,
  "pendingConfigLoads": 0,
  "activeDependencyIo": [],
  "forced": [],
  "noSafeForceClose": ["pg-read-replica"]
}
```

---

# 545. Matriz de testes adicional V25 — casos 601–650

Adicionar cumulativamente aos 600+ casos V8→V24:

```text
601. Redis singleton boot + graceful shutdown
     → one physical resource; quit once; no reconnect after shutdown generation.

602. Redis quit error/timeout
     → forced policy follows locked ioredis contract; graceful=false if not clean.

603. PostgreSQL sem read replica
     → readDb aliases primary; pool.end exactly once.

604. PostgreSQL com DATABASE_READ_URI
     → two physical pools; replica + primary close exactly once, ordered after query drain.

605. read replica startup failure
     → readDb aliases primary; no phantom replica resource remains in registry.

606. operational SQLite shutdown
     → db closes only after active users drained.

607. cold-store queued write + SIGTERM
     → flush completes/cancels per policy before SQLite close; queue zero.

608. cold-store active flush + close attempt
     → lifecycle guard prevents DB close under active flush.

609. HTTP keep-alive idle connection + SIGTERM
     → admission freezes; idle closes; listener settles.

610. HTTP active request + SIGTERM
     → request abort/drain occurs inside grace; no indefinite server.close wait.

611. HTTP active request exceeds grace
     → normal connection force-close path used; graceful=false; upgraded sockets remain separately owned.

612. poster store createReadStream client abort
     → local stream closes; fd count returns baseline.

613. poster store createWriteStream write failure
     → source/destination both terminal; temp file cleanup contract passes.

614. FileHandle path throws after open
     → close in finally; zero handle leak.

615. nginx fs.Dir normal iteration
     → directory handle terminal.

616. nginx fs.Dir early return/abort
     → runtime contract/test proves close; no residual fd.

617. art proxy upstream normal completion
     → source body consumed/stream terminal; pool connection reusable.

618. art proxy client disconnect before finish
     → upstream stream destroyed/cancelled; no connection retained indefinitely.

619. Kitsu dynamic import
     → dynamicBoundary occurrence resolves package + locked capability record.

620. Kitsu request parent abort
     → library call cancels OR bounded exception prevents late publish and terminates by absolute deadline.

621. Fanart SDK client cache eviction
     → disposer runs if package owns resources OR NO_CLOSE_REQUIRED_PROVEN fixture documents stateless client.

622. Fanart shutdown with populated LRU
     → zero resource-owning SDK client residual.

623. name-to-imdb request deadline
     → call cannot publish after owner deadline; underlying work cancellation/bounded policy proven.

624. new runtime package with network capability imported without capability record
     → CI fails.

625. stale dependency capability record after package removal/rename
     → CI fails.

626. package-lock changes axios/fetch-socks/kitsu lifecycle-critical version only
     → lifecycle-contract-drift gate fires even with zero source diff.

627. undici HTTP_PROXY path
     → expected proxy policy proven.

628. Axios IMDb path with HTTP_PROXY/NO_PROXY
     → actual locked Axios behavior matches declared policy; divergence explicit if intentional.

629. SDK proxy behavior differs from undici
     → manifest records divergence; no silent assumption of global dispatcher.

630. direct/SDK retry tries to extend absolute request deadline
     → rejected/capped by OperationContext budget.

631. config getOrLoad A starts, then save B, then A resolves
     → A cannot overwrite B in memory or Redis.

632. two config saves in same millisecond
     → storage revisions are distinct and ordered even if configVersion timestamps collide.

633. writer clocks skewed between replicas/processes
     → storage revision order remains authoritative; wall clock cannot reverse config.

634. save B commits primary while read replica still returns A
     → config cache never regresses from B to A.

635. Redis cache expires during replica lag
     → correctness-critical config miss reads primary OR detects stale replica and falls back primary.

636. Redis unavailable; stale local pending load races save
     → local generation fence prevents stale in-process publication.

637. process 1 stale load vs process 2 newer save
     → revision-aware shared cache rejects older envelope.

638. config envelope equal revision + different canonical digest
     → hard consistency error/metric; no arbitrary last-write-wins.

639. old raw config cache entry during migration
     → dual-read accepted under explicit schema; re-write emits envelope only.

640. rollback baseline ignores extra DB revision column
     → old app continues reading config_data; migration is forward-compatible.

641. manager/account config writer
     → uses same revision/publish authority; no configCache.del-only stale window.

642. OAuth mutation that rewrites config
     → same revision authority; pending loader cannot resurrect prior token/config body.

643. system/cache-warmer config write
     → revision monotonic and cache publication fenced.

644. request config snapshot
     → carries one revision from start to finish; never mixes config bodies/revisions.

645. frontend useDeviceAuth interval + unmount
     → interval cleared; polling request cancelled/late result fenced.

646. frontend RestartManager interval + route change
     → interval cleanup exactly once.

647. frontend RecommendationsIntegration interval + unmount
     → no orphan polling.

648. frontend createObjectURL path + replacement/unmount
     → revokeObjectURL exactly once per owned URL.

649. changed frontend file adds event listener/fetch without owner cleanup/classification
     → frontend effect CI gate fails.

650. combined shutdown stress:
     active HTTP request + SDK call + poster stream + stale config load + background flush + pg replica
     → admission freezes; stale config publication rejected; work drains/aborts; streams terminate;
       transports close; storage closes last; every authoritative registry zero or explicit forced leftover;
       graceful=true only on genuinely clean terminal state.
```

---

# 546. Definition of Done V25

A implementação da #742 só pode sustentar a claim máxima desta V25 quando, cumulativamente ao DoD V8→V24:

```text
[ ] dev HEAD/tree continuam exatamente no snapshot ou todos os delta gates foram rerodados
[ ] issue #742 status/comments foram rechecados antes do PR final

[ ] Process Resource Occurrence Manifest fecha storage/listener/filesystem/transport resources
[ ] Redis físico possui owner/close/forced contract
[ ] pg primary/read-replica aliasing fecha exactly-once
[ ] operational SQLite e cold-store SQLite são recursos distintos no registry
[ ] HTTP listener/connections/upgraded sockets possuem owners não sobrepostos
[ ] local ReadStream/WriteStream/FileHandle/Dir occurrences estão classificados
[ ] proxy/client disconnect fecha upstream stream/body

[ ] DependencyCapabilityManifest fecha Kitsu/Fanart/name-to-imdb e demais packages de I/O
[ ] dynamic import/require boundaries são reconciliados
[ ] lifecycle-critical package-lock drift dispara revalidação
[ ] proxy/signal/retry/deadline semantics são provadas por transport, não presumidas

[ ] configVersion Date.now não é usado como correctness generation
[ ] config revision é storage-monotonic e retornada pelo write authority
[ ] config cache usa envelope versionado + stale-publication fence
[ ] getOrLoad antigo não pode sobrescrever save novo
[ ] DATABASE_READ_URI nunca pode causar revision regression
[ ] correctness-critical config miss usa primary ou stale-replica detection+fallback
[ ] todos saveUserConfig/configCache writers convergem à mesma publish authority
[ ] config migration/rollback/dual-read-single-write passam

[ ] scanner possui runtime roots + broad/reachability reconciliation
[ ] package capability import guard fecha SDK/network/storage boundaries novos
[ ] frontend effects possuem manifest separado e zero occurrence não classificada
[ ] qualquer leak real de timer/listener/fetch/objectURL em surface tocada está corrigido

[ ] shutdown final zera async/process resources/network/streams/file handles/config loads/writes
[ ] graceful=true nunca mascara leftover ou NO_SAFE_FORCE_CLOSE
[ ] observabilidade não expõe secrets/UUID completo/URLs sensíveis

[ ] casos 601–650 passam além dos 600+ casos V8→V24
[ ] build backend + build frontend + lint + test harness + integration/migration/concurrency passam
[ ] PR Guard executa somente metadata em pull_request_target; scanners/tests rodam em pull_request sem secrets
```

---

# 547. Resultado final da auditoria V25

Após reauditar a V24 inteira e revalidar o snapshot atual, o desenho funcional da #742 permanece aprovado:

```text
release evidence neutra
+ policy regional pós-cache
+ Worldwide golden-master
+ releaseRegion com provenance
+ canonical config/filter/source contexts
+ stale-negative revalidation
+ filtered pagination/cursor correctness
+ search/Discover/Jellyfin/warmer parity
+ runtime freshness/abort/shared-work closure
+ transport ownership V24
```

A V25 acrescenta as peças que faltavam para a **prova física de projeto completo**:

```text
+ persistent storage resources no manifest
+ HTTP listener/connection resources no manifest
+ local stream/file-handle closure
+ SDK/dependency-encapsulated I/O capability registry
+ lifecycle dependency fingerprint do lockfile
+ per-transport proxy/cancellation/retry policy proof
+ storage-monotonic config revision
+ stale getOrLoad publication fencing
+ DATABASE_READ_URI replica-regression protection
+ dynamic import/runtime-root closure
+ frontend effect lifecycle manifest
```

A mudança de maior impacto correctness-critical é a geração de configuração: o snapshot atual usa `configVersion = Date.now()` e um `getOrLoad()` que pode publicar um load antigo depois de um save. Portanto a implementação da #742 não deve usar `configVersion` como fencing token para `releaseRegion`; deve primeiro materializar a revision monotônica/CAS definida nesta camada.

Com as seções 531–547 incorporadas, o plano passa a exigir **650+ casos de teste** e quatro reconciliações autoritativas (async, process resources, network callers e frontend effects), sem reduzir runtime/upstream claims a promessas estáticas.

## 547.1. Claim defensável final

É defensável afirmar:

> **V25 fornece cobertura estática rastreável e arquiteturalmente fechada do snapshot `6e83e22ab9de5093f9918a1871157f401feebb03` para a #742 e para os lifecycles process/browser explicitamente inventariados, com todo fato que depende de runtime, dependência externa, upstream, replica, concorrência ou shutdown convertido em gate executável.**

Ainda não é defensável, antes da implementação e execução dos gates, afirmar:

```text
100% de ausência de bugs em produção;
100% de comportamento de upstream externo;
100% de teardown de dependency sem validar sua versão lockada;
100% de linearizabilidade cross-region fora do contract implementado;
100% de performance sem benchmark;
100% de commits posteriores ao snapshot.
```

Isso não é uma limitação escondida do plano: é exatamente a fronteira que o DoD transforma em evidência executável.

## 547.2. Ordem recomendada de implementação após V25

```text
PR 0  — test harness + lifecycle scanner + manifests + dependency fingerprint
PR 1  — config revision/storage migration + ConfigCache stale-publication fencing
PR 2  — Release Evidence V2 + Worldwide golden master + regional evaluator
PR 3  — CanonicalFilterContext/OperationContext + catalog/search integration
PR 4  — filtered pagination/cursors/source identity/freshness
PR 5  — Discover provenance/builder/import/edit-save/preview parity
PR 6  — Jellyfin/in-process/warmer/merged/custom closure
PR 7  — process resource + dependency-I/O + stream/storage shutdown closure
PR 8  — frontend release-region UI + frontend effect closure das surfaces tocadas
PR 9  — migration/load/concurrency/shutdown stress + observability + rollout gates
```

Se o PR Guard impedir esse shape, preservar a ordem de dependências; não juntar config-generation fencing depois dos consumers que dependem dele.

---

# 548. Reauditoria normativa V26 — snapshot atual + Persistent-Artifact Closure

## 548.1. Snapshot revalidado

A V26 foi revalidada contra:

```text
repository: cedya77/aiometadata
branch: dev
HEAD: d270a3a7f3b6e41304d9f91045b1d481311c3c96
tree: b4db5931c47035862fac075ac01ec02fe1e621c0
tree entries: 584
blobs: 545
directories: 39
tree truncated: false

published baseline:
v3.1.0
commit 6e83e22ab9de5093f9918a1871157f401feebb03

current dev vs published baseline:
ahead by 1 commit
behind by 0
```

A issue principal continua:

```text
#742 — Add region-specific support to “Hide Unreleased Movies”
state: open
comments: 0
```

Esta confirmação substitui qualquer frase histórica que ainda trate `6e83e22` como o HEAD atual.

---

## 548.2. Delta V25 → V26

Delta exato:

```text
6e83e22ab9de5093f9918a1871157f401feebb03
→
d270a3a7f3b6e41304d9f91045b1d481311c3c96

commits: 1
paths: 4

M addon/lib/dashboardApi.js
M addon/lib/imdbRatingProjection.ts
M addon/lib/imdbRatings.ts
A addon/lib/imdbRatingsTable.ts
```

O commit é:

```text
Feat/imdb ratings memory (#749)
```

Mudanças semanticamente relevantes para a auditoria:

```text
Redis hash de ratings
→ tabela imutável em memória

+ snapshot binário:
  addon/data/imdb-ratings.bin

+ ETag persistido no próprio snapshot

+ fs.readFile
+ fs.mkdir
+ fs.writeFile
+ fs.rename

+ undici HEAD/GET
+ stream.pipeline
+ zlib.createGunzip
+ readline.createInterface

+ process-local update single-flight
+ retryTimer exponencial
+ setInterval periódico
+ refresh de startup detached quando snapshot existe
+ limpeza detached das antigas keys Redis
```

O delta não implementa a #742 e não altera diretamente a arquitetura funcional de release visibility.

Ele altera, porém, a prova de:

```text
async closure
process resource closure
network caller closure
persistent storage closure
startup loser ownership
shutdown ordering
local artifact crash consistency
multi-process deployment assumptions
```

Portanto o Rebase Gate da própria V25 foi corretamente disparado.

---

## 548.3. Resultado da reauditoria

A arquitetura funcional acumulada permanece aprovada:

```text
release evidence neutra
+ release policy pós-cache
+ Worldwide golden-master
+ regional movie evaluator
+ series sem releaseRegion
+ canonical filter/source/config contexts
+ stale-negative revalidation
+ filtered pagination
+ source membership / filter signatures
+ search/Discover/Jellyfin/warmer parity
+ request clock / freshness
+ abort/shared-flight/transport closure
+ config storage revision/fencing
```

A V26 encontrou uma lacuna nova na **prova de projeto completo**:

> recurso aberto e artefato persistido são duas dimensões diferentes.

Exemplo:

```text
await fs.writeFile(path, bytes)
```

pode não deixar um `FileHandle` vivo após o retorno e, por isso, passar por um scanner orientado a resources.

Mesmo assim ele pode:

```text
- substituir estado persistente;
- deixar arquivo parcial;
- criar temp file órfão;
- quebrar restart;
- divergir entre replicas;
- apagar fallback antigo cedo demais;
- produzir marker inconsistente;
- publicar sucesso sem persistência real.
```

Isso exige um quinto universo autoritativo.

---

# 549. Blockers objetivos novos V26

Adicionar cumulativamente aos blockers V8→V25:

```text
HU. O snapshot V25 deixou de ser atual: dev avançou de `6e83e22` para `d270a3a`.
    Qualquer claim "FINAL" baseada no HEAD anterior é inválida até o Delta Gate ser fechado.

HV. Os quatro manifests V25 não representam artefatos persistentes produzidos por operações one-shot.
    `writeFile()`/`rename()` pode terminar sem handle residual e ainda assim alterar correctness de restart.

HW. O scanner V25 cobre FileHandle/ReadStream/WriteStream/Dir, mas não possui closure explícita para
    `readFile`, `writeFile`, `rename`, `unlink`, `rm`, variantes sync e writers nativos como
    `v8.writeHeapSnapshot`.

HX. O novo `install()` de IMDb ratings inicia `void dropLegacyRedisCopy()` antes de `saveSnapshot()`.
    Em uma atualização obtida da rede, uma falha de persistência pode coexistir com remoção antecipada
    do fallback Redis legado. O cache é reconstruível, mas o ordering de migração não está transacionalmente
    definido.

HY. `saveSnapshot()` captura a exceção e retorna `void`; o caller continua para `markUpdated()` e a operação
    externa pode reportar sucesso mesmo quando o snapshot em disco não foi persistido. É necessário separar
    "memory candidate published" de "durable snapshot persisted".

HZ. O delta novo possui `retryTimer`, `ratingsUpdateInterval`, `updateInFlight` e refresh de startup
    `void runRatingsUpdate()`; não existe disposer atual que congele admission, cancele timers, aborte I/O
    e drene o trabalho antes de storage/transports fecharem.

IA. `readline.createInterface`, `zlib.createGunzip`, `Transform`/`PassThrough` e outros stream constructors
    não estão explicitamente entre os seeds mínimos V25. `pipeline` ajuda a descobrir a composição, mas não
    substitui ownership individual/terminal proof quando o pipeline é interrompido.

IB. `imdb-ratings.bin.tmp` possui nome fixo. O single-flight atual é process-local. Se duas replicas escreverem
    o mesmo volume, o temp path/final path não possuem cross-process writer fencing.

IC. `RatingsTable` V1 valida magic/version/length/order, mas não possui checksum de payload; corrupção de mesmo
    tamanho pode continuar estruturalmente válida. O formato também precisa de política explícita para IDs
    duplicados e para o limite matemático do truque `Float64Array(id * n + row)`.

ID. `initializeRatings()` é executado como startup task com timeout de 300 s. Sem AbortSignal/late-loser fence,
    timeout do orchestrator não cancela necessariamente HEAD/GET/parse/write nem impede scheduler/retry de nascer
    depois que o startup owner perdeu authority.

IE. O blind spot de artefatos persistentes não nasceu no #749. O snapshot já contém, entre outros:
    cache migration flag, mapper caches, anime list cache, wiki cache, poster warm summary, poster cache files e
    heap diagnostics. Uma claim "projeto completo" precisa classificá-los ou limitar explicitamente o escopo.

IF. Reads de arquivos do runtime (`/sys/fs/cgroup`, assets estáticos etc.) e writes de build/CI não podem ser
    confundidos com durable app state. Sem `executionDomain`/`artifactClass`, ampliar o scanner geraria
    falsos positivos e allowlists vagas.

IG. Um artifact write pode ser logicamente atômico por `rename` sem ser crash-durable contra power loss.
    O plano precisa distinguir `ATOMIC_REPLACE` de `FSYNC_DURABLE`; exigir fsync indiscriminadamente para cache
    reconstruível seria custo sem benefício, mas chamar `rename` de durability forte seria impreciso.

IH. `undici.request()` não torna status HTTP inválido automaticamente em falha de domínio. HEAD/GET do dataset
    precisam de status policy e body-terminal proof explícitos; o callback vazio de `stream.pipeline(..., () => {})`
    não é, sozinho, prova de lifecycle/cancellation.

II. `IMDB_RATINGS_UPDATE_INTERVAL_HOURS` usa `parseInt` sem validação positiva/bounded no delta atual.
    `NaN`, zero, valor negativo ou excessivo não podem definir scheduler correctness por acidente.

IJ. O dataset externo é trusted-by-origin, mas continua input não controlado localmente. Row-count/memory bounds,
    zero-row protection, malformed gzip e payload exagerado precisam de gates de availability para evitar que
    refresh derrube o processo ou substitua last-known-good.
```

---

# 550. Quinto universo autoritativo — Persistent Artifact Occurrence Manifest

## 550.1. Cinco universos

A partir da V26 a reconciliação normativa é:

```text
asyncOccurrences
processResourceOccurrences
networkCallerOccurrences
frontendEffectOccurrences
persistentArtifactOccurrences
```

Merge invariant:

```text
actualAsync               - classifiedAsync               = ∅
actualProcessResource     - classifiedProcessResource     = ∅
actualNetCaller           - classifiedNetCaller           = ∅
actualFrontendEffect      - classifiedFrontendEffect      = ∅
actualPersistentArtifact  - classifiedPersistentArtifact  = ∅

classified occurrence apontando para AST node/symbol inexistente = CI fail
wildcard/path-prefix grandfathering sem occurrence id = proibido
```

Os universos podem se cruzar.

Exemplo:

```text
posterCache/store.ts

createWriteStream
→ processResource occurrence

temp file + rename
→ persistentArtifact occurrence

upstream fetch
→ networkCaller occurrence

deferred eviction
→ async occurrence
```

Um único path pode e deve possuir múltiplos records quando possui responsabilidades distintas.

---

## 550.2. Schema mínimo

```ts
type ArtifactExecutionDomain =
  | 'BACKEND_RUNTIME'
  | 'FRONTEND_BROWSER'
  | 'BUILD_CI'
  | 'MIGRATION'
  | 'EXTERNAL_RUNTIME';

type ArtifactClass =
  | 'AUTHORITATIVE_STATE'
  | 'REBUILDABLE_DURABLE_CACHE'
  | 'DERIVED_SUMMARY'
  | 'MIGRATION_MARKER'
  | 'DIAGNOSTIC_ARTIFACT'
  | 'TEMP_STAGING'
  | 'STATIC_INPUT'
  | 'EXTERNAL_RUNTIME_READONLY';

type CommitProtocol =
  | 'DIRECT_OVERWRITE'
  | 'TEMP_THEN_RENAME'
  | 'DATABASE_MANAGED'
  | 'APPEND'
  | 'READ_ONLY'
  | 'OTHER';

type DurabilityLevel =
  | 'BEST_EFFORT_REBUILDABLE'
  | 'LOGICAL_ATOMIC_REPLACE'
  | 'FSYNC_DURABLE'
  | 'DATABASE_DURABLE'
  | 'NOT_APPLICABLE';

interface PersistentArtifactOccurrenceRecord {
  id: string;
  file: string;
  symbol: string;
  astFingerprint: string;

  executionDomain: ArtifactExecutionDomain;
  artifactClass: ArtifactClass;

  artifactPathAuthority: string;
  physicalArtifactKey: string;

  readers: string[];
  writers: string[];
  deleters: string[];

  schemaVersionAuthority: string | null;
  integrityAuthority: string | null;

  commitProtocol: CommitProtocol;
  durabilityLevel: DurabilityLevel;

  tempPathPolicy: string | null;
  recoveryPolicy: string;
  corruptionPolicy: string;

  multiProcessPolicy:
    | 'INSTANCE_LOCAL'
    | 'SHARED_SINGLE_WRITER'
    | 'SHARED_FENCED_WRITER'
    | 'READ_ONLY_SHARED'
    | 'NOT_APPLICABLE';

  writerFenceAuthority: string | null;

  shutdownOwner: string | null;
  pendingWriteRegistry: string | null;

  rollbackCompatibility: string;
  retentionPolicy: string | null;

  containsSecrets:
    | 'NO'
    | 'POSSIBLE'
    | 'YES';

  terminalProof: string;
}
```

`physicalArtifactKey` é a autoridade de aliasing:

```text
dois helpers escrevendo o mesmo arquivo
→ um artefato físico
→ um commit protocol
→ uma recovery policy
```

---

## 550.3. O que é artifact occurrence

Entram:

```text
fs.promises.readFile / fs.readFile quando o arquivo participa de state/recovery
fs.promises.writeFile / fs.writeFile
fs.promises.rename / fs.rename
fs.promises.unlink / fs.unlink
fs.promises.rm / fs.rm
fs.copyFile
fs.truncate
fs.appendFile
fs.open quando há state file
sync equivalents
createWriteStream/createReadStream quando persistem/consomem state
v8.writeHeapSnapshot
SQLite/DB path declarations como DATABASE_MANAGED references
temp/staging files
migration marker files
cache snapshots
persisted summaries
diagnostic artifacts
```

Nem todo `readFile()` é durable app state.

Exemplos:

```text
/sys/fs/cgroup/*
→ EXTERNAL_RUNTIME_READONLY

frontend bundle index.html
→ STATIC_INPUT

scripts/generate-build-info.js output
→ BUILD_CI domain

addon/data/imdb-ratings.bin
→ REBUILDABLE_DURABLE_CACHE
```

A classificação evita falsos positivos sem esconder ocorrências.

---

# 551. Scanner V26 — Artifact + Stream Constructor Closure

## 551.1. Seeds adicionais obrigatórios

Adicionar ao lifecycle scanner:

```text
# one-shot fs state
fs.readFile / fs.promises.readFile / fsp.readFile
fs.writeFile / fs.promises.writeFile / fsp.writeFile
fs.rename / fs.promises.rename / fsp.rename
fs.unlink / fs.promises.unlink / fsp.unlink
fs.rm / fs.promises.rm / fsp.rm
fs.mkdir / fs.promises.mkdir / fsp.mkdir
fs.copyFile
fs.appendFile
fs.truncate

# sync equivalents
readFileSync
writeFileSync
renameSync
unlinkSync
rmSync
mkdirSync
copyFileSync
appendFileSync
truncateSync

# stream constructors / wrappers
Readable
Writable
Transform
PassThrough
createReadStream
createWriteStream
readline.createInterface
createInterface imported from readline
zlib.createGunzip / createGzip / createInflate / createDeflate
stream.pipeline
stream/promises.pipeline

# native artifact writers
v8.writeHeapSnapshot

# path authorities
path.join(..., 'addon', 'data', ...)
runtime configurable cache/data dirs
diagnostics dirs
SQLite paths
```

Scanner por nome textual sozinho não basta.

Exigir:

```text
import/binding resolution quando disponível
+
broad lexical safety net
+
runtime-root reachability
+
manual dynamic-boundary reconciliation
```

---

## 551.2. Seeds confirmados no snapshot atual

O manifest deve materializar pelo menos:

```text
addon/lib/imdbRatings.ts
→ addon/data/imdb-ratings.bin
→ addon/data/imdb-ratings.bin.tmp

addon/lib/cache-path-migration.ts
→ addon/data/.migration-completed
→ legacy cache files deletados
→ Redis migration marker associado

addon/lib/id-mapper.js
→ anime-list-full.json.cache
→ imdb_mapping.json.cache
→ trakt-anime-movies.json.cache
→ animeapi.tsv.cache

addon/lib/anime-list-mapper.js
→ anime-list-full.xml.cache

addon/lib/wiki-mapper.ts
→ mapping CSV caches
→ ETag state associado

addon/lib/posterCache/store.ts
→ cached image artifacts + temp files

addon/lib/posterCache/warmQueue.ts
→ warm-summary.json + .tmp

addon/lib/posterCache/nginxImport.ts
→ import marker + imported cache artifacts

addon/index.ts
→ heap-*.heapsnapshot
→ *.heapprofile quando suportado
```

Essa lista é seed.

A authority continua sendo o scanner gerado contra a árvore, não a lista manual.

---

## 551.3. Shared atomic-file helper

Recomendação arquitetural:

```text
addon/lib/persistentArtifact.ts
```

ou módulo equivalente com primitive comum:

```ts
interface AtomicWriteResult {
  committed: boolean;
  durable: boolean;
  bytes: number;
}

async function atomicReplaceFile(
  finalPath: string,
  data: Uint8Array | string,
  options: {
    signal?: AbortSignal;
    tempPolicy: 'unique-per-process' | 'unique-per-operation';
    durability: 'best-effort' | 'fsync-file' | 'fsync-file-and-dir';
    mode?: number;
  }
): Promise<AtomicWriteResult>;
```

Responsabilidades:

```text
- temp path não colide entre operations/processes;
- write completo antes do rename;
- optional fsync conforme artifact class;
- rename dentro do mesmo filesystem;
- cleanup do temp em erro/cancel;
- não remover last-known-good final antes do commit;
- signal/lifecycle owner explícito;
- metric/trace do commit result;
- nunca logar conteúdo sensível.
```

Não é obrigatório migrar todo cache existente no mesmo PR da #742.

É obrigatório:

```text
classificar todos
+
usar helper nos novos artifacts correctness-relevant
+
corrigir qualquer path tocado cuja recovery atual seja incompatível com seu contrato declarado.
```

---

# 552. Durable Artifact Correctness Gate

## 552.1. Quatro momentos distintos

Para cada artifact write:

```text
candidateBuiltAt
candidatePublishedInMemoryAt
artifactCommittedAt
artifactDurableAt
```

Eles não são sinônimos.

Para cache reconstruível:

```text
memory publish pode preceder durable commit
```

desde que:

```text
- falha do durable commit seja observável;
- last-known-good artifact não seja apagado prematuramente;
- cleanup/migration só use durable proof quando necessário;
- restart behavior permaneça definido.
```

Para authoritative state:

```text
não publicar sucesso externo antes do commit/durability contract requerido.
```

---

## 552.2. Atomicidade ≠ durability física

Definições:

```text
TEMP_THEN_RENAME
→ evita final parcialmente sobrescrito dentro da semântica normal do filesystem
→ LOGICAL_ATOMIC_REPLACE

TEMP_THEN_RENAME + fsync(file) + fsync(parent dir), onde suportado/necessário
→ pode satisfazer FSYNC_DURABLE

rename sozinho
≠
garantia universal contra power-loss
```

Para `REBUILDABLE_DURABLE_CACHE`, `LOGICAL_ATOMIC_REPLACE` pode ser suficiente.

O manifest deve dizer isso explicitamente.

---

## 552.3. Recovery no startup

Todo artifact persistido precisa de uma dessas políticas:

```text
VALIDATE_AND_USE
VALIDATE_OR_REBUILD
IGNORE_IF_UNKNOWN_VERSION
QUARANTINE_AND_REBUILD
MIGRATE_THEN_USE
FAIL_STARTUP
```

Para cache:

```text
unknown schema
corrupt payload
truncated file
invalid checksum
parse zero rows
→ não publicar
→ preservar/baixar last-known-good quando possível
→ rebuild
```

Para marker:

```text
marker diz complete
+
side effect obrigatório ausente
→ reconciliation
```

Marker sozinho não substitui estado real quando ambos podem divergir.

---

# 553. IMDb Ratings Snapshot Gate V26

## 553.1. Artifact authority

Definir:

```text
IMDB_RATINGS_ARTIFACT_SCHEMA = 2   # recomendado após integrity addition

final:
addon/data/imdb-ratings.bin

temp:
unique per operation/process
```

Exemplo:

```text
imdb-ratings.bin.tmp.<pid>.<generation>.<nonce>
```

O nome exato não é importante.

A propriedade de **não colisão** é.

---

## 553.2. Ordem de commit recomendada

Quando não existe snapshot válido:

```text
GET dataset
→ parse candidate table
→ validate candidate
→ persist temp
→ validate/commit final
→ publish durable status
→ install in-memory table
→ cleanup legacy Redis copy
→ publish maintenance markers
```

Quando já existe last-known-good em memória e a política deseja latência mínima:

```text
GET dataset
→ parse candidate
→ validate candidate
→ install atomically in memory
→ attempt durable commit
→ report memoryUpdated=true
→ report persisted=true|false
→ delete legacy Redis copy SOMENTE se já havia durable snapshot válido
   ou o novo durable commit passou
```

O plano aceita qualquer uma das duas ordens se o contract for explícito.

É proibido:

```text
apagar o único fallback durável
antes de possuir durable proof substituto
```

---

## 553.3. Resultado estruturado

Substituir boolean único internamente por algo equivalente:

```ts
interface RatingsUpdateResult {
  fetched: boolean;
  changed: boolean;
  memoryUpdated: boolean;
  persisted: boolean;
  etag: string | null;
  count: number;
  reason:
    | 'etag-match'
    | 'updated'
    | 'network-failure'
    | 'invalid-status'
    | 'parse-failure'
    | 'zero-rows'
    | 'persist-failure'
    | 'cancelled';
}
```

A API externa pode manter shape compatível, mas não deve perder observabilidade.

Exemplo:

```text
force update:
memoryUpdated=true
persisted=false
→ operação atual pode ser útil
→ mensagem/metric registra degraded persistence
→ nunca fingir "snapshot persisted".
```

---

## 553.4. Legacy Redis cleanup

`dropLegacyRedisCopy()` é migration cleanup.

Regras:

```text
1. idempotent;
2. tracked no BackgroundWorkRegistry;
3. retry-safe;
4. não executa após Redis close authority;
5. não bloqueia serving de uma tabela válida;
6. só marca `legacyRedisCopyDropped=true` após unlink efetivo;
7. falha não invalida a tabela nova;
8. cleanup inicial não precede durable replacement proof.
```

O current `void dropLegacyRedisCopy()` deve ser absorvido pelo owner registry.

---

## 553.5. Maintenance markers

Separar semanticamente, se necessário:

```text
maintenance:last_imdb_ratings_memory_update
maintenance:last_imdb_ratings_snapshot_commit
maintenance:last_imdb_ratings_upstream_check
```

ou manter uma única key apenas se sua semântica for claramente documentada.

Nunca:

```text
disk save falha
+
marker significa "snapshot persistido"
```

---

# 554. RatingsTable Binary Format / Integrity Gate

## 554.1. Formato versionado

O V1 atual possui:

```text
MAGIC
FORMAT_VERSION
row count
etag length
etag
ids
votes
ratings
```

Isso já fecha:

```text
magic
version
exact total length
ascending ids
```

A V26 recomenda V2 com integrity footer/header:

```text
payloadLength
payloadDigest
```

Digest recomendado:

```text
SHA-256
```

Não por segurança criptográfica contra attacker local, mas por:

```text
- bit rot;
- partial/corrupt same-size file;
- copy/storage corruption;
- unambiguous validation.
```

CRC32 também seria tecnicamente suficiente para corrupção acidental, mas SHA-256 já existe no runtime e reduz ambiguidade de contract.

---

## 554.2. Compatibility

Policy:

```text
reader V2:
- aceita V2;
- pode aceitar V1 durante migration;
- ao próximo successful update escreve somente V2.

unknown future version:
- não tentar interpretar;
- rebuild.

rollback para versão que só entende V1:
- version mismatch deve degradar para rebuild, não crash.
```

Se múltiplas versões escreverem um volume compartilhado:

```text
→ fleet/multi-writer gate obrigatório;
→ não aceitar ping-pong de formatos silencioso.
```

---

## 554.3. Invariantes da tabela

Definir e testar:

```text
id:
tt + positive decimal
<= 0xffffffff

votes:
0..0xffffffff

rating:
finite
provider-valid domain
encoded deterministically

row order:
strictly increasing OR duplicates explicitly resolved

row count:
bounded

payload:
exactly one complete table
```

IDs duplicados:

```text
preferência V26:
reject candidate as malformed
```

ou:

```text
deterministic dedupe policy versionada
```

Nunca deixar `binary search` escolher uma duplicata sem contrato.

---

## 554.4. Float64 sorting bound

O otimizado:

```text
key = id * n + row
```

só é correctness-safe enquanto:

```text
maxId * n + maxRow <= Number.MAX_SAFE_INTEGER
```

Antes de usar:

```ts
if (!Number.isSafeInteger(maxId * n + (n - 1))) {
  // fallback deterministic sort
}
```

ou eliminar o encoding composto.

Não usar o tamanho atual do dataset como prova eterna.

---

## 554.5. Resource bounds

Adicionar sanity bounds:

```text
MAX_RATINGS_ROWS
MAX_ETAG_BYTES
MAX_SNAPSHOT_BYTES
optional upstream content-length sanity
decompressed row/byte budget
```

Ao exceder:

```text
reject candidate
keep last-known-good
metric
retry/backoff conforme error class
```

Não instalar partial.

---

# 555. IMDb Ratings Network / Stream Lifecycle Gate

## 555.1. OperationContext

`runRatingsUpdate()` recebe/cria context:

```ts
interface RatingsOperationContext {
  signal: AbortSignal;
  deadlineAt: number;
  generation: bigint | string;
  owner:
    | 'startup'
    | 'periodic'
    | 'retry'
    | 'manual'
    | 'shutdown-drain';
}
```

O mesmo signal/deadline deve alcançar:

```text
HEAD
GET
response body
gunzip
readline iteration
parse
artifact write quando cancelável/adequado
Redis marker/cleanup quando ainda autorizado
```

---

## 555.2. HTTP status contract

Para HEAD/GET:

```text
2xx expected
```

Se status fora da policy:

```text
do not parse as dataset
do not install
do not persist
terminalize/cancel body
classify failure
```

Se no futuro for usado conditional GET:

```text
304
→ só válido quando existe last-known-good correspondente
```

---

## 555.3. Body terminal proof

Cada `undici.request` precisa terminar por um dos estados:

```text
CONSUMED
CANCELLED
ABORTED
DESTROYED
```

HEAD também precisa de contract da versão lockada.

Não assumir:

```text
"é HEAD, então não existe lifecycle do body"
```

sem prova/teste da versão de undici.

---

## 555.4. Pipeline ownership

Preferir primitive cuja completion seja awaitable:

```text
stream/promises.pipeline(...)
```

ou wrapper equivalente.

Se mantiver callback pipeline:

```text
callback error
+
stream error
+
AbortSignal
+
terminal registration
```

precisam convergir.

`readline.Interface` também possui owner.

No abort:

```text
close Interface
destroy/cancel decompressed stream
abort source body
settle pipeline
```

---

# 556. IMDb Ratings Scheduler / Shutdown Closure

## 556.1. Estado que precisa de owner

O current snapshot possui:

```text
ratingsUpdateInterval
retryTimer
updateInFlight
inFlightForced
detached startup refresh
detached legacy Redis cleanup
possible snapshot write
HEAD/GET body
gunzip stream
readline interface
```

A V25 antiga que dizia apenas:

```text
stop interval + active update drain
```

não é suficiente para o HEAD atual.

---

## 556.2. Disposer obrigatório

Criar algo equivalente:

```ts
async function stopImdbRatingsUpdates(
  shutdown: OperationContext
): Promise<{
  clean: boolean;
  forced: string[];
}>;
```

Ordem:

```text
1. set ratingsAdmissionFrozen=true
2. reject/short-circuit new periodic/retry/manual admissions
3. clear ratingsUpdateInterval
4. clear retryTimer
5. abort active operation context
6. prevent retry re-arm in finally/error path
7. drain updateInFlight within deadline
8. drain tracked legacy Redis cleanup
9. drain/finish permitted snapshot commit
10. assert no ratings background owner remains
```

`forceUpdateImdbRatings()` iniciado depois de freeze:

```text
→ 503/explicit shutting-down result
```

não uma nova operação.

---

## 556.3. Retry generation fence

Race a impedir:

```text
update fails
↓
shutdown clears retryTimer
↓
failure handler ainda roda
↓
scheduleRetryIfFailed() rearma retryTimer
```

Regra:

```text
schedulerGeneration captured at operation start
+
admissionFrozen check at scheduling point
```

ou token equivalente.

Após freeze:

```text
retryTimer === null
```

deve ser invariant terminal.

---

## 556.4. Manual force vs normal update

Current policy:

```text
force during non-force update
→ wait current
→ run one forced follow-up
```

Preservar, mas formalizar:

```text
N concurrent force callers
→ at most one required forced follow-up per generation
```

Se shutdown começa antes do follow-up:

```text
→ cancellation wins
→ no new force admission
```

---

# 557. Startup Task / Late-Loser Closure V26

`addon/server.ts` executa IMDb ratings como startup task com:

```text
timeoutMs = 300_000
```

Timeout de orchestrator não é cancellation por si só.

Contrato V26:

```text
startup task gets StartupOperationContext
↓
deadline/AbortSignal passed to initializeRatings
↓
timeout aborts context
↓
late result loses commit authority
```

Após timeout:

```text
proibido:
- instalar candidate novo;
- criar periodic interval;
- criar retry timer;
- escrever maintenance success marker;
- iniciar legacy cleanup;
```

a menos que o orchestrator execute **ownership transfer explícito** para BackgroundWorkRegistry.

Caso snapshot local já tenha sido carregado antes do timeout:

```text
serving do snapshot já validado pode permanecer;
background revalidation precisa de owner separado.
```

---

# 558. Multi-Process / Replica Artifact Gate

## 558.1. Canonical Docker

O compose documentado monta:

```text
/app/addon/data
```

em volume persistente.

Isso prova persistência de restart na implantação canônica.

Não prova:

```text
single process forever
single writer em Kubernetes
single writer em shared NFS
no rolling mixed-version writer
```

---

## 558.2. Artifact scope obrigatório

Cada artifact declara:

```text
INSTANCE_LOCAL
ou
SHARED_*
```

Para IMDb ratings, escolher explicitamente uma policy.

### Opção A — instance local

```text
cada replica possui seu próprio addon/data
→ process-local singleflight é suficiente para writer concurrency local
→ temp path ainda deve ser unique por operação para crash leftovers
```

### Opção B — volume compartilhado

Exigir:

```text
distributed writer lease/fence
ou
leader-only writer
```

e:

```text
unique temp
atomic final replace
format compatibility
lease owner token
no stale writer commit after lease loss
```

Process-local Promise não é distributed lock.

---

## 558.3. Shared volume + rolling deploy

Teste:

```text
old reader
new writer
new reader
old writer
```

Resultado precisa ser uma destas políticas:

```text
SUPPORTED with format/fence proof
ou
REJECTED by deployment/fleet gate
```

Não deixar comportamento implícito.

---

# 559. Existing Persistent Artifact Closure

O novo manifest não serve só ao commit #749.

## 559.1. Cache migration marker

`addon/lib/cache-path-migration.ts` combina:

```text
addon/data/.migration-completed
+
Redis migration:<version>
+
legacy file deletion
+
ETag deletion
```

Definir reconciliation:

```text
disk marker present / Redis marker absent
disk marker absent / Redis marker present
Redis unavailable
partial legacy deletion
flag write failure
restart between steps
```

Como os artifacts deletados são caches reconstruíveis:

```text
migration may be idempotent
```

mas isso deve ser teste, não suposição.

---

## 559.2. ID/anime/wiki caches

Caches locais de mapping:

```text
direct write
+
ETag remoto/Redis
+
startup fallback
```

Cada writer precisa declarar:

```text
atomic write ou best-effort rebuildable
parser validation
ETag/data coherence
last-known-good behavior
```

Se ETag é atualizado mas arquivo falha:

```text
não criar estado em que próxima inicialização acredita que cache antigo corresponde ao ETag novo.
```

A recomendação é:

```text
candidate file commit
→ ETag commit
```

ou reconciliation equivalente.

---

## 559.3. Poster warm summary

`warm-summary.json` já usa temp + rename, mas a persistência é detached por Promise chain.

Exigir:

```text
pending write registration
shutdown drain
no re-arm after shutdown
temp cleanup/recovery
unique writer policy
```

`persisting=false` não é um registry autoritativo cross-module.

---

## 559.4. Heap diagnostics

Heap snapshot é:

```text
DIAGNOSTIC_ARTIFACT
```

Não precisa participar do request correctness.

Precisa declarar:

```text
retention
disk-budget/operational policy
path sanitization
admin authorization
shutdown behavior se snapshot está em progresso
```

O manifest pode marcar:

```text
USER_ACTION_OWNED + DIAGNOSTIC_ARTIFACT
```

---

# 560. Shutdown V26 — ordem final com persistent artifacts

A ordem V25 é substituída, nos pontos relevantes, por:

```text
0. shutdown generation começa
   - nenhum novo owner não essencial é admitido

1. freeze inbound admissions
   - HTTP
   - upgraded/in-process
   - manual maintenance jobs
   - config writers
   - ratings force-update

2. freeze background producers
   - schedulers
   - retry timers
   - warmers
   - refresh-ahead
   - artifact periodic writers

3. cancel timers/immediates/deferred callbacks

4. abort logical operations
   - request contexts
   - startup/background contexts
   - network calls
   - pipelines/readline
   - retry sleeps
   - stream owners

5. drain active logical work
   - requests
   - shared flights
   - config loads/writers
   - ratings update
   - mapper updates
   - poster warmers

6. settle correctness-relevant pending artifact commits
   - config-related writes
   - IMDb snapshot if policy chooses drain
   - poster summary
   - migration marker transitions
   - cold-store/write-behind

7. flush remaining write-behind

8. close inbound/transport resources
   - HTTP listener
   - connections
   - upgraded sockets
   - outbound dispatchers/agents/SDK transports

9. close persistent database/storage resources
   - cold-store SQLite
   - operational SQLite OR pg replica + primary
   - Redis
   IMPORTANT:
   - Redis-dependent cleanup/markers must already have settled or been cancelled

10. dispose memory/client registries

11. final assertion
```

Final assertion V26:

```text
async == 0
processResource == 0 excluding proven external-runtime-owned
activeNetwork == 0
activeStreams == 0
activeFileHandles == 0
activeReadlineInterfaces == 0
pendingArtifactWrites == 0
pendingArtifactMigrations == 0
pendingConfigLoads == 0
pendingWrites == 0
frontend effect test manifest == classified
```

`graceful=true` continua proibido com leftover não-external.

---

# 561. Mandatory File / Caller / Artifact Map V26

Adicionar cumulativamente:

```text
addon/lib/imdbRatings.ts
→ network owner
→ scheduler/retry owner
→ startup detached refresh
→ legacy Redis cleanup
→ snapshot read/write/rename
→ shutdown disposer
→ result split memory/persistence

addon/lib/imdbRatingsTable.ts
→ binary format authority
→ integrity/version authority
→ ID/rating/vote invariants
→ duplicate policy
→ sort precision bound
→ resource budget bound

addon/server.ts
→ startup timeout signal
→ late-loser authority
→ explicit ownership transfer if startup refresh continues in background

addon/lib/cache-path-migration.ts
→ disk marker + Redis marker reconciliation
→ legacy artifact deletion idempotence

addon/lib/id-mapper.js
addon/lib/anime-list-mapper.js
addon/lib/wiki-mapper.ts
→ mapping artifact + ETag/data coherence
→ recovery classification

addon/lib/posterCache/warmQueue.ts
→ pending warm-summary artifact write
→ shutdown drain

addon/lib/posterCache/store.ts
addon/lib/posterCache/nginxImport.ts
→ existing stream/handle records
+
persistent artifact/temp/marker records

addon/index.ts
→ heap diagnostic artifact class

README.md / compose documentation
docs/image-cache.md
.env.example
→ artifact persistence/deployment assumptions where relevant

scripts/lifecycle-occurrence-scanner.*
→ one-shot fs + stream constructor + native artifact seeds

scripts/persistent-artifact-classifications.json
ou equivalente
→ authoritative classifications
```

---

# 562. Observabilidade V26

Adicionar:

```text
persistent_artifact_read_total{artifact,result}
persistent_artifact_write_total{artifact,result}
persistent_artifact_commit_total{artifact,result,protocol}
persistent_artifact_recovery_total{artifact,reason}
persistent_artifact_corrupt_total{artifact,reason}
persistent_artifact_temp_cleanup_total{artifact,result}
persistent_artifact_pending{artifact}

imdb_ratings_update_total{owner,result}
imdb_ratings_update_inflight
imdb_ratings_retry_scheduled_total
imdb_ratings_retry_delay_seconds
imdb_ratings_snapshot_load_total{result}
imdb_ratings_snapshot_commit_total{result}
imdb_ratings_snapshot_integrity_failure_total{reason}
imdb_ratings_legacy_cleanup_total{result}
imdb_ratings_table_rows
imdb_ratings_memory_updated_timestamp
imdb_ratings_snapshot_committed_timestamp

startup_late_publish_rejected_total{job}
```

Cardinality rules:

```text
artifact = enum estável, não raw path/user path
reason = enum
owner = enum
nunca ETag cru se puder carregar dados sensíveis
nunca URL upstream completa com query/token
```

Shutdown report V26:

```json
{
  "graceful": false,
  "activeResources": [],
  "activeNetwork": [],
  "activeStreams": [],
  "activeReadlineInterfaces": 0,
  "pendingArtifactWrites": ["imdb-ratings"],
  "pendingArtifactMigrations": [],
  "pendingConfigLoads": 0,
  "forced": ["imdb-ratings:abort"],
  "noSafeForceClose": []
}
```

---

# 563. Matriz de testes adicional V26 — casos 651–700

Adicionar cumulativamente aos 650+ casos V8→V25:

```text
651. snapshot fingerprint
     → dev HEAD == d270a3a7f3b6e41304d9f91045b1d481311c3c96 e tree == b4db5931c47035862fac075ac01ec02fe1e621c0
       OU Rebase Gate executado novamente.

652. delta 6e83e22 → d270a3a
     → exatamente 1 commit / 4 paths classificados; nenhum occurrence novo escapa manifests.

653. new file reachability
     → addon/lib/imdbRatingsTable.ts é alcançado pelo runtime import graph e pelo scanner.

654. persistent artifact scanner
     → imdb-ratings.bin, migration marker, mapper caches, poster summary/cache e diagnostics aparecem no manifest.

655. sync fs scanner
     → readFileSync/writeFileSync/native artifact writer de runtime ou build recebe executionDomain correto.

656. external readonly file
     → cgroup/runtime read é EXTERNAL_RUNTIME_READONLY; não vira falso pending artifact write.

657. poster warm-summary normal commit
     → temp write + rename termina, pendingArtifactWrites volta a zero.

658. poster warm-summary crash/temp recovery
     → final válido continua utilizável; temp órfão é ignorado/limpo por policy.

659. cache migration marker normal
     → disk + Redis marker convergem e legacy delete é idempotente.

660. cache migration interruption
     → restart entre legacy delete e marker write não corrompe estado; rerun converge.

661. id-mapper local cache write/read
     → candidate inválido/parcial não se torna last-known-good silencioso.

662. anime-list mapper local cache failure
     → restart refaz download/fallback conforme contract, sem aceitar partial.

663. wiki cache + ETag ordering
     → ETag não pode afirmar versão nova quando durable cache correspondente falhou.

664. poster cache artifact atomicity
     → failed temp write/rename não remove final válido; cleanup terminal.

665. heap diagnostics
     → artifact é autorizado, path-safe e retention/disk policy observável.

666. new runtime writeFile added sem classification
     → CI falha Persistent Artifact Occurrence Gate.

667. valid IMDb V2 snapshot load
     → table, ETag, count e digest válidos; nenhum download obrigatório para serving inicial.

668. missing IMDb snapshot
     → startup baixa candidate; zero phantom loaded state.

669. bad magic / unknown format version
     → snapshot rejeitado; rebuild; processo não crasha.

670. truncated IMDb snapshot
     → exact-length/integrity validation falha; nenhuma partial table publicada.

671. same-size bit corruption
     → digest falha; nenhum rating corrompido é servido como válido.

672. ETag round-trip
     → UTF-8/bounded ETag serializa e desserializa deterministicamente.

673. snapshot write + rename success
     → final novo visível somente após complete temp; commit metric success.

674. snapshot write failure
     → current in-memory semantics explícitas; durable=false; legacy fallback não é apagado indevidamente.

675. snapshot rename failure
     → old final preservado; temp cleaned/quarantined; durable=false.

676. crash before rename
     → restart usa old final; temp não é confundido com committed artifact.

677. crash after rename before Redis marker
     → restart usa novo final e reconcilia marker; não redownload desnecessário obrigatório.

678. legacy Redis cleanup ordering
     → cleanup só ocorre após durable replacement proof aplicável.

679. initial persist failure
     → legacy Redis keys permanecem; no destructive migration gap.

680. Redis unavailable during legacy cleanup
     → ratings continuam servindo; cleanup retry/idempotence não rearma após shutdown.

681. concurrent scheduled/manual update
     → um process-local update flight; sem duplicate download.

682. force during normal update
     → exatamente um forced follow-up necessário; N callers não multiplicam refresh.

683. retry backoff
     → 15m exponential bounded pelo update interval; success zera failure count/timer.

684. shutdown with retry timer pending
     → timer cleared; generation fence impede re-arm.

685. shutdown during HEAD
     → signal aborta; body terminal; no late install/marker.

686. shutdown during GET
     → response body terminal; dispatcher connection não fica retida.

687. shutdown during gunzip/readline parse
     → pipeline/interface fecham; candidate não publica após authority loss.

688. shutdown during artifact write
     → chosen drain/cancel policy preserva final válido; pending registry zera ou forced leftover explícito.

689. startup task timeout at 300s
     → active network/parse aborta OU owner é explicitamente transferido; late startup owner não cria scheduler.

690. snapshot-loaded startup background revalidation
     → detached refresh é registrado e drenável; não é fire-and-forget invisível.

691. scheduler creation after shutdown freeze
     → interval/retry admission rejeitada.

692. invalid IMDB_RATINGS_UPDATE_INTERVAL_HOURS
     → NaN/0/negative/overflow usam validated fallback ou fail-fast documentado; nunca timer acidental.

693. IMDb HTTP status matrix
     → HEAD/GET 404/429/500/non-2xx não instala payload; body terminal; failure class observável.

694. invalid gzip / zero parsed rows
     → current table/snapshot preservados; no empty swap.

695. atomic in-memory table swap under readers
     → readers observam old ou new complete table, nunca arrays parcialmente trocados.

696. duplicate IMDb IDs
     → explicit reject/dedupe policy; binary search result deterministic.

697. numeric id boundary
     → tt1, max uint32, >uint32, malformed/leading edge cases seguem contract.

698. Float64 sort precision boundary
     → Number.MAX_SAFE_INTEGER guard dispara fallback antes de perder ordem.

699. shared-volume dual writer
     → fenced/leader writer evita temp/final corruption OU deployment gate declara configuração unsupported.

700. combined V26 shutdown stress:
     active #742 catalog request
     + config stale load
     + IMDb update in GET/parse
     + pending IMDb snapshot commit
     + legacy Redis cleanup
     + poster warm-summary persist
     + pg read replica
     → admission freeze; abort/drain; artifact commit/cancel policy; no late retry/scheduler;
       transports close; Redis only after Redis-dependent cleanup; all five manifests terminal;
       graceful=true somente se todos os owners reais estiverem limpos.
```

---

# 564. Definition of Done V26

A implementação da #742 só pode sustentar a claim máxima V26 quando, cumulativamente ao DoD V8→V25:

```text
[ ] dev HEAD/tree continuam exatamente no snapshot V26 ou Rebase/Delta/Occurrence gates foram rerodados
[ ] issue #742 state/comments foram rechecados no PR final

[ ] cinco universos autoritativos estão materializados:
    async
    process resources
    network callers
    frontend effects
    persistent artifacts

[ ] PersistentArtifactOccurrenceManifest possui zero occurrence runtime não classificada
[ ] fs async + sync one-shot writers estão no scanner
[ ] stream/readline/zlib constructors relevantes estão no scanner
[ ] v8.writeHeapSnapshot e native artifact writers possuem classification
[ ] executionDomain evita confundir runtime state com build/CI/external readonly

[ ] cada artifact runtime possui physicalArtifactKey
[ ] cada artifact possui class + commit protocol + recovery policy
[ ] temp paths possuem collision policy
[ ] atomic replace não é descrito falsamente como fsync durability
[ ] multi-process/shared-volume policy é explícita
[ ] DATABASE_MANAGED artifacts continuam sob seu DB gate sem double-accounting

[ ] imdb-ratings.bin possui format/integrity contract versionado
[ ] corrupt/truncated/unknown snapshot não publica tabela
[ ] row count/etag/snapshot budgets são bounded
[ ] duplicate ID policy é explícita
[ ] Float64 sort optimization possui safe-integer guard/fallback

[ ] IMDb HEAD/GET valida status
[ ] todo response body possui terminal proof
[ ] gunzip/pipeline/readline possuem owner e AbortSignal/deadline
[ ] current update flight é abortável/drainable
[ ] retryTimer é cancelado e não rearma após shutdown freeze
[ ] periodic interval é cancelado
[ ] detached startup refresh está no BackgroundWorkRegistry
[ ] detached legacy Redis cleanup está no BackgroundWorkRegistry

[ ] startup 300s timeout cancela ou transfere ownership explicitamente
[ ] late startup loser não instala table/scheduler/marker sem authority

[ ] snapshot persist result distingue memoryUpdated de persisted
[ ] legacy Redis cleanup não remove o único fallback antes de durable replacement proof
[ ] maintenance marker semantics não afirmam persistência que falhou

[ ] cache migration disk/Redis markers reconciliam restart parcial
[ ] mapper/wiki cache data e ETag possuem ordering/recovery contract
[ ] poster warm-summary pending persist participa do shutdown drain
[ ] diagnostics artifact possui retention/disk/access contract

[ ] shutdown final zera pendingArtifactWrites/pendingArtifactMigrations
[ ] Redis fecha somente após work Redis-dependent autorizado ter settled/cancelled
[ ] graceful=true não mascara artifact write residual

[ ] casos 651–700 passam
[ ] casos 1–650 continuam passando
[ ] backend build + frontend build + lint + generated scanners passam
[ ] migration/concurrency/shutdown/rollback suites passam
[ ] PR Guard continua sem executar código não confiável com secrets em pull_request_target
```

---

# 565. Claim defensável V26

Depois da incorporação desta camada, é defensável afirmar:

> **V26 fornece cobertura estática rastreável e arquiteturalmente fechada do snapshot
> `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree
> `b4db5931c47035862fac075ac01ec02fe1e621c0` para a #742 e para os domínios de lifecycle/state explicitamente
> inventariados, reconciliando cinco universos autoritativos e transformando runtime/upstream/dependency/
> replica/crash/shutdown assumptions em gates executáveis.**

Ainda não é defensável, antes de implementação e execução:

```text
100% de ausência de bugs em produção
100% de comportamento de TMDB/IMDb/Simkl/outros upstreams
100% de teardown de dependência sem validar versão lockada
100% de crash-durability física em todos filesystems quando contract é apenas rename
100% de comportamento em deployment compartilhado que o Fleet Gate declara unsupported
100% de performance sem benchmark
100% de commits posteriores a d270a3a
```

A fronteira é deliberada e mensurável.

---

# 566. Ordem recomendada de implementação V26

A ordem V25 é refinada para:

```text
PR 0A — rebase fingerprint + test harness + cinco manifests + scanners + dependency fingerprint
        - adicionar PersistentArtifactOccurrenceManifest
        - adicionar fs one-shot + stream/readline/native writer seeds
        - gerar baseline classifications sem wildcards

PR 0B — fechar delta #749 antes de usar a claim "projeto completo"
        - IMDb snapshot result semantics
        - artifact integrity/version/recovery
        - status/body/pipeline cancellation
        - retry/interval/startup-refresh/legacy-cleanup owners
        - stopImdbRatingsUpdates
        - startup timeout signal/late-loser fence
        - shared-volume policy

PR 1  — config revision/storage migration + ConfigCache stale-publication fencing

PR 2  — Release Evidence V2 + Worldwide golden master + regional evaluator

PR 3  — CanonicalFilterContext/OperationContext + catalog/search integration

PR 4  — filtered pagination/cursors/source identity/freshness

PR 5  — Discover provenance/builder/import/edit-save/preview parity

PR 6  — Jellyfin/in-process/warmer/merged/custom closure

PR 7  — process resource + dependency-I/O + persistent artifact + stream/storage shutdown closure
        - classificar/melhorar mapper/wiki/poster/migration artifacts tocados pelo DoD

PR 8  — frontend release-region UI + frontend effect closure das surfaces tocadas

PR 9  — migration/load/concurrency/crash-recovery/shutdown stress
        + observability + rollout + homogeneous-fleet gates
```

Dependências obrigatórias:

```text
PR 0A
↓
PR 0B
↓
PR 1
↓
PR 2/3/4/5/6
↓
PR 7/8
↓
PR 9
```

`PR 0B` pode ser incorporado ao `PR 7` se o maintainer preferir menos PRs, mas os gates precisam existir antes
da claim final e antes do stress suite.

---

# 567. Checklist executivo final V26

Antes de entregar este plano ao Codex/implementador:

```text
[ ] confirmar `git rev-parse HEAD`
[ ] confirmar `git rev-parse HEAD^{tree}`
[ ] compare V26 HEAD vs d270a3a
[ ] rerodar tree counts
[ ] rerodar issue #742 state/comments
[ ] gerar manifests do snapshot real
[ ] falhar se houver occurrence nova não classificada
[ ] executar tests 1–700
[ ] executar builds/lint
[ ] executar integration com Redis + DB
[ ] executar crash/restart artifact fixtures
[ ] executar shutdown stress
[ ] revisar métricas/logs para secrets
[ ] revisar rollout/rollback/fleet homogeneity
```

Se qualquer item de snapshot mudar:

```text
não editar manualmente a lista e seguir;
rerodar o gate que a mudança dispara.
```

---

# 568. Resultado final da auditoria V26

O plano V25 não estava incorreto no desenho funcional da #742.

O que mudou objetivamente foi:

```text
1. o HEAD avançou;
2. um arquivo runtime novo entrou na árvore;
3. o delta acrescentou um durable local snapshot e novos owners assíncronos;
4. a própria V25 revelou uma classe que seu scanner não formalizava:
   persistent artifact state produzido sem handle persistente.
```

A V26 fecha isso com:

```text
+ snapshot atual d270a3a / tree b4db5931
+ delta classification completa
+ quinto universe: persistentArtifactOccurrences
+ scanner fs one-shot/sync/native writers
+ artifact class / atomicity / durability / recovery model
+ IMDb snapshot migration/integrity gate
+ IMDb scheduler/retry/startup/shutdown closure
+ readline/zlib/stream constructor closure
+ startup 300s late-loser fence
+ multi-process/shared-volume policy
+ existing mapper/wiki/poster/migration artifact closure
+ 50 testes adicionais, totalizando 700+ casos acumulados
```

Não há necessidade de reescrever a arquitetura central da #742.

A melhoria V26 é de **prova, lifecycle e persistência**, não de mudança do comportamento regional pretendido.

---
# 569. Reauditoria V27 — snapshot continua estável, mas a prova V26 ainda tinha boundaries operacionais não fechados

A V27 foi revalidada novamente contra:

```text
repository: cedya77/aiometadata
branch: dev
HEAD: d270a3a7f3b6e41304d9f91045b1d481311c3c96
HEAD^{tree}: b4db5931c47035862fac075ac01ec02fe1e621c0
release publicada: v3.1.0 @ 6e83e22ab9de5093f9918a1871157f401feebb03
issue #742: OPEN / enhancement / 0 comentários
```

O `dev` não avançou em relação à V26. Portanto esta camada não nasce de novo code drift; ela nasce de uma
reconciliação mais profunda entre:

```text
- storage novo do #749;
- storage legado da v3.1.0;
- rolling deploy / rollback;
- readiness real versus readiness reportada;
- settings persistidos no banco versus ordem de import dos módulos;
- residência física dos artifacts;
- allocation antes de validar snapshot;
- schema real do dataset IMDb;
- semântica exata dos timers Node.
```

A arquitetura funcional da #742 permanece válida. A V27 corrige **migration/bootstrap/control-plane proof**.

---

# 570. Blockers objetivos novos V27

Adicionar cumulativamente aos blockers V8→V26:

```text
IK. Upgrade pre-#749 → #749 não possui bootstrap a partir do Redis legado. Se não existe
    `addon/data/imdb-ratings.bin`, mas `imdb:ratings` está íntegro e o IMDb está indisponível,
    a versão nova deixa de servir ratings apesar de existir uma cópia válida usada pela v3.1.0.

IL. `install()` chama cleanup dos Redis keys legados depois que a tabela nova existe. Em rolling deploy,
    uma réplica v3.1.0 ainda usa `HGET/HMGET imdb:ratings` em cada lookup. Uma réplica nova pode apagar
    o storage ainda ativo da réplica antiga. Durable snapshot local NÃO prova fleet migration safety.

IM. O delta #749 também removeu `imdb:ratings` e `imdb-ratings-etag` de `PRESERVED_CACHE_KEYS` no
    dashboard. Mesmo que o cleanup automático seja adiado, um cache-clear durante janela mixed-version
    pode quebrar old readers. A política de compatibilidade precisa cobrir todos os deleters, não só
    `dropLegacyRedisCopy()`.

IN. Sem snapshot válido, `initializeRatings()` faz `await runRatingsUpdate()` mas ignora o boolean de
    falha. O initializer resolve normalmente; `server.ts` executa `readiness.markReady('imdbRatings')`.
    Resultado possível: boot mostra componente ready com 0 ratings e retry pendente. Readiness está
    semanticamente falsa, embora o componente seja corretamente classificado como degradable.

IO. O projeto possui settings DB-backed que são hidratados por `initializeSettings()` somente dentro de
    `startServer()`, porém vários consumidores congelam `process.env` em module load e são importados antes
    disso. `requiresRestart: true` não corrige a ordem: após restart o módulo pode capturar env/default
    antes que o valor salvo no dashboard seja aplicado. O próprio projeto já possui um workaround explícito
    no comprehensive catalog warmer, provando que o boundary é real e não apenas teórico.

IP. `scripts/check-env-registry.ts` detecta setting desconhecido e module-load read sem `requiresRestart`,
    mas não prova que DB-backed settings foram hidratados ANTES do module evaluation nem que existe um
    post-hydration refresh hook. Portanto o current env gate ainda aceita bootstrap semanticamente incorreto.

IQ. `MAX_SNAPSHOT_BYTES` só é uma defesa real se for aplicada ANTES de materializar o arquivo inteiro.
    `fs.readFile(SNAPSHOT_PATH)` aloca o payload antes que `RatingsTable.fromBuffer()` possa rejeitar
    count/length. Um arquivo local enorme/corrompido pode causar memory pressure/OOM antes do validation gate.

IR. `RatingsTable.fromLines()` pula a primeira linha incondicionalmente e depois aceita linhas parseáveis,
    mas não valida o header oficial `tconst\taverageRating\tnumVotes` nem a versão estrutural do TSV.
    Payload gzip válido porém semanticamente errado pode produzir candidate aparentemente utilizável.

IS. `/app/addon/data` é persistente na implantação Docker canônica porque o compose documentado monta volume.
    Isso não é propriedade intrínseca do path. Writable container layer, read-only filesystem, tmpfs,
    volume persistente e shared volume possuem guarantees diferentes em process restart/container recreate.
    `PersistentArtifactOccurrenceManifest` precisa declarar storage backing/residency, não apenas artifact class.

IT. `IMDB_RATINGS_UPDATE_INTERVAL_HOURS` continua usando `parseInt`. Além de NaN/0/negative já citados na V26,
    `parseInt('24foo') === 24` e delays acima do limite de timer do Node não podem ser aceitos implicitamente.
    O registry não possui hoje min/max para esse setting. Scheduler duration precisa de parser estrito e bound.

IU. Quando snapshot novo e Redis legado coexistem, eles podem representar gerações/ETags diferentes
    (por rollback, mixed fleet ou atualização parcial). Carregar o arquivo e apagar o Redis apenas porque o
    arquivo é estruturalmente válido pode destruir uma cópia mais nova. Cross-store source authority/freshness
    precisa ser reconciliada antes de cleanup destrutivo.

IV. Há drift objetivo de defaults entre control-plane e consumers: `settingsRegistry.ts` declara `168h` para
    `ANIME_LIST_UPDATE_INTERVAL_HOURS`, `WIKI_MAPPER_UPDATE_INTERVAL_HOURS`,
    `KITSU_TO_IMDB_UPDATE_INTERVAL_HOURS` e `TRAKT_ANIME_MOVIES_UPDATE_INTERVAL_HOURS`, enquanto consumers
    atuais usam fallback literal `24h`; a documentação de Wiki também declara `24h`. Mesmo sem DB override,
    dashboard/docs/runtime podem discordar. O registry precisa virar default authority única ou o scanner deve
    falhar qualquer divergência.
```

---

# 571. Sexto universo autoritativo — Runtime Setting Occurrence Manifest

## 571.1. Seis universos a partir da V27

A reconciliação normativa passa a ser:

```text
asyncOccurrences
processResourceOccurrences
networkCallerOccurrences
frontendEffectOccurrences
persistentArtifactOccurrences
runtimeSettingOccurrences
```

Merge invariant:

```text
actualAsync               - classifiedAsync               = ∅
actualProcessResource     - classifiedProcessResource     = ∅
actualNetCaller           - classifiedNetCaller           = ∅
actualFrontendEffect      - classifiedFrontendEffect      = ∅
actualPersistentArtifact  - classifiedPersistentArtifact  = ∅
actualRuntimeSetting      - classifiedRuntimeSetting      = ∅

classified occurrence apontando para symbol/AST node inexistente = CI fail
wildcard por diretório para esconder setting occurrence = proibido
```

O sexto universo não substitui `settingsRegistry.ts`. Ele prova **quando e de onde** o valor efetivo é lido.

## 571.2. Record mínimo

```ts
interface RuntimeSettingOccurrenceRecord {
  occurrenceId: string;
  settingKey: string | null;
  envVar: string;

  file: string;
  symbol: string;
  lineHint?: number;

  executionDomain:
    | 'RUNTIME_BACKEND'
    | 'RUNTIME_FRONTEND'
    | 'BUILD_CI'
    | 'TEST_ONLY';

  sourceClass:
    | 'ENV_ONLY'
    | 'DB_OVERRIDABLE'
    | 'INTERNAL_RUNTIME'
    | 'LEGACY_ALIAS';

  readPhase:
    | 'MODULE_LOAD'
    | 'BOOTSTRAP_AFTER_SETTINGS'
    | 'LAZY_RUNTIME'
    | 'REQUEST_TIME';

  requiresRestart: boolean;
  liveUpdatePolicy:
    | 'NOT_SUPPORTED'
    | 'READ_LAZILY'
    | 'APPLY_SIDE_EFFECT'
    | 'POST_HYDRATION_REFRESH';

  parserAuthority: string | null;
  boundsAuthority: string | null;
  hydrationAuthority: string | null;
  postHydrationRefreshOwner: string | null;

  bootstrapSafe: boolean;
  terminalProof: string;
}
```

## 571.3. Seeds do scanner

Reutilizar e ampliar `scripts/check-env-registry.ts` para materializar, não apenas avisar:

```text
process.env.FOO
process.env['FOO']
process.env["FOO"]
getSetting('FOO')
envInt('FOO', ...)
helpers equivalentes de env/settings
module-level const/let/var
module-level IIFE
module-level client/dispatcher/resource constructor derivado de setting
```

Além do textual scanner, exigir:

```text
- import graph a partir do entrypoint real;
- boundary exato em que initializeSettings() termina;
- lista de módulos avaliados antes desse boundary;
- classificação envOnly vs DB-overridable do settings registry;
- post-hydration refresh hook quando module-load read for intencional;
- stale classification failure.
```

## 571.4. Regra central

```text
DB_OVERRIDABLE
+
MODULE_LOAD
+
module avaliado antes de initializeSettings()
+
sem POST_HYDRATION_REFRESH
=
CI FAIL
```

`requiresRestart=true` sozinho NÃO satisfaz esse gate.

---

# 572. Settings Bootstrap Ordering Gate

## 572.1. Problema concreto do entrypoint atual

Hoje a ordem conceitual é:

```text
server module evaluation
  ↓
imports estáticos avaliam módulos consumidores
  ↓
alguns capturam process.env em const/module scope
  ↓
startServer()
  ↓
database.initialize()
  ↓
initializeSettings()
  ↓
DB overrides finalmente entram em process.env
```

Logo um setting salvo no dashboard pode chegar tarde demais ao consumer.

Exemplos confirmados no snapshot:

```text
addon/lib/imdbRatings.ts
→ IMDB_RATINGS_UPDATE_INTERVAL_HOURS

addon/lib/wiki-mapper.ts
→ WIKI_MAPPER_UPDATE_INTERVAL_HOURS

addon/lib/id-mapper.js
→ ANIME_LIST_UPDATE_INTERVAL_HOURS
→ KITSU_TO_IMDB_UPDATE_INTERVAL_HOURS
→ TRAKT_ANIME_MOVIES_UPDATE_INTERVAL_HOURS
→ ANIME_API_OVERLAY_ENABLED

addon/utils/concurrency.ts
→ META_CONCURRENCY
```

O `comprehensiveCatalogWarmer.js` já possui comentário/refresh específico dizendo que o módulo é importado antes
de os dashboard settings serem carregados no env. A V27 transforma esse workaround local em contrato global.

## 572.2. Arquitetura recomendada — bootstrap em duas fases

Preferência V27:

```text
minimal bootstrap entry
  ↓
initialize database using bootstrap-safe envOnly settings
  ↓
initializeSettings()
  ↓
apply DB overrides to effective settings
  ↓
initialize outbound proxy/global dispatcher
  ↓
dynamic import runtime graph
  ↓
start server / initialize resources / schedulers
```

Estrutura possível:

```text
addon/bootstrap.ts
addon/serverRuntime.ts
```

Sem exigir esses nomes.

Regra importante:

```text
HTTP proxy/global dispatcher deve ser configurado DEPOIS da hydration
mas ANTES de qualquer runtime module que abra client/agent/SDK transport.
```

`DATABASE_URI` e qualquer setting indispensável para abrir o banco que contém os próprios settings precisa ser
`ENV_ONLY/bootstrap-safe`, evitando dependência circular.

## 572.3. Alternativa aceitável

Se o maintainer não quiser split do entrypoint:

```text
module-load consumers podem permanecer
SOMENTE se possuírem refreshSettingsAfterInitialization() explícito
chamado depois de initializeSettings()
e antes de criar timers/resources derivados daquele valor.
```

Isso é menos preferível porque exige disciplina distribuída.

## 572.4. O que não vale como correção

```text
- apenas requiresRestart=true;
- apenas mudar process.env depois do import;
- apenas mostrar changedSinceBoot no dashboard;
- reiniciar duas vezes;
- ler o valor correto só no dashboard enquanto o runtime usa outro;
- allowlist do scanner sem prova de post-hydration refresh.
```

## 572.5. Default Authority / Documentation Consistency Gate

O snapshot atual possui divergência concreta:

```text
settingsRegistry.ts:
ANIME_LIST_UPDATE_INTERVAL_HOURS         = 168
WIKI_MAPPER_UPDATE_INTERVAL_HOURS        = 168
KITSU_TO_IMDB_UPDATE_INTERVAL_HOURS      = 168
TRAKT_ANIME_MOVIES_UPDATE_INTERVAL_HOURS = 168

consumers module-load:
id-mapper.js fallbacks                    = 24
wiki-mapper.ts fallback                    = 24

docs/ENVIRONMENT_VARIABLES.md:
WIKI_MAPPER_UPDATE_INTERVAL_HOURS          = 24
```

Isso deve ser impossível depois da V27.

Regra:

```text
registry default = única authority programática
consumer sem valor externo/DB = usa registry default
docs/.env example = gerados ou validados contra registry
fallback literal divergente = CI FAIL
```

Se algum setting precisa de default diferente por deployment/domain:

```text
criar setting/contract distinto
```

não esconder a diferença em fallback literal local.

## 572.6. Effective runtime setting snapshot

Para settings que criam recurso/scheduler:

```ts
interface EffectiveRuntimeSetting<T> {
  key: string;
  value: T;
  source: 'db' | 'env' | 'default' | 'legacy-env';
  resolvedAt: number;
  requiresRestart: boolean;
}
```

Log/metrics podem expor `source` e valor apenas quando não sensível.

---

# 573. Legacy IMDb Redis Bootstrap / Cross-Store Migration Gate

## 573.1. Estados de boot

O initializer precisa distinguir explicitamente:

```text
A. valid disk snapshot
B. no disk snapshot + valid legacy Redis hash
C. no disk snapshot + no usable legacy Redis + network available
D. no usable source
E. disk + legacy Redis coexistentes com generation/ETag divergente
```

Nunca reduzir tudo a:

```text
loadSnapshot() ? use disk : download internet
```

## 573.2. Availability-preserving upgrade

Recomendação V27 para upgrade da v3.1.0:

```text
no valid disk snapshot
+
legacy Redis hash exists
→ enable temporary legacy lookup fallback immediately
→ migrate legacy Redis to RatingsTable in bounded background/startup-owned work
→ validate candidate
→ persist new snapshot
→ switch readers atomically to memory table
→ keep/delete legacy storage according to fleet cleanup eligibility
```

Enquanto a table ainda não está pronta:

```text
single lookup → legacy HGET fallback
list projection → legacy HMGET fallback
```

Esse fallback é **transicional**; não reverte a arquitetura final para Redis-per-lookup.

## 573.3. Import do hash legado

Nunca:

```text
HGETALL 1M+ fields
```

como requisito implícito.

Preferir:

```text
HSCAN bounded batches
→ strict parse "rating|votes"
→ row/resource budget
→ build candidate arrays
→ deterministic sort/dedupe policy
```

Se migration excede startup deadline:

```text
legacy lookup continua servindo
+
ownership transfere ao BackgroundWorkRegistry
```

ou cancellation/join explícito.

## 573.4. Cross-store source authority

Se disk snapshot e Redis legado coexistem:

```text
same source ETag/generation
→ disk snapshot pode ser preferido

ETag/generation diverge
→ não executar destructive cleanup
→ serving policy explícita
→ revalidar upstream ou comparar provenance/freshness suficiente
→ reconciliar antes de apagar uma cópia
```

O snapshot V2 deve carregar, no mínimo:

```text
sourceEtag
sourceFetchedAt ou upstream-check provenance equivalente
formatVersion
content digest
```

Não usar file mtime como source freshness authority.

## 573.5. Legacy data inválida

```text
malformed Redis value
zero usable rows
row count fora de bound
legacy ETag incoerente
Redis indisponível
```

→ não promover a source a authoritative table.

Preservar last-known-good disponível e seguir network/retry policy.

---

# 574. Mixed-Version Fleet / Rollback Gate para IMDb ratings

## 574.1. O problema

Pre-#749:

```text
old replica
→ getImdbRating() = Redis HGET imdb:ratings
→ list projection = Redis HMGET imdb:ratings
```

Post-#749:

```text
new replica
→ in-memory table + disk snapshot
→ cleanup legado pode UNLINK imdb:ratings
```

Logo:

```text
new durable snapshot local
≠
permission to delete storage still used by old live replicas
```

## 574.2. Reutilizar o Fleet Gate existente

Não criar um segundo mecanismo de fleet identity se o projeto já implementar capability/fleet admission para os
gates anteriores.

Adicionar capability explícita, por exemplo conceitualmente:

```text
imdbRatingsReader = redis-v1 | file-memory-v2
imdbRatingsLegacyRedisRequired = true | false
```

O nome exato não é normativo.

## 574.3. Cleanup eligibility

`dropLegacyRedisCopy()` só pode deletar quando:

```text
new durable snapshot válido
AND
nenhuma replica live conhecida depende de redis-v1
AND
rollback policy permite destruição
AND
nenhum migration/reconciliation pendente
```

Em single-replica self-host comprovado:

```text
fleet condition pode resolver localmente
```

Em multi-replica:

```text
heartbeat/capability TTL/fleet epoch ou deployment gate equivalente
```

é obrigatório.

## 574.4. Dashboard cache clear entra na mesma policy

Enquanto `legacyRedisRequired=true` em qualquer live replica:

```text
imdb:ratings
imdb-ratings-etag
```

continuam preservados contra generic cache clear.

O deleter do dashboard precisa consultar a mesma migration authority; não manter uma lista independente que pode
se desalinhar.

## 574.5. Rollback window

Antes de destruir legacy storage, definir:

```text
rollback-supported-until
ou
explicit migration finalized
```

Se rollback para v3.1.0 é parte do release plan:

```text
Redis legado permanece disponível até o rollback gate ser encerrado
```

Depois da finalização:

```text
rollback antigo pode exigir network rebuild
```

mas isso precisa ser documentado e testado, nunca descoberto em incidente.

## 574.6. Mixed-fleet value parity

IMDb rating é enrichment, não membership correctness da #742. Portanto a V27 NÃO obriga dual-write de todo refresh
apenas para manter cada réplica no mesmo decimal durante uma janela curta.

Ela obriga:

```text
- zero destructive availability regression;
- cleanup compatível;
- source generation observável;
- policy explícita se mixed-fleet value skew temporário for aceito.
```

Se o produto exigir exact value parity durante rolling deploy:

```text
dual-write transicional OU homogeneous activation gate
```

passa a ser obrigatório.

---

# 575. IMDb Ratings Readiness Truthfulness Gate

## 575.1. Initializer precisa retornar estado, não `void`

Substituir semântica interna por algo equivalente:

```ts
type RatingsInitState =
  | { state: 'ready-memory'; count: number; source: 'snapshot' | 'network' }
  | { state: 'ready-legacy-fallback'; count: number }
  | { state: 'degraded-no-ratings'; retryScheduled: boolean; error: string }
  | { state: 'cancelled'; error: string };
```

Não é necessário expor exatamente esse type externamente.

## 575.2. Mapping para readiness

```text
valid memory table
→ imdbRatings READY

valid legacy lookup fallback ativo
→ READY ou explicit transitional-ready
   + migration status separado

no usable table/fallback
+
initial fetch failed
→ imdbRatings DEGRADED
→ global addon pode continuar ready porque component kind já é degradable

startup cancellation/ownership transfer
→ state conforme orchestrator contract
```

É proibido:

```text
count=0
ratingsLoaded=false
initializer resolved normally
→ readiness.markReady
```

## 575.3. Retry continua permitido em degraded

`DEGRADED` não significa parar:

```text
retry timer/background update pode continuar
```

mas precisa de owner/lifecycle V26.

Quando um retry instala uma tabela válida:

```text
readiness.markReady('imdbRatings')
```

é permitido **depois** do transition atomically observed.

## 575.4. Snapshot válido + upstream indisponível

```text
snapshot válido carregado
+
background revalidation falha
→ serving readiness continua READY
→ refresh health/upstreamCheck status pode ficar degraded/stale separadamente
```

Não degradar serving apenas porque a maintenance check falhou.

## 575.5. Boot line/dashboard

Estados precisam ser coerentes:

```text
READY 1,005,889 ratings
READY legacy fallback, migration pending
DEGRADED no usable ratings, retry scheduled
```

Nunca:

```text
✔ imdbRatings 0 ratings
```

quando a tabela não está initialized.

---

# 576. Artifact Residency / Data-Root Capability Gate

## 576.1. Extensão do PersistentArtifactOccurrenceManifest

Adicionar:

```ts
storageBacking:
  | 'PERSISTENT_VOLUME'
  | 'CONTAINER_WRITABLE_LAYER'
  | 'EPHEMERAL_TMPFS'
  | 'READ_ONLY_FILESYSTEM'
  | 'EXTERNAL_MANAGED'
  | 'UNKNOWN';

survives:
  | 'PROCESS_RESTART'
  | 'CONTAINER_RESTART'
  | 'CONTAINER_RECREATE'
  | 'NODE_REPLACEMENT'
  | 'UNKNOWN';

pathAuthority: string;
writableRequirement: 'REQUIRED' | 'OPTIONAL_DEGRADE' | 'READ_ONLY';
```

## 576.2. Canonical Docker contract

Na implantação documentada:

```text
host/volume data dir
→ /app/addon/data
```

Portanto artifacts ali podem sobreviver container recreate **quando o volume está realmente montado**.

O runtime não deve afirmar isso apenas porque o path é `/app/addon/data`.

## 576.3. Noncanonical deploys

Classificar explicitamente:

```text
no volume, writable image layer
→ funciona durante container lifetime
→ snapshot rebuild após recreate é esperado

read-only root filesystem sem data volume writable
→ memory serving funciona
→ durable cache persistence degraded

shared volume
→ multi-process gate V26/V27

ephemeral tmpfs
→ process/container semantics documentadas
```

## 576.4. Data-root authority

Evitar cada módulo inventar independentemente:

```text
path.join(process.cwd(), 'addon', 'data', ...)
```

Preferir uma authority comum derivada do app root/data root já validado.

A V27 não exige criar env novo se não houver necessidade de produto. Exige um helper/authority único.

## 576.5. Startup capability probe

Para artifacts rebuildable cuja persistência é opcional:

```text
resolve data root
→ mkdir quando permitido
→ create unique probe temp
→ write
→ rename no mesmo dir
→ unlink
→ classify writable/rename-capable
```

Falha:

```text
EACCES / EROFS / ENOSPC / EDQUOT / other
→ observável
→ componente pode degradar persistence sem crash se serving em memória continua válido
```

Não executar destructive probe em artifact final.

---

# 577. Snapshot Pre-Allocation / Disk-Pressure Gate

## 577.1. Bound antes de `readFile`

Para `imdb-ratings.bin`:

```text
lstat/stat
→ regular file policy
→ size <= MAX_SNAPSHOT_BYTES
→ só então read/parse
```

Se houver risco de TOCTOU relevante:

```text
open handle
→ fstat(handle)
→ bounded read pelo mesmo handle
```

Como o artifact é local/rebuildable, threat model pode permanecer operational e não hostile-multiuser, mas a
allocation bound precisa ocorrer antes da allocation integral.

## 577.2. Não confiar no header antes do file-size bound

```text
count/etagLength
```

só são lidos depois que o payload físico já passou no maximum byte budget.

## 577.3. Write-side failures

Classificar explicitamente:

```text
ENOSPC
EDQUOT
EACCES
EROFS
EXDEV
EMFILE/ENFILE quando aplicável
```

Regras:

```text
- final last-known-good não é removido;
- temp é limpo/quarantined conforme policy;
- memoryUpdated/persisted continuam distintos;
- maintenance marker não diz durable success;
- repeated local-storage failure não vira tight retry loop.
```

## 577.4. Temp coexistence budget

Atomic replace pode exigir temporariamente:

```text
old final + new temp
```

Logo disk planning usa peak commit footprint, não apenas tamanho final.

Não é necessário reservar espaço com heurística frágil; é obrigatório tratar a falha de commit como estado
esperado e observável.

---

# 578. IMDb Dataset Schema / Provenance Gate

## 578.1. Header obrigatório

Depois de gzip:

```text
tconst\taverageRating\tnumVotes
```

é o schema authority atual.

Permitir opcional BOM somente se documentado/testado.

Não:

```text
skip first line whatever it is
```

## 578.2. Data row contract

Cada linha não vazia precisa obedecer:

```text
exactly 3 semantic fields
id = tt + positive decimal <= uint32
rating = strict finite decimal no provider-valid range
votes = strict base-10 non-negative integer <= uint32
```

`parseFloat('8.1x')` e `parseInt('100x', 10)` não podem passar silenciosamente.

## 578.3. Invalid row policy

Escolher uma política versionada:

```text
STRICT:
qualquer non-empty malformed data row rejeita o candidate inteiro
```

ou:

```text
BOUNDED_TOLERANCE:
invalidRowCount/ratio possui threshold explícito
excedeu → reject candidate
```

Preferência V27 para dataset oficial pequeno/estruturado:

```text
STRICT com trailing empty line permitida
```

## 578.4. Provenance

Registrar por update:

```text
source URL enum/id
source ETag
source check time
source fetched time
schema/header version
compressed bytes quando conhecido
parsed row count
filtered-by-min-votes count
invalid row count
digest do committed snapshot
```

Sem colocar URL query/secret em metrics.

## 578.5. Gzip válido não implica dataset válido

Pipeline success + zero stream error é necessário, mas não suficiente.

Commit authority exige cumulativamente:

```text
HTTP status valid
body terminal
compression parse valid
header valid
row invariants valid
resource bounds valid
non-zero candidate
binary snapshot integrity valid
```

---

# 579. Scheduler Numeric-Bounds / Duration Gate

## 579.1. Parser estrito

Para hours de scheduler:

```ts
parseStrictPositiveIntegerHours(raw)
```

Aceitar:

```text
"24"
"168"
```

Rejeitar:

```text
""
"0"
"-1"
"1.5"
"24foo"
"NaN"
"Infinity"
whitespace-only
```

Whitespace externo pode ser trimado.

## 579.2. Timer bound do Node

Antes de chamar `setTimeout/setInterval`:

```text
delayMs deve ser inteiro seguro
> 0
<= máximo suportado pelo primitive/runtime lockado
```

Para o runtime Node atual, não depender de overflow/clamping automático.

Se o produto quiser intervalos maiores que um único timer suporta:

```text
usar scheduler por deadline/chained timer
```

em vez de limitar silenciosamente.

## 579.3. Registry alignment

Para `IMDB_RATINGS_UPDATE_INTERVAL_HOURS`:

```text
settingsRegistry min/max/validate
+
runtime parser
+
docs/.env example
```

precisam descrever o mesmo domain.

O mesmo rule deve ser aplicado aos outros scheduler intervals encontrados pelo Runtime Setting Occurrence Gate,
não apenas ao IMDb.

## 579.4. Persisted DB value

Valor salvo no dashboard e marcado `requiresRestart`:

```text
restart
→ bootstrap hydration
→ parser strict
→ effective scheduler uses saved value
```

Esse teste fecha simultaneamente Settings Bootstrap + Duration Gate.

---

# 580. Observabilidade V27

Adicionar cumulativamente:

```text
runtime_setting_resolved_total{setting,source,phase}
runtime_setting_bootstrap_violation_total{setting}
runtime_setting_effective_value_info{setting,source}   # somente não sensível e bounded labels

imdb_ratings_source_state{source=disk|legacy_redis|network|none}
imdb_ratings_legacy_fallback_active
imdb_ratings_legacy_migration_total{result}
imdb_ratings_cross_store_reconcile_total{result,reason}
imdb_ratings_legacy_cleanup_eligible
imdb_ratings_fleet_legacy_reader_count

imdb_ratings_readiness_state{state=ready|legacy_fallback|degraded}
imdb_ratings_dataset_schema_failure_total{reason}
imdb_ratings_invalid_rows_total
imdb_ratings_snapshot_oversize_total
imdb_ratings_data_root_capability{writable,backing}
persistent_artifact_storage_failure_total{artifact,reason}
```

Cardinality:

```text
setting = registry key enum
source/state/reason = enums
não expor secret value
não usar raw path como label de alta cardinalidade
não usar ETag como label
```

Dashboard V27 deve conseguir distinguir:

```text
serving source
durable source
migration pending
last upstream check
last successful update
persistence degraded
readiness state
```

---

# 581. Matriz de testes adicional V27 — casos 701–750

Adicionar cumulativamente aos 700+ casos V8→V26:

```text
701. snapshot fingerprint V27
     → dev HEAD == d270a3a7f3b6e41304d9f91045b1d481311c3c96 e tree == b4db5931c47035862fac075ac01ec02fe1e621c0
       OU Rebase/Delta/Occurrence gates rerodados.

702. Runtime Setting Occurrence Manifest
     → todas as ocorrências process.env/getSetting/env helper runtime estão classificadas; zero unmatched.

703. DB-overridable module-load setting antes de initializeSettings sem refresh
     → CI falha Settings Bootstrap Ordering Gate.

704. ENV_ONLY bootstrap setting em module load
     → permitido quando necessário para abrir database/bootstrap resource e classificado.

705. lazy runtime setting lido após hydration
     → usa DB override efetivo sem restart extra.

706. comprehensive catalog warmer workaround existente
     → scanner reconhece post-hydration refresh owner; não cria falso positivo.

707. salvar IMDB_RATINGS_UPDATE_INTERVAL_HOURS=12 no dashboard + restart
     → scheduler efetivo usa 12h, bootValues/changedSinceBoot coerentes.

708. salvar WIKI_MAPPER_UPDATE_INTERVAL_HOURS=48 + restart
     → wiki scheduler efetivo usa 48h.

709. salvar ANIME_LIST_UPDATE_INTERVAL_HOURS/KITSU/TRAKT intervals + restart
     → id-mapper captura valores hidratados, não defaults pré-settings.

710. zero override/default authority
     → Anime/Wiki/Kitsu/Trakt update intervals efetivos usam o mesmo default do registry (`168h` no snapshot atual);
       docs/runtime fallback divergente faz CI falhar.

711. proxy setting requiresRestart salvo no DB + restart
     → global outbound dispatcher é configurado depois da hydration e antes de outbound clients.

712. runtime graph tenta abrir outbound client antes do proxy/settings bootstrap
     → bootstrap gate falha/test harness detecta ordering violation.

713. initializeSettings falha
     → runtime side-effect graph/schedulers não inicia parcialmente.

714. bootstrap reentry/double initialization
     → database/settings initialization idempotent ou erro explícito; nenhum duplicated resource owner.

715. settings source telemetry
     → non-sensitive value/source corretos; sensitive setting nunca expõe value.

716. upgrade v3.1.0 com no disk snapshot + legacy Redis válido + IMDb offline
     → ratings continuam disponíveis pelo legacy fallback; readiness não mente.

717. legacy Redis bootstrap migration normal
     → HSCAN bounded → valid table → snapshot commit → atomic reader switch.

718. legacy Redis migration excede startup deadline
     → fallback continua servindo; owner transfere/cancela conforme policy; sem second migration concorrente.

719. malformed legacy Redis row
     → strict parse; candidate não instala silenciosamente; legacy source permanece intacta até decision.

720. legacy Redis zero usable rows
     → source não é promovida; network/retry path segue; no destructive cleanup.

721. disk snapshot + legacy Redis same ETag/generation
     → disk pode servir; reconciliation determina cleanup eligibility sem redownload obrigatório.

722. disk snapshot ETag A + legacy Redis ETag B
     → zero destructive cleanup até source authority ser reconciliada.

723. valid disk older + legacy Redis newer comprovado
     → policy não apaga source nova; revalidation/migration converge deterministicamente.

724. mixed fleet: old redis-v1 reader + new file-v2 reader
     → new replica NÃO unlink legacy Redis.

725. last old replica leaves fleet
     → cleanup eligibility muda apenas após capability TTL/fleet proof.

726. dashboard cache clear durante mixed fleet
     → imdb legacy keys permanecem preservadas.

727. dashboard cache clear após migration finalized
     → legacy keys podem ser removidas conforme same migration authority.

728. rollback para v3.1.0 dentro da janela suportada
     → legacy Redis ainda existe; old reader continua disponível sem network obrigatório.

729. rollback depois de explicit migration finalization
     → comportamento documentado/testado; rebuild requirement não é surpresa silenciosa.

730. two new replicas tentam legacy migration simultânea em shared deployment
     → process/fleet policy impede destructive race; Redis source não é apagada prematuramente.

731. no snapshot + no legacy Redis + initial network failure
     → imdbRatings state DEGRADED, não READY; retry scheduled quando autorizado.

732. degraded initial state + retry success
     → readiness transiciona atomically para READY com count > 0.

733. valid snapshot + background revalidation failure
     → serving readiness permanece READY; refresh health mostra falha separadamente.

734. valid legacy fallback + migration pending
     → serving status explícito, não N/A; migration observável.

735. boot summary sem usable ratings
     → mostra degraded/retry, nunca success glyph com 0 initialized ratings.

736. shutdown enquanto degraded retry pendente
     → timer cancelado; readiness não transiciona depois do shutdown freeze.

737. canonical persistent data volume
     → artifact manifest registra persistent backing e recreate guarantee conforme deployment fixture.

738. writable container layer sem volume
     → artifact funciona; reporta non-persistent-across-recreate; sem claim falsa de durability.

739. read-only filesystem sem writable data volume
     → in-memory table pode servir; persist result degraded; zero destructive legacy cleanup.

740. ENOSPC durante snapshot temp write
     → old final preservado; temp cleanup; memory/persist result separado; retry não entra tight loop.

741. EROFS/EACCES data root
     → capability probe/report correto; process behavior segue artifact class.

742. shared volume temp/final
     → temp no mesmo filesystem; EXDEV não é mascarado; writer fence V26 continua válido.

743. oversized snapshot antes de readFile
     → stat/open-size gate rejeita sem alocar payload inteiro.

744. snapshot file cresce/troca entre stat e read
     → bounded same-handle policy ou second bound impede oversized allocation/publication.

745. official IMDb TSV header
     → aceito e schema version registrado.

746. wrong TSV header com linhas numericamente parseáveis
     → candidate rejeitado; last-known-good permanece.

747. TSV row `tt123\t8.1x\t100`
     → strict parser rejeita; parseFloat prefix não é aceito.

748. TSV row `tt123\t8.1\t100x`
     → strict integer parser rejeita; parseInt prefix não é aceito.

749. IMDB_RATINGS_UPDATE_INTERVAL_HOURS="24foo"/0/negative/unsafe/overflow
     → registry/runtime rejeita ou usa validated documented fallback; nenhum 1ms/tight-loop timer.

750. combined V27 migration/bootstrap/shutdown stress
     → DB settings hidratam antes dos consumers; old/new ratings storage coexistence não sofre destructive cleanup;
       degraded readiness é truthful; SIGTERM fecha runtime com seis occurrence universes zerados ou leftovers
       external/explicitamente classificados.
```

---

# 582. Definition of Done V27

A implementação da #742 só pode sustentar a claim máxima V27 quando, cumulativamente ao DoD V8→V26:

```text
[ ] dev HEAD/tree continuam no snapshot V27 ou Rebase/Delta/Occurrence gates foram rerodados
[ ] issue #742 state/comments foram rechecados no merge HEAD

[ ] seis universos autoritativos estão materializados:
    async
    process resources
    network callers
    frontend effects
    persistent artifacts
    runtime settings

[ ] RuntimeSettingOccurrenceManifest possui zero occurrence runtime não classificada
[ ] scripts/check-env-registry ou sucessor prova bootstrap ordering, não só requiresRestart
[ ] DB_OVERRIDABLE + MODULE_LOAD antes de settings hydration sem refresh = CI fail
[ ] bootstrap-safe/envOnly settings estão explicitamente classificados
[ ] outbound proxy/global dispatcher nasce depois da settings hydration e antes de clients
[ ] dashboard-saved requiresRestart setting realmente afeta runtime após um restart
[ ] registry default é authority única; fallback/docs divergentes falham CI

[ ] upgrade pre-#749 possui availability-preserving path quando legacy Redis existe
[ ] legacy migration usa bounded scan/read, não HGETALL obrigatório
[ ] disk/legacy Redis source divergence possui reconciliation authority
[ ] durable local snapshot sozinho não autoriza destructive legacy cleanup
[ ] mixed-version fleet não perde ratings por UNLINK feito por replica nova
[ ] dashboard cache clear respeita a mesma legacy cleanup eligibility
[ ] rollback window/finalization está documentada e testada

[ ] initial ratings failure sem source útil marca DEGRADED, não READY
[ ] retry success pode promover readiness para READY
[ ] snapshot válido + refresh failure não derruba serving readiness
[ ] boot/dashboard distinguem ready/degraded/migration/persistence

[ ] persistent artifact records declaram storageBacking/survival/writability
[ ] canonical volume não é confundido com garantia intrínseca do path
[ ] read-only/ephemeral/no-volume deploys possuem comportamento explícito
[ ] data-root/path authority é comum aos artifacts runtime relevantes

[ ] snapshot size bound ocorre antes da allocation integral
[ ] storage errors ENOSPC/EDQUOT/EACCES/EROFS/EXDEV possuem policy
[ ] temp commit peak footprint/recovery não apaga final válido

[ ] IMDb TSV header/schema é validado
[ ] row numeric parsing é strict, não prefix-accepting
[ ] malformed non-empty row policy é versionada
[ ] source/schema/provenance counters são observáveis

[ ] scheduler intervals possuem strict parser + runtime-safe delay bound
[ ] registry min/max/validate e runtime parser permanecem alinhados

[ ] casos 701–750 passam
[ ] casos 1–700 continuam passando
[ ] backend/frontend build + lint + generated scanners passam
[ ] upgrade/migration/rollback/mixed-fleet fixtures passam
[ ] read-only/ephemeral/persistent data-root fixtures passam
[ ] shutdown stress termina com seis universos reconciliados
```

---

# 583. Ordem recomendada de implementação V27

A ordem V26 é refinada para eliminar bootstrap/migration hazards antes da feature regional:

```text
PR 0A — snapshot fingerprint + harness + seis manifests/scanners
        - manter cinco manifests V26
        - adicionar RuntimeSettingOccurrenceManifest
        - ampliar check-env-registry para hydration/import-order proof

PR 0B — settings bootstrap ordering
        - two-stage bootstrap OU refresh hooks formalizados
        - DB settings hidratados antes de module-load consumers relevantes
        - proxy/global dispatcher depois da hydration
        - strict scheduler setting parsers/bounds

PR 0C — ratings cross-store migration/readiness
        - legacy Redis fallback/migration
        - source reconciliation disk ↔ Redis
        - fleet-safe cleanup + dashboard clear policy
        - truthful readiness
        - data-root residency/pre-read/schema gates
        - manter todo lifecycle/artifact hardening V26

PR 1  — config revision/storage migration + ConfigCache fencing

PR 2  — Release Evidence V2 + Worldwide golden master + regional evaluator

PR 3  — CanonicalFilterContext/OperationContext + catalog/search integration

PR 4  — filtered pagination/cursors/source identity/freshness

PR 5  — Discover provenance/builder/import/edit-save/preview parity

PR 6  — Jellyfin/in-process/warmer/merged/custom closure

PR 7  — process resource + dependency-I/O + artifact/storage/shutdown closure restante

PR 8  — frontend release-region UI + frontend effect closure

PR 9  — full migration/load/concurrency/crash/shutdown/mixed-fleet stress
        + observability + rollout + rollback drill
```

Dependência:

```text
PR 0A
↓
PR 0B
↓
PR 0C
↓
PR 1
↓
PR 2/3/4/5/6
↓
PR 7/8
↓
PR 9
```

Razão:

```text
não construir #742 em cima de settings que podem estar usando valores errados após restart
nem em cima de um storage migration que pode quebrar rolling fleet/rollback.
```

---

# 584. Resultado final da auditoria V27

A V26 já era extremamente forte no desenho da #742, lifecycle e persistent artifacts. A V27 encontrou gaps que
não exigem reescrever o release-visibility engine; exigem fechar **bootstrap e migração entre gerações do sistema**.

Ajustes V27:

```text
+ snapshot d270a3a / tree b4db5931 revalidado, sem drift novo
+ sexto universo: runtimeSettingOccurrences
+ settings hydration/import-order gate
+ two-stage bootstrap recomendado
+ prova de que requiresRestart sozinho não basta
+ default authority única para registry/runtime/docs (fecha drift 168h vs 24h)
+ legacy Redis availability fallback/migration
+ cross-store ETag/generation reconciliation
+ mixed-version fleet-safe Redis cleanup
+ dashboard cache-clear incluído na migration authority
+ rollback compatibility window
+ truthful IMDb readiness/degraded transition
+ artifact storage residency/backing semantics
+ pre-read allocation bound
+ data-root capability/read-only/ENOSPC handling
+ strict IMDb TSV schema/header/numeric parsing
+ strict scheduler duration + Node timer bounds
+ 50 novos casos, total acumulado 750+ casos
```

Claim defensável V27:

> **Para o snapshot `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree
> `b4db5931c47035862fac075ac01ec02fe1e621c0`, o plano passa a reconciliar seis universos autoritativos
> e fecha, além da arquitetura funcional da #742, lifecycle, resources, network, frontend effects, artifacts,
> runtime settings bootstrap, cross-store upgrade/rollback e readiness semantics através de gates executáveis.**

Ainda não afirmar antes da implementação/execução:

```text
- ausência literal de todos os bugs;
- comportamento futuro dos upstreams;
- performance sem benchmark;
- crash durability além do contract declarado pelo filesystem/artifact class;
- suporte a deployment que o fleet/residency gate classifique como unsupported;
- cobertura de commits posteriores ao snapshot sem rerun dos gates.
```

Conclusão arquitetural:

```text
A. não mudar o núcleo conceitual da #742;
B. implementar primeiro bootstrap/settings + migration/readiness;
C. depois implementar evidence/policy/pagination/região;
D. só chamar de FINAL quando os 750+ casos e generated manifests estiverem verdes no merge HEAD.
```

---

# 585. Reauditoria normativa V28 — Durability-Convergence, Legacy-Scan Consistency & Deployment-Entrypoint Closure

A V28 foi executada contra o **mesmo snapshot V27**, agora com foco adversarial em três perguntas:

```text
1. uma migração que lê storage legado em batches realmente lê UMA geração coerente?
2. uma atualização válida que não conseguiu persistir converge depois para durável sem depender de novo upstream?
3. o que o plano prova no source é exatamente o que produção executa e o rollout usa para admitir tráfego?
```

Revalidação do snapshot em 2026-09-25:

```text
dev HEAD  = d270a3a7f3b6e41304d9f91045b1d481311c3c96
tree SHA  = b4db5931c47035862fac075ac01ec02fe1e621c0
tree      = 584 entries / 545 blobs / 39 trees
v3.1.0    = 6e83e22ab9de5093f9918a1871157f401feebb03
dev       = 1 commit ahead de v3.1.0
issue #742 = open / 0 comments
```

Evidências concretas rechecadas no código:

```text
pre-#749 / v3.1.0 imdbRatings.ts:
  build temp hash
  → HSET batches
  → RENAME temp → imdb:ratings
  → SET imdb-ratings-etag

current imdbRatings.ts:
  install(memory, etag)
  → saveSnapshot()
  → markUpdated(shared Redis marker)

current server.ts:
  source graph é importado estaticamente antes de startServer()/initializeSettings()

current index.ts:
  /health/live
  /health/ready
  → createReadinessGate(... allowPaths ['/health']) antes das rotas de negócio

current production entry:
  Docker entrypoint → node dist/server/server.js
  tsconfig.backend → module=CommonJS

current Docker HEALTHCHECK:
  GET /health/live
```

Conclusão desta reauditoria:

> A V27 está correta no desenho principal, mas **HSCAN bounded não equivale a snapshot coerente**, **ETag-match não equivale a durable convergence** e **source-order proof não equivale automaticamente a emitted/runtime/deployment proof**.

---

# 586. Blockers adicionais V28

Continuando a sequência cumulativa de blockers:

```text
IW. A migração V27 propõe HSCAN em batches do hash legado. O writer v3.1.0 publica uma nova geração com
    RENAME; um RENAME entre dois HSCAN pode fazer o importer observar partes de gerações diferentes ou
    invalidar a semântica do cursor. HSCAN não é snapshot isolation.

IX. O ETag legado é gravado DEPOIS do RENAME. Existe janela em que hash e ETag pertencem a gerações
    diferentes. Um único read de ETag antes/depois do scan não pode ser tratado como transação cross-key.

IY. Na arquitetura que permite install em memória antes do durable commit, persist failure cria
    durability debt. Se currentEtag já foi atualizado, o próximo HEAD pode responder o mesmo ETag e o
    código pode concluir "unchanged" sem tentar persistir novamente a geração já servida em memória.

IZ. `changed=false` no upstream e `persisted=true` local são dimensões independentes. O plano V27
    separa os booleans, mas ainda não torna obrigatória a convergência posterior do estado dirty.

JA. O bootstrap V27 é especificado no source TypeScript, porém produção executa CommonJS emitido em
    `dist/server/server.js`. Um refactor pode passar o source scanner e ainda gerar/importar runtime graph
    cedo demais no artifact compilado ou por um entrypoint alternativo.

JB. Há múltiplas portas de entrada operacionais (compiled production, TS/dev, Docker entrypoint e comandos
    de CI/build). Um único "entrypoint real" não basta se qualquer caminho puder bypassar hydration/order.

JC. O Docker HEALTHCHECK atual consulta `/health/live`; liveness prova processo/listener, não readiness.
    A semântica V27 de readiness é inútil para rollout se router/fleet admission considerar a replica apta
    apenas porque o healthcheck de liveness ficou verde.

JD. O snapshot IMDb é potencialmente INSTANCE_LOCAL, enquanto `maintenance:last_imdb_ratings_update` é
    Redis compartilhado. Uma replica pode exibir como seu um sucesso produzido por outra replica.

JE. O comando manual/maintenance de ratings, quando executado contra uma replica instance-local, não
    implica que as demais replicas foram atualizadas. "force update completed" precisa de scope explícito.

JF. HEAD é uma otimização de validator. 405/501/proxy incompatível não deve tornar GET impossível; por
    outro lado 429/5xx não autorizam blind GET que agrave rate limit. A policy precisa ser por failure class.

JG. HEAD/304/ETag-match só podem evitar fetch quando existe local source correspondente válida. Eles nunca
    liquidam automaticamente durability debt nem autorizam cleanup legado sem durable-generation proof.

JH. O documento preserva centenas de seções históricas com precedência textual por domínio. Sem um índice
    mecânico de autoridade e uma matriz issue→invariant→code→test→evidence, um agente de implementação pode
    escolher uma instrução antiga superseded apesar de o plano conter a regra nova em outra seção.
```

Esses blockers não mudam o objetivo da #742. Eles tornam o plano **implementável sem ambiguidade em upgrade, build e deployment reais**.

---

# 587. Sétimo universo — `RuntimeEntrypointOccurrenceManifest`

A V28 eleva a reconciliação de seis para **sete universos autoritativos**.

Além de async/resources/network/frontend/artifacts/runtime-settings, gerar:

```ts
interface RuntimeEntrypointOccurrence {
  occurrenceId: string;
  artifact: string;
  mode:
    | 'PROD_CONTAINER'
    | 'PROD_NODE'
    | 'DEV_TS'
    | 'DEV_JS'
    | 'CI_BUILD'
    | 'CI_TEST'
    | 'OTHER';

  sourceEntrypoint: string | null;
  emittedEntrypoint: string | null;
  command: string;

  nodeSelector: string | null;
  moduleSystem: 'COMMONJS' | 'ESM' | 'MIXED' | 'UNKNOWN';

  settingsHydrationBoundary: string | null;
  firstRuntimeGraphImport: string | null;
  outboundDispatcherBoundary: string | null;

  livenessProbe: string | null;
  readinessProbe: string | null;
  trafficAdmissionOwner: string | null;

  dataRootMountContract: string | null;
  artifactScope: 'INSTANCE_LOCAL' | 'SHARED' | 'UNKNOWN';

  parity:
    | 'PROVEN'
    | 'INTENTIONALLY_DIFFERENT'
    | 'UNPROVEN';

  disposition:
    | 'COVERED'
    | 'NO_RUNTIME_EFFECT'
    | 'TEST_ONLY'
    | 'UNSUPPORTED';
}
```

Ocorrências mínimas do snapshot:

```text
package.json start:backend
package.json start:backend:ts
package.json dev:server / dev:server:ts
Dockerfile
Docker HEALTHCHECK
docker/entrypoint.sh
tsconfig.backend.json
.github/workflows/* que selecionam Node/build/runtime
qualquer compose/documented production command que seja release contract
```

Regra central:

```text
runtime entry/probe/deployment occurrence sem classificação
→ CI FAIL
```

Mudança no source entrypoint só é considerada fechada quando:

```text
source order proven
AND
emitted order proven
AND
production command proven
AND
traffic admission proven
```

---

# 588. Legacy Redis Coherent-Snapshot / Old-Writer Gate

## 588.1. Fato histórico que muda a migration policy

O writer v3.1.0 não atualiza o hash in-place durante todo o download. Ele faz:

```text
write temp hash
→ RENAME temp hash para imdb:ratings
→ SET imdb-ratings-etag
```

Isso é bom para readers antigos, mas cria dois boundaries para o importer novo:

```text
HSCAN é multi-command
RENAME pode acontecer entre commands
ETag é cross-key e não muda atomicamente com o RENAME
```

Portanto:

```text
HSCAN bounded
≠
coherent legacy snapshot
```

## 588.2. Policy preferida para mixed fleet

Enquanto existir **legacy writer live conhecido**:

```text
legacy Redis pode servir como fallback de lookup
MAS
não promover um HSCAN multi-batch a durable file-v2 authoritative snapshot
```

Preferir uma destas rotas:

```text
A. baixar/validar o dataset oficial para construir file-v2
ou
B. aguardar homogeneous/fleet proof de que nenhum writer legado pode trocar o hash
```

Isso separa:

```text
legacy read availability
≠
legacy bulk-import authority
```

## 588.3. Import depois de old-writer closure

Quando não existe writer legado capaz de publicar nova geração:

```text
read etagBefore
read hlenBefore
HSCAN bounded all batches
strict parse + deterministic dedupe
compute candidate digest/count
read hlenAfter
read etagAfter
```

Aceitar candidate somente quando a policy provar coerência suficiente:

```text
no legacy writer
AND
hash permaneceu presente
AND
bounds válidos
AND
count/digest invariants válidos
AND
(etagBefore == etagAfter OU explicit NO_ETAG provenance policy)
AND
hlenBefore == hlenAfter
```

Esses checks não transformam HSCAN em transação; o **no-legacy-writer proof** é o boundary principal.

## 588.4. ETag/hash lag window

Estados possíveis do writer antigo:

```text
old hash + old ETag
new hash + old ETag   ← janela real
new hash + new ETag
```

O importer nunca deve tratar:

```text
new hash + old ETag
```

como sourceGeneration comprovada.

Se detectar incoerência:

```text
continue serving legacy fallback
no cleanup
no promote
network revalidation ou retry após writer closure
```

## 588.5. Cleanup

Legacy cleanup continua exigindo V27 + agora:

```text
no old readers
AND
no old writers
AND
no legacy bulk-import in flight
AND
durableGeneration proof
```

---

# 589. IMDb Durability-Debt / Persistence-Convergence Gate

## 589.1. Estado explícito

Adicionar conceito equivalente:

```ts
interface RatingsDurabilityState {
  memoryGeneration: string | null;
  durableGeneration: string | null;
  memoryEtag: string | null;
  durableEtag: string | null;
  dirty: boolean;
  lastPersistError: string | null;
  nextPersistRetryAt: number | null;
}
```

O generation token exato pode reutilizar digest/source generation já definido.

Invariante:

```text
dirty === (memoryGeneration != durableGeneration)
```

com policy explícita para source inicial sem artifact.

## 589.2. ETag-match NÃO quita durability debt

Caso:

```text
GET geração G
→ install memory G
→ persist G falha ENOSPC
→ currentEtag = E
→ próxima manutenção HEAD retorna E
```

Resultado obrigatório:

```text
upstream changed = false
MAS
local dirty = true
→ retry durable commit de G
```

Nunca:

```text
etag-match
→ success terminal
```

quando `memoryGeneration != durableGeneration`.

## 589.3. Retry de persistência sem redownload

Se a candidate table validada permanece instalada:

```text
retry local snapshot commit
```

não exige baixar o dataset novamente.

Policy:

```text
bounded exponential/backoff apropriado para storage failure
cap/jitter se necessário
capability recheck quando útil
no tight loop
no network amplification
```

## 589.4. Reinício antes da convergência

Se processo morre com:

```text
memoryGeneration=G2
durableGeneration=G1
dirty=true
```

restart carrega G1.

Isso é permitido porque G2 não era durable, mas:

```text
metrics/log/dashboard precisam ter declarado a dívida
legacy cleanup não pode ter destruído fallback exigido
next upstream check precisa convergir novamente para G2/G3
```

## 589.5. Shutdown

Durante graceful shutdown:

```text
dirty artifact
→ bounded final persist attempt se ainda houver commit authority e deadline
OU
→ leftover explícito `dirty-not-flushed`
```

Não prolongar shutdown indefinidamente.

## 589.6. Cleanup authority

```text
legacy Redis cleanup eligibility
→ depende de durableGeneration, não apenas memoryGeneration/currentEtag
```

## 589.7. Markers

Separar no mínimo semanticamente:

```text
last_memory_install
last_snapshot_commit
last_upstream_unchanged_check
last_persist_failure
```

`upstream unchanged` nunca é sinônimo de `snapshot durable`.

---

# 590. HTTP Validator / Fetch Authority Gate

## 590.1. GET é source authority; HEAD é otimização

O updater não pode depender da existência universal de HEAD.

Classificação recomendada:

```text
HEAD 2xx + same validator
→ upstream unchanged candidate
→ ainda executar durability convergence local se dirty

HEAD 405/501
→ validator probe unsupported
→ fallback para GET policy

HEAD 429
→ respeitar Retry-After/backoff
→ não blind-GET imediatamente

HEAD 5xx/network failure
→ failure class explícita
→ GET fallback somente se policy justificar, sem duplicar tempestade
```

## 590.2. Preferência opcional: conditional GET

Uma implementação mais simples pode substituir HEAD+GET por:

```text
GET If-None-Match: <validator>
```

Então:

```text
304 + matching local valid source
→ unchanged

200
→ parse/validate/install/persist policy normal
```

Não é obrigatório trocar a estratégia se HEAD ficar corretamente classificado.

## 590.3. Validator só vale com local source correspondente

```text
304 / same ETag
+
no valid memory/durable candidate correspondente
→ NÃO pode responder "cache valid" por autoridade vazia
```

Precisa full GET/recovery conforme policy.

## 590.4. HEAD/GET race

Se:

```text
HEAD ETag=A
GET body ETag=B
```

B/body validado é a source efetivamente instalada.

Nunca atribuir A à body B.

## 590.5. Lifecycle permanece cumulativo

Todos os contracts V26 continuam:

```text
status validation
body terminal proof
AbortSignal/deadline
stream/gunzip/readline ownership
resource bounds
retry generation fence
```

---

# 591. Source→Emitted Bootstrap / Entrypoint Parity Gate

## 591.1. Production truth

No snapshot:

```text
TypeScript source: addon/server.ts
build:            tsc -p tsconfig.backend.json
module output:    CommonJS
production:       node dist/server/server.js
Docker entry:     docker/entrypoint.sh → node dist/server/server.js
```

Logo:

```text
source import graph proof
```

é necessário, mas não suficiente.

## 591.2. Emitted bootstrap proof

CI deve executar uma prova sobre o artifact realmente compilado.

Exemplos aceitáveis:

```text
A. static emitted graph scanner
B. integration sentinel modules que registram evaluation order
C. child-process boot fixture com DB-backed override conhecido
D. combinação A+B/C
```

O teste precisa provar no `dist`:

```text
bootstrap-safe database/settings modules primeiro
→ initializeSettings concluído
→ effective process/runtime settings aplicados
→ proxy/global dispatcher configurado
→ runtime graph consumers avaliados
→ resources/schedulers criados
```

## 591.3. Entrypoint matrix

Todos os caminhos suportados devem convergir para o mesmo contract:

```text
npm start / start:backend
start:backend:ts
dev:server:ts
Docker entrypoint
CI smoke boot
qualquer novo production command
```

Se um path intencionalmente divergir:

```text
INTENTIONALLY_DIFFERENT
+
reason
+
separate test
```

## 591.4. No source-only green

```text
source scanner PASS
+
emitted/runtime fixture FAIL
=
CI FAIL
```

## 591.5. Artifact fingerprint

Evidence bundle registra:

```text
source HEAD/tree
package-lock digest
tsconfig.backend digest
Dockerfile digest
entrypoint.sh digest
emitted server entry digest
Node runtime identity
```

Isso fecha a cadeia:

```text
source → compiler config → emitted artifact → container command
```

---

# 592. Deployment Liveness / Readiness / Traffic-Admission Gate

## 592.1. Semânticas separadas

```text
/health/live
→ processo/listener vivo

/health/ready
→ required startup + live dependency readiness policy

traffic admission
→ decisão do router/orchestrator de enviar requests de negócio
```

Nunca colapsar os três.

## 592.2. Estado atual

O Docker HEALTHCHECK atual usa:

```text
/health/live
```

Enquanto `index.ts` possui readiness gate que devolve 503 para rotas de negócio durante startup.

Isso protege correctness dentro do app, mas não prova que um rollout/router só admite a replica depois de ready.

## 592.3. Deployment contract obrigatório

Para cada deployment suportado, documentar/testar uma destas formas:

```text
A. container health = readiness (/health/ready)
```

ou:

```text
B. container liveness = /health/live
   + router/orchestrator readiness check separado = /health/ready
```

ou mecanismo equivalente que prove a mesma propriedade.

## 592.4. Fleet admission

Uma replica nova NÃO conta como capability-ready/homogeneous para gates destrutivos apenas porque:

```text
process iniciou
listener bindou
/health/live = 200
```

Ela entra na frota autoritativa somente após:

```text
required settings hydrated
required storage/resource init complete
readiness gate satisfied conforme policy
capability heartbeat publicado depois desse boundary
```

## 592.5. Bootstrap mais longo

Se o split V27 mover mais trabalho antes do listener:

```text
Docker start-period / orchestrator startup grace
```

precisa ser compatível.

Alternativamente, um minimal bootstrap health listener pode existir, desde que:

```text
liveness != readiness
business traffic continua bloqueado
runtime graph não é importado cedo para servir health
```

## 592.6. Degradable components

`imdbRatings` continua degradable conforme V27.

Portanto:

```text
ratings DEGRADED
não implica automaticamente matar/restartar a replica
```

Readiness global segue a política de component kind; o dashboard precisa mostrar o componente degradado separadamente.

---

# 593. Replica-Scope Observability / Maintenance Control-Plane Gate

## 593.1. State scope é parte do dado

Para qualquer indicador de ratings:

```text
INSTANCE_LOCAL
SHARED_FLEET
AGGREGATED_FLEET
```

precisa ser conhecido.

Snapshot em disco instance-local não pode herdar automaticamente o scope de um marker Redis compartilhado.

## 593.2. Marker compartilhado atual

`maintenance:last_imdb_ratings_update` em Redis pode ser escrito por replica A e lido por replica B.

Se snapshots são instance-local:

```text
B não pode apresentar esse timestamp como "meu snapshot foi atualizado".
```

Opções:

```text
- marker instance-scoped;
- status local obtido da memória/artifact da própria replica;
- aggregator explícito que mostra fleet summary e per-replica states;
- shared artifact/leader policy que torne o marker realmente shared-authoritative.
```

## 593.3. Manual force/update scope

Endpoint/ação manual precisa declarar:

```text
LOCAL_REPLICA
ou
FLEET_FANOUT
ou
LEADER_SHARED_ARTIFACT
```

Se LOCAL_REPLICA:

```text
UI/API response diz local
não afirma "todas as replicas atualizadas"
```

Se FLEET_FANOUT:

```text
per-replica result
partial failure semantics
idempotency/request id
bounded timeout
no double force storm
```

## 593.4. Cleanup scope

Legacy cleanup eligibility continua fleet-scoped.

Não usar um marker local de snapshot commit como prova de que:

```text
all replicas migrated
```

## 593.5. Cardinality

Prometheus não precisa receber UUID efêmero de toda replica como label.

Preferir:

```text
local gauges por process
fleet counts agregados
instance identity em structured logs/status payload quando necessário
```

---

# 594. Normative Authority + Requirement Traceability Gate

A V28 mantém o histórico porque ele preserva decisões e evidência, mas um documento com 33k+ linhas precisa ser executável por humano e agente sem escolher acidentalmente texto superseded.

## 594.1. `NormativeAuthorityIndex`

Gerar artifact versionado, por exemplo:

```yaml
release-visibility:
  authority: [2, 3, 4, 25-...]
  latest_overrides: [585-600]

runtime-settings-bootstrap:
  authority: [571, 572, 591]

imdb-ratings-migration:
  authority: [548-568, 573-579, 588-593]
```

O formato exato não é normativo.

Cada record contém:

```text
domain
authoritativeSections
supersededSections
MUST/SHOULD/OPTION/DECISION status
code paths
manifest/gate owner
test ids
evidence outputs
```

## 594.2. Conflict linter

CI/document tooling precisa detectar:

```text
dois MUST ativos e incompatíveis no mesmo domain
sem precedence record
→ FAIL
```

Não é necessário NLP perfeito; pode ser um registry explícito mantido junto ao plano/harness.

## 594.3. `Issue742TraceabilityMatrix`

Mapear cada pedido observável da issue:

```text
regional Hide Unreleased Movies
Digital/Physical/TV 4|5|6
configurable release region
Worldwide default/fallback
regional TMDB catalog inheritance quando aplicável
backward compatibility
```

para:

```text
requirement id
invariant
effective config rule
backend code path
frontend code path
test ids
metric/evidence
rollout/rollback check
```

## 594.4. No orphan requirement / no orphan implementation

Antes do merge:

```text
issue requirement sem test/evidence → FAIL
changed correctness code sem requirement/gate/disposition → FAIL
```

## 594.5. Handoff rule

Agente de implementação deve começar pelo:

```text
NormativeAuthorityIndex
+
Issue742TraceabilityMatrix
+
current snapshot fingerprint
```

Não por uma busca livre de qualquer ocorrência histórica de uma palavra.

---

# 595. Evidence Bundle / Generated Proof Gate V28

O evidence bundle já exigido nas versões anteriores passa a ter um manifest raiz único:

```ts
interface AuditEvidenceBundleV28 {
  snapshot: {
    head: string;
    tree: string;
    packageLockDigest: string;
    runtimeFingerprint: string;
  };

  universes: {
    async: string;
    processResources: string;
    networkCallers: string;
    frontendEffects: string;
    persistentArtifacts: string;
    runtimeSettings: string;
    runtimeEntrypoints: string;
  };

  authorityIndex: string;
  issueTraceability: string;
  testReport: string;
  buildReport: string;
  emittedBootstrapProof: string;
  migrationDrill: string;
  rolloutDrill: string;
  rollbackDrill: string;
  shutdownDrill: string;
}
```

Cada path/digest acima precisa apontar para artifact produzido pelo merge HEAD.

Regra:

```text
"FINAL" claim
+
missing evidence artifact
=
claim inválida
```

O bundle não substitui testes; ele prova **qual snapshot e qual execução** sustentam a claim.

---

# 596. Observabilidade V28

Adicionar cumulativamente:

```text
imdb_ratings_durability_state{state=clean|dirty|no-durable}
imdb_ratings_persist_retry_total{result,reason}
imdb_ratings_persist_debt_seconds
imdb_ratings_memory_generation_changed_total
imdb_ratings_durable_generation_changed_total

imdb_ratings_legacy_import_consistency_total{result,reason}
imdb_ratings_legacy_writer_present
imdb_ratings_legacy_import_deferred_total{reason}

imdb_ratings_validator_probe_total{method,result}
imdb_ratings_validator_fallback_total{reason}

runtime_entrypoint_parity_violation_total{mode}
deployment_readiness_admission_mismatch_total{deployment}

imdb_ratings_maintenance_scope_info{scope=local|fleet|leader}
imdb_ratings_manual_update_total{scope,result}

audit_authority_conflict_total{domain}
audit_traceability_orphan_total{kind}
```

Cardinality rules:

```text
não usar ETag/digest/path/user/replica UUID como metric label não bounded
reason/mode/scope/domain = enum fechado
per-replica debugging detalhado → structured status/log, não cardinality infinita
```

Dashboard/status precisa distinguir simultaneamente:

```text
memory generation
local durable generation
dirty persistence
upstream validator status
legacy fallback/import state
local vs fleet maintenance scope
readiness component state
```

---

# 597. Matriz de testes adicional V28 — casos 751–800

Adicionar cumulativamente aos 750 casos V8→V27:

```text
751. snapshot fingerprint V28
     → dev HEAD == d270a3a7f3b6e41304d9f91045b1d481311c3c96 e tree == b4db5931c47035862fac075ac01ec02fe1e621c0
       OU Rebase/Delta/sete Occurrence gates rerodados.

752. RuntimeEntrypointOccurrenceManifest
     → todos os entrypoints/build/probes/deployment artifacts suportados classificados; zero unmatched.

753. legacy HSCAN começa em geração A e v3.1.0 executa RENAME para geração B no meio
     → candidate NÃO é promovido; fallback continua disponível; zero cleanup.

754. legacy writer troca hash antes do primeiro HSCAN e depois fica quiescent
     → import aceita apenas após old-writer closure/coherence proof.

755. RENAME mid-scan preserva HLEN por coincidência mas ETag muda
     → candidate rejeitado/deferred; HLEN sozinho não prova coerência.

756. new hash publicado + old ETag ainda visível
     → importer detecta/assume janela incoerente; no promote/no cleanup.

757. no legacy writer + stable ETag/HLEN + valid bounded scan
     → candidate determinístico pode virar table/snapshot conforme migration policy.

758. HSCAN retorna duplicate field/revisit permitido pelo cursor semantics
     → dedupe determinístico; count/digest final estável; nenhuma dupla linha publicada.

759. mixed fleet com old redis-v1 writer vivo
     → legacy lookup fallback serve, mas bulk HSCAN promotion é deferred ou substituído por network build.

760. último legacy writer sai da fleet
     → somente após capability TTL/fleet proof a bulk migration pode adquirir authority.

761. GET instala memory G2 e snapshot write falha
     → durabilityState dirty; durableGeneration continua G1; serving não mente sobre persistência.

762. ciclo seguinte recebe HEAD/validator unchanged para G2 enquanto dirty
     → retry local persist de G2 ocorre; ETag-match não encerra a operação como fully durable.

763. filesystem recupera após failure
     → persist retry converge durableGeneration para G2 sem redownload obrigatório.

764. ENOSPC persiste por múltiplos ciclos
     → bounded storage backoff; sem tight loop e sem download repetido apenas para tentar gravar o mesmo G2.

765. shutdown com dirty G2
     → bounded final flush OU leftover dirty-not-flushed explícito; shutdown não trava indefinidamente.

766. legacy cleanup enquanto memory=G2/durable=G1
     → proibido, mesmo que currentEtag corresponda a G2.

767. markers memory install / snapshot commit / upstream unchanged
     → timestamps/semantics independentes e coerentes.

768. crash/restart antes de dirty G2 persistir
     → G1 durable carrega; sistema revalida/converge sem afirmar que G2 era durable.

769. manual force update memory success + persist failure
     → API/UI retorna degraded persistence, não success durable genérico.

770. validator unchanged + dirty state + legacy source
     → zero destructive cleanup até durable convergence.

771. HEAD retorna 405
     → classificado unsupported; GET fallback executa conforme policy; updater continua funcional.

772. HEAD retorna 501
     → mesmo contract de unsupported-method, sem transformar em outage permanente.

773. HEAD retorna 429 + Retry-After
     → backoff respeitado; nenhum blind GET imediato que duplique pressão.

774. HEAD retorna 500/503
     → failure class observável; fallback GET segue policy explícita, sem falso unchanged.

775. same ETag/304 sem local memory/durable source correspondente
     → validator não é autoridade vazia; full recovery fetch é exigido.

776. conditional GET 304 + local valid clean generation
     → sem parse/install; status unchanged válido.

777. conditional GET 304 + local dirty generation
     → local persistence convergence continua antes de status fully healthy.

778. HEAD observa ETag A e GET devolve body/ETag B
     → B é a provenance instalada; A não contamina snapshot metadata.

779. abort entre HEAD fallback e GET
     → ambos os request/body owners terminalizam; nenhum retry/commit pós-shutdown indevido.

780. npm start / start:backend
     → executa o bootstrap autoritativo compilado, sem bypass.

781. start:backend:ts / dev TS
     → mesma hydration ordering sem depender de comportamento exclusivo do dist.

782. Docker entrypoint
     → termina em exatamente um supported production bootstrap path.

783. novo script/command aponta direto para serverRuntime e bypassa bootstrap
     → RuntimeEntrypointOccurrence Gate falha CI.

784. emitted CommonJS artifact
     → DB-overridable consumer não é required/evaluated antes do hydration boundary.

785. source import-order scanner PASS mas emitted-order sentinel FAIL
     → build bloqueado; source-only proof não basta.

786. Docker smoke boot com DB IMDB_RATINGS_UPDATE_INTERVAL_HOURS=12
     → compiled runtime realmente agenda 12h após um restart único.

787. built image com proxy DB override
     → global dispatcher configurado depois da hydration e antes do primeiro outbound runtime client.

788. source/build fingerprints divergentes do evidence bundle
     → FINAL claim bloqueada.

789. durante startup: /health/live=200 e /health/ready=503
     → comportamento reconhecido como liveness-only; traffic admission continua fechado.

790. router/fleet tenta admitir replica apenas por /health/live
     → Deployment Admission Gate falha.

791. /health/ready passa conforme required dependency policy
     → somente então replica entra em traffic/capability admission.

792. initializeSettings falha após listener/liveness disponível
     → business routes continuam 503/bloqueadas; readiness nunca vira 200 por engano.

793. imdbRatings degradable-no-ratings
     → component mostra DEGRADED; global readiness segue component-kind policy sem esconder a degradação.

794. bootstrap split aumenta startup time além do health start grace fixture
     → deployment config é ajustada ou minimal health strategy comprovada; sem restart loop silencioso.

795. capability heartbeat/fleet homogeneous marker antes de readiness
     → rejeitado; heartbeat autoritativo só nasce depois do admission boundary.

796. replica A possui durable G2 e replica B possui durable G1 em instance-local mode
     → status local de B não usa shared marker de A para afirmar G2.

797. Redis shared marker atualizado por A
     → dashboard/status em B distingue shared fleet event de local durable commit.

798. manual force endpoint em instance-local mode
     → response declara LOCAL_REPLICA ou executa fanout/leader contract; nunca afirma fleet update sem prova.

799. Issue742TraceabilityMatrix
     → cada requisito observável da issue possui invariant + code path + test ids + evidence; zero orphan requirement.

800. combined V28 proof
     → 7 occurrence universes zerados/classificados, authority index sem conflito ativo, cases 1–800 verdes,
       source→emitted→container bootstrap parity provada, HSCAN não mistura gerações, durability debt converge,
       readiness controla admission e shutdown termina sem owner/dirty state não classificado.
```

---

# 598. Definition of Done V28

A implementação da #742 só pode sustentar a claim máxima V28 quando, cumulativamente ao DoD V8→V27:

```text
[ ] dev HEAD/tree continuam no snapshot V28 ou Rebase/Delta/sete Occurrence gates foram rerodados
[ ] issue #742 state/comments foram rechecados no merge HEAD

[ ] sete universos autoritativos estão materializados:
    async
    process resources
    network callers
    frontend effects
    persistent artifacts
    runtime settings
    runtime entrypoints/deployment

[ ] RuntimeEntrypointOccurrenceManifest possui zero entry/probe/deployment occurrence não classificada
[ ] todos os production/dev/CI entrypoints suportados convergem para o bootstrap contract
[ ] source ordering e emitted CommonJS ordering passam separadamente
[ ] Docker/production smoke fixture prova DB override efetivo no runtime compilado

[ ] HSCAN legado nunca é tratado como snapshot isolado sob legacy writer vivo
[ ] mixed fleet distingue legacy reader de legacy writer capability
[ ] ETag/hash cross-key lag window não autoriza promote/cleanup
[ ] bulk legacy import só publica com coherent-source/fleet proof

[ ] memoryGeneration e durableGeneration são autoridades distintas
[ ] persist failure cria durability debt observável
[ ] ETag/304 unchanged não encerra durability debt
[ ] persistence retry converge sem redownload desnecessário
[ ] shutdown/cleanup consultam durableGeneration, não só currentEtag/memory state

[ ] HEAD é otimização, não single point of availability
[ ] 405/501/429/5xx possuem policies distintas e testadas
[ ] 304/same ETag exige local source correspondente válida
[ ] HEAD→GET validator/provenance não mistura gerações

[ ] /health/live e /health/ready possuem contratos separados
[ ] traffic/fleet admission consome readiness ou mecanismo equivalente comprovado
[ ] liveness-only não torna nova replica eligible para destructive fleet gates
[ ] startup grace/healthcheck continua compatível depois do bootstrap split

[ ] local durable status nunca é inferido de marker shared escrito por outra replica
[ ] manual ratings update declara LOCAL/FLEET/LEADER scope
[ ] fleet cleanup não usa local marker como prova global

[ ] NormativeAuthorityIndex gerado resolve domínios/superseded sections
[ ] Issue742TraceabilityMatrix possui zero requirement órfão
[ ] correctness change sem requirement/gate/disposition falha o guard
[ ] evidence bundle V28 aponta para artifacts produzidos pelo merge HEAD

[ ] casos 751–800 passam
[ ] casos 1–750 continuam passando
[ ] backend/frontend build + lint + generated scanners + emitted bootstrap proof passam
[ ] upgrade/migration/rollback/mixed-reader+writer fixtures passam
[ ] persistent/dirty/recovery storage fixtures passam
[ ] deployment readiness/admission fixtures passam
[ ] shutdown stress termina com sete universos reconciliados
```

---

# 599. Ordem recomendada de implementação V28

Refinar a V27 assim:

```text
PR 0A — snapshot + authority/traceability + sete manifests
        - manter os seis manifests V27
        - adicionar RuntimeEntrypointOccurrenceManifest
        - gerar NormativeAuthorityIndex
        - gerar Issue742TraceabilityMatrix
        - root EvidenceBundle manifest

PR 0B — bootstrap/settings + source→emitted/runtime parity
        - two-stage bootstrap ou refresh hooks
        - DB settings antes de consumers
        - proxy/global dispatcher ordering
        - build emitted-order sentinel
        - todos os entrypoints convergentes
        - liveness/readiness/admission contract

PR 0C — ratings migration + durability convergence
        - legacy lookup fallback
        - old-reader/old-writer capability distinction
        - coherent legacy bulk-import policy
        - cross-store reconciliation
        - memoryGeneration/durableGeneration + dirty persistence
        - persist retry without redownload
        - HEAD/conditional-fetch validator policy
        - replica-scope markers/manual control plane
        - fleet-safe cleanup + truthful readiness
        - data-root/schema/resource gates V27

PR 1  — config revision/storage migration + ConfigCache fencing

PR 2  — Release Evidence V2 + Worldwide golden master + regional evaluator

PR 3  — CanonicalFilterContext/OperationContext + catalog/search integration

PR 4  — filtered pagination/cursors/source identity/freshness

PR 5  — Discover provenance/builder/import/edit-save/preview parity

PR 6  — Jellyfin/in-process/warmer/merged/custom closure

PR 7  — process resource + dependency-I/O + artifact/storage/shutdown closure restante

PR 8  — frontend release-region UI + frontend effect closure

PR 9  — full 1–800 suite + migration/load/concurrency/crash/shutdown/mixed-fleet
        + emitted/container smoke + readiness/admission rollout + rollback drill
```

Dependência:

```text
0A
↓
0B
↓
0C
↓
1
↓
2/3/4/5/6
↓
7/8
↓
9
```

Motivo:

```text
primeiro provar o runtime que realmente será executado,
depois tornar migration/durability seguros,
e só então construir e expor a feature regional.
```

---

# 600. Contrato de handoff para Codex/implementador

Para reduzir interpretação livre, o handoff deste plano deve começar com este contrato:

```text
1. verificar HEAD/tree exatos;
2. se houver drift, parar a claim e executar todos os delta/occurrence gates aplicáveis;
3. ler NormativeAuthorityIndex antes das seções históricas;
4. usar Issue742TraceabilityMatrix como acceptance contract;
5. implementar PR 0A → 0B → 0C antes da feature regional;
6. não remover compatibility path/legacy storage antes do gate correspondente ficar verde;
7. não marcar teste como "simulado" quando o DoD exige integration/process/container fixture;
8. produzir evidence bundle no merge HEAD;
9. reportar explicitamente qualquer requisito não implementado, teste não executado ou upstream não verificável;
10. não declarar FINAL apenas por build/lint verde.
```

Output esperado de cada PR:

```text
changed files
requirements satisfeitos
gates afetados
tests executados + resultado
manifests regenerados
migrations introduzidas
rollout impact
rollback impact
known residuals
```

Regra para Codex:

> Texto histórico superseded serve como rationale/evidence; implementação segue a authority mais recente do domínio.

---

# 601. Resultado final da auditoria V28

A V27 já fechava corretamente o núcleo funcional da #742 e a maior parte dos boundaries de lifecycle, settings,
persistent artifacts e migration. A V28 não reescreve esse desenho. Ela fecha os **últimos boundaries operacionais
que ainda podiam transformar uma especificação correta em um rollout incorreto**.

Ajustes V28:

```text
+ snapshot d270a3a / tree b4db5931 revalidado novamente, sem drift
+ sétimo universo: runtimeEntrypoint/deployment occurrences
+ legacy HSCAN coerente: old writer RENAME não pode produzir mixed-generation snapshot
+ distinção old reader vs old writer na fleet
+ ETag/hash lag window formalizada
+ durability debt memoryGeneration != durableGeneration
+ persistence convergence mesmo quando upstream está unchanged
+ ETag/304 não substitui durable proof
+ HEAD tratado como optimization com failure-class fallback
+ source TypeScript → emitted CommonJS → Docker entrypoint parity
+ liveness/readiness/traffic-admission closure
+ instance-local snapshot vs shared marker/control-plane scope
+ NormativeAuthorityIndex + Issue742TraceabilityMatrix
+ root evidence bundle para sustentar a claim no merge SHA
+ 50 novos casos, total acumulado 800+ casos
```

Claim defensável V28:

> **Para o snapshot `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree
> `b4db5931c47035862fac075ac01ec02fe1e621c0`, o plano passa a reconciliar sete universos autoritativos
> e fecha a cadeia inteira source→build→runtime→deployment, além de release evidence/policy/pagination,
> lifecycle/resources/network/frontend/artifacts/settings, upgrade cross-store, mixed-version reader/writer,
> durability convergence, readiness/admission e rollback por gates executáveis e evidence artifacts.**

Ainda não afirmar antes da implementação/execução:

```text
- ausência literal de todos os bugs;
- que 800 casos escritos equivalem a 800 casos executados;
- comportamento futuro/imutável de TMDB, IMDb, Redis, filesystem ou proxies;
- performance sem benchmark no hardware/deployment alvo;
- crash durability maior que a garantida pelo filesystem/artifact contract;
- fleet safety sem capability/readiness/admission evidence real;
- cobertura de qualquer commit posterior ao snapshot sem rerun dos gates;
- "100% de precisão" fora do significado rigoroso: cobertura rastreável do snapshot + gates para o que é runtime/external.
```

Conclusão arquitetural V28:

```text
A. manter o núcleo Release Evidence → Canonical Context → Visibility → Filter → Pagination;
B. transformar o plano em spec mecanicamente autoritativa via AuthorityIndex/Traceability;
C. provar bootstrap no artifact compilado e admission no deployment real;
D. impedir HSCAN mixed-generation enquanto writer legado existir;
E. fazer memory success convergir obrigatoriamente para durability ou permanecer explicitamente dirty;
F. só permitir destructive cleanup com durable + fleet + rollback proof;
G. só chamar de FINAL quando os 800+ casos, sete manifests e evidence bundle estiverem verdes no merge HEAD.
```

---
# 602. Reauditoria V29 — Delivery-Control-Plane, Merge-Admission, Multi-Arch, Fatal-Lifecycle & Shutdown-Withdrawal Closure

A V28 já fecha de forma excepcionalmente ampla o domínio funcional da #742, o lifecycle interno, os recursos,
settings bootstrap, cross-store migration, persistent artifacts, emitted bootstrap, readiness/admission e a
traceabilidade normativa. A V29 preserva esse desenho e fecha uma camada adicional que ficou fora da claim:
**a cadeia que transforma um commit correto em um merge/release realmente protegido e reproduzível**, além de
dois boundaries de término do processo que ainda não estavam explicitamente normativos.

## 602.1. Snapshot revalidado

No snapshot desta V29:

```text
dev HEAD = d270a3a7f3b6e41304d9f91045b1d481311c3c96
Tree SHA = b4db5931c47035862fac075ac01ec02fe1e621c0
Issue #742 = open / 0 comments
Release publicada base = v3.1.0 @ 6e83e22ab9de5093f9918a1871157f401feebb03
```

Não houve source drift desde V28.

A revalidação do delivery/control-plane encontrou, porém, fatos que não são congelados apenas pelo Git tree:

```text
- .github/workflows/pr-guard.yml usa pull_request_target somente para intake metadata/API;
- .github/workflows/env-registry-check.yml é hoje o único check de código claramente presente em PR/push;
- docker-release.yml publica linux/amd64 + linux/arm64;
- workflows usam ubuntu-latest e actions/* / docker/* action refs por major tag;
- Dockerfile usa node:24-alpine, também selector móvel;
- docker-release.yml pode ser executado por workflow_call ou workflow_dispatch sobre uma release tag;
- release-please.yml pode acionar docker-release após criação da release;
- a listagem de repository rulesets observável nesta auditoria retornou vazia;
- classic branch-protection não pôde ser provada pela integração usada na auditoria (403), portanto seu estado
  é UNKNOWN, não deve ser inferido como ausente nem como presente.
```

A consequência é importante:

```text
source CI definition != merge enforcement
PR-head green != merge-commit evidence
merge-commit evidence != released-image evidence
Git SHA != complete delivery-control-plane fingerprint
```

## 602.2. Oitavo universo autoritativo

A V29 eleva a reconciliação para **oito universos**:

```text
1. async occurrences
2. process-resource occurrences
3. network-caller occurrences
4. frontend-effect occurrences
5. persistent-artifact occurrences
6. runtime-setting occurrences
7. runtime-entrypoint/deployment occurrences
8. delivery-control-plane occurrences
```

Criar `DeliveryControlPlaneOccurrenceManifest` na seção 604.

## 602.3. Escopo da claim V29

A V29 não transforma configurações externas do GitHub, registry, runner ou orchestrator em fatos presumidos.
Ela transforma esses pontos em evidence/gates explícitos.

Logo:

```text
CODE_COMPLETE
pode existir sem maintainer-level repository settings access;

FINAL_V29
exige prova observável de merge/release admission ou declaração explícita de boundary externo não controlável.
```

Não bloquear a implementação funcional da #742 apenas porque um contributor não possui permissão de admin do
repositório. Bloquear, sim, a **claim máxima** de que falha de CI é mecanicamente impossível de mesclar/publicar
quando essa propriedade não foi provada.

---

# 603. Blockers adicionais V29

Adicionar cumulativamente aos blockers V8→V28:

```text
JI. Um workflow de correctness pode falhar e ainda assim não impedir merge se seu check não for REQUIRED no
    branch/ruleset efetivo. V28 exige guards verdes, mas não fecha a autoridade que transforma status em
    merge-admission.

JJ. Repository rulesets, classic branch protection, Actions policy e permissões organizacionais podem mudar
    sem alterar HEAD/tree. O Git snapshot sozinho não congela o delivery control plane.

JK. V28 exige evidence bundle do merge HEAD, mas não fixa um trigger/post-merge/merge-group contract que
    garanta produzir a evidence para o commit efetivamente integrado, nem impede uma release de consumir um
    commit sem esse bundle.

JL. `ubuntu-latest`, `actions/checkout@v4`, `actions/setup-node@v4`, `docker/*-action@vN` e outros action refs
    por tag são dependências móveis. Seu comportamento/resolved SHA pode mudar sem source drift no projeto.

JM. `docker-release.yml` permite reconstruir uma versão já publicada. Como o Dockerfile usa base móvel e os
    Actions/runners também podem mudar, reconstruir a mesma tag sem policy pode repontar um SemVer imutável
    para bytes/digest diferentes.

JN. O release publica `linux/amd64` e `linux/arm64`, mas V28 não possui um gate explícito que prove bootstrap,
    native dependencies, artifact format e smoke behavior nas duas plataformas publicadas.

JO. `RatingsTable` serializa `Uint32Array` copiando bytes nativos da arquitetura, enquanto o header declara
    versão/magic mas não byte order. amd64 e arm64 atuais são little-endian, porém o formato persistente não
    deve depender implicitamente disso.

JP. O shutdown contract fecha admission interno e resources, mas não exige que `/health/ready` seja retirado
    e que a elegibilidade/capability heartbeat da replica seja revogada **antes** do drain. Um router pode
    continuar escolhendo uma replica que já iniciou teardown.

JQ. O deadline interno de shutdown não está ligado ao stop/termination grace externo. Docker/Kubernetes/systemd
    podem enviar SIGKILL antes de flush/drain terminar, invalidando a expectativa de graceful convergence.

JR. `addon/server.ts` trata `uncaughtException` como fatal, mas o handler explícito de `unhandledRejection`
    apenas loga e continua. Esse listener substitui a segurança de um fail-fast implícito e permite servir após
    um erro assíncrono global cujo estado pode ser desconhecido.

JS. `NormativeAuthorityIndex` é exigido como primeira leitura do handoff, mas ele próprio só passa a existir
    quando PR 0A o gera. Falta um seed mínimo autoritativo para inicializar o próprio generator/linter sem
    depender de interpretação livre do documento inteiro.

JT. Evidence artifacts de CI podem expirar. Um path/digest para artifact que deixou de existir não sustenta
    uma claim histórica reproduzível nem uma reconstrução manual posterior.

JU. O release workflow atual compila a imagem, mas não possui dependência normativa de `AuditEvidenceBundle`
    do tag commit. Build success não equivale a cases/manifests/migration/shutdown evidence green.

JV. O runtime/dependency fingerprint V21/V25 não inclui de forma completa runner image + resolved action SHAs
    + Buildx/QEMU + platform-specific installed native dependency set. Esses componentes podem alterar o
    artifact final sem mudança no package lock.

JW. Um check executado só em `pull_request` não cobre direct push, merge queue nem commit de release; um check
    executado só em `push` não fornece feedback pré-merge. A cobertura de delivery precisa classificar todos
    os ingress paths realmente permitidos.

JX. A V28 possui readiness-admission de startup, mas não fecha a transição inversa READY→DRAINING→TERMINATED
    no control plane externo. Startup safety sem withdrawal safety ainda deixa uma janela operacional.
```

---

# 604. DeliveryControlPlaneOccurrenceManifest — oitavo universo

## 604.1. Objetivo

Inventariar tudo que pode transformar source em status de merge, tag, release ou imagem publicada.

Schema conceitual:

```ts
interface DeliveryControlPlaneOccurrence {
  id: string;
  sourcePath: string | null;
  kind:
    | 'WORKFLOW'
    | 'WORKFLOW_TRIGGER'
    | 'CHECK_STATUS'
    | 'REQUIRED_CHECK_BINDING'
    | 'ACTION_DEPENDENCY'
    | 'RUNNER_SELECTOR'
    | 'RUNTIME_SELECTOR'
    | 'CONTAINER_BASE'
    | 'BUILD_PLATFORM'
    | 'PUBLISH_TARGET'
    | 'TAG_MUTATION'
    | 'REPOSITORY_RULESET'
    | 'CLASSIC_BRANCH_PROTECTION'
    | 'RELEASE_ADMISSION'
    | 'EVIDENCE_RETENTION';

  event?: string;
  refSemantics?: string;
  permissions?: Record<string, string>;
  secretsExposure?: 'NONE' | 'GITHUB_TOKEN_ONLY' | 'OTHER';
  checkoutUntrustedCode?: boolean;

  selector?: string | null;
  resolvedIdentity?: string | null;
  immutable?: boolean | 'UNKNOWN';

  targetBranchOrTag?: string | null;
  platforms?: string[];

  enforcement:
    | 'ENFORCED'
    | 'OBSERVED_NOT_ENFORCED'
    | 'UNKNOWN'
    | 'NOT_APPLICABLE';

  owner:
    | 'SOURCE_REPO'
    | 'REPOSITORY_ADMIN_CONTROL_PLANE'
    | 'GITHUB_HOSTED_RUNNER'
    | 'OCI_REGISTRY'
    | 'EXTERNAL_OPERATOR';

  classification:
    | 'REQUIRED_FOR_PR'
    | 'REQUIRED_FOR_MERGE'
    | 'REQUIRED_FOR_RELEASE'
    | 'METADATA_ONLY'
    | 'OPTIONAL_PREVIEW'
    | 'OUT_OF_SCOPE_WITH_REASON';

  evidence: string[];
}
```

## 604.2. Scanner/source scope

Classificar no mínimo:

```text
.github/workflows/*.yml
Dockerfile
.nvmrc
package.json engines/scripts
release-please-config.json
.release-please-manifest.json
container publish targets/tags
GitHub rulesets/branch-protection evidence quando acessível
```

Scanner de workflow precisa entender, no mínimo:

```text
on.pull_request
on.pull_request_target
on.push
on.merge_group
on.workflow_call
on.workflow_dispatch
permissions
uses
checkout ref
runner
node selector
build platforms
registry/tag mutations
```

## 604.3. Regras de segurança

Preservar V23:

```text
pull_request_target
→ metadata/API only
→ nunca checkout/exec PR head não confiável
→ nunca npm ci/script do fork com token write
```

Correctness code execution:

```text
pull_request
permissions: contents: read
no production secrets
```

Release code execution:

```text
trusted tag/commit only
minimal write permissions
exact commit provenance
```

## 604.4. Zero-occurrence rule

CI falha quando:

```text
workflow novo não classificado
novo `uses:` sem dependency record
publish target/tag mutation sem release policy
novo merge ingress path sem correctness status owner
platform publicada sem smoke/evidence path
ruleset/protection state necessário à claim = UNKNOWN e claim solicitada = FINAL_V29
```

---

# 605. Merge-Admission / Required-Status / Merge-Commit Evidence Gate

## 605.1. Status verde precisa ser autoridade de merge

Criar check estável, por exemplo:

```text
Issue742 / Audit & Regression
```

Ele agrega ou depende de:

```text
build backend
build frontend
lint
node:test suites
8 occurrence manifests
NormativeAuthorityIndex / traceability lint
migration/rollback fixtures
emitted bootstrap proof
shutdown/fatal lifecycle tests relevantes
```

O nome exato pode mudar, mas precisa ser estável se for configurado como required status.

## 605.2. Enforcement evidence

Classificar o branch alvo:

```ts
type MergeEnforcementState =
  | 'REQUIRED_STATUS_PROVEN'
  | 'RULESET_PROVEN'
  | 'CLASSIC_PROTECTION_PROVEN'
  | 'NOT_ENFORCED'
  | 'UNKNOWN';
```

Nesta auditoria:

```text
repository rulesets observáveis = []
classic branch protection = UNKNOWN por falta de permissão de leitura da integração
```

Portanto não afirmar hoje:

```text
"um failing audit check impede merge"
```

sem evidence adicional do maintainer/control plane.

## 605.3. PR head, merge ref e merge commit

Cobrir três identidades diferentes:

```text
PR_HEAD_SHA
PR_MERGE_REF_SHA / merge-group candidate quando aplicável
ACTUAL_MERGE_SHA
```

A evidence final deve apontar para `ACTUAL_MERGE_SHA` ou para uma merge-group candidate que seja provadamente o
commit publicado sem alteração posterior.

## 605.4. Trigger contract

Recommended:

```text
pull_request
→ feedback pré-merge seguro

merge_group
→ obrigatório se merge queue for habilitada

push: dev
→ evidence pós-merge do commit real
```

Direct push permitido ao branch:

```text
→ push audit obrigatório
```

Direct push proibido:

```text
→ ruleset/protection evidence comprova a proibição
```

## 605.5. Base branch drift

Se o branch mudou depois do último PR check:

```text
strict required status / up-to-date requirement
OU
merge-group check
OU
post-merge audit antes de release
```

Nenhum check antigo deve ser usado como evidence do merge commit por semelhança de source branch.

---

# 606. Release-Admission / Immutable-Publication / Evidence-Anchoring Gate

## 606.1. Release precisa consumir evidence do tag commit

Antes de publicar imagem release:

```text
resolve release tag → commit SHA
resolve AuditEvidenceBundleV29 for that exact SHA
verify bundle digests
verify required release-grade gates green
only then build/push
```

Docker build success sozinho não substitui isso.

## 606.2. Manual rebuild de versão publicada

`workflow_dispatch` de release precisa de policy explícita.

Opções válidas:

```text
A. IMMUTABLE_SEMVER
   tag 3.1.0 já existe → rebuild que produziria digest diferente é recusado;

B. REBUILD_REVISION
   publicar 3.1.0-r1 / provenance equivalente sem mover o artifact original;

C. IDENTICAL_REPRODUCIBLE
   republish apenas se manifest digest final for idêntico ao já publicado.
```

Proibido:

```text
mesmo SemVer histórico
→ ambiente/toolchain diferente
→ digest diferente
→ tag silenciosamente repontada
```

## 606.3. Evidence anchor durável

Actions artifact temporário pode ser convenience, não única authority histórica.

Para release FINAL, ancorar no mínimo:

```text
commit SHA
source tree SHA
AuditEvidenceBundle digest
OCI multi-platform manifest digest
per-platform image digests
runtime/delivery fingerprint
```

em um local com lifecycle compatível com a release, por exemplo:

```text
release asset
OCI attestation/annotation
content-addressed evidence store
ou artifact retention explicitamente >= lifecycle suportado
```

Não é obrigatório adotar uma tecnologia específica de signing para a #742. É obrigatório impedir que a prova
histórica dependa exclusivamente de um artifact efêmero já expirado.

## 606.4. Preview/testing

Preview/testing podem ter retention menor e tags móveis, desde que declaradas:

```text
MUTABLE_NON_RELEASE
```

Não reutilizar esse contract para SemVer estável.

---

# 607. CI/Build Dependency Fingerprint Gate

## 607.1. Extensão do runtime fingerprint

Adicionar ao evidence bundle:

```ts
interface DeliveryDependencyFingerprint {
  runnerLabel: string;
  runnerImageIdentity: string | null;

  actions: Array<{
    uses: string;
    requestedRef: string;
    resolvedSha: string | null;
  }>;

  nodeVersion: string;
  npmVersion: string;
  dockerBaseRequested: string;
  dockerBaseDigest: string | null;

  buildxVersion: string | null;
  qemuVersion: string | null;

  platform: string;
  arch: string;
  libc: string | null;
  nodeAbi: string | null;
  installedDependencyDigest: string;
}
```

## 607.2. Floating selector semantics

Selectors como:

```text
ubuntu-latest
node-version: 24
node:24-alpine
actions/checkout@v4
docker/build-push-action@v5
```

não são immutable identities.

Policy mínima válida:

```text
resolver e registrar identity efetiva em cada evidence-producing run
+
rerun relevante quando identity efetiva muda
```

Hardening preferido para release-grade paths:

```text
pin immutable SHA/digest quando operacionalmente aceitável
+
renovação automatizada/revisada
```

## 607.3. Action supply-chain boundary

Mudança do resolved SHA de um action usado pelo audit/release:

```text
→ delivery fingerprint muda
→ não reutilizar evidence antiga como se o executor fosse idêntico
```

Isso é independente de `package-lock.json`.

---

# 608. Multi-Architecture Release Parity Gate

## 608.1. Platforms publicadas são contract

O release atual publica:

```text
linux/amd64
linux/arm64
```

Logo ambos entram no DoD de release.

## 608.2. Per-platform smoke

Para cada platform publicada:

```text
build image
boot compiled dist
load DB/settings fixture
exercise /health/live + /health/ready
run minimal catalog/meta/search smoke
load/write/read ratings snapshot fixture
shutdown gracefully
```

Quando native execution não estiver disponível:

```text
QEMU smoke é aceitável para semantic gate básico
```

mas performance benchmark não deve ser inferido de emulação.

## 608.3. Native dependencies

Registrar actual installed set por plataforma porque package-lock pode conter optional/prebuilt variants.

Testar explicitamente módulos nativos que afetam boot/storage/image processing quando presentes.

## 608.4. Semantic parity != binary equality

amd64 e arm64 images não precisam ter o mesmo binary digest.

Precisam satisfazer:

```text
same application version
same source commit/tree
same config/schema contracts
same observable #742 behavior
same snapshot format contract
same readiness/shutdown semantics
```

---

# 609. Ratings Snapshot Byte-Order / Architecture-Portability Gate

## 609.1. Problema atual

O formato binário usa header explicitamente little-endian em alguns campos, porém arrays `ids` e `votes` são
persistidos copiando bytes de `Uint32Array`.

Isso torna o byte order do payload implícito no host.

Mesmo que os targets publicados hoje sejam little-endian:

```text
persisted format contract
!=
"funciona nas duas arquiteturas atuais por coincidência de endian"
```

## 609.2. Formato canônico

Para próximo format version, preferir:

```text
byteOrder = LITTLE_ENDIAN explícito e normativo
```

Writer:

```text
encode uint32 fields em LE independente do host
```

Reader:

```text
decode LE independente do host
```

Alternativa aceitável:

```text
header contém endian marker
reader rejeita/rebuilda format de byte order não suportado
```

Preferência V29 = canonical LE para portabilidade e fixtures determinísticos.

## 609.3. Compatibility

V1 existente:

```text
aceitar apenas sob policy de architecture/endian compatível comprovada
OU
migrar/rebuildar para V2/V3 canônico
```

Unknown/mismatched byte order:

```text
no crash
no silent reinterpretation
rebuild/recovery
```

## 609.4. Fixtures

Adicionar:

```text
canonical known-bytes fixture
amd64 writer → arm64 reader
arm64 writer → amd64 reader
synthetic byte-swapped payload
unknown endian/version
checksum + endian mismatch
```

---

# 610. Shutdown Readiness-Withdrawal / Fleet-Eligibility Revocation Gate

## 610.1. Nova primeira fase do shutdown

Antes de drenar requests/resources:

```text
READY
→ DRAINING
```

A authority central de lifecycle deve, atomicamente ou na ordem comprovada:

```text
1. marcar process state DRAINING;
2. /health/ready passa a 503 imediatamente;
3. business admission local fecha;
4. fleet/capability heartbeat deixa de anunciar eligibility;
5. manual/background admission novo fecha;
6. então iniciar HTTP drain + cancellation + flush + resource close.
```

## 610.2. Liveness durante drain

`/health/live` não precisa virar 503 imediatamente.

Policy preferida:

```text
live=200 durante bounded graceful drain
ready=503 durante todo DRAINING
process termina ao fim
```

Isso evita que um orchestrator interprete graceful drain como hang e antecipe restart/kill.

Se o deployment exige outra semântica, documentar/testar explicitamente.

## 610.3. Fleet markers

Ao entrar DRAINING:

```text
replica não conta para homogeneous-fleet admission/cleanup proof
```

Heartbeat existente:

```text
revoke explicitamente
OU
deixar TTL curto expirar, mas cleanup gate precisa considerar draining state/propagation window
```

Não usar uma replica em teardown como prova de capability viva.

## 610.4. Request race

Request que chega após withdrawal:

```text
não inicia novo correctness-critical work
```

Request já admitido antes:

```text
drain/cancel policy existente V21–V28
```

---

# 611. External Termination-Grace / Forced-Kill Recovery Gate

## 611.1. Duas autoridades de deadline

Existem:

```text
internalShutdownDeadline
externalTerminationGrace
```

Invariante:

```text
internalShutdownDeadline + safetyMargin < externalTerminationGrace
```

quando o deployment promete graceful completion.

## 611.2. Deployment sources

Classificar por modo:

```text
Docker/Compose stop timeout / stop_grace_period
Kubernetes terminationGracePeriodSeconds + preStop/readiness propagation
systemd TimeoutStopSec
outro orchestrator equivalente
```

Se não existir manifest no repo:

```text
owner = EXTERNAL_OPERATOR
state = UNKNOWN until deployment evidence supplied
```

## 611.3. Forced kill é fault model obrigatório

Mesmo com grace correta, testar:

```text
SIGKILL / abrupt container loss
```

Resultado após restart:

```text
last-known-good durable artifacts carregam
orphan temp tratado
leases expiram/fence protege late ownership
memory-only generation não é inventada como durable
legacy cleanup não deixou sistema sem recovery source
```

## 611.4. Timeout escalation

Ao atingir internal deadline:

```text
registrar unfinished owners
parar novas tentativas
best-effort final telemetry
exit não-zero quando fatal/incomplete policy exigir
```

Não estender indefinidamente até o orchestrator cortar o processo de forma opaca.

---

# 612. Fatal Process Error / Unhandled-Rejection Gate

## 612.1. Regra normativa

Um `unhandledRejection` global não é warning comum.

Com handler explícito instalado, escolher e testar uma policy. Preferência V29:

```text
unhandledRejection
→ log structured fatal event
→ transition READY/BOOTING → DRAINING_FATAL
→ withdraw readiness/admission
→ abort tracked work
→ bounded shutdown
→ process exits code 1
```

Não continuar servindo indefinidamente.

## 612.2. `uncaughtException`

Preservar fail-stop:

```text
log
→ bounded shutdown only
→ no attempt to resume normal serving
→ exit 1
```

O shutdown não deve iniciar novos jobs não essenciais.

## 612.3. Fatal during bootstrap

Se fatal ocorrer antes de readiness:

```text
ready nunca vira 200
capability heartbeat nunca é publicado
listener pode continuar live apenas durante bounded teardown conforme policy
```

## 612.4. Failure inside shutdown

Shutdown fatal handler precisa ser idempotente.

```text
second fatal/signal
→ não cria segunda shutdown sequence
```

Se o próprio shutdown falhar:

```text
internal deadline governa hard exit
```

## 612.5. Detached-work goal continua

Este gate não é desculpa para deixar promises sem owner/catch.

A regra ideal continua:

```text
zero unhandled rejection em operação normal
```

O fatal handler é último containment boundary, não mecanismo de controle cotidiano.

---

# 613. Bootstrap Authority Seed / Generator-Paradox Gate

## 613.1. Problema

V28 corretamente exige:

```text
NormativeAuthorityIndex primeiro
```

mas PR 0A precisa produzir esse index.

Para evitar circularidade, adicionar no próprio plano um seed mínimo que seja suficiente para gerar/validar o
artifact completo.

## 613.2. `BootstrapAuthoritySeedV29`

Seed mínimo normativo:

```yaml
release-visibility-core:
  latest: [2-25, 424-468]

lifecycle-network-resources:
  latest: [469-547]

persistent-artifacts-ratings:
  latest: [548-568, 573-579, 588-590, 609]

runtime-settings-bootstrap:
  latest: [569-572, 591]

runtime-entrypoint-deployment:
  latest: [585-593, 610-612]

normative-traceability:
  latest: [594-601, 613]

delivery-control-plane:
  latest: [602-608, 614-616]
```

O range é um bootstrap map, não substitui o `NormativeAuthorityIndex` detalhado.

## 613.3. Self-hosting rule

Generator:

```text
lê seed
→ gera full index
→ linter verifica que generated index preserva seed authorities
→ generated index passa a ser authority mecânica detalhada
```

Divergência seed vs generated:

```text
FAIL
```

## 613.4. Stable requirement IDs

Além do issue traceability, cada novo MUST V29 recebe IDs estáveis, por exemplo:

```text
DELIVERY-MERGE-001
DELIVERY-RELEASE-001
MULTIARCH-001
SHUTDOWN-WITHDRAW-001
FATAL-001
SNAPSHOT-ENDIAN-001
```

Isso evita que line/section drift quebre a rastreabilidade.

---

# 614. Evidence Bundle V29 / Long-Lived Provenance

Estender V28:

```ts
interface AuditEvidenceBundleV29 extends AuditEvidenceBundleV28 {
  deliveryControlPlaneManifest: string;
  repositoryEnforcementProof: string;
  mergeCommitAudit: string;
  releaseAdmissionProof: string;
  deliveryDependencyFingerprint: string;

  platformEvidence: {
    amd64: string;
    arm64: string;
  };

  ociManifestDigest: string | null;
  perPlatformImageDigests: Record<string, string>;

  shutdownWithdrawalProof: string;
  terminationBudgetProof: string;
  fatalLifecycleProof: string;
  snapshotByteOrderProof: string;

  evidenceAnchor: {
    kind: 'RELEASE_ASSET' | 'OCI_ATTESTATION' | 'CONTENT_ADDRESSED' | 'CI_ARTIFACT';
    locator: string;
    retentionClass: 'RELEASE_LIFETIME' | 'BOUNDED' | 'UNKNOWN';
    digest: string;
  };
}
```

Regra:

```text
FINAL_V29
+
merge SHA mismatch
OU release tag SHA mismatch
OU missing platform evidence
OU missing/expired evidence anchor
OU enforcement state UNKNOWN
=
claim rebaixada, não silenciosamente aceita.
```

---

# 615. Observabilidade e audit status V29

Runtime/app metrics adicionais quando aplicáveis:

```text
process_lifecycle_state{state=booting|ready|draining|draining_fatal}
readiness_withdrawal_total{reason}
fatal_process_event_total{kind=unhandled_rejection|uncaught_exception}
shutdown_forced_escalation_total{reason}
shutdown_unfinished_owner_count{class}
```

Ratings/storage:

```text
imdb_ratings_snapshot_format_info{version,byte_order}
imdb_ratings_snapshot_rebuild_total{reason=endian|version|checksum|corrupt}
```

Delivery evidence não precisa virar Prometheus runtime. Produzir CI/release summary fechado:

```text
repository enforcement state
merge SHA audited
resolved action SHAs
runner identity
base-image digest
platform image digests
OCI manifest digest
evidence anchor/retention
```

Cardinality:

```text
SHA/digest completo em evidence artifact/log estruturado,
não como label Prometheus.
```

---

# 616. Casos adicionais V29 — 801–850

Adicionar aos 800 casos existentes:

```text
801. correctness workflow falha no PR, mas required-status enforcement não é provado
     → implementation pode ser CODE_COMPLETE; FINAL_V29 é bloqueada/UNKNOWN.

802. required check comprovadamente configurado e check falha
     → merge admission nega o commit.

803. PR check verde, base `dev` avança antes do merge
     → strict/merge-group/post-merge policy revalida; evidence antiga não representa merge SHA.

804. direct push para dev ocorre
     → push audit executa para o SHA real ou repository policy prova que direct push é impossível.

805. merge queue habilitada
     → `merge_group` candidate executa o audit exigido antes da fila publicar.

806. release tag aponta para commit sem AuditEvidenceBundleV29
     → docker release não publica release-grade image.

807. evidence bundle existe, mas snapshot.head != release tag commit
     → release admission falha.

808. `actions/checkout@v4` resolve para SHA diferente da execução anterior
     → delivery fingerprint muda; evidence registra nova executor identity.

809. `ubuntu-latest` runner image muda sem repo commit
     → delivery fingerprint muda; release evidence não reutiliza fingerprint antigo.

810. `node:24-alpine` resolve para novo base digest
     → Runtime-Semantics + Delivery Dependency gates rerodam/registram nova base.

811. manual rebuild de 3.1.0 gera OCI digest diferente do original
     → immutable policy recusa ou publica rebuild revision; não reponta silenciosamente SemVer estável.

812. manual rebuild de versão existente produz exatamente o mesmo manifest digest
     → idempotent republish permitido somente pela policy explícita.

813. linux/amd64 image boot smoke
     → compiled entrypoint/settings/readiness/catalog smoke passam.

814. linux/arm64 image boot smoke
     → mesmos contracts sem depender de resultado amd64.

815. optional/native dependency set difere legitimamente por platform
     → fingerprints distintos, semantic tests equivalentes.

816. snapshot canônico produzido no path amd64 é lido pelo arm64 fixture
     → mesmo rows/etag/digest semanticamente.

817. snapshot canônico produzido no path arm64 é lido pelo amd64 fixture
     → mesma semântica.

818. payload synthetic byte-swapped
     → reader rejeita/rebuilda; nunca interpreta silenciosamente IDs/votes incorretos.

819. unknown format/endian marker
     → controlled rebuild, no crash, no false READY data.

820. multi-platform OCI manifest
     → evidence contém manifest digest + ambos platform digests.

821. SIGTERM chega em estado READY
     → /health/ready muda para 503 antes de resource close/drain prolongado.

822. durante graceful drain
     → /health/live segue policy documentada, preferencialmente 200 até bounded exit.

823. nova business request chega depois de DRAINING
     → rejeitada/não inicia novo correctness work.

824. capability/fleet heartbeat estava ativo quando shutdown começa
     → eligibility é revogada ou marcada draining antes de destructive fleet decisions.

825. cleanup gate consulta fleet enquanto replica está DRAINING
     → draining replica não conta como capability saudável.

826. internal shutdown budget = 20s; external grace = 60s
     → contract passa com safety margin explícita.

827. external grace efetiva menor que internal budget
     → Deployment Termination Gate falha; não afirmar graceful shutdown garantido.

828. SIGKILL ocorre com ratings memory G2/durable G1
     → restart carrega G1 e reconverge; G2 não é inventada como durable.

829. SIGKILL ocorre com temp snapshot completo mas rename não concluído
     → recovery policy preserva last-known-good e trata orphan temp.

830. segundo SIGTERM durante shutdown
     → shutdown idempotente; nenhuma segunda sequência/flush concorrente.

831. unhandledRejection após READY
     → fatal event + readiness withdrawal + bounded shutdown + exit 1.

832. unhandledRejection durante bootstrap
     → readiness nunca abre e nenhum fleet heartbeat saudável é publicado.

833. uncaughtException durante dirty snapshot flush
     → bounded fatal shutdown; durable authority não é falsificada.

834. fatal event ocorre enquanto shutdown já está DRAINING
     → escalate/idempotent state; sem recursion infinita.

835. detached promise possui catch/owner correto
     → fatal handler não dispara; normal registry semantics prevalecem.

836. PR 0A começa sem generated NormativeAuthorityIndex
     → BootstrapAuthoritySeedV29 fornece authority mínima suficiente.

837. generated authority index contradiz seed V29
     → generator/linter falha.

838. implementação cita seção histórica superseded como MUST ativo sem precedence record
     → conflict/authority linter falha.

839. Issue742Traceability está completa, mas delivery MUST novo não possui stable requirement id/test
     → no-orphan V29 falha.

840. CI artifact que continha evidence bundle expirou
     → historical FINAL claim perde proof até regeneration/long-lived anchor; não fingir disponibilidade.

841. release asset/OCI evidence anchor possui digest diferente do bundle local
     → release provenance falha.

842. pull_request_target tenta checkout/exec PR head em nova alteração de workflow
     → DeliveryControlPlane gate falha por security boundary.

843. correctness pull_request workflow solicita write permission/production secret sem justification
     → delivery security classification falha.

844. classic branch protection continua inacessível à auditoria
     → enforcement permanece UNKNOWN, nunca convertido em ENFORCED por inferência.

845. maintainer fornece branch-protection/ruleset evidence com required audit check
     → enforcement pode subir para REQUIRED_STATUS_PROVEN.

846. workflow_dispatch de docker release aponta para tag válida mas sem post-merge audit green
     → release admission bloqueia publicação.

847. action major tag é movida upstream entre duas builds da mesma source
     → resolved-action fingerprint detecta diferença; same-source != same-delivery-environment.

848. shutdown withdrawal precisa de propagation delay externo documentado
     → internal drain respeita o deployment contract sem aceitar novos requests durante a janela.

849. deployment não expõe mecanismo capaz de consumir readiness
     → code-level readiness contract passa; deployment FINAL permanece explicitamente UNPROVEN.

850. combined V29 proof
     → oito universos classificados/zerados, cases 1–850 verdes, authority seed/index coerentes,
       actual merge SHA auditado, release admission ligado à evidence, amd64+arm64 parity provada,
       snapshot byte order canônico, readiness retirada antes do drain, fatal rejection fail-stop,
       external termination budget classificado e evidence release-grade ancorada de forma durável.
```

---

# 617. Definition of Done V29

Além de todo DoD V8→V28:

```text
[ ] dev HEAD/tree continuam em d270a3a.../b4db5931... ou todos os delta/eight-universe gates foram rerodados
[ ] issue #742 state/comments rechecados no merge/release SHA

[ ] oito universos autoritativos materializados e reconciliados
[ ] DeliveryControlPlaneOccurrenceManifest possui zero occurrence não classificada

[ ] correctness CI roda em pull_request com permissions mínimas e sem secrets de produção
[ ] pull_request_target continua metadata-only e nunca executa código não confiável
[ ] ingress paths pull_request / push / merge_group / workflow_dispatch são classificados

[ ] repository merge enforcement está PROVEN ou claim máxima é explicitamente rebaixada
[ ] required check possui nome estável e binding observável quando maintainer control plane permitir
[ ] actual merge SHA produz audit/evidence própria

[ ] release tag commit precisa de AuditEvidenceBundleV29 correspondente
[ ] docker release não publica release-grade image sem release-admission proof
[ ] SemVer stable rebuild policy é explícita e não reponta artifact histórico silenciosamente
[ ] long-lived evidence anchor preserva commit/tree/bundle/image digests

[ ] runner/action/base-image/toolchain effective identities entram no delivery fingerprint
[ ] mudança de resolved action/runner/base digest invalida reuse de evidence onde semanticamente relevante

[ ] linux/amd64 build + smoke passam
[ ] linux/arm64 build + smoke passam
[ ] platform-specific native dependency fingerprints são capturados
[ ] OCI manifest + per-platform digests entram na evidence

[ ] ratings snapshot format declara byte order canônico
[ ] cross-arch snapshot fixtures passam
[ ] byte-swapped/unknown-endian payload degrada para rebuild, nunca silent corruption

[ ] shutdown inicia retirando readiness/admission/fleet eligibility
[ ] /health/ready=503 durante DRAINING
[ ] no new correctness work começa após DRAINING boundary
[ ] external termination grace é >= internal deadline + safety margin ou deployment fica UNPROVEN
[ ] abrupt-kill recovery fixture passa

[ ] unhandledRejection é fatal containment, não log-and-continue
[ ] uncaughtException/unhandledRejection/signal shutdown são idempotentes
[ ] fatal during bootstrap nunca abre readiness

[ ] BootstrapAuthoritySeedV29 existe no documento
[ ] generated NormativeAuthorityIndex preserva seed e não possui conflicts
[ ] stable requirement IDs cobrem novos MUSTs de delivery/lifecycle

[ ] cases 801–850 passam
[ ] cases 1–800 continuam verdes
[ ] EvidenceBundleV29 corresponde ao merge/release SHA exato
```

---

# 618. Ordem recomendada de implementação V29

Não transformar a #742 em um único PR gigante. Preservar a divisão V28 e acrescentar dois foundation tracks.

```text
PR 0A — authority/traceability/eight manifests
        - sete manifests V28
        - DeliveryControlPlaneOccurrenceManifest
        - BootstrapAuthoritySeedV29
        - generated NormativeAuthorityIndex
        - Issue742TraceabilityMatrix
        - root EvidenceBundle schema V29

PR 0B — settings bootstrap / emitted runtime parity
        - igual V28

PR 0C — ratings migration / durability / byte-order portability
        - igual V28
        - canonical binary byte order
        - cross-arch fixtures

PR 0D — delivery control plane / merge + release admission
        - safe correctness workflow
        - push/merge-group coverage conforme repo policy
        - required-status evidence integration
        - release tag → evidence verification
        - delivery dependency fingerprint
        - evidence anchoring
        - immutable rebuild policy
        - amd64/arm64 smoke

PR 0E — shutdown withdrawal / fatal lifecycle / termination budget
        - READY→DRAINING authority
        - readiness + fleet eligibility withdrawal
        - external termination budget
        - unhandledRejection fail-stop
        - fatal/idempotent shutdown tests

PR 1 — config + migration + revision/fencing
PR 2 — release evidence
PR 3 — canonical context + evaluator/filter integration
PR 4 — pagination/cursor/search neutrality
PR 5 — TMDB Discover / builder / provenance / preview parity
PR 6 — Jellyfin / merged/custom/personal/recommendation parity
PR 7 — process resources/artifacts/background/shutdown closure
PR 8 — frontend/settings UX
PR 9 — full 1–850 suite + migration/rollback/load/fault + release evidence
```

Se upstream review scope não aceitar 0D/0E junto da feature:

```text
- abrir como foundation PRs separados;
- não remover os gates do plano;
- marcar FINAL_V29 como pending external/foundation closure até eles existirem.
```

Isso preserva reviewability sem mentir sobre assurance.

---

# 619. Handoff final V29 para agente/Codex

Antes de editar código:

```text
1. verificar dev HEAD/tree;
2. verificar issue #742 state/comments;
3. ler BootstrapAuthoritySeedV29;
4. gerar/validar NormativeAuthorityIndex;
5. materializar os oito manifests;
6. verificar repository enforcement evidence; UNKNOWN permanece UNKNOWN;
7. classificar workflows/actions/runners/release ingress;
8. não executar código de fork em pull_request_target;
9. criar test harness + correctness workflow seguro;
10. implementar 0B/0C/0D/0E conforme dependências;
11. preservar Worldwide golden master e todo core #742;
12. executar cases 1–850;
13. produzir evidence para actual merge SHA;
14. antes de release, verificar tag SHA == evidence SHA;
15. smoke amd64 + arm64;
16. registrar OCI/platform digests e long-lived evidence anchor;
17. somente então usar claim FINAL_V29.
```

Quando não houver permissão de admin para provar branch/ruleset:

```text
não inventar;
registrar repositoryEnforcement = UNKNOWN;
continuar implementação/testes;
solicitar maintainer evidence apenas no merge/release handoff.
```

---

# 620. Resultado final da auditoria V29

A V28 já era uma especificação de engenharia excepcionalmente profunda. A V29 encontrou gaps reais não por
reabrir o core funcional da #742, mas por seguir a cadeia um passo além: **do commit aprovado até o artifact
publicado, e do estado READY até o processo efetivamente terminado**.

Ajustes V29:

```text
+ snapshot d270a3a / tree b4db5931 revalidado, sem source drift
+ oitavo universo: delivery-control-plane occurrences
+ merge status verde separado de merge enforcement real
+ actual merge SHA evidence / push + merge-group closure
+ release tag → AuditEvidenceBundle admission
+ repository ruleset/branch-protection state tratado como external evidence, nunca inferido
+ floating GitHub Actions/runner/base-image identities entram no fingerprint
+ release SemVer rebuild/immutability policy
+ long-lived evidence anchoring
+ explicit amd64 + arm64 release parity
+ platform/native dependency fingerprint
+ canonical byte order para ratings snapshot persistente
+ READY→DRAINING readiness/fleet withdrawal
+ external termination-grace vs internal shutdown deadline
+ abrupt-kill recovery
+ unhandledRejection fail-stop
+ BootstrapAuthoritySeed para eliminar circularidade do AuthorityIndex
+ 50 novos casos, total acumulado 850+ casos
```

Claim defensável V29:

> **Para o snapshot `d270a3a7f3b6e41304d9f91045b1d481311c3c96` / tree
> `b4db5931c47035862fac075ac01ec02fe1e621c0`, a especificação passa a reconciliar oito universos
> autoritativos e cobre a cadeia source→build→runtime→deployment→merge/release delivery, além de toda a
> arquitetura funcional e operacional V8→V28. O que depende de runtime, upstream, filesystem, orchestrator,
> GitHub repository settings, runner/action resolution ou registry permanece condicionado a evidence/gates
> executáveis, nunca a suposição.**

Ainda não afirmar antes da execução:

```text
- ausência literal de todos os bugs;
- que 850 casos especificados já passaram;
- branch protection/ruleset enforcement que não foi observado;
- reproducibilidade bit-for-bit sem toolchain/base/action identities fixadas;
- graceful shutdown garantido sem termination-grace externo conhecido;
- performance arm64/amd64 sem benchmark nativo;
- imutabilidade de upstream Actions/base images/tags fora do fingerprint/pinning;
- cobertura de commit posterior ao snapshot sem rerun;
- "100%" como infalibilidade. O significado rigoroso continua sendo cobertura rastreável + gates executáveis
  + evidence do snapshot/merge/release realmente testado.
```

Conclusão arquitetural V29:

```text
A. manter integralmente Release Evidence → Canonical Context → Visibility → Filter → Pagination;
B. usar AuthoritySeed → AuthorityIndex → Traceability antes de implementação;
C. tratar CI definition, merge enforcement e release admission como autoridades diferentes;
D. produzir proof no actual merge SHA, não apenas no PR head;
E. publicar release somente quando tag SHA e evidence SHA coincidirem;
F. provar amd64/arm64 e snapshot portable byte order;
G. retirar readiness/fleet eligibility antes do shutdown drain;
H. alinhar internal shutdown deadline ao external termination grace;
I. tratar unhandledRejection como fatal containment;
J. só chamar de FINAL_V29 quando os 850+ casos, oito manifests, merge/release evidence e long-lived anchor
   estiverem verdes e correspondendo ao artifact efetivamente publicado.
```

---
