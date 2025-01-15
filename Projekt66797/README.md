## Wprowadzone zmiany w projekcie

1. **Poprawa ścieżki do pliku statycznego (obrazka):**
    - Zmieniono nazwę folderu `static.images` na standardowy folder `static/images`, zgodnie z konwencją Spring Boot.
    - Zmieniono ścieżkę w szablonie `greeting.html` z:
      ```html
      <img th:src="@{/static.images/Vistula.png}" />
      ```
      na:
      ```html
      <img th:src="@{/images/vistula.png}" />
      ```

2. **Dodanie plików szablonów Thymeleaf:**
    - Stworzono plik `greeting.html` w folderze `src/main/resources/templates` do obsługi endpointu `/greeting`.
    - Opcjonalnie dodano `index.html` jako stronę startową dla endpointu `/`.

3. **Zmiana kontrolera:**
    - Użyto adnotacji `@Controller` zamiast `@RestController`, aby obsługiwać widoki w szablonach Thymeleaf.
    - W metodzie `greeting` dodano przekazywanie zmiennych do modelu (np. imienia podanego w parametrze `name`).
---

Dzięki tym zmianom aplikacja działa poprawnie w trybie MVC z Thymeleaf, obsługując zarówno dynamiczne generowanie stron, jak i statyczne zasoby.