# Sarcasm's manifests

Sarcasm's collection of [repo](https://gerrit.googlesource.com/git-repo)
manifests for various open source projects.

# autotest

    mkdir autotest
    cd autotest
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m autotest.xml
    repo sync

# llvm + clang + clang-tools-extra

    mkdir llvm
    cd llvm
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m llvm-tools.xml
    repo sync
    ln -s .repo/manifests/notes/llvm-tools.md README.md

# irony

To work on irony and derived projects:

    mkdir irony
    cd irony
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m irony.xml
    repo sync

To also include third party projects, use:

    repo init -g all -m irony.xml

To go back to the default, officially supported projects, use:

    repo init -g default -m irony.xml

# lsp

To work on emacs-lsp and cquery:

    mkdir lsp
    cd lsp
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m lsp.xml
    repo sync --fetch-submodules

Syncing and looking for differences:

    repo manifest --revision-as-HEAD -o old.xml
    repo sync --fetch-submodules
    repo manifest --revision-as-HEAD -o new.xml
    repo diffmanifests $(pwd)/{old,new}.xml

Launcher Emacs with specified configuration:

    emacs -mm -Q -l dot-emacs/init.el
