```bash

grpcurl -d '{"a_given_json_attribute": "'$1'"}' \
-plaintext \
-emit-defaults \
-import-path /Users/auser-mac/Documents/repos/aProtoDirectory/protoSomething/theDir \
-import-path /Users/auser-mac/Documents/repos/anotherProtoDirectory/protoSomethingElse/theDir \
-proto theactualprotofile.proto \
-H 'A_HEADER_KEY: a-header-value' \
localhost:8090 the.package.name.of.the.ProtoObjectWanted/TheMethodToCall | tr -d '\n'

```
