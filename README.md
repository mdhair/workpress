# Workpress
### A "Work Box" for Wordpress
A work box, as defined by a Google search, means "a portable box used for storing or holding tools"`. And that is what I intend Workpress to be; a protable box used for storing all my favorite Wordpress development tools.

Workpress is a simple Vagrant base box running Ubuntu 14.04 and targeted for Wordpress development. Workpress is intended for Wordpress developers (like me) that would love to have a simple Vagrant box that installs Wordpress and all their favorite development tools. It is for people that find other great projects such as [VVV](https://github.com/Varying-Vagrant-Vagrants/VVV), [VCCW](https://github.com/vccw-team/vccw), and [Scotch Box](https://github.com/scotch-io/scotch-box) a little too bulky for their work.

### Installation
*Note: If you have already downloaded my box from [Hashicorp Atlas](https://atlas.hashicorp.com/jalenconner/boxes/workpress), please note that you will need to follow the below installation instructions to get it properly running. If you haven't downloaded it yet, please do NOT do so. It is much easier to do so here...*

1. Install VirtualBox - https://www.virtualbox.org/
1. Install Vagrant - http://www.vagrantup.com/
    * Verify Vagrant installed by running `vagrant -v` in your terminal.
1. Download Workpress:
    * Download and extract the GitHub repository - https://github.com/jalenconner/workpress/archive/master.zip
    * Clone the Github repository - `git clone https://github.com/jalenconner/workpress.git`
1. Navigate to the folder you just downloaded and run `vagrant up` in your terminal. Please by patient; it always take a little time to download and boot up the VM the first time.
1. Visit http://192.168.33.10 in your browser and you will see the Wordpress 5-min installation page.
1. Follow the on-screen guide to setup your Wordpress installation settings.
1. That's it! Where you expecting more?

### Usage
Workpress is setup to use the IP address of 192.168.33.10. If this IP is conflicting with something on your network, you may change it in the Vagrantfile to the IP address of your choosing and then run `vagrant reload` in your terminal.

Also, you may add your own shared folders to the Vagrant file, but please do not change or remove the synced folders already specified. Doing so will (may?) break Apache and the ability to view your Wordpress site in your browser.

##### Basic Vagrant Commands
Start or resume your server - `vagrant up`

Pause your server - `vagrant suspend`

Turn off your server - `vagrant halt`

SSH into your server - `vagrant ssh`

### What's Installed

* [Ubuntu Server 14.04.3 LTS (64-bit; Trusty Tahr)](http://www.ubuntu.com/server)
* [Apache 2.4.x](https://httpd.apache.org)
* [PHP 5.5.x](https://www.php.net/)
* [MYSQL 5.5.x](https://www.mysql.com)
* [Ruby 1.9.3](https://www.ruby-lang.org/en/)
* [Sass 3.4.x](http://sass-lang.com)
* [Vim 7.4.x](http://www.vim.org)
* [Git 1.9.x](https://git-scm.com)
* [Wget 1.x](https://www.gnu.org/s/wget/)
* [cURL 7.35.x](http://curl.haxx.se)
* [Node.js 0.10.x](https://nodejs.org/en/)
* [npm 1.3.x](https://www.npmjs.com)
* [WP-CLI 0.21.x](http://wp-cli.org)
* [Wordpress 4.3.1](https://wordpress.org)

View the [full list of packages](https://github.com/jalenconner/workpress/blob/master/PACKAGES.md).   
Is there something that you think ought to be included here? Open an issue and let me know!

### Credentials
##### SSH Users
Username | Password
---------|---------
root | rootpass
vagrant | vagrant
##### MYSQL Users
Username | Password
---------|---------
root | rootpass
wordpressuser | wordpresspass
##### MYSQL Details
Property | Value
---------|------
database name | wordpress
database user | wordpressuser
database password | wordpresspass
database host | localhost

### Contributing
I know Workpress definitely could use some help and I'm sure it probably has its share of bugs too... So I'd love for anyone to help assist me develop this box further. Just open an issue and let me know what it is; be it a bug, tip, feature idea, question, or anything!

### Change Log
Current Version : 1.0.0

View the full [changelog](https://github.com/jalenconner/workpress/blob/master/CHANGELOG.md).

### License
© 2015 Jalen Davenport

Apache 2.0; view [license](https://github.com/jalenconner/workpress/blob/master/LICENSE)

### Thanks
I'd like to give my thanks to [Christian Di Lorenzo](https://github.com/rcdilorenzo) for giving me the idea for the name of this project and to [Luke Holloway](https://github.com/hollowaydesignfirm) for his support and assistance.
