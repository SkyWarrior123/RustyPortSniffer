# RustyPortSniffer

A small asynchronous TCP port scanner written in Rust using `std` library.

## Usage

From the project directory, scan port 8080 on localhost:

```sh
cargo run -- --address 127.0.0.1 --start 8080 --end 8081
```

The end port is exclusive. A port is reported only if a TCP service is listening on it via
```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

Example output:

```sh
@SkyWarrior123 ➜ /workspaces/RustyPortSniffer (main) $ cargo run -- --address 127.0.0.1 --start 8080 --end 8081
	Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.02s
	 Running `target/debug/ip_sniffer --address 127.0.0.1 --start 8080 --end 8081`
.
8080 is open
```