# fish-archive

Fork of [shoriminimoe/fish-extract](https://github.com/shoriminimoe/fish-extract) with added support for compressing files.

### Installation

Install with [fisher](https://github.com/jorgebucaran/fisher):

```shell
fisher install givensuman/fish-archive
```

### Usage

#### `extract`

Extract archive file(s)

```shell
extract foo.tar.gz          # runs tar -xvzf foo.tar.gz
extract foo.tar.gz bar.zip  # runs tar -xvzf foo.tar.gz && unzip bar.zip
```

#### `compress`

Compress file(s) into an archive

File names are inferred where possible, and default to `archive.tar` when not

```shell
compress foo.tar.gz foo # runs `tar -cvzf foo.tar.gz foo`
compress foo            # runs `tar -cvzf foo.tar.gz foo`
compress foo bar        # runs `tar -cvf archive.tar foo bar`
```

### Supported Formats

| Supported | Extension                    | Description                          |
| :-------: | :--------------------------- | :----------------------------------- |
|    ✅     | `7z`                         | 7zip file                            |
|    ✅     | `Z`                          | Z archive (LZW)                      |
|    ✅     | `bz2`, `bz`                  | Bzip2 file                           |
|    ✅     | `gz`                         | Gzip file                            |
|    ✅     | `iso`                        | Optical Disc Image                   |
|    ✅     | `jar`                        | Java Archive                         |
|    ✅     | `lrz`                        | LRZ archive                          |
|    ✅     | `lz4`                        | LZ4 archive                          |
|    ✅     | `lzma`                       | LZMA archive                         |
|    ✅     | `tar.Z`, `taz`               | Tarball with LZW compression         |
|    ✅     | `tar.bz2`, `tbz2`            | Tarball with bzip2 compression       |
|    ✅     | `tar.bz`, `tbz`              | Tarball with bzip compression        |
|    ✅     | `tar.gz`, `tgz`              | Tarball with gzip compression        |
|    ✅     | `tar.lrz`                    | Tarball with lrzip compression       |
|    ✅     | `tar.lz4`                    | Tarball with lz4 compression         |
|    ✅     | `tar.lz`                     | Tarball with lzip compression        |
|    ✅     | `tar.lzo`                    | Tarball with lzop compression        |
|    ✅     | `tar.xz`, `txz`              | Tarball with lzma2 compression       |
|    ✅     | `tar.lzma`, `tar.zma`, `tlz` | Tarball with lzma compression        |
|    ✅     | `tar.zst`, `tzst`            | Tarball with zstd compression        |
|    ✅     | `tar`                        | Tarball                              |
|    ✅     | `xpi`                        | Mozilla XPI module file              |
|    ✅     | `xz`                         | LZMA2 archive                        |
|    ✅     | `zip`                        | Zip archive                          |
|    ✅     | `zst`                        | Zstandard file (zstd)                |
|    ✅     | `zz`                         | ZLIB file                            |
|    ❌     | `aar`                        | Android library file                 |
|    ❌     | `apk`                        | Android app file                     |
|    ❌     | `cab`                        | Microsoft cabinet archive            |
|    ❌     | `cpio`                       | Cpio archive                         |
|    ❌     | `deb`                        | Debian package                       |
|    ❌     | `ear`                        | Enterprise Application aRchive       |
|    ❌     | `ipa`                        | iOS app package                      |
|    ❌     | `ipsw`                       | iOS firmware file                    |
|    ❌     | `rar`                        | WinRAR archive                       |
|    ❌     | `rpm`                        | RPM package                          |
|    ❌     | `sublime-package`            | Sublime Text package                 |
|    ❌     | `war`                        | Web Application archive (Java-based) |

### License

[MIT](../LICENSE)

