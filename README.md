# 📘 Manual Completo de Instalação e Configuração
*Cordova + Android Studio + Gradle + VS Code + Node.js + Java*

---

## 📖 Introdução
Este manual descreve o processo completo para configurar um ambiente de desenvolvimento *Cordova* no Windows, incluindo todas as dependências necessárias.

O *Cordova* permite criar aplicativos móveis multiplataforma (Android/iOS) usando *HTML, CSS e JavaScript*. Para funcionar, ele depende de várias ferramentas que trabalham em conjunto:

- *Node.js* → Gerencia pacotes e executa o Cordova.
- *Cordova* → Framework para criar e compilar apps híbridos.
- *Java (JDK)* → Necessário para compilar código Android.
- *Android Studio (SDK)* → Fornece ferramentas e bibliotecas do Android.
- *Gradle* → Sistema de build usado pelo Android.
- *Visual Studio Code* → Editor de código leve e extensível.
- *ADB (Android Debug Bridge)* → Ferramenta de linha de comando para comunicação com dispositivos Android.

---

## 1. 🟢 Node.js
### O que é?
O *Node.js* é um ambiente de execução JavaScript fora do navegador. Ele vem com o *NPM (Node Package Manager)*, usado para instalar pacotes como o Cordova.

### Instalação
- *Download*: [https://nodejs.org](https://nodejs.org)
- Instale a versão *LTS (Long Term Support)*.

### Verificação
bash
node -v
npm -v


---

## 2. 📦 Cordova
### O que é?
O *Cordova* é o framework que permite criar aplicativos móveis híbridos. Ele gera o projeto Android/iOS e usa o Gradle para compilar.

### Instalação
bash
npm install -g cordova


### Verificação
bash
cordova -v


---

## 3. ☕ Java (JDK)
### O que é?
O *Java Development Kit (JDK)* é necessário porque o Android é baseado em Java. O Gradle e o Android SDK usam o JDK para compilar o código.

### Instalação
- *Download*: [https://adoptium.net/](https://adoptium.net/)
- Instale o *Temurin JDK 11 ou 17*.

### Verificação
bash
java -version
javac -version


---

## 4. 📱 Android Studio (SDK)
### O que é?
O *Android Studio* é o IDE oficial do Android. Mesmo que você use o VS Code, precisa dele porque fornece o *Android SDK* (bibliotecas, ferramentas e emuladores).

### Instalação
- *Download*: [https://developer.android.com/studio](https://developer.android.com/studio)
- Durante a instalação, marque:
  - *Android SDK*
  - *Android SDK Platform*
  - *Android SDK Build-Tools*
  - *Android Virtual Device (AVD)*

### Configuração
Abra o Android Studio → *More Actions → SDK Manager*
- Instale a versão mais recente do SDK.
- *Obrigatório instalar*:
  - *Android API Level 35 (Android 14)*
  - *Android SDK Build-Tools 35.x*
  - *Android SDK Platform-Tools* (inclui o *ADB*)
  - *Command-line Tools*

---

## 5. ⚙️ Gradle
### O que é?
O *Gradle* é o sistema de automação de builds usado pelo Android. Ele compila o código, baixa dependências e gera o APK.

### Instalação
- *Download*: [https://gradle.org/releases/](https://gradle.org/releases/)
- Baixe o arquivo *bin.zip*.
- Extraia em C:\Gradle\gradle-x.x.x.

### Verificação
bash
gradle -v


---

## 6. 🖥️ Visual Studio Code
### O que é?
O *VS Code* é um editor de código leve e extensível, ideal para editar projetos Cordova.

### Instalação
- *Download*: [https://code.visualstudio.com/](https://code.visualstudio.com/)

### Extensões recomendadas
- *Cordova Tools*
- *Java Extension Pack*
- *Debugger for Java*
- *Android iOS Emulator*

---

## 7. 🔧 Configuração das Variáveis de Ambiente (Windows)
As variáveis de ambiente permitem que o sistema encontre as ferramentas instaladas.

### Como configurar
1. Abra: *Painel de Controle → Sistema → Configurações Avançadas → Variáveis de Ambiente*.
2. Adicione as seguintes variáveis:

#### Variáveis do Sistema
- *JAVA_HOME*
  C:\Program Files\Eclipse Adoptium\jdk-17

- *ANDROID_HOME*
  C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk

- *GRADLE_HOME*
  C:\Gradle\gradle-x.x.x

- *ANDROID_SDK_ROOT*
  C:\Users\SEU_USUARIO\AppData\Local\Android\Sdk

#### Path (editar e adicionar)
%JAVA_HOME%\bin
%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\tools
%ANDROID_HOME%\tools\bin
%GRADLE_HOME%\bin
