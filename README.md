Library Management System

Rules:
1. The library has books and magazines.
2. Each book is identified the unique by ISBN (International Standard Book Number, string of length 13). The title, publisher, authors (may be more than one author), year of publication (later than 1900) are also recorded.
3. Each magazine is identified by ISSN (International Standard Serial Number, string of length 8). The title and publisher are recorded for each magazine.
4. A magazine may have several issues, each of which is identified by volume number, issue number (both are positive integers) and ISSN of the magazine. The publication date (later than 01/01/1900) is also recorded for each issue.
5. Publishers have unique name and website. We also record the address (city, state and country) of a publisher.
6. Materials in the library includes both books and magazine issues. The library has one or more copies of each material. Each copy is identified by its unique ID (the value is between 1000000 and 9999999), i.e. each ID identifies a unique item in the library. The purchase date and price are also recorded for each copy. A flag is also used to represent whether the copy is lost.
7. Readers of the library have unique ID. Names of readers are also recorded.
8. There are two types of readers: faculty and student. A reader must be either a faculty or a student, not both.
9. Faculties may reserve materials (materials not copies). For each reservation, we record the date of reservation and expiration date. When a reservation is closed (expired, fulfilled or canceled), we also record the close date.
10. When a reader borrows a copy from the library, a record is generated. Each record is identified by the combination of the reader, the copy and the checkout time. For each record, we need to store its checkout time, due date, return date (null value before return).
11. There may be some fines related to a checkout record. Each fine is identified by the checkout record and the reason of fine (must be chosen from “lost copy”, “damaged copy”, “late return”, “others”). One checkout record may have several fines with different reason (e.g. damaged copy + late return). The amount of fine, issue date and payment date are also recorded.