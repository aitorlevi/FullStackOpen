sequenceDiagram
participant user
participant browser
participant server

    user->>browser: Fill input text
    user->>browser: Click button Save
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: 201 Created
    deactivate server

    Note right of browser: The js file updates data.json
