# Secure Smart Grid Industrial Control Systems

**Cryptographic encryption, anomaly detection, and classification for Smart Grid ICS** — code accompanying a journal paper. The notebooks cover a hybrid cryptographic scheme for securing smart-grid communications, cryptanalysis against it, and ML pipelines for anomaly classification and zero-day attack detection on industrial control traffic.

## Notebooks

| Notebook | Contents |
|---|---|
| `ENCRYPTION AND DECRYPTION.ipynb` | Hybrid encryption scheme built on **ECC + HKDF** (elliptic-curve key agreement → HKDF-derived keys → symmetric cipher) for smart-grid payloads |
| `HKPE COMPARISION.ipynb` | Benchmarks of the proposed hybrid scheme against baseline ciphers |
| `CRYPTANALYSIS.ipynb` | Security analysis / attack evaluation of the proposed scheme |
| `ANOMALY DETECTION.ipynb` | Unsupervised/ML anomaly detection on smart-grid ICS traffic |
| `CLASSIFICATION.ipynb` | Supervised attack classification (Random Forest pipeline with ROC/AUC evaluation) |
| `DNP3 CLASSIFICATION.ipynb` | Classification of **DNP3** protocol traffic |
| `STATISTICAL TESTS.ipynb` | Statistical validation of results |
| `ZERODAY.ipynb` | Zero-day / unseen-attack scenario evaluation |

> The notebooks ship inside `JOURNAL CODES.zip` — extract it to run them:
> ```bash
> unzip "JOURNAL CODES.zip"
> ```

## Requirements

- Python 3.8+
- `cryptography` (ECC, HKDF, symmetric ciphers)
- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `tqdm`

```bash
pip install cryptography pandas numpy scikit-learn matplotlib seaborn tqdm
```

## Usage

Each notebook is self-contained: extract the zip, launch Jupyter, and run the notebooks in the order listed above. Classification/anomaly notebooks expect the paper's smart-grid ICS dataset.

## Citation

This code accompanies a journal paper — if you use it, please cite the associated publication.
