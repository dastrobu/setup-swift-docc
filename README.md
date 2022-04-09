<p align="center">
  <a href="https://github.com/dastrobu/setup-swift-docc/"><img alt="setup-swift-docc status" src="https://github.com/dastrobu/setup-swift-docc/workflows/test/badge.svg"></a>
</p>

# Setup the [Swift DocC](https://www.swift.org/documentation/docc/) Compiler

To generate nice documentation pages from a Swift package with help of DocC, this action can be used as follows

```yaml
- uses: dastrobu/setup-swift-docc@v0
- run: docc convert
    DemoSwiftPackage/Sources/DemoSwiftPackage/DemoSwiftPackage.docc
    --fallback-display-name DemoSwiftPackage
    --fallback-bundle-identifier DemoSwiftPackage
    --fallback-bundle-version 1
    --additional-symbol-graph-dir DemoSwiftPackage/.build
    --output-path docs
```

for a full example, see [test.yaml](.github/workflows/test.yaml).
