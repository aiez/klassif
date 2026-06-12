<!-- Copyright (c) 2026 Tim Menzies, MIT License https://opensource.org/licenses/MIT -->
<a href="https://timm.fyi"><img align="right" alt="Author" src="https://img.shields.io/badge/Author-timm-dc143c?logo=readme&logoColor=white"></a><img align="right" alt="Language" src="https://img.shields.io/badge/Language-CSV-000080?logo=files&logoColor=white"><img align="right" alt="License" src="https://img.shields.io/badge/License-MIT-32cd32?logo=open-source-initiative&logoColor=white"><img align="right" alt="Purpose" src="https://img.shields.io/badge/Purpose-Data·Classification-7b68ee?logo=githubcopilot&logoColor=white">

### [http://tiny.cc/klassif](http://tiny.cc/klassif)
Example classification datasets: 73 CSV files (anneal, audiology,
COMPAS, diabetes, soybean, vote, ...) with self-describing
headers — the klass column ends in '!', so no separate schema
files are needed. Data only, no code.

```bash
# install
git clone http://tiny.cc/konfig ../konfig
git clone http://tiny.cc/klassif klassif && cd klassif
make help
```

<a href="http://tiny.cc/klassif"><img width="150" align="right" alt="qr" src="https://tiny.cc/tiny/qr-image/tiny.cc~klassif~l~150.png"></a>

**Sections:** [NAME](#name) | [DATA](#data) | [SEE ALSO](#see-also) | [LICENSE](#license) | [AUTHOR](#author)

## NAME

    klassif - classification benchmark CSVs. headers are the
    schema; the symbolic goal column ends in '!'.

## DATA

    CSV with self-describing header; no separate schema file:

      first char UPPER  -> numeric (Num)
      first char lower  -> symbolic (Sym)
      suffix '+'        -> numeric goal, maximize
      suffix '-'        -> numeric goal, minimize
      suffix '!'        -> symbolic goal (klass)
      suffix 'X'        -> ignore
      else              -> predictor
      missing value     -> '?'

    E.g. diabetes.csv: Preg,Plas,Pres,Skin,Insu,Mass,Pedi,Age,klass!

## SEE ALSO

    konfig    http://tiny.cc/konfig   shared Makefile, dotfiles
    optimiz   http://tiny.cc/optimiz  optimization datasets
    regress   http://tiny.cc/regress  regression datasets
    lull      http://tiny.cc/lull     code that reads these files

## LICENSE

    MIT. https://choosealicense.com/licenses/mit/

## AUTHOR

    Tim Menzies <timm@ieee.org>
