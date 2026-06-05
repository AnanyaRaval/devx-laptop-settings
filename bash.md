# Settings for bash

* Install `oh-my-bash`
- `bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"`
- Changes in `~/.bashrc`
```bash
OSH_THEME="brainy"
ENABLE_CORRECTION="true"
COMPLETION_WAITING_DOTS="true"
THEME_SHOW_SUDO="true"
THEME_SHOW_SCM="true"
THEME_SHOW_CLOCK="true"

completions=(
    git
    composer
    ssh
)

aliases=(
    general
)

plugins=(
    git
    bashmarks
)

source "$OSH"/oh-my-bash.sh
```

- Changes in `~/.oh-my-bash/themes/brainy/brainy.theme.sh`
```bash
function ___brainy_prompt_user_info {
local color=$_omb_prompt_bold_purple
:
}

function ___brainy_prompt_dir {
+  local color=$_omb_prompt_bold_yellow
:
 }
function ___brainy_prompt_scm {
+  local color=$_omb_prompt_bold_re
:
}
function ___brainy_prompt_clock {
+  printf "%s|%s|%s|%s" "$color" "$info" "$_omb_prompt_bold_yellow" "$box"
:
}
```
 