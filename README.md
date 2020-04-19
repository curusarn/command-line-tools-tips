# command-line-tools-tips
Tips on how to create awesome command-line tools


## Use a good library to parse options, generate help, and generate completions

Any tool that you expect other people to use should accept both short (`-o`) and long (`--long-option`) options. Arguments and options should be accepted in any order if possible.
Your tool should have help and completions for common shells; These should be always up to date with the actual options of the tool.

Why? Tools should save effort and time. Providing expected behaviour and completions saves time.

Writing and maintianing this is not fun and takes time. Luckily there are libraries that provide all this. Find a good one. Switch languages if yours does not have one. I'm serious - not providing completions because it is hard in a language **you** chose to use is idiotic. You owe good `--help` and completions to your users. This alone is a reason why you should not write serious command-line tools in bash.


Go: https://github.com/spf13/cobra  
Python: TODO


## Avoid using white on green (and green on white)

Green does not have a great contrast ratio.  
In many terminal themes the contrast is insufficient which results in unreadable text.

For example, check out the color tool for material design: https://material.io/resources/color/#!/?view.left=1&view.right=0&primary.color=64DD17

Example of tool that breaks this tip is `tig`.
