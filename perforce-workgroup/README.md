## Perforce Workgroup

### About Perforce

Perforce is a centralized version control system (CVCS) that tracks and manages changes to software code and other digital assets. It is a popular choice for large-scale development projects because of its scalability, performance, and security.

Perforce uses a client-server architecture, with a single server that stores all of the versions of all of the files in a project. Clients connect to the server to checkout files, make changes, and submit those changes back to the server. This architecture makes Perforce very efficient, as it only requires the client to download the files that it needs to work on.

Perforce also supports a number of features that are important for large-scale development projects, such as:

Branching and merging: Perforce allows developers to create branches of the codebase, which are independent lines of development. This allows developers to work on new features without affecting the main codebase. Perforce also provides powerful merging tools that make it easy to merge changes from different branches back into the main codebase.

Labeling: Perforce allows developers to label specific versions of the codebase. This is useful for identifying specific releases of a product.

Permissions: Perforce allows administrators to control who can access and modify files. This is important for protecting sensitive data and ensuring that only authorized developers can make changes to the codebase.

Perforce is a powerful and versatile version control system that is well-suited for large-scale development projects. It is a popular choice for a variety of industries, including software development, game development, and semiconductor manufacturing.

### About AYON Integration

Perforce integration is important mainly for game engine related media creation. Apart of it's capabilities, Perforce is widely used solution for Unreal project synchronization.

### Decisions

Decisions are in `decisions` folder as simple markdown files with some header
and the reasoning behind the decision. Every decisions must have separate markdown
file, named with tracking code starting with **AYD** (short for AYON Decision) and three digit padded numerical sequence such as **AYD-001**. For more info, use the decision file as a reference.

### Reports

Reports are in `reports` folder in files named `YY/MM/DD-report.md` format. Apart of the report
itself, it must have a date and the name of the reporter.

### Notes

Names can be `name <email@address>` or just names or even github users.
