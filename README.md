# chips.omp.json

The development repository for the Oh-My-Posh Theme Based on Material Design Component: Chips.

[![chips.omp.json highlight](https://github.com/CodexLink/chips.omp.json/blob/latest/assets/highlight.png)](https://ohmyposh.dev/docs/themes#chips)

<hr/>

**NOTE**: The theme is ready for deployment on the oh-my-posh theme directory, however, I wanna investigate its slow execution time. I suspect this may be from the transient using the cached data from the execution time, but who knows. When a solution was found, some features may be cut off.

## Features

- Backtracking Transient Prompt for Previous Recent Execution Time and Command Return Code
- Color-Adjustable with Palettes (Reduces Clutter for Modifying Theme)
- Color-Changing Segments Based on Activity (Conditions)
- Color Candidates uses Material Palette Color from A100 to A400.
- Hideable (Primary Top and Secondary Left Candidate) Segments
- Minimalized Console Title
- Segments Individualized as a Seperate Component

## Screenshots

- TODO

## Leftout Features

The following are some of the features that I cut off **_for now_**, due to me, not using it, or has no other ways for me to test it.

- SSH Session Detection [0]
- Other Programming Language Detection [1]
- Battery Indicator [2]

* [0] I can easily invoke this in the Root Indicator Segment, but I have no device that can test it.
* [1] I don't have other programming languages, and for now, I'm planning to add Rust and Flutter. Let me know if other's really needs it.
* [2] As a Laptop User, I would want this one, but does not feel to be fitting for any parts of the segment. I will let this one off for now and will think of it again once I'm done with other things.

## Contribution

- TODO.

## Technicals

- TODO.

## TODO

Some thing I would want to do to finish the initial production of this theme repository.

- [ ] markdownlint.json config.
- [ ] PR request for including to the bundle.

## FAQ

1. Why?
   > Because why not. I understand there are a lot themes were published, but we all have preferences.

## Tools Used

- [regular expressions 101](https://regex101.com/) - Just a regex validator.
