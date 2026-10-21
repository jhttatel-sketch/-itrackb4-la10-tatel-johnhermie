# Laravel 12 - Lab Activity 10: Your Own Lookup Table

## G1: Which column did you turn into a table, and why that one and not another?

I turned the `genre` information into a separate `genres` table and added a `genre_id` foreign key to the `books` table. I chose genre because multiple books can share the same genre, so storing genres separately avoids repeating genre names and makes them easier to manage.

## G2: What number did screenshot 6 show, and why exactly that number?

Screenshot 6 showed **7 queries**: one query retrieved all six books, and six additional queries retrieved each book's genre individually. This happened because I accessed the `genre` relationship without eager loading.

## G3: Your belongsTo method is named in the singular. What would break if you made it plural?

My `Book` model uses the singular relationship method `genre()` because each book belongs to one genre. If I renamed it to `genres()` without updating the other code, calls such as `with('genre')` and `$book->genre` would fail because Laravel would not find the relationship under the original name.
