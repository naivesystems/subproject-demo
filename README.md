```
podman pull ghcr.io/naivesystems/analyze:latest

mkdir -p output

podman run --rm \
  -v $PWD:/src:O \
  -v $PWD/.naivesystems:/config:Z \
  -v $PWD/output:/output:Z \
  -w /src/ \
  ghcr.io/naivesystems/analyze:latest \
  /opt/naivesystems/misra_analyzer --src_dir demo/ -show_results
```

See also [https://github.com/naivesystems/analyze/wiki/Command%E2%80%90Line-Flags#src_dir](https://github.com/naivesystems/analyze/wiki/Command%E2%80%90Line-Flags#src_dir)
