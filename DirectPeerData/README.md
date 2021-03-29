Direct Peer Data is computed using a daily RIB download from all RouteViews and RIPE BGP collector's data and RPKI ROA validity statud from RIPE rpki-validator validated ROAs (https://rpki-validator.ripe.net/roas).
We call Direct Peers the ASNs sending BGP data to the collectors (they are sometimes called vantage point ASNs).
Prefix-origin ASN pairs are extracted for all direct peers and their RPKI status is computed using the valid ROAs sync that day using the procedure described in RFC 6483 (https://tools.ietf.org/html/rfc6483).

The files have 9 tab-separated columns:
- direct_peer: ASN of direct peer
- v4_valid: Number of IPv4 prefix-origin ASN pairs from the direct peer ASN RIB data that are valid according to valid ROAs.
- v4_invalidLenght: Number of IPv4 prefix-origin ASN pairs from the direct peer ASN RIB data that are invalid because of the Max Length Attirbute according to the ROA data.
- v4_invalidASN: Number of IPv4 prefix-origin ASN pairs from the direct peer ASN RIB data that are invalid because of the origin ASN according to the ROA data.
- v4_unknown: Number of IPv4 prefix-origin ASN pairs from the direct peer ASN RIB data that are not covered by any valid ROAs (i.e. RPKI status 'unknown').
- v6_valid: Number of IPv6 prefix-origin ASN pairs from the direct peer ASN RIB data that are valid according to valid ROAs.
- v6_invalidLenght: Number of IPv6 prefix-origin ASN pairs from the direct peer ASN RIB data that are invalid because of the Max Length Attirbute according to the ROA data.
- v6_invalidASN: Number of IPv6 prefix-origin ASN pairs from the direct peer ASN RIB data that are invalid because of the origin ASN according to the ROA data.
- v6_unknown: Number of IPv6 prefix-origin ASN pairs from the direct peer ASN RIB data that are not covered by any valid ROAs (i.e. RPKI status 'unknown').
