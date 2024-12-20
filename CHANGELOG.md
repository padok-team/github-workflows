# Changelog

## [1.5.0](https://github.com/padok-team/github-workflows/compare/v1.4.0...v1.5.0) (2024-12-20)


### Features

* **tf-quality:** fix version for checkov-action ([14b097d](https://github.com/padok-team/github-workflows/commit/14b097d9f6cfa2d409c82753e56294f1f659a677))


### Bug Fixes

* .github/workflows/terraform-quality.yml ([14aa612](https://github.com/padok-team/github-workflows/commit/14aa6123fe9ac41519e83eb8561d58112cfcaae4))

## [1.4.0](https://github.com/padok-team/github-workflows/compare/v1.3.1...v1.4.0) (2024-12-20)


### Features

* **terragrunt:** checks ([763ebe5](https://github.com/padok-team/github-workflows/commit/763ebe594e3f10e9da465d2833c46dc9aa990904))

## [1.3.1](https://github.com/padok-team/github-workflows/compare/v1.3.0...v1.3.1) (2024-05-10)


### Bug Fixes

* **deps:** update actions/checkout digest to 0ad4b8f ([41d9f67](https://github.com/padok-team/github-workflows/commit/41d9f67fbcdf013e416e300e080c1cfe674d3eeb))

## [1.3.0](https://github.com/padok-team/github-workflows/compare/v1.2.0...v1.3.0) (2024-05-10)


### Features

* **terraform-quality:** update tfswitch version ([8f900ea](https://github.com/padok-team/github-workflows/commit/8f900eac342aef3cfb62758a8e03ee42321c771b))

## [1.2.0](https://github.com/padok-team/github-workflows/compare/v1.1.2...v1.2.0) (2024-04-12)


### Features

* **terraform-quality:** add the option to setup baseline for checkov ([eed2d28](https://github.com/padok-team/github-workflows/commit/eed2d287b30b5730b6dbca3ff72813b4b3137352))
* **terraform-quality:** add the option to setup skip paths for checkov ([96fd381](https://github.com/padok-team/github-workflows/commit/96fd381f58edc106ec1c46a5065053f64a435dae))

## [1.1.2](https://github.com/padok-team/github-workflows/compare/v1.1.1...v1.1.2) (2023-12-15)


### Bug Fixes

* **release-please:** remove deprecated default-branch options ([a88daf8](https://github.com/padok-team/github-workflows/commit/a88daf8659416e9a74927a51a5c3c40e876819a9))
* **semantic-check:** use lts node version ([8b23c48](https://github.com/padok-team/github-workflows/commit/8b23c4810a8f1f4df91ad8b1e749d2117f468a90))

## [1.1.1](https://github.com/padok-team/github-workflows/compare/v1.1.0...v1.1.1) (2023-12-15)


### Bug Fixes

* use a token to avoid rate limit ([74a426a](https://github.com/padok-team/github-workflows/commit/74a426a3ef29a0ade0cbacdaff9a6ae47042d29d))

## [1.1.0](https://github.com/padok-team/github-workflows/compare/v1.0.1...v1.1.0) (2023-05-05)


### Features

* introduce workflow input to skip checkov ([0207e23](https://github.com/padok-team/github-workflows/commit/0207e234fda0462142a90e17d57bce86ec48d854))

## [1.0.1](https://github.com/padok-team/github-workflows/compare/v1.0.0...v1.0.1) (2022-10-21)


### Bug Fixes

* **release:** add id to release step ([a8f5221](https://github.com/padok-team/github-workflows/commit/a8f522192c62676c1104a3f92de831cc40ebc85b))

## 1.0.0 (2022-10-21)


### Features

* add commitlint and release-please workflows ([1c7db15](https://github.com/padok-team/github-workflows/commit/1c7db15b71ae777f930879125c1e5732b7b60645))
* add local release and semantic check jobs, add version.txt ([2976835](https://github.com/padok-team/github-workflows/commit/2976835c0c9850e92295898dc7259b3a59bf1ad0))
* add terraform workflows ([a0f53e5](https://github.com/padok-team/github-workflows/commit/a0f53e504125e2420a60236aa310d087ee391e80))
* add terraform-docs workflow ([c4fdbcf](https://github.com/padok-team/github-workflows/commit/c4fdbcf061193d62d43f21d91de52773e0a879fd))
* **release:** add update-major-minor-tags input and corresponding steps ([6eb2fd2](https://github.com/padok-team/github-workflows/commit/6eb2fd29dbc3c9453ec564176c9394f1436921f5))
* **terraform-lint:** add workdir input, set default workdir to it in job ([dc94fa2](https://github.com/padok-team/github-workflows/commit/dc94fa21f06a9aa9307bdc64d195ad300b46c0f2))


### Bug Fixes

* **deps:** add renovate.json ([ff09aac](https://github.com/padok-team/github-workflows/commit/ff09aac71ad8d871386805fb1ff2badde0fb6082))
* remove backslashes in commitlint install job, remove hello job ([edcd024](https://github.com/padok-team/github-workflows/commit/edcd0244ca2ec6659c66c3dd6ee883c6ada91f62))
* set default workdir in jobs ([3088613](https://github.com/padok-team/github-workflows/commit/3088613f5fee92e44f5700364d99f27b838e55a6))
* upgrade checkout action to v3, add repository variable, add comment ([a21df48](https://github.com/padok-team/github-workflows/commit/a21df485a8333aa4f183ef67cc1843c091ab8ffc))
* use .bin folder for tfswitch install script ([57665bf](https://github.com/padok-team/github-workflows/commit/57665bfd6ad6e806ae8ca635aea66e733c6f45db))
* use .bin path for terraform ([0b6392c](https://github.com/padok-team/github-workflows/commit/0b6392cbd0d251be32cc607d9eb878fef5247fc0))
