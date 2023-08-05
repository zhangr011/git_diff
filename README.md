# git_diff
According to https://tech.marksblogg.com/git-track-changes-in-media-office-documents.html

## config in .git/config
>

    [alias]
        wdiff = diff --word-diff=color --unified=1

    [diff "word"]
        textconv=pandoc --to=markdown
        binary=true
        prompt=false

    [diff "excel"]
        textconv=python3 ~/repo/git_diff/xlsx-dump.py
        binary=true

    [diff "powerpoint"]
        textconv=python ~/repo/git_diff/pptx-dump.py
        binary=true

    [diff "pdf"]
        textconv=python3 ~/repo/git_diff/pdf-dump.py
        binary=true

    [diff "images_videos"]
        textconv=exiftool
        binary=true
