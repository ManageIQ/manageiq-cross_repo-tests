source "https://rubygems.org"

# gem "manageiq-cross_repo", "~> 1.0"

# Use custom branch of `manageiq-cross_repo` to allow bisecting rails for
# debugging purposes and custom modifications.
#
# This will be experimental and suseptable to false negatives (since using a
# particular version of activerecord with a locked version of rails is most
# likely going to fail.  Experimentation of bisecting all of rails or just
# activerecord is going to have to happen to deterime the best course of
# action.
#
gem "manageiq-cross_repo", :git    => "https://github.com/NickLaMuro/manageiq-cross_repo",
                           :branch => "rails-bisect"
