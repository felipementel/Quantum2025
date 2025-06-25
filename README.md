## Configuração do Ambiente

### 1. Instalar Dependências

A primeira célula do notebook instala automaticamente todas as dependências necessárias.

### 2. Configurar Variáveis de Ambiente

1. **Copie o arquivo de exemplo:**

   ```bash
   cp .env.example .env
   ```

2. **Edite o arquivo `.env` e adicione seu token da IBM Quantum:**

   ```env
   IBM_QUANTUM_TOKEN=seu_token_aqui
   ```

3. **Para obter seu token:**
   - Acesse [IBM Quantum Platform](https://quantum.cloud.ibm.com/)
   - Faça login ou crie uma conta gratuita
   - Vá para sua conta e copie o token da API

⚠️ **Importante**: A partir de julho de 2025, a IBM migrou para a nova plataforma. Use sempre `https://quantum.cloud.ibm.com/` ao invés da versão clássica.

## Como Usar o projeto AlgoritmoShor

1. Configure o ambiente conforme descrito acima
2. Abra o notebook `AlgoritmoShor.ipynb`
3. Execute as células em ordem
4. O algoritmo tentará fatorar o número N = 77

## Sobre o Algoritmo de Shor

O algoritmo de Shor é um algoritmo quântico para fatoração de números inteiros desenvolvido por Peter Shor em 1994. Ele oferece uma aceleração exponencial em relação aos melhores algoritmos clássicos conhecidos para este problema.

### Etapas do Algoritmo

1. **Verificação preliminar**: Testa fatores triviais
2. **Escolha de base**: Seleciona um número `a` coprimo com N
3. **Estimativa de fase quântica (QPE)**: Encontra o período da função f(x) = a^x mod N
4. **Verificação do período**: Confirma se o período é útil
5. **Cálculo dos fatores**: Usa o período para encontrar os fatores de N

## Estrutura do Código

- `etapa_2_verificacao_preliminar()`: Verifica fatores triviais
- `etapa3()`: Escolhe base aleatória
- `etapa4()`: Implementa QPE usando Qiskit
- `etapa5()`: Verifica se o período é válido
- `etapa6()`: Calcula os fatores finais
- `Uf()`: Implementa a operação modular controlada

## Requisitos

- Python 3.8+
- Conta na IBM Quantum Network (gratuita)
- Jupyter Notebook ou Jupyter Lab

## Segurança

⚠️ **Importante**:

- Nunca commite o arquivo `.env` no controle de versão
- Mantenha seu token da IBM Quantum privado
- O arquivo `.env` já está incluído no `.gitignore`

## Licença

Este projeto é apenas para fins educacionais e de pesquisa.
