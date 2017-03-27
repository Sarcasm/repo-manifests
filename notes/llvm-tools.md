# Build notes

    mkdir build
    cd build
    env CC=clang CXX=clang++ cmake -G Ninja \
        -DCMAKE_BUILD_TYPE=Release \
        -DLLVM_ENABLE_ASSERTIONS=ON \
        -DLLVM_PARALLEL_LINK_JOBS=2 \
        ../llvm
    ninja

# git svn dcommit

    cd llvm/tools/clang
    git checkout -b master
    repo sync .
    git svn init https://llvm.org/svn/llvm-project/cfe/trunk --username=MY_USER
    git config svn-remote.svn.fetch :refs/remotes/origin/master
    git svn rebase -l
    sudo cpan upgrade Term::ReadKey  # only on perl updates
    git svn dcommit --interactive
    git branch -D master
