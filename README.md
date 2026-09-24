# protocols-fun

Interactive, byte-level anatomy pages for network protocols across the
stack - modern (TCP, UDP, ICMP, ARP, DHCP, BGP, SNMP) and eventually
obscure/legacy (IPX, POCSAG, SITOR, ARPANET IMP-IMP, and whatever else
turns out to be worth breaking down byte by byte).

Hosted at https://protocols.databurn.org/ (GitHub Pages, from this repo).

Sibling repos: [ipv6-fun](https://github.com/hed0rah/ipv6-fun) covers
IPv6/ICMPv6/NDP in depth with its own interactive pages - this repo
covers everything else, and cross-links back to ipv6-fun rather than
duplicating it. [namespaces-fun](https://github.com/hed0rah/namespaces-fun)
and [bpf-fun](https://github.com/hed0rah/bpf-fun) are the other members
of this family.

## What's Here

```
index.html          the hub - an OSI-layers-as-subway-map view of every protocol here
tcp/tcp-anatomy.html TCP: fixed header, flags (1981 vs the 2001 ECN bits), options
```

Each protocol page uses one shared engine (hover a field to light its
bytes and read the decode, click a field marked `+` for its lookup
table) but its own distinct palette - deliberately different from both
`ipv6-fun`'s pages and the `acidcat` audio-format anatomy pages, even
though all three share the same underlying design language.

Where a protocol has a historically significant revision that changed
its wire format or behavior (TCP's flags byte gaining ECN bits in 2001;
more as they come up), that revision gets its own tab rather than a
footnote - the goal is to show what changed and when, not just the
current state.

## Where the pages are edited

The pages are written in
[hed0rah.github.io](https://github.com/hed0rah/hed0rah.github.io)'s
`protocols-fun/` directory and mirrored here, and this repo is what GitHub
Pages serves at protocols.databurn.org. hed0rah.github.io/protocols-fun/
redirects to it. The mirror keeps this repo's own `README.md`, `CNAME`
and `.gitignore`.

## Requirements

None to view - every page is self-contained HTML/CSS/JS. RFC citations
are linked inline; see each page's own References section.
