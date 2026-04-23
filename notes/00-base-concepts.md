# Conceitos Base

## As cinco palavras da criptografia

**Plaintext:** a mensagem original, legível.
Exemplo: "Atacar ao amanhecer"

**Ciphertext:** a mensagem embaralhada, ilegível.
Exemplo: "Dwdfdu dr dpdqkhfhu"

**Chave (Key):** o segredo que transforma um no outro.
Sem a chave, não é possível recuperar a mensagem original.

**Cifrar (Encrypt):** plaintext + chave → ciphertext

**Decifrar (Decrypt):** ciphertext + chave → plaintext

**Quebrar (Break / Cryptanalysis):** recuperar o plaintext sem ter a chave.
O jogo do atacante.

Toda a criptografia — clássica, moderna e quântica — gira em torno dessas cinco palavras.

---

## Algoritmo vs. Chave

Dois conceitos que costumam ser confundidos, mas são completamente diferentes:

- **Algoritmo:** as regras públicas do processo. O *mecanismo*. A "receita".
- **Chave:** o segredo específico escolhido para aquela cifragem. O "ingrediente secreto" que personaliza a receita.

### Analogia do cadeado

- **Algoritmo** = o design do cadeado de combinação. Qualquer pessoa sabe como funciona mecanicamente (gira as rodinhas até alinhar os dígitos corretos). O fabricante publica o manual.
- **Chave** = a combinação específica, tipo `7341`. Isso é o segredo.

Duas pessoas podem ter o mesmo modelo de cadeado (mesmo algoritmo) com combinações diferentes (chaves diferentes). Conhecer o modelo não ajuda a abrir o cadeado de outra pessoa.

---

## Princípio de Kerckhoffs (1883)

> A segurança deve depender apenas do segredo da chave, não do segredo do algoritmo.

Tradução: **algoritmos devem ser públicos e escrutinados por todo mundo. Apenas a chave é secreta.**

### Por quê

Algoritmos secretos oferecem segurança falsa. Quando alguém descobre como funcionam (e sempre descobre. Engenharia reversa existe), a segurança evapora.

Já um algoritmo público que resistiu a milhares de matemáticos tentando quebrá-lo por décadas (AES, por exemplo), esse se pode confiar.

### Security through obscurity

O oposto do Princípio de Kerckhoffs é o princípio errado que empresas ingênuas adotam:

> "Nosso algoritmo é secreto, por isso é seguro."

Isso se chama **security through obscurity** e é considerado anti-padrão em criptografia moderna. Auditor de cripto sério identifica isso como **red flag** imediato no relatório.