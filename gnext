#!/bin/zsh

function __gnext_intention_file {
    STORAGE=~/.gnext_intentions
    mkdir -p ${STORAGE}

    intention_file="${STORAGE}/$(basename $(git rev-parse --show-toplevel)).txt"
    echo "${intention_file}"
}

function gnext {
    echo "$*" > "$(__gnext_intention_file)"
}

function gdone {
    intention_file="$(__gnext_intention_file)"
    git status
    planned_msg=$(cat "$intention_file")
    read "edited_msg?Message [${planned_msg}]: "
    commit_msg="${edited_msg:-${planned_msg}}"
    git commit -am "${commit_msg}"
    rm "$intention_file"
}

function gnope {
    rm "$(__gnext_intention_file)"
    git reset --hard
}
