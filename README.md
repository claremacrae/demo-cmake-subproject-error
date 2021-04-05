# demo-cmake-subproject-error

Demo a common pattern of tests being used, unintentionally, when a library is used via add_subdirectory, FetchContent and similar

This was created to use an example when logging:

* [Catch2 issue #2202](https://github.com/catchorg/Catch2/issues/2202): "Catch2's tests should never be run, if it is loaded as a sub-project"