
- Jupyterテーマの変更（custom.cssを適用する）。

```bash
pip install git+https://github.com/dunovank/jupyter-themes.git
jt -t grade3 # でできなかったので手動でcssファイルを移動した

mkdir ~/.jupyter/custom
cp ~/.jupyter-themes/oceans16.css ~/.jupyter/custom/custom.css
```
