# chips.omp.json

The development repository for the Oh-My-Posh Theme Based on Material Design Component: Chips. This repository contains the cutting edge for the theme than the provided theme from the oh-my-posh repository. Weekly changes were reflected.

[![chips.omp.json highlight #1](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_1.png)](https://ohmyposh.dev/docs/themes#chips)
[![chips.omp.json highlight #2](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight_2.png)](https://ohmyposh.dev/docs/themes#chips)

## Features

- Backtracking Transient Prompt for Previous Recent Execution Time and Command Return Code
- Color-Adjustable with Palettes (Reduces Clutter for Modifying Theme)
- Color-Changing Segments Based on Activity (Conditions)
- Color Candidates uses Material Palette Color from A100 to A400.
- Hideable (Primary Top and Secondary Left Candidate) Segments
- Minimalized Console Title
- Segments Individualized as a Seperate Component

## Screenshots

### More General Prompt Display

The following screenshots may be differ due to some of the segments hiding feature. Please refer to Technicals for more information.

### Backtracked Insights from Previous Commands

### Color-Adjusting Segments

###

## Installation

## Leftout Features

The following are some of the features that I cut off **_for now_**, due to me, not using it, or has no other ways for me to test it.

1. SSH Session to Segment
   - I don't know what part or side of prompt where it can be appreciated. Sure, I can put it on right-side 2nd primary prompt, but not sure yet, let me know your thoughts on **Issue**.
2. Other Programming Language Project Segment
   - SSH Session to Segment is possible but I have two reasons on why I cannot implement them:
     - a. I don't know how to test this yet.
     - b. I can probably SSH to my phone but glyphs will probably be broken.

- Programming languages that I have is currently **Python** and I'm currently planning to add Rust and Flutter in the future. let me know what other programming languages I can include by issuing them in **Issue**.
  > Note that, you have to make sure that language is supported from one of the segments offered in **oh-my-posh Segment Section**. Otherwise, create a feature request.

## Technicals

The following contains information on how I was able to manipulate the theme to provide my needs.

### Dealing with the Environment Variables, both Empty and Empty or Invalid Value

### Dealing with the Limitation of Transient Prompt

### Adding Segment on One Segment without Duplication

### `toBool` in sprig doesn't exists. Now what?

### Solution to Leading and Trailing Diamonds being treated as Text on Templates

## TODO

Some thing I would want to do to finish the initial production of this theme repository.

- [ ] PR request for including to the bundle.

## Contribution

- TODO.

## FAQ

1. Why?

   > Preferences. Most themes IMO are somewhat clusterred, which provides no spaces or respect from these segment themselves since they are interconnected from one another.

2. The prompt feels too slow...

   > There are two verdicts. [a] The data being queued from the both local (which is 'git', it parses your branch and repo state, note that I did not use **posh-git** in this theme, see FAQ #5.) and from remote (via HTTP, queueing Wakatime stats (if possible)). And your powershell (`pwsh`) version (You need to upgrade as upstream as possible). The figure below shows the debug output just from typing `oh-my-posh debug`.

3. Why `transient prompt` contains one-liner that contains multiple segments?

   > Accoding to the docs and as per explanation provided by the creator from my Issue, 'transient prompt` use case is intended to be more simplier than the other prompt because its nature was to provide a clean output from other prompts. With its feature limitation, I want to do more than just that, by providing previous and current insights about the command, I was able to create or manifest the structure of the segment to be more the same as how I display other segment from other prompt.

4. Sometimes my prompt just hangs. Why?

   > If you are using Wakatime, you have to keep note that the cache time is set to `10m` or 10 minutes by default. Therefore, every 10 minutes the prompt will do an HTTP request to get the latest upstream of your stats. If you are not using Wakatime and this issue occurs, please investigate the state of the prompt by **debugging** it. Please let me know with sufficient information if it persists.

5. Why did you not use `posh-git`? You know that `git` segment is slower right?
   > I'm aware. oh-my-posh `posh-git` docs doesn't show any examples or further modification than what is being provided in the `git` segment. While I do understand the compromise of performance over customization, I think its best to customize the output to further understand more about what are the symbols behind them. Because in my perspective, I'm pretty much confused about it. To solve the contention from this issue, I'm hoping that `posh-git` is customizable as `git` segment.

## Tools Used

- [regular expressions 101](https://regex101.com/) — Just a regex validator.
