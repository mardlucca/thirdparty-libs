Included files:

### File: metal-cpp_macOS12_iOS15
- **URL**: https://developer.apple.com/metal/cpp/files/metal-cpp_macOS12_iOS15.zip
- **Reason for including:** strangely, currently cannot download file via tooling like *curl* or *bazel*. 
   Original zip file is also not a Bazel project.
- **Notes**: library can be included as a Bazel dependecy like this:

In your WORKSPACE:

```starlark
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
  name = "metal-cpp",
  urls = ["https://github.com/mardlucca/thirdparty-libs/raw/master/cpp/macos/metal-cpp_macOS12_iOS15.zip"],
  sha256 = "0648fc6f60d037c241e50c908e0bd2984f904c3202b56d8924c181c31075b453"
)
```

And in your build, add a dependency like this:

```starlark
  deps = [
    "@metal-cpp//:metal-cpp"
  ]  
```
