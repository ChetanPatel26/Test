@RestController
@RequestMapping("/api/books")
public class BookController {

    // For the sake of simplicity, let's use a static list
    private static List<Book> books = Arrays.asList(
        new Book(1L, "Spring Boot Guide", "John Doe"),
        new Book(2L, "Learning Spring", "Jane Smith")
    );

    @GetMapping
    public List<Book> getAllBooks() {
        return books;
    }

    @GetMapping("/{id}")
    public Book getBookById(@PathVariable Long id) {
        return books.stream().filter(book -> book.getId().equals(id)).findFirst().orElse(null);
    }
}
