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

**Sections:** [NAME](#name) | [DATA](#data) | [FILES](#files) | [SEE ALSO](#see-also) | [LICENSE](#license) | [AUTHOR](#author)

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

## FILES

[COMPAS53.csv](#file-compas53-csv) | [anneal.csv](#file-anneal-csv) | [anneal.orig.csv](#file-anneal-orig-csv) | [arrhythmia.csv](#file-arrhythmia-csv) | [audiology.csv](#file-audiology-csv) | [autos.csv](#file-autos-csv) | [balance.scale.csv](#file-balance-scale-csv) | [breast.cancer.csv](#file-breast-cancer-csv) | [breast.w.csv](#file-breast-w-csv) | [breastcancer.csv](#file-breastcancer-csv) | [bridges.version1.csv](#file-bridges-version1-csv) | [bridges.version2.csv](#file-bridges-version2-csv) | [car.csv](#file-car-csv) | [cmc.csv](#file-cmc-csv) | [colic.csv](#file-colic-csv) | [colic.orig.csv](#file-colic-orig-csv) | [column2C.csv](#file-column2c-csv) | [column3C.csv](#file-column3c-csv) | [credit.a.csv](#file-credit-a-csv) | [credit.g.csv](#file-credit-g-csv) | [cylinder.bands.csv](#file-cylinder-bands-csv) | [dermatology.csv](#file-dermatology-csv) | [diabetes.csv](#file-diabetes-csv) | [ecoli.csv](#file-ecoli-csv) | [flags.csv](#file-flags-csv) | [german.csv](#file-german-csv) | [glass.csv](#file-glass-csv) | [haberman.csv](#file-haberman-csv) | [heart.c.csv](#file-heart-c-csv) | [heart.h.csv](#file-heart-h-csv) | [heart.statlog.csv](#file-heart-statlog-csv) | [hepatitis.csv](#file-hepatitis-csv) | [hypothyroid.csv](#file-hypothyroid-csv) | [ionosphere.csv](#file-ionosphere-csv) | [iris.csv](#file-iris-csv) | [kr.vs.kp.csv](#file-kr-vs-kp-csv) | [labor.csv](#file-labor-csv) | [letter.csv](#file-letter-csv) | [lymph.csv](#file-lymph-csv) | [mnist_1.csv](#file-mnist_1-csv) | [mushroom.csv](#file-mushroom-csv) | [nursery.csv](#file-nursery-csv) | [optdigits.csv](#file-optdigits-csv) | [page.blocks.csv](#file-page-blocks-csv) | [pendigits.csv](#file-pendigits-csv) | [postoperative.patient.data.csv](#file-postoperative-patient-data-csv) | [primary.tumor.csv](#file-primary-tumor-csv) | [segment.csv](#file-segment-csv) | [shuttle.landing.control.csv](#file-shuttle-landing-control-csv) | [sick.csv](#file-sick-csv) | [solar.flare1.csv](#file-solar-flare1-csv) | [solar.flare2.csv](#file-solar-flare2-csv) | [sonar.csv](#file-sonar-csv) | [soybean.csv](#file-soybean-csv) | [spambase.csv](#file-spambase-csv) | [spect.test.csv](#file-spect-test-csv) | [spect.train.csv](#file-spect-train-csv) | [spectf.test.csv](#file-spectf-test-csv) | [spectf.train.csv](#file-spectf-train-csv) | [spectrometer.csv](#file-spectrometer-csv) | [splice.csv](#file-splice-csv) | [sponge.csv](#file-sponge-csv) | [tae.csv](#file-tae-csv) | [tic-tac-toe.csv](#file-tic-tac-toe-csv) | [trains.csv](#file-trains-csv) | [vehicle.csv](#file-vehicle-csv) | [vote.csv](#file-vote-csv) | [vowel.csv](#file-vowel-csv) | [waveform5000.csv](#file-waveform5000-csv) | [weather.csv](#file-weather-csv) | [weathernom.csv](#file-weathernom-csv) | [wine.csv](#file-wine-csv) | [zoo.csv](#file-zoo-csv)

## SEE ALSO

    konfig    http://tiny.cc/konfig   shared Makefile, dotfiles
    optimiz   http://tiny.cc/optimiz  optimization datasets
    regress   http://tiny.cc/regress  regression datasets
    luamine   http://tiny.cc/luamine  code that reads these files

## LICENSE

    MIT. https://choosealicense.com/licenses/mit/

## AUTHOR

    Tim Menzies <timm@ieee.org>
