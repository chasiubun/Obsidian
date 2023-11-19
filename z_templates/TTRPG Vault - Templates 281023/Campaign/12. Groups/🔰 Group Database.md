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
    accessor: __file__
    position: 1
    isHidden: false
    sortIndex: 0
    isSorted: true
    isSortedDesc: false
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
  __created__:
    key: __created__
    id: __created__
    input: calendar_time
    label: Created
    accessorKey: __created__
    isMetadata: true
    isDragDisabled: false
    skipPersist: false
    csvCandidate: true
    accessor: __created__
    position: 11
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
      persist_formula: false
      source_data: current_folder
  __modified__:
    key: __modified__
    id: __modified__
    input: calendar_time
    label: Modified
    accessorKey: __modified__
    isMetadata: true
    isDragDisabled: false
    skipPersist: false
    csvCandidate: true
    accessor: __modified__
    position: 12
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
      persist_formula: false
      source_data: current_folder
  Alignment:
    input: select
    accessor: Alignment
    key: Alignment
    label: Alignment
    position: 6
    skipPersist: false
    accessorKey: Alignment
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Neutral", value: "Neutral", color: "hsl(99, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
  NoteIcon:
    input: select
    accessor: NoteIcon
    key: NoteIcon
    label: NoteIcon
    position: 5
    skipPersist: false
    accessorKey: NoteIcon
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Group", value: "Group", color: "hsl(250, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
      option_source: manual
  AssociatedReligion:
    input: tags
    accessor: AssociatedReligion
    key: AssociatedReligion
    label: AssociatedReligion
    position: 8
    isSorted: false
    isSortedDesc: false
    skipPersist: false
    accessorKey: AssociatedReligion
    isHidden: false
    sortIndex: -1
    options:
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
      option_source: manual
  Type:
    input: tags
    accessor: Type
    key: Type
    label: Type
    position: 7
    skipPersist: false
    accessorKey: Type
    isHidden: false
    width: 128
    sortIndex: -1
    options:
      - { label: "Trade", value: "Trade", color: "hsl(126, 95%, 90%)"}
      - { label: "Mage", value: "Mage", color: "hsl(327, 95%, 90%)"}
      - { label: "Clan", value: "Clan", color: "hsl(51, 95%, 90%)"}
      - { label: "Army", value: "Army", color: "hsl(304, 95%, 90%)"}
      - { label: "Worship", value: "Worship", color: "hsl(81, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
      option_source: manual
  Pronounced:
    input: text
    accessor: Pronounced
    key: Pronounced
    label: Pronounced
    position: 2
    skipPersist: false
    accessorKey: Pronounced
    isHidden: false
    sortIndex: -1
    width: 190
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
  Location:
    input: tags
    accessor: Location
    key: Location
    label: Location
    position: 10
    skipPersist: false
    accessorKey: Location
    isHidden: false
    width: 137
    sortIndex: -1
    options:
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      persist_formula: false
      source_data: current_folder
      option_source: manual
  HQ:
    input: tags
    accessorKey: HQ
    key: HQ
    id: HomeBase
    label: HQ
    position: 9
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Hierarchy:
    input: text
    accessorKey: Hierarchy
    key: Hierarchy
    id: Hierarchy
    label: Hierarchy
    position: 4
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 260
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Aliases:
    input: text
    accessor: Alias
    key: Aliases
    label: Aliases
    position: 3
    skipPersist: false
    accessorKey: Aliases
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
      persist_formula: false
      source_data: current_folder
config:
  enable_show_state: false
  group_folder_column: 
  remove_field_when_delete_column: true
  cell_size: normal
  sticky_first_column: true
  show_metadata_created: true
  show_metadata_modified: true
  source_data: current_folder
  source_form_result: root
  show_metadata_tasks: false
  frontmatter_quote_wrap: false
  row_templates_folder: /
  current_row_template: z_Templates/1. DM Templates/1. Story World Templates/People/Template - Group.md
  pagination_size: 10
  source_destination_path: /
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: top
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  font_size: 16
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
  show_metadata_tags: false
filters:
  enabled: false
  conditions:
```