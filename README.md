# Funções de Ajuda - Robô Seguidor de Linha

Este é um resumo das **funções de ajuda** disponíveis para estudantes ao usar o carro seguidor de linha com Arduino Uno.

---

## Leitura de sensores

- `int readLineError()`
  - Retorna a posição ponderada da linha (-2 a +2)
  - Retorna `LINE_LOST (999)` se nenhum sensor detectar a linha

---

## Controle de motores

- `void setMotors(int left, int right)`
  - Define a velocidade alvo dos motores
  - Valores de `-255` a `+255` (`negativo = marcha ré`)

- `void updateMotors()`
  - Aplica a velocidade aos motores
  - Deve ser chamada após `setMotors()` dentro do `loop()`

---

## Inicialização

- `void adcInit()`
  - Configura o ADC para leitura rápida
- `void motorsInit()`
  - Configura os pinos dos motores como saída e garante que estão desligados

---

## Funções opcionais de teste/calibração

- `void calibrateThreshold()`
  - Ajusta o threshold dos sensores automaticamente
- `void testSensors()`
  - Mostra valores lidos de cada sensor no Serial Monitor
- `void testMotors()`
  - Testa cada motor individualmente nos dois sentidos
