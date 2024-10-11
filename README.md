# GXJZY Campus Network Research
This repository contains research and findings on the GXJZY campus network detection mechanisms. It is intended for individuals familiar with this network system and interested in its technical aspects.

## Detection Methods

The following detection methods have been identified for GXJZY:

> **Note**: Unchecked items indicate detection methods that have not been confirmed. While I haven't found evidence of their use, this does not mean they don't exist or won't be implemented in the future.

- [x] **HTTP User-Agent detection**
- [x] **TCP Time-to-Live detection**
- [x] **TCP Identification detection**
- [ ] **TCP Timestamp Skew Detection**
- [ ] **Deep packet inspection (DPI)**

## Solutions
**The solutions listed below are specifically designed for use with OpenWrt.**

| Detection       | Solution                                              |
|-----------------|-------------------------------------------------------|
| User-Agent      | [UA2F](https://github.com/Zxilly/UA2F)                |
| Time-to-Live    | ipopt                                                 |
| Identification  | [kmod-rkp-ipid](https://github.com/CHN-beta/rkp-ipid) |

## Instructions

In this section, I will show you how to use `gxjzy_cn` from this repository for campus login.

1. Open your browser and navigate to the campus login authentication platform.
2. If you are already logged in, please log out.
3. Press `F12` to open the developer tools, and navigate to the "Network" tab.
4. Click on **Preserve Log** to retain the network requests.
5. Log in once using your credentials.
6. Find a request targeting `/api/login.php` and record the values of the `user` and `pass` fields in the Payload (note: the `pass` should be an MD5 hash).
7. *Coming soon.*
