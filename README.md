# Build ubuntu docker environment for macos m1 clion

## docker iamge pull url： `docker pull bysouffle/remote-env-macm1`

##  build
```
  docker build -t bysouffle/remote-env-macm1:v1.0 -f Dockerfile.clion-remote-macm1 .
```

## run
```
  docker run -d --cap-add sys_ptrace -p127.0.0.1:2333:22 --name clion_remote_env bysouffle/remote-env-macm1:v1.0
  param:
      -p127.0.0.1:2333:22 
        ip  mapping_prot ssh_internal_port
  
```
