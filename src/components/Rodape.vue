<template>
  <footer class="rodape paragrafo">
    <p>
      Desenvolvido por 
      <a href="https://github.com/yoruwitch" target="_blank">Evelyn Fernandes</a> 
      & Alura | 2025 - Projeto fictício sem fins comerciais.
    </p>
  </footer>
</template>


<style scoped>

.rodape {
  background: var(--verde-escuro, #263A29);
  padding: 1.5rem 7.5rem;
  display: flex; 
  justify-content: center; 
  align-items: center; 
  text-align: center; 
  flex-wrap: nowrap;
  gap: 0.5rem; 
}

a {
  text-decoration: none;
  color: var(--creme);
  margin: 0;
  padding: 0;
  white-space: nowrap;
}




@media only screen and (max-width: 1300px) {
  .rodape {
    padding: 1.5rem 3.75rem;
  }
}

@media only screen and (max-width: 767px) {
  .rodape {
    padding: 1.5rem;
  }
} 
</style>
