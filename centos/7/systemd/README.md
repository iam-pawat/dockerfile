Buid it.
docer build --rm --no-cache -t httpd .

Launch it.
docker run --privileged --name httpd -v /sys/fs/cgroup:/sys/fs/cgroup:ro -p 80:80 -d httpd
