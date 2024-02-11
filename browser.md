# Browsers
- Main function: Show the resource user has requested from the server
- Resources can be HTML, PDF, Image, etc
- Location of resource is specified by a URI (Uniform Resource Identifier)
- HTML and CSS have specifications which tell browser how to display them
- Specifications are maintained by W3C
- Browser components:
    1. UI 
    2. Browser engine - coordinates and organizes actions between UI and rendering engine
    3. Rendering engine - Responsible for displaying requested content
    4. Networking
    5. JS Interpreter
    6. Data storage - Persistence layer
    7. UI backend

Note: Important for browsers to be able to multiple instances of rendering engine for each tab

## Flow
1. Networking layer sends contents of requested document to rendering engine
2. Rendering engine then parses HTML to make DOM
3. Render tree(CSSOM + DOM) construction 
4. Layout of render tree(give coordinates)
5. Paint the tree(render tree nodes painted using UI backend
- HTML rendered in chunks to show contents to user ASAP

- Error handling is internal and not shown to user. The parser is lenient with bad formatted code and works around it.

Note: Any language that needs to be parsed should be deterministic and may / may not be CFG. HTML is not a CFG whereas CSS is.

# Processing <script>
- The browser executes the <script> tag as soon as it reaches it. The parsing is stopped until the script is not executed.
- If script is external, it should be fetched from the external resource first.
- "defer" changes the halting behavior
- WebKit blocks scripts when they try to access style sheets which are unloaded. Firefox blocks all scripts when stylesheet is being loaded and parsed.

# Render tree
- Purpose of render tree is to be able to paint all the elements in the right order to be displayed.
- Calculating values of render like coordinates, size, etc is called layout (recursive process btw)
