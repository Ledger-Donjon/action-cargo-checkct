# cargo-checkct GitHub Actions

This GitHub Actions runs [cargo-checkct](https://github.com/Ledger-Donjon/cargo-checkct/) on your code.

## Usage

```yml
uses: Ledger-Donjon/action-cargo-checkct@v1
with:
    directory: ./target_workspace
    binsec-version: 0.10.0
    unisim-version: 0.0.10
    cargo-checkct-ref: f7bc61f5ad08dedece61ec199911f6ecd3272eeb
    skip_unknown: false
    timeout: 600
```

Or if using the default parameters values:
```yml
uses: Ledger-Donjon/action-cargo-checkct@v1
with:
    directory: ./target_workspace
```

*Note: This composite action only runs on `ubuntu-latest` based workflows.* 

### Parameter: directory

Path to the target workspace (containing the `checkct` directory).

This parameter is mandatory. 


### Parameter: binsec-version

Enforce the `binsec` version used.

This parameter is optional. By default the latest `binsec` version will be used.


### Parameter: unisim-version

Enforce the `unisim-archsec` version used.

This parameter is optional. By default the latest `unisim-archsec` version will be used.


### Parameter: cargo-checkct-ref

Enforce the `cargo-checkct` reference used.

This parameter is optional. By default the a commit is fixed to a tested `cargo-checkct` version
for the default `binsec` and `unisim-archsec` versions. But it could also be set to `main` for instance.


### Parameter: skip_unknown

Do not raise an error if `binsec` cannot conclude on the tested implementation.

This parameter is optional. By default, the flag is not set (`false`).


### Parameter: timeout

Set a timeout in seconds.

This parameter is optional. By default, the timeout will be set to 10 minutes (600 seconds).


## License

Licensed under the Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or <http://www.apache.org/licenses/LICENSE-2.0>) or the MIT license ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>), at your option.
