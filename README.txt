🎶 OBS Jukebox Widget

Um widget de **jukebox para OBS**, feito em HTML + JavaScript usando a **YouTube IFrame API**.  
Ele exibe capa, título, autor, barra de progresso e controles básicos de uma playlist/vídeo do YouTube ou YouTube Music.

✨ Funcionalidades

- Exibição da **capa** (thumbnail) da música/álbum.
- **Título** em carrossel animado (quando for maior que o espaço).
- **Autor/canal** abaixo do título.
- **Fundo em degradê** usando cores extraídas da thumbnail.
- **Barra de progresso** com bolinha animada + tempo decorrido/total.
- **Botões funcionais**:
  - ▶️ / ⏸ Play/Pause (ícone alterna automaticamente).
  - ⏭ Próxima faixa.
- **Shuffle ativado por padrão** → as músicas da playlist são tocadas em ordem aleatória.
- **Loop infinito** → quando a playlist acaba, ela reembaralha e continua.
- **Input de link** (playlist ou vídeo único):
  - Salva no navegador (LocalStorage).
  - Esconde automaticamente, mas pode ser reaberto ao passar o mouse na parte superior.

📂 Instalação no OBS

1. Baixe o arquivo `obs_jukebox_widget.html`.
2. No OBS, adicione **Fonte de Navegador**.
3. Marque **"Arquivo local"** e selecione o arquivo.
4. Defina largura/altura (mínimo recomendado: `400x150`).
5. Clique em **OK**.

Agora o widget aparecerá na sua cena!

🎛️ Como usar

1. No widget, cole um link do **YouTube** ou **YouTube Music** (playlist ou vídeo único).
2. Clique em **Carregar**.
3. A música começará automaticamente:
   - Se for **playlist** → modo shuffle e loop automático.
   - Se for **vídeo único** → repete indefinidamente.

Controles no widget
- **Pause/Play** → pausa ou retoma a música.
- **Próxima faixa** → avança para a próxima música aleatória.

Controle de volume
Por padrão o Browser Source do OBS **não envia áudio para o mixer**.  
Para capturar o som:
1. Clique com o botão direito na **Fonte de Navegador** no OBS.
2. Vá em **Propriedades**.
3. Habilite **“Controlar áudio via Mixer do OBS”** (ou equivalente na sua versão).
4. O áudio do Jukebox aparecerá no **Mixer** do OBS, podendo ajustar volume e aplicar filtros.

⚙️ Personalização

No `<style>` do arquivo, você pode ajustar:
- `--accent` → cor dos botões.
- `--progress-fg` → cor da barra de progresso/bolinha.
- `--progress-bg` → cor de fundo da barra.
- Tamanho das fontes (`.title` e `.author`).

🚧 Limitações

- Se um vídeo da playlist não permitir embed, ele será **pulado automaticamente**.
- O áudio **só aparece no Mixer** se você ativar manualmente no OBS (veja acima).
- O carrossel do título é contínuo, mas pode ser ajustado no CSS (`@keyframes scrollText`).

---

💡 Dica: use uma playlist no **YouTube Music** com todas as músicas que você quer e deixe o widget em shuffle. Assim ele nunca repete na mesma ordem e roda infinito na live.
