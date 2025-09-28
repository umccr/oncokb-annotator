- Build `meta.yaml` using [grayskull](https://github.com/conda/grayskull):

```shell
grayskull pypi https://github.com/umccr/oncokb-annotator -o oncokb-annotator-output
```

- Build conda package:

```shell
conda build oncokb-annotator-output
```

- Upload to Anaconda channel:
  - token: under `Settings -> Access`, need to allow both read and write access to the API site.

```shell
anaconda -t <token> upload miniforge3/envs/condabuild/conda-bld/noarch/oncokb-annotator-3.4.1.9000-py_0.conda
```
