# Halo2 KZG SRS

A tool to convert KZG SRS in other formats to [`summa-dev/summa-solvency - V3`](https://github.com/summa-dev/summa-solvency/tree/v3) format that includes more g2 points than [`pse/halo2`](https://github.com/privacy-scaling-explorations/halo2).

Currently supported and WIP formats are:

- [ ] [Perpetual Powers of Tau](https://github.com/privacy-scaling-explorations/perpetualpowersoftau)
- [x] [SnarkJS](https://github.com/iden3/snarkjs)

## Download the converted SRS

Since the conversion of large SRS takes much time to run, here are the converted SRS downloadable directly. There are also simple tests ran in CI to validate these converted SRS are well formed (same ration testing with the source).

Note that `pse/halo2` has been updated to read/write in raw format by default since [PR#111](https://github.com/privacy-scaling-explorations/halo2/pull/111).

| Curve   | Source  | K    | File in raw format                |
| ------- | ------- | ---- | --------------------------------- |
| `bn254` | `hermez`| `1`  | hermez-raw-1-extended             |
| `bn254` | `hermez`| `2`  | hermez-raw-2-extended             |
| `bn254` | `hermez`| `3`  | hermez-raw-3-extended             |
| `bn254` | `hermez`| `4`  | hermez-raw-4-extended             |
| `bn254` | `hermez`| `5`  | hermez-raw-5-extended             |
| `bn254` | `hermez`| `6`  | hermez-raw-6-extended             |
| `bn254` | `hermez`| `7`  | hermez-raw-7-extended             |
| `bn254` | `hermez`| `8`  | hermez-raw-8-extended             |
| `bn254` | `hermez`| `9`  | hermez-raw-9-extended             |
| `bn254` | `hermez`| `10` | hermez-raw-10-extended            |
| `bn254` | `hermez`| `11` | hermez-raw-11-extended            |
| `bn254` | `hermez`| `12` | hermez-raw-12-extended            |
| `bn254` | `hermez`| `13` | hermez-raw-13-extended            |
| `bn254` | `hermez`| `14` | hermez-raw-14-extended            |
| `bn254` | `hermez`| `15` | hermez-raw-15-extended            |
| `bn254` | `hermez`| `16` | hermez-raw-16-extended            |
| `bn254` | `hermez`| `17` | hermez-raw-17-extended            |
| `bn254` | `hermez`| `18` | hermez-raw-18-extended            |
| `bn254` | `hermez`| `19` | hermez-raw-19-extended            |
| `bn254` | `hermez`| `20` | hermez-raw-20-extended            |
| `bn254` | `hermez`| `21` | hermez-raw-21-extended            |
| `bn254` | `hermez`| `22` | hermez-raw-22-extended            |
| `bn254` | `hermez`| `23` | hermez-raw-23-extended            |
| `bn254` | `hermez`| `24` | hermez-raw-24-extended            |
| `bn254` | `hermez`| `25` | hermez-raw-25-extended            |
| `bn254` | `hermez`| `26` |                                   |

## Manually convert from the source

### Perpetual Powers of Tau

To get SRS with `k = 10` from latest response of Perpetual Powers of Tau, we can run:

```shell
wget https://ppot.blob.core.windows.net/public/response_0071_edward
mkdir ./srs
cargo run --release --bin convert-from-perpetual-powers-of-tau response_0071_edward ./srs/perpetual-powers-of-tau-raw- 10
```

Then it will output the SRS with `1 <= k <= 10` with path `./srs/perpetual-powers-of-tau-raw-{k}`.

### SnarkJS

To get SRS with `k = 10` from Hermez's setup, we can run:

```shell
wget https://hermez.s3-eu-west-1.amazonaws.com/powersOfTau28_hez_final_10.ptau
mkdir ./srs
cargo run --release --bin convert-from-snarkjs powersOfTau28_hez_final_10.ptau ./srs/hermez-raw- 10
```

Then it will output the SRS with `1 <= k <= 10` with path `./srs/hermez-raw-{k}`.
