# 🧮 Calculadora em Python (Terminal e GUI)

Este repositório contém dois exemplos simples de calculadora desenvolvidos em Python:

1. ✅ **Calculadora via Terminal** (interação em texto com `input`)
2. ✅ **Calculadora com Interface Gráfica (GUI)** usando `Tkinter`

---

## 📟 Calculadora no Terminal

```python
def menu():
    print("=== Calculadora Simples ===")
    print("1 - Soma")
    print("2 - Subtração")
    print("3 - Multiplicação")
    print("4 - Divisão")
    print("0 - Sair")

while True:
    menu()
    escolha = input("Escolha uma opção: ")

    if escolha == "0":
        print("Encerrando a calculadora.")
        break

    num1 = float(input("Digite o primeiro número: "))
    num2 = float(input("Digite o segundo número: "))

    if escolha == "1":
        print(f"Resultado: {num1 + num2}")
    elif escolha == "2":
        print(f"Resultado: {num1 - num2}")
    elif escolha == "3":
        print(f"Resultado: {num1 * num2}")
    elif escolha == "4":
        if num2 == 0:
            print("Erro: divisão por zero.")
        else:
            print(f"Resultado: {num1 / num2}")
    else:
        print("Opção inválida. Tente novamente.")

    print()  # Linha em branco
```

---

## 🖥️ Calculadora com Interface Gráfica (Tkinter)

```python
import tkinter as tk
from tkinter import messagebox

def calcular(operacao):
    try:
        num1 = float(entrada1.get())
        num2 = float(entrada2.get())

        if operacao == "+":
            resultado = num1 + num2
        elif operacao == "-":
            resultado = num1 - num2
        elif operacao == "*":
            resultado = num1 * num2
        elif operacao == "/":
            if num2 == 0:
                raise ZeroDivisionError
            resultado = num1 / num2

        resultado_var.set(f"Resultado: {resultado}")

    except ValueError:
        messagebox.showerror("Erro", "Digite apenas números.")
    except ZeroDivisionError:
        messagebox.showerror("Erro", "Divisão por zero não é permitida.")

# Interface
janela = tk.Tk()
janela.title("Calculadora Simples")

tk.Label(janela, text="Número 1").pack()
entrada1 = tk.Entry(janela)
entrada1.pack()

tk.Label(janela, text="Número 2").pack()
entrada2 = tk.Entry(janela)
entrada2.pack()

tk.Button(janela, text="Somar", command=lambda: calcular("+")).pack(fill='x')
tk.Button(janela, text="Subtrair", command=lambda: calcular("-")).pack(fill='x')
tk.Button(janela, text="Multiplicar", command=lambda: calcular("*")).pack(fill='x')
tk.Button(janela, text="Dividir", command=lambda: calcular("/")).pack(fill='x')

resultado_var = tk.StringVar()
tk.Label(janela, textvariable=resultado_var, font=("Arial", 14)).pack(pady=10)

janela.mainloop()
```

---

## 📌 Requisitos

- Python 3.10 ou superior
- Tkinter (`sudo apt install python3-tk` no Ubuntu)

---

## 🏁 Status do Projeto

![Badge de Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=flat-square)

---

Sinta-se à vontade para forkar, testar e modificar! 🚀


---

## 🖼️ Resultado da Interface Gráfica

![Calculadora](https://github.com/user-attachments/assets/23853c03-2474-4f1b-b712-db3008d9e5a8)
 
