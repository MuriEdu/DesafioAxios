# **Desafio Técnico: Consumindo uma API com Axios no Frontend**  
**Objetivo:** Aprender a configurar o Axios, criar um serviço de API e exibir dados em uma aplicação frontend.  

---

## **📌 Requisitos do Desafio**  
Você deverá criar uma aplicação frontend que:  
✅ **Configura o Axios** em um arquivo separado (`api.ts`)  
✅ **Consome uma API pública** e exibe os dados na tela  
✅ **Trata estados de carregamento e erro**  
✅ **Exibe os dados de forma organizada**  

---

## **🔧 API Recomendada**  
Use a **[JSONPlaceholder](https://jsonplaceholder.org/)**, uma API fake para testes:  
🔹 **Endpoint:** `https://jsonplaceholder.org/posts`  
🔹 **Retorna:** Lista de posts (título, corpo e ID)  

---

## **📝 Passo a Passo (Guia de Aprendizado)**  

### **1️⃣ Configurando o Projeto**  
1. Crie um projeto React + TypeScript com Vite:  
   ```bash
   npm create vite@latest nome-do-projeto -- --template react-ts
   cd nome-do-projeto
   npm install axios
   npm run dev
   ```
2. Instale o **Axios** (biblioteca para requisições HTTP).  

---

### **2️⃣ Criando o Arquivo `api.ts`**  
🔹 **O que fazer?**  
- Crie uma pasta `src/api` e dentro dela um arquivo `api.ts`.  
- Configure o Axios com:  
  - `baseURL` (endereço base da API)  
  - `timeout` (tempo máximo de espera)  
  - `headers` (opcional, para definir `Content-Type: application/json`)  

❓ **Como aprender isso?**  
📌 **Documentação do Axios:** [axios-http.com/docs/intro](https://axios-http.com/docs/instance)

---

### **3️⃣ Criando um Componente para Consumir a API**  
🔹 **O que fazer?**  
1. Crie um componente (ex.: `PostsList.tsx`).  
2. Use **useState** para armazenar:  
   - `posts` (dados da API)  
   - `loading` (estado de carregamento)  
   - `error` (mensagem de erro, se houver)  
3. Use **useEffect** para fazer a chamada à API quando o componente carregar.  
4. Trate os estados:  
   - **Carregando:** Exiba "Carregando..."  
   - **Erro:** Mostre uma mensagem de erro  
   - **Sucesso:** Renderize os posts em uma lista  

❓ **Como aprender isso?**  
📌 **Artigo:** [Consumindo uma API com React.JS e Axios](https://www.devmedia.com.br/consumindo-uma-api-com-react-js-e-axios/42900)
📌 **Vídeo:** [Consumindo API com React + Axios](https://www.youtube.com/watch?v=DaVx0R0c5ls)

---

### **4️⃣ Exibindo os Dados na Tela**  
🔹 **O que fazer?**  
- Mapeie os posts e mostre:  
  ```tsx
  {posts.map(post => (
    <div key={post.id}>
      <h3>{post.title}</h3>
      <p>{post.body}</p>
    </div>
  ))}
  ```
- Estilize com CSS (opcional).  

---

### **5️⃣ Desafios Extras (Opcionais)**  
🟡 **Search:** Adicione um campo de busca para filtrar posts pelo título.  
🟡 **Error Handling:** Melhore o tratamento de erros para diferentes tipos de falhas.  

---

## **📤 Entrega do Projeto**  
1. Crie um repositório no GitHub.  
2. Adicione um **README.md** explicando:  
   - Como executar o projeto
   - Faça uma breve descrição de como funciona seu código e o que as principais funções fazem
   - Quais desafios extras foram implementados (se aplicável)  
3. Envie o link para avaliação!  

---

## **🎯 Dicas e Recursos**  
- **Teste sua API** no [Postman](https://www.postman.com/) ou [Insomnia](https://insomnia.rest/) antes de codar.  
- **Debugging:** Use `console.log(response)` para ver os dados retornados.  
- **TypeScript:** Defina uma `interface` para os dados da API.  

**Boa sorte! Se ficar travado, pesquise no Google ou peça ajuda!** 🚀
