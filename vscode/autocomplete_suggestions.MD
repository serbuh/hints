Disable Accept suggestion on tab:

`Ctrl+Shift+P`: `Preferences: Open Keyboard Shortcuts`
And manually remove bindings that are related to `acceptSelectedSuggestion`

Or edit json `keybindings.json`  
`Ctrl+Shift+P`: `Preferences: Open Keyboard Shortcuts (JSON)`

```json
// Place your key bindings in this file to override the defaults
[
    {
        "key": "tab",
        "command": "-acceptSelectedSuggestion",
        "when": "suggestWidgetHasFocusedSuggestion && suggestWidgetVisible && textInputFocus"
    },
    {
        "key": "tab",
        "command": "-workbench.action.terminal.acceptSelectedSuggestion",
        "when": "simpleSuggestWidgetHasFocusedSuggestion && terminalFocus && terminalHasBeenCreated && terminalIsOpen && terminalSuggestWidgetVisible || simpleSuggestWidgetHasFocusedSuggestion && terminalFocus && terminalIsOpen && terminalProcessSupported && terminalSuggestWidgetVisible"
    }
]
```