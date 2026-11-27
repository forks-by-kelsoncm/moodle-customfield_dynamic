# Changelog

## 3.0.0 - 2026-11-27
- Fix course backup, restore and duplication on Moodle 4.5/5.3: `data_controller::get_value()` returned an array
  (`explode()`), which core wrote straight into `course.xml` (`core_text::trim_ctrl_chars(): ... array given`). It
  now returns the stored string (ids separated by comma); restore writes the same string back. The stored format
  does not change.
- New `data_controller::get_values()` and `data_controller::split_values()` for the list of selected ids.
- Multiple selection forms receive the list of ids; the default value is joined without spaces.
- `requires` Moodle 4.5 (2024100700), `supported` 4.5 to 5.3.
- PHPUnit tests for the stored value, display, form data, backup/restore and course duplication.

## 2021020712
- Original release by Sooraj Singh ("Version for Moodle 3.7 onwards").
