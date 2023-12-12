# WidgetExec - Aplicativo Android

## Visão Geral

WidgetExec é um aplicativo Android desenvolvido em Java usando o Android Studio. Permite aos usuários adicionar e remover dinamicamente campos de texto.
## Funcionalidades

- **Adição Dinâmica de Widgets**: Os usuários podem adicionar campos de entrada para habilidades clicando no botão `Adicionar Habilidade`.
- **Remoção Dinâmica de Widgets**: Os usuários podem remover o último campo de entrada adicionado clicando no botão `Remover Habilidade`.

## Uso

1. **Adicionar Habilidade**: Clique no botão `Adicionar Habilidade` para adicionar um novo campo de entrada para habilidades.
2. **Remover Habilidade**: Clique no botão `Remover Habilidade` para remover o último campo de entrada adicionado.

## Como executar

Para usar este aplicativo, siga estas etapas:

1. Clone o repositório: git clone https://github.com/ItaloSixx/WidgetExec.git
3. Abra o projeto no AndroidStudio.
4. Compile e execute o aplicativo em um dispositivo Android ou emulador.

Caso ocorra algum erro relacionado a SDK, no arquivo Gradle Scripts/build.gradle.kts (Module:app), altere o valor de compileSdk para 34.

## Funcionamento
O código deste projeto utiliza conceitos de criação dinâmica de widgets para permitir aos usuários adicionar e remover elementos de forma flexível.

### Layout `habilidadesContainer`
Tendo criado um layout dedicado para receber esses elementos dinâmicos, a manutenção e o entendimento do código são aprimorados.

O `habilidadesContainer` é um novo layout inserido no layout principal do aplicativo. Ele é definido como um `LinearLayout` vertical no arquivo de layout XML. Esse layout desempenha um papel importante ao oferecer um espaço específico para abrigar os elementos dinâmicos gerados durante a execução do aplicativo.

### Adição dinâmica
Quando o botão "Adicionar Habilidade" é clicado, o método `addHabilidadeEditText()` é chamado. Esse método incrementa o contador de habilidades (`habilidade`), cria um novo widget `EditText` e o adiciona ao contêiner de habilidades (`habilidadesContainer`). 

### Remoção dinâmica
O método `rmvUltimoHabilidadeEditText()` é chamado quando o botão `Remover Habilidade` é clicado. Este método verifica se há habilidades adicionadas antes de prosseguir. Se houver, o último `EditText` adicionado é removido do contêiner e a referência correspondente é removida da lista. O contador de habilidades é atualizado conforme necessário.

### Array Associativo (editTextList)
A lista editTextList é um exemplo de um array associativo (ou lista associativa). É uma estrutura de dados que mantém referências aos elementos EditText adicionados dinamicamente. Isso facilita a manipulação posterior desses elementos, como a remoção do último `EditText` ao clicar no botão `Remover Habilidade`.

## Conclusão

Ao implementar a adição dinâmica de elementos, neste caso, `EditText`, em um layout separado (`habilidadesContainer`), ganhamos flexibilidade. Essa abordagem não se limita a `EditText` e pode ser estendida para qualquer elemento do XML.

...











