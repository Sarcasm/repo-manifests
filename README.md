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
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m clang-tools-extra.xml
    repo sync

# irony

To work on irony and derived projects:

    mkdir irony
    cd irony
    repo init -u https://github.com/Sarcasm/repo-manifests.git -m irony.xml
    repo sync