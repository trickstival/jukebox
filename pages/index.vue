<template>
  <div class="app">
    <div class="media">
      <div class="toolbar">
        <h3>Indiespensavel</h3>
      </div>
      <!-- <div class="meta">
        <p class="player">Salomão está reproduzindo</p>
        <h2 class="title">Parcels - Bemyself</h2>
      </div>-->

      <div class="video"></div>

      <div class="actions">
        <button>Gostei</button>
        <button>Não Gostei</button>
        <button>Salvar</button>
      </div>

      <div class="dj-area">
        <p class="active-playlist">
          Playlist:
          <strong>Nome da playlist</strong>
        </p>
        <p class="next-song">
          Sua proxima música:
          <strong>Nome da musica aqui</strong>
        </p>
      </div>
    </div>
    <div class="side">
      <div class="chat">
        <ul class="messages">
          <li
            v-for="i in 50"
            :key="i"
            :class="['message', { my: i % 3 === 0 }]"
          >
            <div class="bubble">
              <p class="message-user">Salomão</p>
              <p class="message-body">
                {{ String('a as').repeat(Math.floor(Math.random() * 50)) }}
              </p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {}
}
</script>

<style>
.app {
  display: flex;
  background: #000
    url('https://img5.goodfon.com/original/1366x768/f/9b/cloudnone-wish-music-cover-monstercat.jpg');
}

.toolbar {
  height: 50px;
  display: flex;
  align-items: center;
  padding: 1em;
}

.media {
  flex: 1;
}

.meta {
  padding: 1.618em;
  text-shadow: 2px 2px 0 #000;
}

.meta .player {
  opacity: 0.82;
  margin-top: 0.25em;
}

.side {
  width: 360px;
  height: 100vh;
  display: flex;
}

.chat {
  flex: 1;
}

.messages {
  list-style: none;
  height: 100%;
  overflow: auto;
}

.message {
  margin: 0.809em;
}

.message .bubble {
  display: inline-block;
  flex: 0 auto;
  padding: 0.809em;
  background: #fff;
  color: #1b1b1b;
  border-radius: 0 1em 1em 1em;
  max-width: 90%;
  text-align: left;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.25);
  font-size: 14px;
}

.message.my {
  border-radius: 1em 1em 0 1em;
  text-align: right;
}

.message.my .bubble {
  border-radius: 1em 1em 0 1em;
  background: #4332b2;
  color: #fff;
}

.message-user {
  font-weight: bold;
  margin: 0 0 0.25em 0;
}

.video {
  width: 486px;
  height: 271px;
  background: #000;
  margin: 0 auto;
}

.actions {
  text-align: center;
  margin: 1.618em 0;
}

.actions button {
  padding: 0.5em 1em;
}

.dj-area {
  background: #fff;
  color: #1b1b1b;
  padding: 0.8em;
  margin: 0 auto;
}
</style>
