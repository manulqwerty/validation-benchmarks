# XBOW benchmark fix report

Date: 2026-05-21
Total: 104 | OK: 54 | Fixed: 20 | Skipped: 30 | Buildable: 74 | Runnable: 74

- **Buildable** = `docker compose build` succeeds (OK + Fixed).
- **Runnable** = additionally, `make run` brings up every service with
  healthcheck green. The list lives in `runnable.txt` at repo root,
  consumed by auto-bounty's `benchmarks/run-bench.py`.

## Build skip breakdown

- **exhausted bumps (3 attempts failed)**: 28
- **no bump rule for image**: 2

## Runtime breakdown (of buildable)

- **running**: 74

## Per-benchmark table

| # | benchmark | build | change | runtime | notes |
|---|---|---|---|---|---|
| 1 | XBEN-001-24 | fixed | bump mysql:5.7.15 → mysql:5.7 | ok |  |
| 2 | XBEN-002-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 3 | XBEN-003-24 | fixed | mysql:5.7.15 -> mysql:5.7 (Dockerfile) | ok |  |
| 4 | XBEN-004-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 5 | XBEN-005-24 | ok | — | ok |  |
| 6 | XBEN-006-24 | ok | — | ok |  |
| 7 | XBEN-007-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 8 | XBEN-008-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 9 | XBEN-009-24 | ok | — | ok |  |
| 10 | XBEN-010-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 11 | XBEN-011-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 12 | XBEN-012-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 13 | XBEN-013-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 14 | XBEN-014-24 | ok | — | ok |  |
| 15 | XBEN-015-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 16 | XBEN-016-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 17 | XBEN-017-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 18 | XBEN-018-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 19 | XBEN-019-24 | ok | — | ok |  |
| 20 | XBEN-020-24 | ok | — | ok |  |
| 21 | XBEN-021-24 | ok | — | ok |  |
| 22 | XBEN-022-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 23 | XBEN-023-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 24 | XBEN-024-24 | ok | — | ok |  |
| 25 | XBEN-025-24 | ok | — | ok |  |
| 26 | XBEN-026-24 | skipped | — | n/a | httpd:2.4.49/50 is intentionally vulnerable; its buster apt sources are archived. Bumping the tag would lose the CVE the benchmark targets |
| 27 | XBEN-027-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 28 | XBEN-028-24 | ok | — | ok |  |
| 29 | XBEN-029-24 | ok | — | ok |  |
| 30 | XBEN-030-24 | ok | — | ok |  |
| 31 | XBEN-031-24 | skipped | — | n/a | httpd:2.4.49/50 is intentionally vulnerable; its buster apt sources are archived. Bumping the tag would lose the CVE the benchmark targets |
| 32 | XBEN-032-24 | ok | — | ok |  |
| 33 | XBEN-033-24 | ok | — | ok |  |
| 34 | XBEN-034-24 | ok | — | ok |  |
| 35 | XBEN-035-24 | ok | — | ok |  |
| 36 | XBEN-036-24 | ok | — | ok |  |
| 37 | XBEN-037-24 | ok | — | ok |  |
| 38 | XBEN-038-24 | ok | — | ok |  |
| 39 | XBEN-039-24 | ok | — | ok |  |
| 40 | XBEN-040-24 | ok | — | ok |  |
| 41 | XBEN-041-24 | fixed | php:7.1-apache -> php:7.2-apache; php:7.1-apache -> php:7.4-apache | ok |  |
| 42 | XBEN-042-24 | ok | — | ok |  |
| 43 | XBEN-043-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 44 | XBEN-044-24 | skipped | — | n/a | php tag bumps did not resolve build; needs targeted version per service |
| 45 | XBEN-045-24 | ok | — | ok |  |
| 46 | XBEN-046-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 47 | XBEN-047-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 48 | XBEN-048-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 49 | XBEN-049-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 50 | XBEN-050-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 51 | XBEN-051-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 52 | XBEN-052-24 | ok | — | ok |  |
| 53 | XBEN-053-24 | ok | — | ok |  |
| 54 | XBEN-054-24 | ok | — | ok |  |
| 55 | XBEN-055-24 | ok | — | ok |  |
| 56 | XBEN-056-24 | ok | — | ok |  |
| 57 | XBEN-057-24 | ok | — | ok |  |
| 58 | XBEN-058-24 | ok | — | ok |  |
| 59 | XBEN-059-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 60 | XBEN-060-24 | ok | — | ok |  |
| 61 | XBEN-061-24 | ok | — | ok |  |
| 62 | XBEN-062-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 63 | XBEN-063-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 64 | XBEN-064-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 65 | XBEN-065-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 66 | XBEN-066-24 | skipped | — | n/a | multiple FROM lines broken (mysql + haproxy); 3-attempt budget exhausted |
| 67 | XBEN-067-24 | fixed | php:7.1-apache -> php:7.2-apache; php:7.2-apache -> php:7.4-apache | ok |  |
| 68 | XBEN-068-24 | ok | — | ok |  |
| 69 | XBEN-069-24 | ok | — | ok |  |
| 70 | XBEN-070-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 71 | XBEN-071-24 | ok | — | ok |  |
| 72 | XBEN-072-24 | ok | — | ok |  |
| 73 | XBEN-073-24 | ok | — | ok |  |
| 74 | XBEN-074-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 75 | XBEN-075-24 | ok | — | ok |  |
| 76 | XBEN-076-24 | ok | — | ok |  |
| 77 | XBEN-077-24 | ok | — | ok |  |
| 78 | XBEN-078-24 | ok | — | ok |  |
| 79 | XBEN-079-24 | ok | — | ok |  |
| 80 | XBEN-080-24 | ok | — | ok |  |
| 81 | XBEN-081-24 | skipped | — | n/a | php tag bumps did not resolve build; needs targeted version per service |
| 82 | XBEN-082-24 | ok | — | ok |  |
| 83 | XBEN-083-24 | ok | — | ok |  |
| 84 | XBEN-084-24 | skipped | — | n/a | node-based build did not finish within harness budget; npm install/run on a multi-stage build |
| 85 | XBEN-085-24 | ok | — | ok |  |
| 86 | XBEN-086-24 | ok | — | ok |  |
| 87 | XBEN-087-24 | skipped | — | n/a | python:2.7 image still ships buster apt sources (archived); no Python 2.7 image with working apt remains |
| 88 | XBEN-088-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 89 | XBEN-089-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 90 | XBEN-090-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 91 | XBEN-091-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 92 | XBEN-092-24 | ok | — | ok |  |
| 93 | XBEN-093-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 94 | XBEN-094-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 95 | XBEN-095-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
| 96 | XBEN-096-24 | ok | — | ok |  |
| 97 | XBEN-097-24 | ok | — | ok |  |
| 98 | XBEN-098-24 | ok | — | ok |  |
| 99 | XBEN-099-24 | skipped | — | n/a | node-based build did not finish within harness budget; npm install/run on a multi-stage build |
| 100 | XBEN-100-24 | fixed | python:3.8-slim-buster -> python:3.8-slim-bullseye | ok |  |
| 101 | XBEN-101-24 | ok | — | ok |  |
| 102 | XBEN-102-24 | ok | — | ok |  |
| 103 | XBEN-103-24 | ok | — | ok |  |
| 104 | XBEN-104-24 | fixed | mysql:5.7.15 -> mysql:5.7 | ok |  |
