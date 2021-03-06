### Installation

1. Install [Package Control](https://packagecontrol.io/installation)
2. Run `git clone https://github.com/monkape/sublime-text-config {DATA DIRECTORY}/Packages/User`
3. Open Sublime Text
4. Run `git reset --hard` (in case Package Control fails to restore theme/scheme)


### Additions

Setting | Description
------- | -----------
<a name="_auto_convert_indentation"></a>[**`_auto_convert_indentation`**][_auto_convert_indentation] | Reflect user's indentation settings in open files automatically. See [`convert_indentation`](#convert_indentation)
<a name="_trim_file_on_save"></a>[**`_trim_file_on_save`**][_trim_file_on_save] | Remove leading and trailing whitespace from a file when saving it. See [`trim_file`](#trim_file)
<a name="_auto_close_find_panel"></a>[**`_auto_close_find_panel`**][_auto_close_find_panel] | Close find panel once it loses focus.
<a name="_highlight_find_selection"></a>[**`_highlight_find_selection`**][_highlight_find_selection] | Highlight find selection while panel is open.


Command | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Args&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description
------- | ---- | -----------
<a name="convert_indentation"></a>[**`convert_indentation`**][convert_indentation] | | Convert indentation to reflect the user's settings. See [`_auto_convert_indentation`](#_auto_convert_indentation)
<a name="trim_file"></a>[**`trim_file`**][trim_file] | | Remove leading and trailing whitespace from a file. See [`_trim_file_on_save`](#_trim_file_on_save)
<a name="toggle_fold_by_level"></a>[**`toggle_fold_by_level`**][toggle_fold_by_level] | `level` : `int` | Fold/unfold regions of given indentation level. If folded regions exist they are unfolded, else code is folded.
<a name="unfold_by_level"></a>[**`unfold_by_level`**][unfold_by_level] | `level` : `int` | Unfold regions of given indentation level.
<a name="toggle_case"></a>[**`toggle_case`**][toggle_case] | | Swap case of characters in selection based on first non-whitespace character. Work on word if selection is empty.
<a name="toggle_line_numbers"></a>[**`toggle_line_numbers`**][toggle_line_numbers] | | Toggle `line_numbers` setting at window level based on active view.
<a name="next_view_in_group"></a>[**`next_view_in_group`**][next_view_in_group] | | Select the next neighbouring file within group.
<a name="prev_view_in_group"></a>[**`prev_view_in_group`**][prev_view_in_group] | | Select the previous neighbouring file within group.
<a name="unselect_lines"></a>[**`unselect_lines`**][unselect_lines] | `forward` : `bool` | Remove first or last selection based on `forward`.
<a name="expand_selection_to_paragraph_sub"></a>[**`expand_selection_to_paragraph_sub`**][expand_selection_to_paragraph_sub] | | Subtract paragraph enclosing the mouse position from selection.
<a name="set_find_string"></a>[**`set_find_string`**][set_find_string] | `string` : `str` | Set `string` as "find" input field of find panels.
<a name="set_replace_string"></a>[**`set_replace_string`**][set_replace_string] | `string` : `str` | Set `string` as "replace" input field of find panels.
<a name="toggle_regex_ext"></a>[**`toggle_regex_ext`**][toggle_regex_ext] | | Run `toggle_regex` regardless of find panels being open, and make it trigger command listeners.
<a name="toggle_case_sensitive_ext"></a>[**`toggle_case_sensitive_ext`**][toggle_case_sensitive_ext] | | Run `toggle_case_sensitive` regardless of find panels being open, and make it trigger command listeners.
<a name="toggle_whole_word_ext"></a>[**`toggle_whole_word_ext`**][toggle_whole_word_ext] | | Run `toggle_whole_word` regardless of find panels being open, and make it trigger command listeners.
<a name="find"></a>[**`find`**][find] | `forward` : `bool` <br> `expand` : `bool` <br> `under` : `bool` <br> `additive` : `bool` <br> `skip` : `bool` <br> `all` : `bool` <br> `open_panel` : `bool` <br> `panel` : `string` <br> `close_panel` : `bool` | Wrapper around `find_next`, `find_prev` and `find_all` commands that makes them always respect whole word and case sensitive settings, regardless of initial selection or panel having focus or not. <br> <br> Also supports `find_under_expand_prev` and `find_under_expand_skip_prev` "missing" commands.
<a name="replace"></a>[**`replace`**][replace] | `forward` : `bool` <br> `expand` : `bool` <br> `under` : `bool` <br> `all` : `bool` <br> `open_panel` : `bool` <br> `panel` : `string` <br> `close_panel` : `bool` | Wrapper around `replace_next` and `replace_all` commands that makes them always respect whole word and case sensitive settings, regardless of initial selection or panel having focus or not. <br> <br> Also supports `replace_prev` "missing" command.
<a name="split_selection"></a>[**`split_selection`**][split_selection] | `empty` : `bool` | Run `split_selection_into_lines` or `split_selection_into_chars` if nothing changed. Optionally ignore empty lines.
<a name="split_selection_into_chars"></a>[**`split_selection_into_chars`**][split_selection_into_chars] | | Split selections into characters.
<a name="join_whitespace"></a>[**`join_whitespace`**][join_whitespace] | | Join multi-line selections into a single line; join consecutive whitespace of single-line selections into a single space, or remove all whitespace if none are consecutive.
<a name="wrap_block_ext"></a>[**`wrap_block_ext`**][wrap_block_ext] | `begin` : `str` <br> `end` : `str` | Wrap and reindent the block of code that follows with `begin` and `end` characters, stopping at the first newline.
<a name="toggle_terminus_view"></a>[**`toggle_terminus_view`**][toggle_terminus_view] | [`terminus_open`](https://github.com/randy3k/Terminus#terminus-api) | Focus last used non-terminus view if terminus is active, else focus last used terminus view or create a new one.


### Modifications

Command | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Args&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Description
------- | ---- | -----------
<a name="extend_show_panel"></a>[**`show_panel`**][extend_show_panel] | `panel` : `str` <br> `reverse` : `bool` <br> `toggle` : `bool` | Close active panel regardless of focus when `toggle` is on.
<a name="extend_single_selection"></a>[**`single_selection`**][extend_single_selection] | `reverse` : `bool` | Add `reverse` parameter to control whether first or last selection will remain.
<a name="extend_move_to_group"></a>[**`move_to_group`**][extend_move_to_group] | `group` : `int` | Move sheet to group and focus it, even when last in group.
<a name="close_others_by_index"></a>[**`close_others_by_index`**][close_others_by_index] | `group` : `int` <br> `index` : `int` | Run on active view if called without parameters. Needed for binding to a key.
<a name="close_to_right_by_index"></a>[**`close_to_right_by_index`**][close_to_right_by_index] | `group` : `int` <br> `index` : `int` | Run on active view if called without parameters. Needed for binding to a key.


[convert_indentation]: ./plugin_convert_indentation.py "View source"
[_auto_convert_indentation]: ./plugin_convert_indentation.py "View source"
[trim_file]: ./plugin_trim_file.py "View source"
[_trim_file_on_save]: ./plugin_trim_file.py "View source"
[toggle_fold_by_level]: ./plugin_toggle_fold_by_level.py "View source"
[unfold_by_level]: ./plugin_toggle_fold_by_level.py "View source"
[toggle_case]: ./plugin_toggle_case.py "View source"
[toggle_line_numbers]: ./plugin_toggle_line_numbers.py "View source"
[next_view_in_group]: ./plugin_switch_view_in_group.py "View source"
[prev_view_in_group]: ./plugin_switch_view_in_group.py "View source"
[unselect_lines]: ./plugin_unselect_lines.py "View source"
[expand_selection_to_paragraph_sub]: ./plugin_expand_selection_to_paragraph_sub.py "View source"
[set_find_string]: ./plugin_set_find_string.py "View source"
[set_replace_string]: ./plugin_set_find_string.py "View source"
[extend_show_panel]: ./plugin_extend_show_panel.py "View source"
[extend_single_selection]: ./plugin_extend_single_selection.py "View source"
[extend_move_to_group]: ./plugin_extend_move_to_group.py "View source"
[toggle_regex_ext]: ./plugin_extend_toggle_find_setting.py "View source"
[toggle_case_sensitive_ext]: ./plugin_extend_toggle_find_setting.py "View source"
[toggle_whole_word_ext]: ./plugin_extend_toggle_find_setting.py "View source"
[split_selection]: ./plugin_split_selection.py "View source"
[split_selection_into_chars]: ./plugin_split_selection.py "View source"
[join_whitespace]: ./plugin_join_whitespace.py "View source"
[set_layout]: ./plugin_extend_set_layout.py "View source"
[close_others_by_index]: ./plugin_extend_close_others_by_index.py "View source"
[close_to_right_by_index]: ./plugin_extend_close_others_by_index.py "View source"
[find]: ./plugin_find.py "View source"
[replace]: ./plugin_find.py "View source"
[wrap_block_ext]: ./plugin_wrap_block_ext.py "View source"
[toggle_terminus_view]: ./plugin_toggle_terminus_view.py "View source"
[_auto_close_find_panel]: ./plugin_auto_close_find_panel.py "View source"
[_highlight_find_selection]: ./plugin_highlight_find_selection.py "View source"
