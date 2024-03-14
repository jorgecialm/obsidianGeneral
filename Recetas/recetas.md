---

database-plugin: basic

---

```yaml:dbfolder
name: new database
description: new description
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 0
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Fecha:
    input: calendar
    accessorKey: Fecha
    key: Fecha
    id: Fecha
    label: Fecha
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Dificultad:
    input: select
    accessorKey: Dificultad
    key: Dificultad
    id: Dificultad
    label: Dificultad
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Facil", value: "Facil", color: "hsl(100, 95%, 90%)"}
      - { label: "Dificil", value: "Dificil", color: "hsl(255, 95%, 90%)"}
      - { label: "Comlicado", value: "Comlicado", color: "hsl(218, 95%, 90%)"}
      - { label: "✔✔✔✔", value: "✔✔✔✔", color: "hsl(253, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
  Etiquetas:
    input: tags
    accessorKey: Etiquetas
    key: Etiquetas
    id: Etiquetas
    label: Etiquetas
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 273
    options:
      - { label: "en proceso", value: "en proceso", color: "hsl(235, 95%, 90%)"}
      - { label: "Terminado", value: "Terminado", color: "hsl(172, 95%, 90%)"}
      - { label: "Sin empezar", value: "Sin empezar", color: "hsl(60, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  calendario_con_hora:
    input: calendar_time
    accessorKey: calendario_con_hora
    key: calendario_con_hora
    id: calendario_con_hora
    label: calendario con hora
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 240
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Fui:
    input: checkbox
    accessorKey: Fui
    key: Fui
    id: Fui
    label: Fui
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  cantidad:
    input: formula
    accessorKey: cantidad
    key: cantidad
    id: cantidad
    label: cantidad
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
config:
  remove_field_when_delete_column: false
  cell_size: normal
  sticky_first_column: false
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: current_folder
  source_form_result: 
  source_destination_path: /
  row_templates_folder: /
  current_row_template: 
  pagination_size: 10
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
      - field: Dificultad
        operator: CONTAINS
        value: "Facil"
        type: select
      - condition: AND
        disabled: true
        color: "hsl(192, 95%, 90%)"
        filters:
        - field: calendario_con_hora
          operator: CONTAINS
          value: ""
          type: calendar_time
```