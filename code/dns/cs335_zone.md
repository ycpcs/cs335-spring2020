zone "cs335.com" {
	type master;
	file "/etc/bind/cs335.com.db";
};

zone "0.168.191.in-addr.arpa" {
	type master;
	file "/etc/bind/191.168.0.db";
};
