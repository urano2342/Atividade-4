gerador-senhas/
│
├── README.md
├── password_generator.py
└── .gitignore
# Gerador de Senhas Seguras

## Descrição
Este projeto implementa um gerador de senhas seguras e personalizáveis usando Python. É simples, eficiente e ideal para garantir a segurança de suas contas.

## Funcionalidades
- Comprimento personalizável das senhas.
- Escolha de incluir:
  - Letras maiúsculas e minúsculas.
  - Números.
  - Caracteres especiais.

## Requisitos
- Python 3.7 ou superior.

## Como Usar
1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/gerador-senhas.git
   cd gerador-senhas
python password_generator.py
git checkout -b minha-feature
git commit -m "Descrição do que foi alterado"

---

#### Arquivo `.gitignore`

```gitignore
# Ignore arquivos Python desnecessários
__pycache__/
*.pyc
.env
import random
import string

def gerar_senha(comprimento, incluir_maiusculas=True, incluir_numeros=True, incluir_especiais=True):
    """
    Gera uma senha segura com base nas preferências do usuário.
    :param comprimento: Tamanho da senha.
    :param incluir_maiusculas: Incluir letras maiúsculas.
    :param incluir_numeros: Incluir números.
    :param incluir_especiais: Incluir caracteres especiais.
    :return: Senha gerada.
    """
    caracteres = string.ascii_lowercase
    if incluir_maiusculas:
        caracteres += string.ascii_uppercase
    if incluir_numeros:
        caracteres += string.digits
    if incluir_especiais:
        caracteres += "!@#$%^&*()-_=+"

    senha = ''.join(random.choice(caracteres) for _ in range(comprimento))
    return senha

if __name__ == "__main__":
    print("=== Gerador de Senhas Seguras ===")
    try:
        comprimento = int(input("Digite o comprimento da senha: "))
        incluir_maiusculas = input("Incluir letras maiúsculas? (s/n): ").strip().lower() == 's'
        incluir_numeros = input("Incluir números? (s/n): ").strip().lower() == 's'
        incluir_especiais = input("Incluir caracteres especiais? (s/n): ").strip().lower() == 's'

        senha = gerar_senha(comprimento, incluir_maiusculas, incluir_numeros, incluir_especiais)
        print(f"\nSua senha gerada é: {senha}")
    except ValueError:
        print("\nErro: Por favor, insira valores válidos.")
git init
git add .
git commit -m "Configuração inicial do projeto"
git checkout -b nova-feature
git add password_generator.py
git commit -m "Implementa funcionalidade de geração de senhas"
git checkout main
git merge nova-feature
