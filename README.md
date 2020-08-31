我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

# Lmsensorsbeat

Welcome to Lmsensorsbeat.  This Beat strives to pull data from lm-sensors so that you can monitor a variety of I2C/SMBus sensors, such as CPU/motherboard temperatures, fan speeds, voltages, etc.  To run this, you may need to:

 1. Install the lm-sensors library and headers (e.g. libsensors4-dev) for your distribution
 2. Load (modprobe) various kernel modules for your sensors if you don't already.  Once you install lm-sensors, you can usually do this automatically by running the "sensors-detect" command

Ensure that this folder is at the following location:
`${GOPATH}/github.com/eskibars`

## Getting Started with Lmsensorsbeat

### Init Project
To get running with Lmsensorsbeat, run the following commands:

```
glide update --no-recursive
make update
```


To push Lmsensorsbeat in the git repository, run the following commands:

```
git init
git add .
git commit
git remote set-url origin https://github.com/eskibars/lmsensorsbeat
git push origin master
```

For further development, check out the [beat developer guide](https://www.elastic.co/guide/en/beats/libbeat/current/new-beat.html).

### Build

To build the binary for Lmsensorsbeat run the command below. This will generate a binary
in the same directory with the name lmsensorsbeat.

```
make
```


### Run

To run Lmsensorsbeat with debugging output enabled, run:

```
./lmsensorsbeat -c lmsensorsbeat.yml -e -d "*"
```


### Test

To test Lmsensorsbeat, run the following commands:

```
make testsuite
```

alternatively:
```
make unit-tests
make system-tests
make integration-tests
make coverage-report
```

The test coverage is reported in the folder `./build/coverage/`


### Update

Each beat has a template for the mapping in elasticsearch and a documentation for the fields
which is automatically generated based on `etc/fields.yml`.
To generate etc/lmsensorsbeat.template.json and etc/lmsensorsbeat.asciidoc

```
make update
```


### Cleanup

To clean  Lmsensorsbeat source code, run the following commands:

```
make fmt
make simplify
```

To clean up the build directory and generated artifacts, run:

```
make clean
```


### Clone

To clone Lmsensorsbeat from the git repository, run the following commands:

```
mkdir -p ${GOPATH}/github.com/eskibars
cd ${GOPATH}/github.com/eskibars
git clone https://github.com/eskibars/lmsensorsbeat
```


For further development, check out the [beat developer guide](https://www.elastic.co/guide/en/beats/libbeat/current/new-beat.html).
