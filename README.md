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
    ln -s .repo/manifests/notes/README.md README.md

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
