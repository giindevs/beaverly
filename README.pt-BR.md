<p align="center">
  <img src="assets/mascot.png" alt="Beaverly" width="140">
</p>

<h1 align="center">Beaverly Shelf</h1>

<p align="center">
  <b>Seus livros, sua estante — 100% no seu computador.</b><br>
  Um app de desktop tranquilo e local para organizar sua biblioteca de e-books e ler
  <b>PDF, EPUB e CBZ</b> com grifos e anotações. Sem precisar de conta.
</p>

<p align="center">
  <a href="https://github.com/giindevs/beaverly/releases/latest"><img src="https://img.shields.io/github/v/release/giindevs/beaverly?label=vers%C3%A3o&color=C0602F" alt="Versão"></a>
  <a href="https://github.com/giindevs/beaverly/releases"><img src="https://img.shields.io/github/downloads/giindevs/beaverly/total?label=downloads&color=6C6F43" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/Windows-x64-0078D6?logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/Linux-x64-1793D1?logo=linux&logoColor=white" alt="Linux">
  <img src="https://img.shields.io/badge/offline--first-privacidade-2E7D32" alt="Offline-first">
</p>

<p align="center">
  <a href="README.md">English</a> · <b>Português&nbsp;(BR)</b>
</p>

---

## ⬇️ Download

