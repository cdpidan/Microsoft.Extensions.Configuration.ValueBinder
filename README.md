﻿Bind complex value(such as JSON, XML) to options

How to use
=============

Install the [Nuget](https://www.nuget.org/packages/Microsoft.Extensions.Configuration.ValueBinder) package.

``` PS
Install-Package Tuhu.Extensions.Configuration.ValueBinder
```
In your testing project, add the following framework

### Bind IConfigurationSection value

``` C#
services.ConfigureValue<TOptions>([string name, ]IConfigurationSection section, [NotNull] Func<FileConfigurationProvider> creator)
```

### Bind string value

``` C#
services.ConfigureValue<TOptions>([string name, ]string value, [NotNull] Func<FileConfigurationProvider> creator)
```

### Bind IConfiguration values

Map child section `Key` to options name, map empty section `key` or `Value`(if is IConfigurationSection) to default options

``` C#
services.ConfigureValues<TOptions>(IConfiguration configuration, [NotNull] Func<FileConfigurationProvider> creator)
```
