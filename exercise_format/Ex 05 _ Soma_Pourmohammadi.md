Exercise 05
class Book:
    def __init__(self, title, author, read=False):
        self.title = title
        self.author = author
        self.read = read

    def __str__(self):
        status = "Read" if self.read else "Unread"
        return f"'{self.title}' by {self.author} - {status}"


class Library:
    def __init__(self):
        self.books = {}

    def add_book(self, title, author, read=False):
        if title in self.books:
            print(f"Book '{title}' already exists in the library.")
        else:
            self.books[title] = Book(title, author, read)
            print(f"Book '{title}' added.")

    def search_by_title(self, title):
        book = self.books.get(title)
        if book:
            print(book)
        else:
            print(f"No book found with title '{title}'.")

    def search_by_author(self, author):
        found = [book for book in self.books.values() if book.author.lower() == author.lower()]
        if found:
            for book in found:
                print(book)
        else:
            print(f"No books found by author '{author}'.")

    def show_all_books(self):
        if self.books:
            for book in self.books.values():
                print(book)
        else:
            print("No books in the library.")

    def show_read_books(self):
        read_books = [book for book in self.books.values() if book.read]
        if read_books:
            for book in read_books:
                print(book)
        else:
            print("No read books found.")

    def show_unread_books(self):
        unread_books = [book for book in self.books.values() if not book.read]
        if unread_books:
            for book in unread_books:
                print(book)
        else:
            print("No unread books found.")

    def show_summary(self):
        total = len(self.books)
        read = sum(book.read for book in self.books.values())
        unread = total - read
        print(f"Total books: {total}")
        print(f"Read books: {read}")
        print(f"Unread books: {unread}")


def main():
    lib = Library()
    while True:
        print("\n=== Personal Library Menu ===")
        print("1. Add a new book")
        print("2. Search book by title")
        print("3. Search books by author")
        print("4. Show all books")
        print("5. Show read books")
        print("6. Show unread books")
        print("7. Show library summary")
        print("8. Exit")
        choice = input("Enter your choice (1-8): ")

        if choice == "1":
            title = input("Enter book title: ")
            author = input("Enter author name: ")
            read_input = input("Have you read this book? (Yes/No): ").lower()
            read = read_input == "Yes"
            lib.add_book(title, author, read)
        elif choice == "2":
            title = input("Enter book title to search: ")
            lib.search_by_title(title)
        elif choice == "3":
            author = input("Enter author name to search: ")
            lib.search_by_author(author)
        elif choice == "4":
            lib.show_all_books()
        elif choice == "5":
            lib.show_read_books()
        elif choice == "6":
            lib.show_unread_books()
        elif choice == "7":
            lib.show_summary()
        elif choice == "8":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")


if __name__ == "__main__":
    main()