Baixe a versão mais recente na **[página de Releases »](https://github.com/giindevs/beaverly/releases/latest)**

| Sistema | Arquivo | Observações |
| --- | --- | --- |
| **Windows 10/11 (x64)** | `beaverly-shelf-setup-<versão>.exe` | Instalador — não pede admin, não precisa do .NET |
| **Linux — AppImage** | `Beaverly-Shelf-<versão>-x86_64.AppImage` | Portátil — dê `chmod +x` e execute |
| **Linux — Debian/Ubuntu** | `beaverly-shelf_<versão>_amd64.deb` | `sudo apt install ./beaverly-shelf_*.deb` |

> **No primeiro uso no Windows:** como o instalador ainda não é assinado digitalmente,
> o Windows SmartScreen mostra *"O Windows protegeu o seu computador"*. Clique em
> **Mais informações → Executar assim mesmo**. É esperado para apps novos e **não** é
> um aviso de vírus.

Passo a passo: **[Instalar no Windows »](docs/install-windows.md)** ·
**[Instalar no Linux »](docs/install-linux.md)**

🛒 *Em breve:* Microsoft Store e Ubuntu (Snap) Store — veja o [roadmap](#-roadmap).

---

## ✨ Recursos

- 📚 **Biblioteca local** — importe seus e-books (arquivos ou pastas), organize por
  autor, série, tags e coleções. Tudo fica na sua máquina.
- 📖 **Leitor embutido** — leia **PDF, EPUB e CBZ** com modo de leitura limpo, sumário,
  seleção de texto e uma barra de seleção estilo navegador (copiar · grifar · nota ·
  buscar na web).
- ✍️ **Grifos e notas** — anote enquanto lê. Seus arquivos originais **nunca são
  alterados** (somente leitura, sempre).
- 🖼️ **Capas e metadados (opcional)** — se quiser, busque capas, sinopses e dados do
  autor online. Só o texto da busca é enviado — nunca seus arquivos — e você confirma
  antes de gravar.
- 🔌 **Addons** — amplie o catálogo com addons no estilo Stremio (serviços instalados
  por URL; nenhum código roda dentro do app).
- 💾 **Backups** — faça backup da sua biblioteca numa pasta que você escolhe (ex.: uma
  pasta sincronizada do OneDrive/Google Drive). O app nunca envia nada sozinho.
- 🌍 **8 idiomas** — português, inglês, espanhol, francês, alemão, italiano, japonês e
  chinês. Na primeira execução o idioma é escolhido automaticamente.
- 🦫 **Seu, offline** — funciona 100% offline, sem cadastro, sem telemetria.

---

## 🔒 Privacidade — offline-first de propósito

O Beaverly Shelf funciona **100% offline e sem conta**. Sua biblioteca, importações,
leitura, anotações e backups são todos locais. A única coisa que toca a rede é o que
**você clica explicitamente** — a busca opcional de capa/metadados (que envia só o
título/autor/ISBN pesquisado, nunca seus arquivos) ou o botão "buscar na web" do leitor.
Nada é enviado automaticamente, não há telemetria, e a conta Beaverly é **opcional**.

---

## 🧩 Ecossistema Beaverly

O Beaverly Shelf é a peça de desktop de um ecossistema maior de leitura. Conheça o resto
em **[beaverly.com.br »](https://beaverly.com.br)**

| App | O que é | Onde |
| --- | --- | --- |
| 🌐 **Beaverly** | A rede social de leitura — catálogo, estantes, progresso, avaliações, metas, clubes. | [beaverly.com.br](https://beaverly.com.br) |
| 🖥️ **Beaverly Shelf** | Este app — gerenciador de biblioteca + leitor para Windows e Linux. | *Você está aqui* |
| 🧭 **Beaverly Companion** | Extensão de navegador para salvar livros e grifos enquanto navega. | Chrome · Edge · Firefox |
| 🗣️ **Beaverly Voice** | Pergunte ao Beaverly na Alexa e no Google Assistente. | [voice.beaverly.com.br](https://voice.beaverly.com.br) |
| 📱 **Beaverly para Android** | Leia e acompanhe seus livros no celular. | *(em breve na Google Play)* |

> ℹ️ Os links e a disponibilidade nas lojas ficam em **[beaverly.com.br](https://beaverly.com.br)** — a fonte oficial.

---

## 📸 Capturas de tela

<!-- Adicione capturas reais em docs/screenshots/ e referencie aqui.
     Sugestão de arquivos: library.png, reader.png, detail.png, onboarding.png.
     Dica: capture em 1280×800 nos temas claro e escuro. -->

| Biblioteca | Leitor |
| --- | --- |
| ![Biblioteca](docs/screenshots/library.png) | ![Leitor](docs/screenshots/reader.png) |

| Detalhes do livro | Primeira execução |
| --- | --- |
| ![Detalhes](docs/screenshots/detail.png) | ![Introdução](docs/screenshots/onboarding.png) |

*(Se as imagens acima aparecerem em branco, elas ainda não foram adicionadas — veja
[docs/screenshots/](docs/screenshots/).)*

---

## 🗺️ Roadmap

- [x] Instalador Windows (`.exe`)
- [x] Pacotes Linux (AppImage + `.deb`)
- [x] Interface em 8 idiomas
- [ ] Publicação na **Microsoft Store** (MSIX) — [guia de publicação](docs/publishing-stores.md)
- [ ] Publicação na **Ubuntu / Snap Store** (snap) — [guia de publicação](docs/publishing-stores.md)
- [ ] Instaladores assinados (remove o aviso do SmartScreen)
- [ ] Versão para macOS

---

## 💬 Feedback e problemas

Achou um bug ou tem uma ideia? **[Abra uma issue »](https://github.com/giindevs/beaverly/issues/new)**
— inclua seu sistema operacional, a versão do app e como reproduzir.

Você também pode enviar feedback dentro do próprio app (**"Fale conosco"**).

---

## ❓ Perguntas frequentes

**Preciso criar conta?**
Não. O Beaverly Shelf funciona 100% offline; a conta é opcional.

**Ele envia meus livros para algum lugar?**
Não. Os arquivos ficam na sua máquina. Só as buscas online (opcionais, iniciadas por
você) enviam um termo de busca (título/autor/ISBN) — nunca seus arquivos.

**É gratuito?**
Sim — o app é grátis para baixar e usar.

**O Windows diz que o arquivo é inseguro. É vírus?**
Não. O instalador ainda não é assinado, então o SmartScreen avisa no primeiro uso.
Clique em *Mais informações → Executar assim mesmo*. A assinatura está no roadmap.

**Onde ficam meus dados?**
Suas bibliotecas são pastas autocontidas que você escolhe. As configurações do app
ficam em `~/.shelf` (ou `%USERPROFILE%\.shelf` no Windows).

---

## 📝 Licença

O Beaverly Shelf é um software proprietário, gratuito para baixar e usar.
© Beaverly. Todos os direitos reservados. A marca, o mascote e o app são propriedade
da Beaverly.

> _Mantenedores: confirmem aqui a licença/os termos exatos antes de publicar._

---

<p align="center"><sub>Feito com 🦫 pela equipe Beaverly.</sub></p>
