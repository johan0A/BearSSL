# BearSSL

This is [BearSSL](https://bearssl.org),
packaged for the [Zig](https://ziglang.org/) build system.

## how to use

1. Add `BearSSL` to the dependency list in `build.zig.zon`:

```sh
zig fetch --save git+https://github.com/johan0A/BearSSL
```

2. Config `build.zig`:

```zig
const bearssl_dep = b.dependency("bearssl", .{
    .target = target,
    .optimize = optimize,
});
root_module.linkLibrary(bearssl_dep.artifact("bearssl"));