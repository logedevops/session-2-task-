root@DESKTOP-POH0T0A:/home/logesh# useradd abi
root@DESKTOP-POH0T0A:/home/logesh# useradd dev
root@DESKTOP-POH0T0A:/home/logesh# useradd leo
root@DESKTOP-POH0T0A:/home/logesh# useradd max
root@DESKTOP-POH0T0A:/home/logesh# groupadd frnds
root@DESKTOP-POH0T0A:/home/logesh# gpasswd -a abi frnds
Adding user abi to group frnds
root@DESKTOP-POH0T0A:/home/logesh# gpasswd -M leo,max teammate
gpasswd: group 'teammate' does not exist in /etc/group
root@DESKTOP-POH0T0A:/home/logesh# groupadd teammate
root@DESKTOP-POH0T0A:/home/logesh# gpasswd -M leo,max teammate
root@DESKTOP-POH0T0A:/home/logesh# userdel dev
root@DESKTOP-POH0T0A:/home/logesh# groupdel -f frnds
root@DESKTOP-POH0T0A:/home/logesh# deluser max teammate
Removing user `max' from group `teammate' ...
Done.
root@DESKTOP-POH0T0A:/home/logesh# useradd -G teammate dev
root@DESKTOP-POH0T0A:/home/logesh# getent group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:syslog,logesh
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:logesh
fax:x:21:
voice:x:22:
cdrom:x:24:logesh
floppy:x:25:logesh
tape:x:26:
sudo:x:27:logesh
audio:x:29:logesh
dip:x:30:logesh
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
gnats:x:41:
shadow:x:42:
utmp:x:43:
video:x:44:logesh
sasl:x:45:
plugdev:x:46:logesh
staff:x:50:
games:x:60:
users:x:100:
nogroup:x:65534:
systemd-journal:x:101:
systemd-network:x:102:
systemd-resolve:x:103:
crontab:x:104:
messagebus:x:105:
systemd-timesync:x:106:
input:x:107:
sgx:x:108:
kvm:x:109:
render:x:110:
syslog:x:111:
uuidd:x:112:
tcpdump:x:113:
_ssh:x:114:
admin:x:115:
netdev:x:116:logesh
logesh:x:1000:
abi:x:1001:
leo:x:1003:
max:x:1004:
teammate:x:1006:leo,dev
dev:x:1005:
