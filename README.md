# SchemaSculptor
SchemaSculptor is GUI tool that allows you to build pl/psql triggers, instead of coding buggy workflows, you should use this tool instead, which allows you to design your workflow graph, then it will implement corresponding pl/psql triggers. Enjoy !


1. Project Setup

Assigned Team: Setup Team

    Set up the project structure with HTML, CSS, and JS files.
    Integrate required libraries:
        GoJS for the workflow editor.
        Any build tools (e.g., Vite, Webpack) if necessary.
    Create a basic static layout for the palette and workflow editor.
    Test library integration to ensure GoJS and drag-and-drop functionality work as expected.

2. Palette Functionality

Assigned Team: Palette Team
Tasks:

    Create a palette containing block types (State, Transition, Logic).
    Add drag-and-drop functionality for palette items.
    Associate metadata with each block type (e.g., State → {key: 'StateName'}).
    Ensure dragged blocks can be identified when dropped onto the workflow editor.

3. Workflow Editor (GoJS Integration)

Assigned Team: Workflow Editor Team
Tasks:

    Configure GoJS editor with basic node and link templates.
    Allow users to:
        Drop nodes (State, Transition, Logic) into the editor.
        Connect nodes with links (i.e., transitions).
    Add default styles for nodes and links.
    Enable deleting or repositioning nodes and links.

4. State Nodes Implementation

Assigned Team: State Node Team
Tasks:

    When a State block is dropped, prompt the user to enter the state name.
    Add the entered state as a labeled node in the editor.
    Support renaming a state via double-clicking the node.
    Define validation rules for state names (e.g., unique names, alphanumeric).

5. Transition Logic Implementation

Assigned Team: Transitions Team
Tasks:

    Implement transition links:
        Dragging a line between two nodes creates a Transition.
        Store metadata about the source and target states for each link.
    Add labels to transitions (e.g., conditions or triggers).
    Enable editing transition logic by clicking on a link (e.g., opening a configuration modal).

6. Logic Blocks Implementation

Assigned Team: Logic Block Team
Tasks:

    Define logic blocks for operations (e.g., "Update Field X," "Trigger Event").
    Allow logic blocks to be dragged into the workflow editor.
    Support connecting logic blocks to transitions.
    Add a modal or dropdown for configuring block-specific parameters.

7. Dynamic Schema Integration

Assigned Team: Schema Team
Tasks:

    Parse the provided SQL schema into usable data structures.
    Populate the palette dynamically based on the schema:
        Add available states from tables with a status field.
        Add fields/columns as options for logic blocks.
    Ensure the editor dynamically adjusts to changes in the schema.

8. Export/Import Workflow

Assigned Team: Data Persistence Team
Tasks:

    Serialize the workflow design into a JSON format.
        Include nodes, transitions, and metadata.
    Provide functionality to import a saved JSON workflow.
    Add UI buttons for exporting and importing workflows.

9. SQL Trigger Code Generation

Assigned Team: SQL Generator Team
Tasks:

    Convert the workflow (nodes, links, and logic) into SQL TRIGGER definitions.
    Include:
        BEFORE or AFTER triggers.
        INSERT, UPDATE, or DELETE events.
        Custom logic from the workflow (e.g., updating related fields).
    Ensure generated code is clean and error-free.

10. UI Enhancements

Assigned Team: UI/UX Team
Tasks:

    Refine the visual design for palette and editor elements.
    Add animations or visual cues (e.g., highlighting connections or errors).
    Implement responsive styling for different screen sizes.
    Ensure a smooth drag-and-drop experience.

11. Validation and Testing

Assigned Team: Testing Team
Tasks:

    Validate workflows to prevent errors (e.g., unconnected nodes, duplicate states).
    Add automated tests for critical features:
        Drag-and-drop functionality.
        JSON import/export.
        SQL generation correctness.
    Test the application on multiple browsers and devices.

12. Documentation

Assigned Team: Documentation Team
Tasks:

    Create user documentation explaining:
        How to use the tool (design workflows, add logic, etc.).
        How to import/export workflows.
    Write developer documentation for maintaining and extending the tool.

Suggested Timeline:

    Week 1: Teams 1–4: Project setup, palette, and basic GoJS editor.
    Week 2: Teams 5–7: State, transition, and logic implementation.
    Week 3: Teams 8–10: Export/import, SQL generation, and UI enhancements.
    Week 4: Teams 11–12: Validation, testing, and documentation.

Would you like me to expand on any specific task, such as SQL generation or GoJS configurations?
