# chips.omp.json

The `passively-active, with cutting edge release` development repository for the Oh-My-Posh Theme Based on Material Design Component: Chips.

[![chips.omp.json highlight #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_1.png)](https://ohmyposh.dev/docs/themes#chips)
[![chips.omp.json highlight #2](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_2.png)](https://ohmyposh.dev/docs/themes#chips)
[![chips.omp.json highlight #3](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_3.png)](https://ohmyposh.dev/docs/themes#chips)

_Designed to be compatible for translucent, dark-and-white influenced background prompts. Based on Material Design Components: Chips, which allows for displayed data to be displayed elegantly. And also, Material Colors were applied varying from A100 to A400 Color Palettes. **More examples below.**_

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

<div align="center">

| Env. Var.                                  | Type   | Default Value                                                                                                                                                                                                                                                                                                                                  | Functionality (Description)                                                                                                                                                                                     |
| ------------------------------------------ | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SEGMENT_DISABLE_BATTERY                    | bool   | **False** _($false)_                                                                                                                                                                                                                                                                                                                           | Hides the `BATTERY` segment found on the top-right of the prompt when value is set to **True** (_$true_).                                                                                                       |
| SEGMENT_DISABLE_DTIME                      | bool   | **False** _($false)_                                                                                                                                                                                                                                                                                                                           | Hides the `DTIME` segment found on the top-right of the prompt when the value is set to **True** (_$true_).                                                                                                     |
| SEGMENT_DISABLE_PROJECT_PYTHON             | bool   | **False** _($false)_                                                                                                                                                                                                                                                                                                                           | Hides the `PYTHON` segment found on the bottom-left prompt along with the **input buffer** when the value is set to **True** (_$true_). This ignores the value of `SEGMENT_DISABLE_PROJECT_PYTHON_VENV`.        |
| SEGMENT_DISABLE_PROJECT_PYTHON_VENV        | bool   | **False** _($false)_                                                                                                                                                                                                                                                                                                                           | Hides the `VENV` string display after `venv` detection when the value is set to **True** (_$true_). This ignores the value of `SEGMENT_PROJECT_PYTHON_ACTIVE_VENV_STR`.                                         |
| SEGMENT_DISABLE_TRANSIENT                  | bool   | **False** _($false)_                                                                                                                                                                                                                                                                                                                           | Completely hides the transient segment that contains previous command's return code and execution time when the value is set to `True`. This ignores the value of `SEGMENT_DISABLE_TRANSIENT_RECENT_EXEC_TIME`. |
| SEGMENT_PROJECT_PYTHON_ACTIVE_VENV_STR     | string | None                                                                                                                                                                                                                                                                                                                                           | Alternatively replaces the name of the `venv` that is currently activated from the prompt. This is useful when the length of the name disrespects the space of your input buffer.                               |
| SEGMENT_DISABLE_TRANSIENT_RECENT_EXEC_TIME | $false | Hides the `execution time` of the previous command executed from the transient prompt.                                                                                                                                                                                                                                                         |
| SEGMENT_DISABLE_WAKATIME                   | $false | Hides the `WAKATIME` segment. Note that the segment is still active when `WAKATIME_API_KEY` is valid to be queued for new data. This feature is only useful when you wanted to hide the segment when the prompt's width makes the prompt display undesirable, but still wants it to be accessible later without reconfiguring your `$PROFILE`. |
| WAKATIME_API_KEY                           | string | None                                                                                                                                                                                                                                                                                                                                           | The string that contains the API key that can make the prompt engine queue at for new data for every `CACHE_TIMEOUT`.                                                                                           |

</div>

#### Notes to Consider

1. Please note that these environment variables are purely **optional**, explicitly declaring them is fine, but this does not mean anything unless their values are the opposite of what is provided in their default values.
2. These environment variables are accessible in runtime or once they are loaded. You do not need to modify `$PROFILE` or the theme itself if these changes are temporary. The theme will adjust in an-instant.
3. Despite adjusting the environment variables both via `$PROFILE` and by on runtime, you do not need to restart your prompt for the changes to take effect.
4. Some segments cannot be disabled because they are the vital part of the theme. Those segments are: **Folder**, **Git**, and **Time Execution**.

## Showcase

Please understood that the theme may look different depending on your configuration such as the font ligatures embedded on your custom font, your prompt and other factors that affects the visuals of your prompt. Please see [my dotfiles](https://github.com/CodexLink/dotfiles-configs-archive) and check the folder `dist/font` if you want to get the same feeling and font + glyphs rendering.

> Note that my custom font has issues in regards to single-width and double-width for other icons, some icons went smaller than what is being rendered from the `oh-my-posh` config export renderer.

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

[![chips.omp.json ssh and root showcase #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_ssh_and_root_variants_1.png)](https://ohmyposh.dev/docs/themes#chips)

[![chips.omp.json ssh and root showcase #2](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_ssh_and_root_variants_2.png)](https://ohmyposh.dev/docs/themes#chips)

</div>

### Transient Prompt with Insights of Previous Command

<div align="center">

[![chips.omp.json transient showcase](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_transient.gif)](https://ohmyposh.dev/docs/themes#chips)

</div>

## TODO Features

The following are some of the features that I cut off **_for now_**, due to the following: I'm not using it, no other ways for me to test it or install it.

1. Other Programming Language Project Segment
   - [ ] Crystal
   - [ ] Flutter
   - [ ] Lua
   - [ ] NPM
   - [ ] Rust

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
