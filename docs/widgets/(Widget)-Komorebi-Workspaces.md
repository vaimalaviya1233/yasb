# Komorebi Workspaces Widget
| Option                     | Type    | Default                  | Description                                                                 |
|----------------------------|---------|--------------------------|-----------------------------------------------------------------------------|
| `label_offline`          | string  | `'Komorebi Offline'`     | The label to display when Komorebi is offline.                              |
| `label_workspace_btn`    | string  | `'{index}'`              | The format string for workspace buttons.                                    |
| `label_workspace_active_btn` | string | `'{index}'`              | The format string for the active workspace button.                          |
| `label_workspace_populated_btn` | string | `'{index}'`              | The format string for the populated workspace button.                          |
| `label_default_name`       | string  | `''`                     | The default name for workspaces.                                            |
| `label_float_override`     | string  | `'Override Active'`                     | The label to display when Komorebi is Float Override Active. |
| `toggle_workspace_layer`  | dict    | `{'enabled': false, 'tiling_label': 'Tiling', 'floating_label': 'Floating'}` | Controls toggling between tiling and floating layers.  |
| `hide_if_offline`       | boolean | `false`         | Whether to hide the widget if Komorebi is offline.                          |
| `label_zero_index`        | boolean | `false`    | Whether to use zero-based indexing for workspace labels.                    |
| `hide_empty_workspaces`  | boolean | `false`      | Whether to hide empty workspaces.                                           |
| `animation`  | boolean | `false`      | Buttons animation.                                           |
| `container_padding`  | dict | `{'top': 0, 'left': 0, 'bottom': 0, 'right': 0}`      | Explicitly set padding inside widget container.

## Example Configuration

```yaml
komorebi_workspaces:
  type: "komorebi.workspaces.WorkspaceWidget"
  options:
    label_offline: "Komorebi Offline"
    label_workspace_btn: "\udb81\udc3d"
    label_workspace_active_btn: "\udb81\udc3e"
    label_workspace_populated_btn: "\udb81\udc3e"
    label_default_name: ""
    label_zero_index: false
    hide_empty_workspaces: false
    hide_if_offline: false
    animation: true
    toggle_workspace_layer:
      enabled: false
      tiling_label: "Tiling"
      floating_label: "Floating"
    container_padding: 
      top: 0
      left: 8
      bottom: 0
      right: 8
```

## Description of Options
- **label_offline:** The label to display when Komorebi is offline.
- **label_workspace_btn:** The format string for workspace buttons, can be icon, {name} or {index}.
- **label_workspace_active_btn:** The format string for the active workspace button, can be icon, {name} or {index}.
- **label_workspace_populated_btn:** The format string for the populated workspace button, can be icon, {name} or {index}.
- **label_default_name:** The default name for workspaces.
- **label_float_override:** The label to display when Komorebi is Float Override Active.
- **toggle_workspace_layer:** Controls toggling between tiling and floating layers.
  - **enabled:** Whether to enable the workspace layer toggle functionality.
  - **tiling_label:** The label to display for the tiling layer.
  - **floating_label:** The label to display for the floating layer.
- **hide_if_offline:** Whether to hide the widget if Komorebi is offline.
- **label_zero_index:** Whether to use zero-based indexing for workspace labels.
- **hide_empty_workspaces:** Whether to hide empty workspaces.
- **animation:** Buttons animation.
- **container_padding:** Explicitly set padding inside widget container.


## Style
```css
.komorebi-workspaces {} /*Style for widget.*/
.komorebi-workspaces .widget-container {} /*Style for widget container.*/
.komorebi-workspaces .ws-btn {} /*Style for buttons.*/
.komorebi-workspaces .ws-btn.populated {} /*Style for buttons which contain window and are not empty.*/
.komorebi-workspaces .ws-btn.active {} /*Style for the active workspace button.*/
.komorebi-workspaces .ws-btn.button-1 {} /*Style for first button.*/
.komorebi-workspaces .ws-btn.button-2 {} /*Style for second  button.*/
.komorebi-workspaces .float-override {} /*Style for float override text and icon.*/
.komorebi-workspaces .workspace-layer {} /*Style for workspace layer text and icon.*/
.komorebi-workspaces .workspace-layer.tiling {} /*Style for workspace layer text and icon when in tiling mode.*/
.komorebi-workspaces .workspace-layer.floating {} /*Style for workspace layer text and icon when in floating mode.*/
```

> [!NOTE]  
> You can use `button-x` to style each button separately. Where x is the index of the button.
