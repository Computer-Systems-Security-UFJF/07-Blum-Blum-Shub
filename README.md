# Blum Blum Shub

Implementação do gerador pseudoaleatório Blum Blum Shub em um notebook Python (`bbs.ipynb`), compatível com Google Colab.

## Parâmetros


| Parâmetro   | Valor      |
| ----------- | ---------- |
| p           | 90107      |
| q           | 104723     |
| s (semente) | 12345      |
| n = p * q   | 9436275361 |


- `p` e `q` são primos maiores que 10000 e congruentes a 3 mod 4.
- `gcd(s, n) = 1`.

## Como usar

Para rodar no Cursor, o ambiente já está em `.venv` (criado com `uv`, só com o `ipykernel`). Selecione o kernel **Python (uv)**.

1. Abra `bbs.ipynb` no Google Colab (ou em qualquer Jupyter).
2. Execute todas as células. O notebook verifica as premissas, gera a sequência de bits, imprime a string completa e salva/baixa o arquivo `bits.txt`.
3. Acesse o [Random Bitstream Tester](https://zsomotech.com/random-bitstream-tester/).
4. Cole a string de bits em **Manual bitstream input** e clique em **Insert Input Stream**.
5. Clique em **Start Test** e tire o print dos resultados.

A quantidade de bits é controlada pela variável `N` no notebook (padrão: 1000000).