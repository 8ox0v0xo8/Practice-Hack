# Burp Suite 抓包 MuMu12

导出证书 bp.der

```bash
openssl x509 -inform DER -in bp.der -out bp.pem

openssl x509 -inform PEM -subject_hash_old -in bp.pem
```

出现 9a5ba575 正确：

```bash
9a5ba575
-----BEGIN CERTIFICATE-----
MIIDqDCCApCgAwIBAgIFANofM/MwDQYJKoZIhvcNAQELBQAwgYoxFDASBgNVBAYT
C1BvcnRTd2lnZ2VyMRQwEgYDVQQIEwtQb3J0U3dpZ2dlcjEUMBIGA1UEBxMLUG9y
dFN3aWdnZXIxFDASBgNVBAoTC1BvcnRTd2lnZ2VyMRcwFQYDVQQLEw5Qb3J0U3dp
Z2dlciBDQTEXMBUGA1UEAxMOUG9ydFN3aWdnZXIgQ0EwHhcNMTQwNjIyMDY1MzA4
WhcNMzQwNjIyMDY1MzA4WjCBijEUMBIGA1UEBhMLUG9ydFN3aWdnZXIxFDASBgNV
BAgTC1BvcnRTd2lnZ2VyMRQwEgYDVQQHEwtQb3J0U3dpZ2dlcjEUMBIGA1UEChML
UG9ydFN3aWdnZXIxFzAVBgNVBAsTDlBvcnRTd2lnZ2VyIENBMRcwFQYDVQQDEw5Q
b3J0U3dpZ2dlciBDQTCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBAN+e
A6SVUaIi3wt4GfRQh5aq7Qa+y+ijxSKQGA18yNxNuq6PsyYPrX0t1kEscB3CnyBr
4vkMLl7KhXkiYZVoyesd117AO3vQqddSY+zoT57LGZBUXm4RNEROOz/KZwosbT+V
JEHMFe/Zvo7pvEVsIRA/fRFGakDBwalKzeA5ryQ7n7Mm1BF0bwzyXJBgv64uRGn+
8kSwd70Kqc2Jx6CWt5qZ8igjcFYwbAEdJNEOryLbtiv7dzlFsojAf+5q10L5S5Yy
FJaPO7SwOPG2Z81lPY9593LGNplstAXMCZNLTl8LN3T08oJfauXEAcXl5T5h6PzO
EG75NkkWuBD0CWVhZiUCAwEAAaMTMBEwDwYDVR0TAQH/BAUwAwEB/zANBgkqhkiG
9w0BAQsFAAOCAQEAULLpMdGwUR3eCB7ZgRtj4PIQFTR3wFxY3LPC1JSTSpYUjSwy
V/EtsdHWdq5i+YBZTXJkf4jdIPNcx5dijj2LxGA4p49r+Bvg8MvEcPac2O/ugavO
ZqRPKi6QLzASODfNDCZLGUyy1vWL1WKoUBRCs9m/eFqwr24SeO5TxOxI421KWJdA
7tTyA1f5pClIo2HZ+P++ventiCeWuth59BNMaajgxFPZloThORXdFe4odw7yxz57
0lD1Gxn7DO0uesXl31ZR3BLdkpHYNTLopL2MZVAsOX8r8ezGhTG3YGbXBvzoaPMO
+Bbvk+8FtkTyMEaxrEb8nSSKQ80w6kYdog1efw==
-----END CERTIFICATE-----
```

将 bp.pem 重命名 9a5ba575.0 上传 MuMu12 /system/etc/security/cacerts/ 修改权限 777
