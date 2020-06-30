# Profiling iglü server

iglü server has a profiler running by default, which you may check at
`https://local.nacdlow.com[:8080]/debug/pprof/`.  

You may use `go tool pprof` to further analyse this, generating a graph of all
function calls and how long they take. You will need `graphviz` package
installed on your system to do this.

## Running the profiler

1. Compile the server using `make` (don't use `go run`!).
2. Run the server `./nacdlow-server run`
3. Do whatever you want, use the features you want to be profiled.
4. Once you are done, run `go tool pprof nacdlow-server https://local.nacdlow.com:8080/debug/pprof/profile`.
5. You'll get a pprof shell, type `web` to run the web interface (this is
	different than the previous!).
6. View the profiler graph on the browser!


