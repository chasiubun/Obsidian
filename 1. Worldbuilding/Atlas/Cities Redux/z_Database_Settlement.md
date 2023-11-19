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
    sortIndex: 1
    width: 219
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
    position: 18
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
    position: 19
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
      source_data: current_folder
  NoteIcon:
    input: select
    accessor: NoteIcon
    key: NoteIcon
    label: NoteIcon
    position: 4
    skipPersist: false
    accessorKey: NoteIcon
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Settlement", value: "Settlement", color: "hsl(212, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
      option_source: manual
  Type:
    input: select
    accessor: Type
    key: Type
    label: Type
    position: 5
    skipPersist: false
    accessorKey: Type
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Thorp", value: "Thorp", color: "hsl(259, 95%, 90%)"}
      - { label: "Hamlet", value: "Hamlet", color: "hsl(168, 95%, 90%)"}
      - { label: "Village", value: "Village", color: "hsl(207, 95%, 90%)"}
      - { label: "Small Town", value: "Small Town", color: "hsl(301, 95%, 90%)"}
      - { label: "Large Town", value: "Large Town", color: "hsl(306, 95%, 90%)"}
      - { label: "Small City", value: "Small City", color: "hsl(324, 95%, 90%)"}
      - { label: "Large City", value: "Large City", color: "hsl(162, 95%, 90%)"}
      - { label: "Metropolis", value: "Metropolis", color: "hsl(344, 95%, 90%)"}
      - { label: "Colony", value: "Colony", color: "hsl(305, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
  Defences:
    input: select
    accessor: Defences
    key: Defences
    label: Defences
    position: 9
    skipPersist: false
    accessorKey: Defences
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Formidable", value: "Formidable", color: "hsl(239, 95%, 90%)"}
      - { label: "Strong", value: "Strong", color: "hsl(293, 95%, 90%)"}
      - { label: "Average", value: "Average", color: "hsl(161, 95%, 90%)"}
      - { label: "Weak", value: "Weak", color: "hsl(274, 95%, 90%)"}
      - { label: "Patheric", value: "Patheric", color: "hsl(342, 95%, 90%)"}
      - { label: "None", value: "None", color: "hsl(217, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
  GovtType:
    input: select
    accessor: GovtType
    key: GovtType
    label: GovtType
    position: 12
    skipPersist: false
    accessorKey: GovtType
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Autocracy", value: "Autocracy", color: "hsl(301, 95%, 90%)"}
      - { label: "Bureaucracy", value: "Bureaucracy", color: "hsl(31, 95%, 90%)"}
      - { label: "Confederacy", value: "Confederacy", color: "hsl(224, 95%, 90%)"}
      - { label: "Democracy", value: "Democracy", color: "hsl(34, 95%, 90%)"}
      - { label: "Dictatorship", value: "Dictatorship", color: "hsl(86, 95%, 90%)"}
      - { label: "Feudalism", value: "Feudalism", color: "hsl(351, 95%, 90%)"}
      - { label: "Gerontocracy", value: "Gerontocracy", color: "hsl(291, 95%, 90%)"}
      - { label: "Hierarchy", value: "Hierarchy", color: "hsl(216, 95%, 90%)"}
      - { label: "Kleptocracy", value: "Kleptocracy", color: "hsl(12, 95%, 90%)"}
      - { label: "Magocracy", value: "Magocracy", color: "hsl(10, 95%, 90%)"}
      - { label: "Matriarchy or Patriarchy", value: "Matriarchy or Patriarchy", color: "hsl(23, 95%, 90%)"}
      - { label: "Meritocracy", value: "Meritocracy", color: "hsl(42, 95%, 90%)"}
      - { label: "Stratocracy", value: "Stratocracy", color: "hsl(242, 95%, 90%)"}
      - { label: "Monarchy", value: "Monarchy", color: "hsl(14, 95%, 90%)"}
      - { label: "Oligarchy", value: "Oligarchy", color: "hsl(72, 95%, 90%)"}
      - { label: "Plutocracy", value: "Plutocracy", color: "hsl(93, 95%, 90%)"}
      - { label: "Republic", value: "Republic", color: "hsl(340, 95%, 90%)"}
      - { label: "Satrapy", value: "Satrapy", color: "hsl(110, 95%, 90%)"}
      - { label: "Theocracy", value: "Theocracy", color: "hsl(174, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
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
    width: 141
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
  Religions:
    input: tags
    accessorKey: Religions
    key: Religions
    id: Religions
    label: Religions
    position: 13
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Sil'jun", value: "Sil'jun", color: "hsl(241, 95%, 90%)"}
      - { label: "Keata", value: "Keata", color: "hsl(311, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Population:
    input: text
    accessorKey: Population
    key: Population
    id: Population
    label: Population
    position: 6
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
  Imports:
    input: tags
    accessorKey: Imports
    key: Imports
    id: Imports
    label: Imports
    position: 14
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Lumber", value: "Lumber", color: "hsl(164, 95%, 90%)"}
      - { label: "Grain", value: "Grain", color: "hsl(96, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Exports:
    input: tags
    accessorKey: Exports
    key: Exports
    id: Exports
    label: Exports
    position: 15
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Lumber", value: "Lumber", color: "hsl(112, 95%, 90%)"}
      - { label: "Grain", value: "Grain", color: "hsl(78, 95%, 90%)"}
      - { label: "Entertainment", value: "Entertainment", color: "hsl(351, 95%, 90%)"}
      - { label: "Games", value: "Games", color: "hsl(169, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Theme:
    input: tags
    accessorKey: Theme
    key: Theme
    id: Theme
    label: Theme
    position: 7
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Gothic", value: "Gothic", color: "hsl(186, 95%, 90%)"}
      - { label: "Victorian", value: "Victorian", color: "hsl(218, 95%, 90%)"}
      - { label: "Medieval", value: "Medieval", color: "hsl(319, 95%, 90%)"}
      - { label: "Las Vegas", value: "Las Vegas", color: "hsl(76, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Rulers:
    input: text
    accessorKey: Rulers
    key: Rulers
    id: Rulers
    label: Rulers
    position: 10
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 129
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Leaders:
    input: text
    accessorKey: Leaders
    key: Leaders
    id: Leaders
    label: Leaders
    position: 11
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 140
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Kingdom:
    input: select
    accessor: Region
    key: Kingdom
    label: Kingdom
    position: 17
    skipPersist: false
    accessorKey: Kingdom
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
      source_data: current_folder
      option_source: manual
  Terrain:
    input: tags
    accessorKey: Terrain
    key: Terrain
    id: Terrain
    label: Terrain
    position: 8
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Hills", value: "Hills", color: "hsl(14, 95%, 90%)"}
      - { label: "Grassland", value: "Grassland", color: "hsl(296, 95%, 90%)"}
      - { label: "Marsh", value: "Marsh", color: "hsl(348, 95%, 90%)"}
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
  PlanetPlane:
    input: select
    accessorKey: PlanetPlane
    key: PlanetPlane
    id: Planet/Plane
    label: Planet/Plane
    position: 16
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
      option_source: manual
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
    width: 173
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      source_data: current_folder
config:
  enable_show_state: false
  group_folder_column: PlanetPlane,Kingdom
  remove_field_when_delete_column: true
  cell_size: compact
  sticky_first_column: true
  show_metadata_created: true
  show_metadata_modified: true
  source_data: current_folder
  source_form_result: root
  show_metadata_tasks: false
  frontmatter_quote_wrap: false
  row_templates_folder: /
  current_row_template: z_templates/TTRPG Vault - Templates 281023/z_Templates/1. DM Templates/1. Story World Templates/Places/Template - Settlement.md
  pagination_size: 10
  source_destination_path: /
  remove_empty_folders: false
  automatically_group_files: true
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