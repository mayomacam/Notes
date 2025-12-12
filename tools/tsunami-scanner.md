`docker pull ghcr.io/google/tsunami-scanner-full`

# Run the image
`docker run -it --rm ghcr.io/google/tsunami-scanner-full bash`

# If you want to use Python plugins
```
tsunami-py-server >/tmp/py_server.log 2>&1 &
or
tsunami-py-server --ip=0.0.0.0 --port=34567 >/tmp/py_server.log 2>&1 &
```
# If you want to use the callback server
```
tsunami-tcs >/tmp/tcs_server.log 2>&1 &`
or
tsunami-tcs --server_address=0.0.0.0 --server_port=61000 >/tmp/tcs_server.log 2>&1 &
```

# Run Tsunami
# Note: If you did not start the python server, omit the `--python-` arguments.
` tsunami --ip-v4-target=127.0.0.1 --python-plugin-server-address=127.0.0.1 --python-plugin-server-port=34567`




