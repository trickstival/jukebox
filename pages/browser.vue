<template>
  <div class="page">
    <div class="header">
      <h1>Jukebox</h1>
      <form>
        <input id type="search" placeholder="Buscar salas..." />
        <button type="submit">Pesquisar</button>
      </form>
    </div>
    <div class="tags">
      <a href="#" class="tag">#Rock</a>
      <a href="#" class="tag">#Pop</a>
      <a href="#" class="tag">#Alternativa</a>
      <a href="#" class="tag">+ Adicionar Categoria</a>
    </div>
    <h2>Resultados da busca</h2>
    <div class="grid">
      <div v-for="i in 20" :key="i" class="card">
        <img
          class="card-bg"
          :src="`https://picsum.photos/200/200?sid=cover_${i}`"
          alt
        />
        <div class="card-content">
          <img
            class="card-image"
            :src="`https://picsum.photos/200/200?sid=cover_${i}`"
            alt
          />
          <p class="card-title">Sala {{ i }}</p>
          <p>Nega Odeth - Sanfoneiro da destruição</p>
          <div class="card-footer">
            <div class="tags">
              <a href="#" class="tag">#Rock</a>
              <a href="#" class="tag">#Pop</a>
              <a href="#" class="tag">#Alternativa</a>
            </div>
            <p class="user-count">
              {{ Math.floor(Math.random() * 20) }} pessoas
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
.card {
  background: rgba(255, 255, 255, 0.1);
  color: #e0e0e0;
  border-radius: 0.25em;
  transition: all 0.21s ease;
  cursor: pointer;
  overflow: hidden;
  position: relative;
}

.card-bg {
  position: absolute;
  object-fit: cover;
  width: 100%;
  height: 100%;
  filter: blur(20px) brightness(25%) grayscale(100%);
  transition: all 0.21s ease;
}

.card-image {
  display: block;
  margin-bottom: 1em;
  position: relative;
  z-index: 1;
  width: 100%;
}

.card-title {
  font-weight: bold;
  margin-bottom: 0.5em;
}

.card-content {
  padding: 0.809em;
  position: relative;
  z-index: 1;
  font-size: 14px;
}

.card:hover .card-bg {
  filter: blur(20px) brightness(50%);
}

.card-footer {
  display: flex;
  justify-content: space-between;
  font-size: 0.809em;
  margin-top: 1em;
}

.tags {
  font-size: 11px;
}

.tag {
  display: inline-block;
  color: inherit;
  text-decoration: none;
  margin: 0 0.25em 0 0;
  background: #fff;
  color: #1b1b1b;
  padding: 0.25em 0.5em;
  border-radius: 1em;
  margin: 0 0.25em 0.25em 0;
}

.tag:hover {
  text-decoration: underline;
}

.card .tag {
  background: rgba(255, 255, 255, 0.125);
  color: inherit;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 0.5em;
  margin-top: 1em;
}

.avatar {
  display: inline-block;
  width: 37px;
  height: 37px;
  border-radius: 50%;
}

.header {
  display: flex;
  position: sticky;
  top: 0;
  z-index: 999;
  align-items: center;
  background: #000;
  padding: 0.809em 0;
}

.header form {
  flex: 1;
  margin: 0 0 0 1em;
  display: flex;
  align-items: center;
}

.header input {
  flex: 1;
  display: block;
  background: #1b1b1b;
  border: none;
  border-radius: 0.25em;
  color: #fff;
  padding: 1em;
  outline: none;
  margin-right: 1em;
}

.header .tags {
  margin-top: 0.5em;
}

.header input:focus {
  background: #ffff;
  color: #1b1b1b;
}

h2 {
  margin: 1em 0;
}
</style>
