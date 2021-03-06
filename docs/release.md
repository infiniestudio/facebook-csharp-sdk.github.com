---
layout: default
title: Publishing a Release
---

This document outlines the process for creating and publishing a new release of the Facebook SDK for .NET. These steps are only needed for administrators of this project. If you are looking to build your own version of the Facebook SDK for .NET you should read the document titled [Building Facebook SDK for .NET from Source](/docs/build).

## Steps to Publish a Release

1. Set the version number in VERSION.
  * Only change the second version number unless this is a major release.
1. After the VERSION numbers are set run a build.
1. git tag vX.X.X
1. git push --tags
1. git clean -xdf
1. jake
1. jake nuget:push:symbolsource[apikey]
1. jake nuget:push:nuget[apikey]

