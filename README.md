# Quick Repository

apt-get update
apt-get install -y build-essential ruby ruby-dev sudo wget

wget http://rock-robotics.org/autoproj_bootstrap
# If you have no write access to this repository:
ruby autoproj_bootstrap git https://github.com/H2020-InFuse/cdff-buildconf.git branch=cdff_dev
# If you have write access:
ruby autoproj_bootstrap git git@github.com:H2020-InFuse/cdff-buildconf.git branch=cdff_dev
# Answer "whether C++11 should be enabled for Rock packages [false]" with "true" and the
# other with default (just hit enter)

source env.sh
autoproj update
autoproj build

