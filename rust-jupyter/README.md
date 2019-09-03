## Usage

Building:

    docker build -t vilunov/rust-jupyter .

Running in REPL mode:

    docker run --rm -it vilunov/rust-jupyter jupyter-console --kernel rust
