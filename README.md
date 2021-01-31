# SwiftLint-Config

ikeh1024's base SwiftLint configuration file.

## SwiftLint Version Support

Here's a reference of which SwiftLint-Config version to use for a given SwiftLint version.

|SwiftLint version|Last supported SwiftLint-Config release|
|:--|:--|
|SwiftLint 0.42.0|Latest|

You can check version as follows

```sh
swiftlint version
```

## Usage

- Create `Run Script` and write aｓ follows

```sh
if which swiftlint >/dev/null; then
  swiftlint autocorrect --format
  swiftlint
else
  echo "SwiftLint does not exist, download from https://github.com/realm/SwiftLint"
fi
```

![image](https://i.imgur.com/B31sNdl.png)

Using a remote reference, your `.swiftlint.yml` could look like this:

```yaml
# リモートに置かれた.ymlファイルの設定を使用する
parent_config: https://raw.githubusercontent.com/pommdau/SwiftLint-Config/v1.0.0/ikeh1024-base-swiftlint-config.yml

# 対象のファイル・フォルダ
included:
# デフォルトからフォルダ名を変更していない場合、プロジェクト名と同名のフォルダを指定すればいい
  - {プロジェクト名}

# 対象外のファイル・フォルダ
excluded:
  - Pods
  - Generated
```

<img width="512" alt="image" src="https://i.imgur.com/IlcKmHv.png">

See the SwiftLint documentation for more details.  
https://github.com/realm/SwiftLint#child--parent-configs-remote

## References
- [uhooi/SwiftLint\-Config](https://github.com/uhooi/SwiftLint-Config/blob/main/README.md)
- [SwiftLintの設定ファイルをサーバーに配置して共有する方法 - Qiita](https://qiita.com/uhooi/items/b5b26caeeefd8dbe1afd)
