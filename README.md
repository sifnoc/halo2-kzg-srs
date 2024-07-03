# Halo2 KZG SRS

A tool to convert KZG SRS in other formats to [`summa-dev/summa-solvency - V3`](https://github.com/summa-dev/summa-solvency/tree/v3) format that includes more g2 points than [`pse/halo2`](https://github.com/privacy-scaling-explorations/halo2).

Currently supported and WIP formats are:

- [ ] [Perpetual Powers of Tau](https://github.com/privacy-scaling-explorations/perpetualpowersoftau)
- [x] [SnarkJS](https://github.com/iden3/snarkjs)

## Download the converted SRS

Since the conversion of large SRS takes much time to run, here are the converted SRS downloadable directly. There are also simple tests ran in CI to validate these converted SRS are well formed (same ration testing with the source).

Note that `pse/halo2` has been updated to read/write in raw format by default since [PR#111](https://github.com/privacy-scaling-explorations/halo2/pull/111).

| Curve   | Source  | K    | File in raw format                                                                                                   |
| ------- | ------- | ---- | -------------------------------------------------------------------------------------------------------------------- |
| `bn254` | `hermez`| `1`  | [hermez-raw-extended-1](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-1)             |
| `bn254` | `hermez`| `2`  | [hermez-raw-extended-2](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-2)             |
| `bn254` | `hermez`| `3`  | [hermez-raw-extended-3](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-3)             |
| `bn254` | `hermez`| `4`  | [hermez-raw-extended-4](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-4)             |
| `bn254` | `hermez`| `5`  | [hermez-raw-extended-5](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-5)             |
| `bn254` | `hermez`| `6`  | [hermez-raw-extended-6](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-6)             |
| `bn254` | `hermez`| `7`  | [hermez-raw-extended-7](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-7)             |
| `bn254` | `hermez`| `8`  | [hermez-raw-extended-8](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-8)             |
| `bn254` | `hermez`| `9`  | [hermez-raw-extended-9](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-9)             |
| `bn254` | `hermez`| `10` | [hermez-raw-extended-10](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-10)           |
| `bn254` | `hermez`| `11` | [hermez-raw-extended-11](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-11)           |
| `bn254` | `hermez`| `12` | [hermez-raw-extended-12](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-12)           |
| `bn254` | `hermez`| `13` | [hermez-raw-extended-13](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-13)           |
| `bn254` | `hermez`| `14` | [hermez-raw-extended-14](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-14)           |
| `bn254` | `hermez`| `15` | [hermez-raw-extended-15](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-15)           |
| `bn254` | `hermez`| `16` | [hermez-raw-extended-16](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-16)           |
| `bn254` | `hermez`| `17` | [hermez-raw-extended-17](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-17)           |
| `bn254` | `hermez`| `18` | [hermez-raw-extended-18](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-18)           |
| `bn254` | `hermez`| `19` | [hermez-raw-extended-19](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-19)           |
| `bn254` | `hermez`| `20` | [hermez-raw-extended-20](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-20)           |
| `bn254` | `hermez`| `21` | [hermez-raw-extended-21](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-21)           |
| `bn254` | `hermez`| `22` | [hermez-raw-extended-22](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-22)           |
| `bn254` | `hermez`| `23` | [hermez-raw-extended-23](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-23)           |
| `bn254` | `hermez`| `24` | [hermez-raw-extended-24](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-24)           |
| `bn254` | `hermez`| `25` | [hermez-raw-extended-25](https://summa-solvency.s3.eu-central-1.amazonaws.com/trusted-setup-hyperplonk2kzg/hermez-raw-extended-25)           |
| `bn254` | `hermez`| `26` |                                                                                                                      |
| `bn254` | `hermez`| `27` |                                                                                                                      |

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
