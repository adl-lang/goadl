# Go ADL Workspace Repo

Repo has `goadlc` and `goadl_rt` as submodules and `go.work` "uses" `goadl_rt`, `goadl_rt/v2`, `goadlc` and `goadlc/out` (for testing).

## Dev

```
git clone https://github.com/adl-lang/goadl.git
cd goadl
git checkout gm-wip-01
git submodule update --init
cd goadlc
# setup local env, specifically adlc is needed (i.e. for adl->ast)
. ./local-setup.sh
# test
go run main.go go v2 --outputdir out -n adl/exer01/struct01.adl
cd out/exer01/struct01
go test -v
```

## Use `goadlc`

```
git clone https://github.com/adl-lang/goadlc.git
git checkout gm-wip-01
go build
```