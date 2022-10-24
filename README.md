# `chips.omp.json`

The `passively-active, with cutting edge release` development repository for the Oh-My-Posh Theme Based on Material Design Component: Chips.

[![chips.omp.json highlight #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_1.png)](https://ohmyposh.dev/docs/themes#chips)
[![chips.omp.json highlight #2](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_2.png)](https://ohmyposh.dev/docs/themes#chips)
[![chips.omp.json highlight #3](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_3.png)](https://ohmyposh.dev/docs/themes#chips)

_Designed to be compatible for translucent, dark-and-white influenced background prompts. Based on Material Design Components: Chips, which allows for displayed data to be displayed elegantly. And also, Material Colors were applied varying from A100 to A400 Color Palettes. **More examples below.**_

# Notice

- Version update to `oh-my-posh` repository will be updated once I finished the list from the TODO features. (Which is expected to be somewhere on the 4th week).

## Features

- Color-Adjustable Segments with Palettes
- Color-Changing Segments Based on Activity Context Conditions
- Color Candidates for Segments uses the Material Palette Color from A100 to A400
- Explicitly-Optional-able (Primary Top and Secondary Left Candidates Only) Segments via **Env Vars** on **Powershell Profile**
- Minimalized Console Title
- Python: Version + Virtual Env. Detection Supported
- Transient Prompt with Insights of Previous Recent Execution Time and Command Return Code, Invoked
- Wakatime Daily Tracking Supported

## Installation

1. Click on the [theme file](https://github.com/CodexLink/chips.omp.json/blob/latest/chips.omp.json) in this repository, then right-click the **Raw** button and save it as `chips.omp.json` to your designated directory (_by default it should be at your home directory_).
2. On your powershell profile (`$PROFILE`), invoke the theme to the oh-my-posh arguments.
   > `oh-my-posh --config ~/chips.omp.json --init --shell pwsh | Invoke-Expression`
3. **Restart your prompt** or **_refresh your prompt_** by running the following command: `. $PROFILE` and you are good to go!

## Environment Variables

The theme is designed to be **flexible** as possible by providing users a choice of filling up the following environment variables that allows for a _segment_ to **disappear** or **explicitly otherwise**.

| Env. Var. (Append `DISABLE_SEGMENT` with prefixes `_`) | Type   | Default Value                              | Functionality (Description)                                                                                                                                                                                                                                                                                                                    |
| ------------------------------------------------------ | ------ | ------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ENABLE_ARROW**<br>\_DIVIDER_COLOR_EXECUTION_RETURN   | bool   | **False** _($false)_                       | Allow for the execution return state color to paint the arrow near the input buffer as an additional indication aside from the transient prompt state. See [more samples](#more-samples%3A-uncategorized) for the context.                                                                                                                     |
| \_BATTERY                                              | bool   | **False** _($false)_                       | Hides the `BATTERY` segment found on the top-right of the prompt when value is set to **True** (_$true_).                                                                                                                                                                                                                                      |
| \_DTIME                                                | bool   | **False** _($false)_                       | Hides the `DTIME` segment found on the top-right of the prompt when the value is set to **True** (_$true_).                                                                                                                                                                                                                                    |
| \_PROJECT_CRYSTAL                                      | bool   | **False** _($false)_                       | Hides the `CRYSTAL` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_).                                                                                                                                                                                                       |
| \_PROJECT_FLUTTER                                      | bool   | **False** _($false)_                       | Hides the `FLUTTER` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_).                                                                                                                                                                                                       |
| \_PROJECT_LUA                                          | bool   | **False** _($false)_                       | Hides the `LUA` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_).                                                                                                                                                                                                           |
| \_PROJECT_NODE                                         | bool   | **False** _($false)_                       | Hides the `NODE` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_).                                                                                                                                                                                                          |
| \_PROJECT_RUST                                         | bool   | **False** _($false)_                       | Hides the `RUST` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_).                                                                                                                                                                                                          |
| \_PROJECT_PYTHON                                       | bool   | **False** _($false)_                       | Hides the `PYTHON` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_). This ignores the value of `DISABLE_SEGMENT_PROJECT_PYTHON_VENV`.                                                                                                                                       |
| \_PROJECT_PYTHON_VENV                                  | bool   | **False** _($false)_                       | Hides the `PYTHON_VENV` string display after `venv` detection when the value is set to **True** (_$true_). This ignores the value of `SEGMENT_PROJECT_PYTHON_ACTIVE_VENV_STR`.                                                                                                                                                                 |
| \_PRIMARY_EXEC_TIME                                    | bool   | **False** _($false)_                       | Hides the `execution time` that is shown (in the primary prompt, _top-right_) after a command has been executed.                                                                                                                                                                                                                               |
| \_TRANSIENT                                            | bool   | **False** _($false)_                       | Completely hides the transient segment that contains previous command's return code and execution time when the value is set to `True`. This ignores the value of `DISABLE_SEGMENT_TRANSIENT_EXEC_TIME`.                                                                                                                                       |
| \_TRANSIENT_EXEC_TIME                                  | bool   | **False** _($false)_                       | Hides the `execution time` of the the transient prompt based on the recent command before the transient prompt.                                                                                                                                                                                                                                |
| \_WAKATIME                                             | bool   | **False** _($false)_                       | Hides the `WAKATIME` segment. Note that the segment is still active when `WAKATIME_API_KEY` is valid to be queued for new data. This feature is only useful when you wanted to hide the segment when the prompt's width makes the prompt display undesirable, but still wants it to be accessible later without reconfiguring your `$PROFILE`. |
| **OVERRIDE_FOLDER_BADGE**<br>BG                        | string | `p:c-badge-folder` (theme-defined palette) | Customizes the **background** of the folder segment from the top-left of the prompt display.                                                                                                                                                                                                                                                   |
| **OVERRIDE_FOLDER_BADGE**<br>FG                        | string | `p:c-badge-text` (theme-defined palette)   | Customizes the **foreground** of the folder segment from the top-left of the prompt display.                                                                                                                                                                                                                                                   |
| **SEGMENT_PROJECT**<br>PYTHON_ACTIVE_VENV_STR          | string | None                                       | Alternatively replaces the name of the `venv` that is currently activated from the prompt. This is useful when the length of the name disrespects the space of your input buffer.                                                                                                                                                              |
| **WAKATIME\_**<br>API_KEY                              | string | None                                       | The string that contains the API key that can make the prompt engine queue for new data for every `CACHE_TIMEOUT`.                                                                                                                                                                                                                             |

#### Notes to Consider

1. Please note that these environment variables are purely **optional**, explicitly declaring them is fine, but this does not mean anything unless their values are the opposite of what is provided in their default values.
2. These environment variables are accessible in runtime or once they are loaded. You do not need to modify `$PROFILE` or the theme itself if these changes are temporary. The theme will adjust in an-instant.
3. Despite adjusting the environment variables both via `$PROFILE` and by on runtime, you do not need to restart your prompt for the changes to take effect.
4. Some segments cannot be disabled because they are the vital part of the theme. Those segments are: **Folder**, and **Git**.

## Showcase

Please understood that the theme may look different depending on your configuration such as the font ligatures embedded on your custom font, your prompt and other factors that affects the visuals of your prompt. Please see [my dotfiles](https://github.com/CodexLink/dotfiles-configs-archive) and check the folder `dist/font` and `cli/win32` if you want to get the same feeling (ie. command-hinting, command-shortcut, etc.) and font + glyphs rendering.

> Note that my custom font has issues in regards to single-width and double-width for other icons, some icons went smaller than what is being rendered from the `oh-my-posh` config export renderer.

**Also please note**, the screenshots provided here has a parsing error for the wakatime, rendering the wakatime segment have a same cyan-like color when it shouldn't be, the section showcasing the `On-Spot Prompt Adjustment` and its preceeding sections shows the fixed color render for the wakatime segment, where I just noticed and was able to fix it in `v1.0.0`.

### Environment Variable Render Variants

<div align="center">

[![chips.omp.json env showcase](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_env_variants.png)](https://ohmyposh.dev/docs/themes#chips)

</div>

### Git States Segment

<div align="center">

[![chips.omp.json git states showcase #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_git_states_1.gif)](https://ohmyposh.dev/docs/themes#chips)

[![chips.omp.json git states showcase #2](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_git_states_2.gif)](https://ohmyposh.dev/docs/themes#chips)

</div>

### SSH and Root Privilege State Segments

<div align="center">

[![chips.omp.json ssh and root showcase](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_ssh_and_root_variants.png)](https://ohmyposh.dev/docs/themes#chips)

</div>

### On-The-Spot Prompt Adjustment

_Please note that this is also possible when modifying `$PROFILE`. Just reload the prompt with `. $PROFILE` and the changes will be reflected._

Also note that I adlib this demonstration, more information and other hideable segments in the [Environment Variables section](#environment-variables).

[![chips.omp.json on-the-spot env. change](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_on_the_spot_env_change.gif)](https://ohmyposh.dev/docs/themes#chips)

### Transient Prompt with Insights of Previous Command

<div align="center">

[![chips.omp.json transient showcase](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_transient.gif)](https://ohmyposh.dev/docs/themes#chips)

</div>

## More Samples: Uncategorized

This section contains slightly out-of-context images of the prompt. This may specifically highlights how it looks like after some work done.

More pictures will be added soon, as if I can remember it.

### Time Execution as Spent on `nvim`

[![chips.omp.json, more sample, transient + console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_transient_plus_console_state.png)](https://ohmyposh.dev/docs/themes#chips)

### After pushing something in `git`

[![chips.omp.json, more sample, git push console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_git_push_console_state.png)](https://ohmyposh.dev/docs/themes#chips)

> Bug notice: The 100% battery bar display is already fixed.

### Extra-complicated git status

[![chips.omp.json, more sample, git complicated display console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_git_console_merge_conflict_console_state.png)](https://ohmyposh.dev/docs/themes#chips)

> Context: I was having a hard time with my PR getting conflict to another branch.

### Bare-minimum console display

[![chips.omp.json, more sample, bare-minimum display console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_bare_minimum_console_display_state.png)](https://ohmyposh.dev/docs/themes#chips)

### Convoluted, overdetailed console display

[![chips.omp.json, more sample, convoluted display console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_convoluted_console_display_state.png)](https://ohmyposh.dev/docs/themes#chips)

### Git: Disconnected/unrecognized/no-remote branch status display

[![chips.omp.json, more sample, git unrecognized branch console state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_git_unrecognized_branch.png)](https://ohmyposh.dev/docs/themes#chips)

### Arrow Near Input Buffer, Inherit Execution Return Color as Additional Indicator

[![chips.omp.json, more sample, arrow input buffer inherit execution color state](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/misc_arrow_input_buffer_change_color_with_execution_state.gif)](https://ohmyposh.dev/docs/themes#chips)

## TODO Features

The following are some of the features that I cut off **_for now_**, due to the following: I'm not using it, no other ways for me to test it or install it.

1. Other Programming Language Project Segment
   - [x] Crystal
   - [ ] Flutter
   - [x] Lua
   - [x] Node
   - [x] Rust

> Note that, if you are going to suggest soemthing that is out of this list, you have to make sure that the language is supported from one of the segments offered in **Oh-My-Posh Segment Section**. Otherwise, request a segment feature from the maintainer and let me know if you want to have it included, **once implemented**.

## FAQ

1. The prompt feels quite slow...

   > There are two verdicts. [a] The data being queued from the both local (which is 'git', it parses your branch and repo state, note that I did not use **posh-git** in this theme, see FAQ #5. In terms of being slow, see this [FAQ entry](https://ohmyposh.dev/docs/faq#the-prompt-is-slow-delay-in-showing-the-prompt-between-commands).) and from remote (via HTTP, queueing Wakatime stats (if possible)). And your powershell (`pwsh`) version (You need to upgrade as upstream as possible). The figure below shows the debug output just from typing `oh-my-posh debug`.

2. Why `transient prompt` contains one-liner that contains multiple segments?

   > Accoding to the docs and as per explanation provided by the creator from my [issue](https://github.com/JanDeDobbeleer/oh-my-posh/issues/2605), 'transient prompt` use case is intended to be more simplier than the other prompt because its nature was to provide a clean output from other prompts. With its feature limitation, I want to do more than just that, by providing previous and current insights about the command, I was able to create or manifest the structure of the segment to be more the same as how I display other segment from other prompt.

3. Sometimes my prompt just hangs. Why?

   > If you are using _**Wakatime**_, you have to keep note that the cache time is set to `5m` or 5 minutes by default. Therefore, every 5 minutes, the prompt will do an HTTP request to get the latest upstream of your stats. If you are not using Wakatime and this issue occurs, please investigate the state of the prompt by **debugging** it (_with the use of _ `oh-my-posh debug`). Please let me know with sufficient information if it persists.

4. Why did you not use `posh-git`? You know that `git` segment is slower right?

   > I'm aware. oh-my-posh `posh-git` docs doesn't show any examples or further modification than what is being provided in the `git` segment. While I do understand the compromise of performance over customization, I think its best to customize the output to further understand more about what are the symbols behind them. Because in my perspective, I'm pretty much confused about it. To solve the contention from this issue, I'm hoping that `posh-git` is customizable as `git` segment.

5. When I disabled the "wakatime" segment, why it's still slow?

   > As of now (08/26/2022), there is no switch for the HTTP query to be disabled when a certain environment variable invalidates truthy condition. I suggest trying to nullify the value of your 'WAKATIME_API_KEY' and see if it works or ignores calling HTTP request.

6. What are your basis for the wakatime's timeout values?

   > They were based on my preference with consideration on my ISP speed. Please adjust them from the theme itself. Environment Variables for adjusting parameters such as timeouts were not supported as of 08/29/2022. **_Let me know if it is because I also need it._**

7. Why does the `Code Return` sometimes returns high value of `signed int` or just big numbers?
   > I'm not quite sure why, but usually when a program has crashed, they will return a reference code or sometimes address that points to the point of error. Though this was just an **asumption** but its something related to that.

> Was your question does not relate to what I put here? Let me know in the **Issue** section.

## Tools

- [Material Design's Color Tool](https://material.io/resources/color/) — Create, share, and apply color palettes to your UI, as well as measure the accessibility level of any color combination.
- [regular expressions 101](https://regex101.com/) — Just a regex validator.

## Contribution

- TODO. — _More information coming soon. Have to construct the template._

## Credits

- [JanDeDobbeleer](https://github.com/JanDeDobbeleer/oh-my-posh) for the amazing zsh-like integration for the powershell.
- [Simple Icons](https://simpleicons.org/) for providing some base colors of a certain icons.
- [Sprig](https://masterminds.github.io/sprig/) for the straightforward documentation without making me going insane.
