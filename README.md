# Snippet Permalink Updater Action

This GitHub Action automatically updates a Markdown file with a permalink to a specific code snippet.

It's useful for keeping documentation up-to-date with the latest version of your code.

## Features

- Finds a specific snippet in a source file using start and end markers
- Generates a permalink to the snippet, including the latest commit ID
- Updates a specified Markdown file with the new permalink

## Usage

To use this action in your workflow, add the following step:

```yaml
- name: Update Markdown with Snippet Permalink
  uses: Robitx/snippet-permalink-updater-action@v1
  with:
    snippet_file: 'path/to/your/source/file.ext'
    start_marker: 'README_REFERENCE_MARKER_START'
    end_marker: 'README_REFERENCE_MARKER_END'
    markdown_file: 'README.md'
    replace_marker: '<!-- README_REFERENCE_MARKER_REPLACE_NEXT_LINE -->'
