

Federated learning -> train shared models while retaining security, privacy and control of data
A local model is trained with local data, then an update is sent to the centralized cloud server.

Differential privacy: publicly sharing information about a dataset by describing patterns within groups of individuals within the dataset while withholding information about each individual
As far as i understand it, it's a framework, not an algorithm

Format-preserving encryption (FPE) -> an encryption algorithm that preserves the format of information

Tokenization: a piece of sensitive data, such as a credit card number, is replaced by a surrogate value known as a token. The sensitive data still needs to be stored securely at one centralized location for subsequent reference

FPE -> obfuscates sensitive information
Tokenization -> completely removes it (storing it in another place)

---

Google Cloud Data Loss Prevention API (DLP)
detects sensitive data in content and then uses a transformation to mask, delete or obscure the data

Many de identification techniques:
- masking (partially or fully replacing characters with a symbol)
- replace with a token
- encrypting and replacing with a randomly generated key
- bucketing

---

The Google Cloud Healthcare API has the de-identify operation, which removes PHI or otherwise sensitive information from healthcare data

---

Another method is PCA

This method can be quite robust because even if one identifies individuals who are unique in some way, it is hard to determine without an explanation of the PCA vector formula what makes them unique

Coarsening is also an option to decrease the granularity of data in order to make it more difficult to identify sensitive data within the dataset