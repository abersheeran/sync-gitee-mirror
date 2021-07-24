# gitee-mirror

使用 GitHub actions 同步 GitHub 仓库到 Gitee 仓库

## 使用说明

在 GitHub actions 配置文件中写入以下内容，其中 `with` 下的部分需要按需修改。

```yaml
- name: sync-gitee-mirror
  uses: abersheeran/sync-gitee-mirror@v1-alpha
  with:
    repository: abersheeran/sync-gitee-mirror
    username: ${{ secrets.USERNAME }}
    password: ${{ secrets.PASSWORD }}
```

- `repository`：填你的用户名与仓库名，格式如样例所示。
- `username`：填写你的 gitee 用户名
- `password`：填写你的 gitee 密码（注意：密码需要以 [Secrets](https://docs.github.com/cn/actions/reference/encrypted-secrets) 方式给出，以保证密码不被泄露, 同时尽量确保密码避免 bash 特殊字符 `` !'"`@ `` 等等）
