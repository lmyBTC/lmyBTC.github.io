# Website Refactoring Plan: Migrate to Tailwind CSS

This document outlines the plan to refactor the entire website from the old CSS structure to a new, modern design based on Tailwind CSS.

## Phase 1: Establish Foundation and Core Articles

*   **Task 1.1: Create a Shared Custom CSS File**
    *   Extract custom styles from the `<style>` block in `core-btc.html` (e.g., `.highlight-term`, `.alert` styles).
    *   Create a new file at `assets/css/custom.css` and place these styles there.
    *   Update the article template to link to this new shared CSS file.

*   **Task 1.2: Refactor the Second Core Article**
    *   Apply the new Tailwind CSS template to `post/core-eth-alt.html`.
    *   Ensure its content is preserved within the new structure.

## Phase 2: Refactor Collection Pages

*   **Task 2.1: Refactor "Core Narrative" Page**
    *   Redesign `post/topic-core.html` using Tailwind CSS.
    *   Rebuild the featured article section and the article grid with the new styling.

*   **Task 2.2: Refactor Main Archive Page**
    *   Completely rebuild `post/archive.html` using Tailwind CSS.
    *   This includes the filter controls and the main article list.

## Phase 3: Refactor Main Site Pages

*   **Task 3.1: Refactor the Home Page**
    *   Rebuild all sections of `index.html` (hero, stats, topics, etc.) using Tailwind CSS.

*   **Task 3.2: Refactor the "About Me" Page**
    *   Apply the new base template to the `about.html` page.

## Phase 4: Migrate All Remaining Articles

*   **Task 4.1: Refactor All Old Articles**
    *   Systematically go through all remaining article files in the `post/` directory and apply the new Tailwind CSS template.

## Phase 5: Cleanup

*   **Task 5.1: Delete Old CSS Files**
    *   Once all pages have been successfully migrated and verified, delete the old, unused CSS files (`main.css`, `assets/css/archive.css`, etc.) to finalize the project cleanup.
