# moodle-customfield_dynamic
 This is a course customfield plugin

> **Fork for AVASUS 3.** [forks-by-kelsoncm/moodle-customfield_dynamic](https://github.com/forks-by-kelsoncm/moodle-customfield_dynamic)
> of [soorajsingh/moodle-customfield_dynamic](https://github.com/soorajsingh/moodle-customfield_dynamic)
> (2021020712, "Version for Moodle 3.7 onwards"), with fixes for Moodle 4.5 and 5.3 offered back upstream.
> Changes are listed in [CHANGELOG.md](CHANGELOG.md).

## Installation
 Intall this plugin directly from UI.
  Site Administration  => Plugin => install plugin  

## Use
    1) Add Dynamic Dropdown Menu field in Course customField
    2) In SQL query field, enter the SQL statement with two select field id and data
        For Eg: select id, data from table_name
    3) Now add / edit a course and select the option from dropdown menu

## Stored value
The value is stored as the selected ids separated by comma (for example `4,15,16`). `data_controller::get_value()`
returns that string, as core expects for backup and restore; `data_controller::get_values()` returns the list of ids.
