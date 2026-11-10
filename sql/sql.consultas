
-- =========================================================
-- FC BARCELONA 2025/26
-- PROJETO DE BI
-- Banco de dados: PostgreSQL
-- =========================================================


-- =========================================================
-- 01. PREPARAÇÃO E VALIDAÇÃO DOS DADOS
-- =========================================================

-- Etapas realizadas na preparação dos dados:
-- - Identificação e remoção de duplicatas.
-- - Correção de erros e inconsistências.
-- - Tratamento de valores ausentes.
-- - Padronização de formatos, como datas.
-- - Verificação da consistência dos dados.


-- =========================================================
-- 02. ESTATÍSTICAS DAS PARTIDAS
-- =========================================================

SELECT
    COUNT(*) AS jogos,
    COUNT(*) FILTER (WHERE result = 'W') AS vitoria,
    COUNT(*) FILTER (WHERE result = 'D') AS empate,
    COUNT(*) FILTER (WHERE result = 'L') AS derrota,
    SUM(goals_for) AS gols_marcados,
    SUM(goals_against) AS gols_sofridos,
    CAST(AVG(posse) AS INT) AS media_posse,
    (
        SELECT opponent
        FROM games.matches
        ORDER BY public DESC
        LIMIT 1
    ) AS oponente_maior_publico,
    (
        SELECT public
        FROM games.matches
        ORDER BY public DESC
        LIMIT 1
    ) AS maior_publico
FROM games.matches;


-- =========================================================
-- 03. ESTATÍSTICAS DOS JOGADORES
-- =========================================================

SELECT
    player,
    position,
    matches_played,
    starts,
    minutes,
    goals,
    assists,
    goals_assists,
    yellow_cards,
    red_cards
FROM player.players
ORDER BY goals_assists DESC, goals DESC;


-- =========================================================
-- 04. CRIAÇÃO DAS VIEWS
-- =========================================================

-- VIEW: RESUMO DA TEMPORADA

CREATE OR REPLACE VIEW games.vw_resumo_temporada AS
SELECT
    COUNT(*) AS jogos,
    COUNT(*) FILTER (WHERE result = 'W') AS vitorias,
    COUNT(*) FILTER (WHERE result = 'D') AS empates,
    COUNT(*) FILTER (WHERE result = 'L') AS derrotas,
    SUM(goals_for) AS gols_marcados,
    SUM(goals_against) AS gols_sofridos,
    ROUND(AVG(posse))::INT AS media_posse,
    (
        SELECT opponent
        FROM games.matches
        ORDER BY public DESC
        LIMIT 1
    ) AS oponente_maior_publico,
    (
        SELECT public
        FROM games.matches
        ORDER BY public DESC
        LIMIT 1
    ) AS maior_publico
FROM games.matches;


-- VIEW: ESTATÍSTICAS DOS JOGADORES

CREATE OR REPLACE VIEW player.vw_estatisticas_jogadores AS
SELECT
    player,
    position,
    matches_played,
    starts,
    minutes,
    goals,
    assists,
    goals_assists,
    yellow_cards,
    red_cards
FROM player.players;


-- =========================================================
-- 05. CONSULTA DAS VIEWS
-- =========================================================

-- Resumo da temporada

SELECT *
FROM games.vw_resumo_temporada;


-- Estatísticas dos jogadores

SELECT *
FROM player.vw_estatisticas_jogadores
ORDER BY goals_assists DESC, goals DESC;
