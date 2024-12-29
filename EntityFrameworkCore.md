要使用C#的Entity Framework Core的dotnet工具（`dotnet ef`），请参考以下步骤及常用命令的说明：

### 1. 安装工具

首先，确保已安装Entity Framework Core工具：

```
dotnet tool install --global dotnet-ef
```

### 2. 常用命令及参数

以下是一些常用的`dotnet ef`命令及其参数说明：

- **dotnet ef migrations add**
  创建新的迁移文件。

  ```
  dotnet ef migrations add <MigrationName> [options]
  ```

  - `<MigrationName>`：迁移名称。
  - `--output-dir <path>`：指定生成文件的目录。
  - 例如dotnet ef migrations add <MigrationName> [options] -o Entities//指定实体类目录
  
- **dotnet ef database update**
  更新数据库到最新或指定的迁移。

  ```
  dotnet ef database update [<Migration>] [options]
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

  - `<Migration>`：目标迁移名称（可选）。
  - `--connection <connectionString>`：指定数据库连接字符串。

- **dotnet ef dbcontext scaffold**
  从现有数据库生成模型。

  ```
  dotnet ef dbcontext scaffold <ConnectionString> <Provider> [options]
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

  - `<ConnectionString>`：数据库连接字符串。
  - `<Provider>`：数据库提供程序（如`Microsoft.EntityFrameworkCore.SqlServer`）。
  - `--output-dir <path>`：指定生成文件的目录。
  - `--context-dir <path>`：指定生成的DbContext类的目录。

- **dotnet ef migrations list**
  列出所有迁移。

  ```
  dotnet ef migrations list [options]
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

### 3. 示例

- 创建迁移：

  ```
  dotnet ef migrations add InitialCreate --output-dir Migrations
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

- 更新数据库：

  ```
  dotnet ef database update
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

- 生成模型：

  ```
  dotnet ef dbcontext scaffold "Server=myServerAddress;Database=myDataBase;User Id=myUsername;Password=myPassword;" Microsoft.EntityFrameworkCore.SqlServer --output-dir Models
  ```

  

  <details class="snippet-vulnerabilities-details" style="box-sizing: border-box; display: block; font-size: 12px; color: var(--fgColor-muted, var(--color-fg-muted)); margin-bottom: var(--base-size-16); margin-top: 0px;"><summary class="snippet-vulnerability-summary" style="box-sizing: border-box; display: flex; cursor: pointer; align-items: center; gap: var(--base-size-4);"><div class="snippet-vulnerability-shield-icon" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--bgColor-danger-emphasis, var(--color-danger-emphasis)); mask: url(&quot;/assets/shield-11821ac8db19.svg&quot;) center center no-repeat;"></div>1 vulnerability detected<div class="snippet-vulnerability-chevron" style="box-sizing: border-box; width: 15px; height: 15px; background-color: var(--fgColor-muted, var(--color-fg-muted)); mask: url(&quot;/assets/chevron-down-e5b767983606.svg&quot;) center center no-repeat;"></div></summary><div class="snippet-vulnerability-details" style="box-sizing: border-box; margin-bottom: var(--base-size-8); margin-left: var(--base-size-20);"><p class="snippet-vulnerability-details-title" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px; font-weight: var(--base-text-weight-semibold, 600);"></p><p class="snippet-vulnerability-details-description" style="box-sizing: border-box; margin-top: 0px; margin-bottom: 0px;"></p></div></details>

这些命令和参数提供了对数据库和迁移的全面管理，您可以根据需要进行调整和使用。详细信息和更多选项可以参考官方文档：[Entity Framework Core Tools](https://learn.microsoft.com/en-us/ef/core/cli/dotnet)。