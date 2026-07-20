## 👽 :29/06/2026

# Component Blog Category

Ajustar @src\components\blog\blog-post-grid.tsx para carregar post de acordo com a categoria
Adicionar 


---

## 👽 :26/06/2026 ---------------------------------------------------

---

# Blog Category

Serão duas implementação

- Implantar sistema de categorização para os posts. 
Ter uma tabela para inserir as categorias.
Relacionar com a tabela de posts.
No frontend página de blog ter uma navegação e filtro de categorias.
Não será implantado o CRUD de Categorias. Apenas o sistema de categorias para o frontend a partir da banco de dados.
Os valores iniciais serão imputados pelo migrations. 
Outros valores serão injetados direto no bando de dados por outro sistema  externo ao projeto.

---

## 🛠️ The Optimized Prompt (EN)

```xml
<task>
Implement a post categorization system linking the database architecture to the frontend blog navigation and filtering, without building a category CRUD.
</task>

<context>
- Category management (Create, Read, Update, Delete) will NOT be implemented in this project.
- Initial category values will be seeded via migrations.
- Future categories will be injected directly into the database by an external system.
- The system only needs to read categories from the database and apply them to the frontend.
</context>

<requirements>
1. **Database & Schema:**
   - Create a `categories` table.
   - Establish a relationship between the `posts` table and the `categories` table (e.g., Many-to-One or Many-to-Many, depending on existing schema).
   - Create a migration file to populate the initial seed data for categories.

2. **Frontend (Blog Page):**
   - Implement a navigation bar/menu displaying the available categories fetched from the database.
   - Implement a filtering mechanism so selecting a category dynamically filters the visible posts.
</requirements>

<instructions>
Review the existing database configuration and blog page implementation. Provide the migration script and the necessary frontend component updates to handle the dynamic filtering based on the new schema relationship.
</instructions>

```

---

# Blog Category - Search

- Implantar um sistema de busca para os posts com capacidade de buscar em todos os posts utilizando de tecnologia ajax assíncrono com interface UI Design com loader quando busca, preview quando digita no campo search após 3 letras (autocomplete - busca preditiva - Search-as-you-type) e filtro por categorias.

---

### 📝 The Pure XML Prompt (EN)

```xml
<task>
Implement an asynchronous, AJAX-powered search system for blog posts featuring a predictive search-as-you-type UI, dynamic loader, preview results, and category filtering.
</task>

<context>
- The search mechanism must query across all available posts.
- The user interface must handle real-time states seamlessly (idle, loading, active typing, and results preview).
- Category filtering needs to work in tandem with the search queries.
</context>

<requirements>
1. **Search-as-you-type (Predictive Autocomplete):**
   - Trigger the search automatically after the user types at least 3 characters.
   - Implement a debounce mechanism to prevent excessive API calls while typing.
   - Display a preview dropdown or panel showing matching post results.

2. **Asynchronous UX/UI States:**
   - Integrate an active loading indicator (spinner/loader) that triggers during the asynchronous data fetch.
   - Smoothly update the DOM/state with the fetched results without reloading the page.

3. **Combined Filtering:**
   - Ensure the search function respects the selected category filter, allowing users to narrow down search results within a specific category.
</requirements>

<instructions>
Analyze the existing frontend blog page and search endpoint. Provide the JavaScript/TypeScript logic for the asynchronous search execution (including debounce and threshold checks), the loading state UI integration, and the updated post-fetching logic that combines text search with category filtering.
</instructions>

```

---

### 🧠 Dicas de Engenharia de Prompt & Vocabulário (PT-BR)

Para este prompt, elevamos o nível técnico dos termos para garantir que a IA não crie uma busca simples síncrona que dependa de um botão de "Enviar".

* **"Debounce mechanism":** Esta é a palavra-chave mais importante aqui. Em sistemas de *Search-as-you-type*, se o usuário digita "React", o sistema dispararia 5 requisições seguidas (uma para R, Re, Rea, Reac, React). O *debounce* atrasa a requisição por alguns milissegundos até o usuário parar de digitar. Usar esse termo evita que a IA gere código ineficiente que derrube o seu servidor.
* **"Threshold" (Check de 3 letras):** Em vez de dizer de forma genérica "check after 3 letters", o termo técnico é *character threshold*. No prompt, especificamos isso claramente em *Requirements*.
* **"In tandem / Combined filtering":** Quando você quer que dois filtros funcionem juntos (buscar a palavra "SaaS" *dentro* da categoria "Negócios"), usamos expressões como *work in tandem* ou *combined filtering*. Isso impede que a IA faça um filtro anular o outro.

