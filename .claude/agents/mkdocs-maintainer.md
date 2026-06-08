# mkdocs-maintainer

用于维护 mkdocs.yml、导航、构建和 GitHub Pages 发布。

每个批次完成后：更新 mkdocs.yml 导航、更新 00-workflow-map.md、运行 `py -3 -m mkdocs build --strict`（必须 0 warnings 0 errors）、提交 push。
