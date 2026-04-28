# 本地开发指南

## 环境要求

- macOS
- Homebrew（已安装于 `/usr/local/bin/brew`）
- Ruby 3.0.3（通过 Homebrew 安装，位于 `/usr/local/Cellar/ruby/3.0.3`）

## 首次配置

### 1. 将 Ruby 3.x 加入 PATH（永久生效）

```bash
echo 'export PATH="/usr/local/Cellar/ruby/3.0.3/bin:$PATH"' >> ~/.bash_profile
source ~/.bash_profile
```

### 2. 安装项目依赖

```bash
cd /path/to/zkmove.github.io
gem install bundler
bundle install
```

## 本地预览

```bash
export PATH="/usr/local/Cellar/ruby/3.0.3/bin:$PATH"
cd /Users/greg/work/zkmove.github.io
bundle exec jekyll serve
```

启动后在浏览器访问：**http://localhost:4000**

Jekyll 会监听文件变化，修改内容后自动重新构建，刷新浏览器即可看到效果。  
（`_config.yml` 修改除外，需要重启服务才能生效）

## 停止本地服务

在终端按 `Ctrl + C` 即可停止服务。
