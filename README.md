# chips.omp.json

The development repository for the Oh-My-Posh Theme Based on Material Design Component: Chips. This repository contains the cutting edge version of the theme than the one provided from the oh-my-posh repository. Updates of the theme from this repository to the oh-my-posh repository will reflect on the weekly basis.

# Notice

Theme is finished! As of `1.3.4`, all neccessary changes were done. Thorough examination or careful evaluation of output with respect to the environment variable will be done for this week, with PR to the official oh-my-posh repository will be instantiated.

[![chips.omp.json highlight #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_1.png)](https://ohmyposh.dev/docs/themes#chips)

## Features

- Backtracking Transient Prompt for Previous Recent Execution Time and Command Return Code
- Color-Adjustable with Palettes (Reduces Clutter for Modifying Theme)
- Color-Changing Segments Based on Activity (Conditions)
- Color Candidates uses Material Palette Color from A100 to A400
- Hideable (Primary Top and Secondary Left Candidate) Segments
- Minimalized Console Title
- Segments Individualized as a Seperate Component

## Installation

- TODO.

## Screenshots

### More General Prompt Display

The following screenshots may be differ due to some of the segments hiding feature. Please refer to Technicals for more information.

### Backtracked Insights from Previous Commands

### Color-Adjusting Segments

###

## Leftout Features

The following are some of the features that I cut off **_for now_**, due to me, not using it, or has no other ways for me to test it.

1. Other Programming Language Project Segment

   - Programming languages that I have is currently **Python** and I'm currently planning to add Rust and Flutter in the future. let me know what other programming languages I can include by issuing them in **Issue**.

     > Note that, you have to make sure that language is supported from one of the segments offered in **oh-my-posh Segment Section**. Otherwise, create a feature request.

## Technicals

The following contains information on how I was able to manipulate the theme to provide my needs.

### Dealing with the Environment Variables, both Empty and Empty or Invalid Value

- TODO.

### Dealing with the Limitation of Transient Prompt

- TODO.

### Adding Segment on One Segment without Duplication

- TODO.

### `toBool` in sprig doesn't exists. Now what?

- TODO.

### Solution to Leading and Trailing Diamonds being treated as Text on Templates

- TODO.

## Contribution

- TODO.

## FAQ

1. Why?

   > Preferences. Most themes IMO are somewhat clusterred, which provides no spaces or respect from these segment themselves since they are interconnected from one another.

2. The prompt feels too slow...

   > There are two verdicts. [a] The data being queued from the both local (which is 'git', it parses your branch and repo state, note that I did not use **posh-git** in this theme, see FAQ #5. In terms of being slow, see this [FAQ entry](https://ohmyposh.dev/docs/faq#the-prompt-is-slow-delay-in-showing-the-prompt-between-commands).) and from remote (via HTTP, queueing Wakatime stats (if possible)). And your powershell (`pwsh`) version (You need to upgrade as upstream as possible). The figure below shows the debug output just from typing `oh-my-posh debug`.

3. Why `transient prompt` contains one-liner that contains multiple segments?

   > Accoding to the docs and as per explanation provided by the creator from my [issue](https://github.com/JanDeDobbeleer/oh-my-posh/issues/2605), 'transient prompt` use case is intended to be more simplier than the other prompt because its nature was to provide a clean output from other prompts. With its feature limitation, I want to do more than just that, by providing previous and current insights about the command, I was able to create or manifest the structure of the segment to be more the same as how I display other segment from other prompt.

4. Sometimes my prompt just hangs. Why?

   > If you are using Wakatime, you have to keep note that the cache time is set to `10m` or 10 minutes by default. Therefore, every 10 minutes the prompt will do an HTTP request to get the latest upstream of your stats. If you are not using Wakatime and this issue occurs, please investigate the state of the prompt by **debugging** it. Please let me know with sufficient information if it persists.

5. Why did you not use `posh-git`? You know that `git` segment is slower right?

   > I'm aware. oh-my-posh `posh-git` docs doesn't show any examples or further modification than what is being provided in the `git` segment. While I do understand the compromise of performance over customization, I think its best to customize the output to further understand more about what are the symbols behind them. Because in my perspective, I'm pretty much confused about it. To solve the contention from this issue, I'm hoping that `posh-git` is customizable as `git` segment.

6. Why start at `1.0.0`?

   > Initial development of theme were not reflected due to the fact that I was having a hard time creating a small script to transport changes from local (home) to remote (cloned repo). Also, as per its state being set to `public`, it was done when I was reporting an [issue in oh-my-posh repository](https://github.com/JanDeDobbeleer/oh-my-posh/issues/2679), wherein theme is required for evaluation of the said report.

7. When I disabled "wakatime" segment, why it still feels so slow?

   > As of now (08/26/2022), there is no switch for the HTTP query to be disabled when a certain environment variable invalidates truthy condition. I suggest trying to nullify the value of your 'WAKATIME_API_KEY' and see if it works or ignores calling HTTP request.

8. What are your basis for the wakatime's timeout values?
   > They were based on my preference with consideration on my ISP speed.

## Tools Used

- [regular expressions 101](https://regex101.com/) — Just a regex validator.

## Credits

- TODO.
