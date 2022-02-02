# My Notes

## Compiler structure

1. Read file into string
1. `language::read_file()`: parse string into `File` structure (defined in `src/language.rs`)
1. `rulebook::gen_rulebook()`: takes `File`, generates rulebook (defined in `src/rulebook.rs`) with sanitized rules, id/name maps
1. `builder::build_runtime_functions():` takes `RuleBook`, generates runtime functions as side effect (does it output them, modify something, or what?)
1. `compiler::compile_book()`: takes `RuleBook`, generates C output based on template (possibly does side effects as well?)
