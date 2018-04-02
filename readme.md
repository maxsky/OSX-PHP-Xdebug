# The compiled PHP Xdebug extension.

Here: [Releases](https://github.com/maxsky/OSX-PHP-Xdebug/releases)

Put `xdebug.so` in `/usr/local/lib/php/extensions` (recommend).

If your PHP installed by HomeBrew, you can add `ext-xdebug.ini` to `/usr/local/etc/php/<version>/conf.d`, and the content:

---

下载瞧这里：[Releases](https://github.com/maxsky/OSX-PHP-Xdebug/releases)

将 `xdebug.so` 放入 `/usr/local/lib/php/extensions`（建议）

如果你是通过 HomeBrew 安装的 PHP，你可以添加 `ext-xdebug.ini` 文件到 `/usr/local/etc/php/<版本>/conf.d`, 内容如下:

---

```
[Xdebug]
zend_extension="/usr/local/lib/php/extensions/xdebug.so"
; auto_trace 'Off' to improve performance（设置为 Off 可提升性能） 
xdebug.auto_trace=On
xdebug.var_display_max_children=512
xdebug.var_display_max_data=2048
xdebug.var_display_max_depth=8
```

然后重启，例如：`brew services restart php@7.1`


