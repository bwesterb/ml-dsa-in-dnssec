This repo is an informal place to list implementations of DNSSEC (authoritative servers, validating resolvers, signers, ...) that support ML-DSA using codepoint 18 from [the IANA registry](https://www.iana.org/assignments/dns-sec-alg-numbers#dns-sec-alg-numbers-1) using the brief definition in [this draft](https://www.iana.org/go/draft-westerbaan-dnssec-mldsa-03).

Pull requests are welcome. This repo will probably become useless around March 2027 and may be frozen around then.

# Authoritative Servers

# Validating Resolvers

- [Cloudflare 1.1.1.1](https://blog.cloudflare.com/post-quantum-dnssec-1111/)

# Signers

# Test zones

- mldsa.huque.com (signed by Shumon Huque)

- [dnstest.dev](https://dnstest.dev) by Cloudflare includes among others

  - `valid.mldsa44.dnstest.dev` signed only by 18
  - `dual-valid.mldsa44.dnstest.dev` signed by 13 and 18
  - `downgrade.mldsa44.dnstest.dev` is like dual, but alg 18 RRsigs are stripped to test downgrade protection of validator


# Future

Peter van Dijk says "MLDSA44 will be in PowerDNS Recursor 5.5 and Auth 5.2."
See the [pull request](https://github.com/PowerDNS/pdns/pull/17773).

A [pull request](https://github.com/rthalley/dnspython/pull/1291) for the validator in dnspython.
