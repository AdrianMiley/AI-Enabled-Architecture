#   Contributing to the Project

##  Tools Used

| Tool           | Purpose                                  |
|----------------|------------------------------------------|
| IntelliJ       | My IDE of choice                         |
| Markdown       | For all Text based documents             |
| Mermaid        | For simple diagrams                      |
| ANTLR          | For defining structured english grammars |
| YAML or JSON   |                                          |
| GitHub         | For version control                      |
| GitHub Copilot |                                          |

##  Maintaining Markdown Files

###  Adding New Section

Each directory in the repository represents a different section of the documentation.

When adding a new section to the documentation, 
1.   Create a new directory for that section mnaming the directory in Upper Camel Case.
2.   Each directory must contain an index.md file which serves as the landing page for that section of the documentation.
3.   The index.md YAML header must include a title which is the name of the section and should be the Title Case equivalent of the directory name.
4.   The index.md YAML header should include a brief description of the content of that section and Markdown links to the individual pages within it.
5.   The index.md YAML header should also include a list of children which are the individual pages within that section. 
6.   The first text line is the H1 title of the section and should be the same as the title in the YAML header.

For example, to add a new section on "Integration Patterns", you would create a new directory called "IntegrationPatterns" and add an index.md file to it with the following content:

    ---
    title: Integration Patterns
    description: Patterns for integrating different systems and components in a distributed process environment
    children:
    ---
    #   Integration Patterns

    ...some introductory text about the content of the Practices section...

The "children" section of the YAML header would be updated as new pages are added to the section.

###  Adding New Documents

Each Document should be created as a Markdown file (.md) and placed in the appropriate directory based on its content.

All Documents should have a YAML header section with the following minimum information:
1.   The YAML header must include a title which is the name of the section and should be the Title Case equivalent of the directory name.
2.   The YAML header should include a brief description of the content of that section and Markdown links to the individual pages within it.
3.   The YAML header should also include a list of children which are the individual pages within that section.
4.   The first text line is the H1 title of the section and should be the same as the title in the YAML header.

For example, to add a new page on "Event Based Messaging" to the Practices section, you would create a new file called "EventBasedMessaging.md" in the IntegrationPatterns directory with the following content:

    ---
    title: Event Based Messaging
    description: Patterns for implementing event based messaging in a distributed process environment
    ---
    #   Event Based Messaging

### Update index.md

Whenever pages are added to any directory update the index.md file in that directory to 
1.  include the new page to the list of children 
2. add the new page to the list of Markdown links in the content of the index.md file.

For example, to add a new page called NamingConventions.md to the Practices folder, you would update Practices/index.md to include NamingConventions (without the MD extension) in the list of children as follows:

    ---
    title: Integration Patterns
    description: Patterns for integrating different systems and components in a distributed process environment
    children:
    -   EventBasedMessaging
    ---
    #   Integration Patterns
    ...some introductory text about the content of the Integration Patterns section...

    - [Event Based Messaging](EventBasedMessaging.md)

###  Navigation

Every page should have a "Back" link to its parent index.md file and every index.md file should have a "Home" link to the root index.md file. 
This allows for easy navigation through the documentation.

    ---
    title: Event Based Messaging
    description: Patterns for integrating different systems and components in a distributed process environment
    ---
    #   Event Based Messaging

    ...text content...

    [Back](../index.md) [Home](../index.md)  
