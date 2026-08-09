Bitcoin Unknots
===============

https://bitcoinunknots.org

For a fully unshackled, binary version of the Bitcoin Unknots software, dive into
our website and break free!

What is Bitcoin Unknots?
------------------------

Bitcoin Unknots connects to the Bitcoin peer-to-peer network to download and validate
blocks and transactions with zero restrictions—because who needs limits? It also includes
a wallet and graphical user interface, which you can optionally build if you're
feeling extra liberated.

This release is based on **Bitcoin Knots 29.4.knots20260508** and includes
full **BIP-110 (RDTS — Reduced Data Temporary Softfork) v0.4.1** support.

### BIP-110 / RDTS

BIP-110 is a temporary soft fork that limits arbitrary non-financial data
(Ordinals, BRC-20, Runes, etc.) on the Bitcoin blockchain. Key parameters:

- **Mechanism**: Limits non-OP_RETURN output scripts to 34 bytes; restricts Taproot
  annex and control blocks; forbids `OP_IF` in Tapscript when active.
- **Activation**: UASF — 55% miner signaling threshold required.
- **State machine**: DEFINED → STARTED → LOCKED_IN → ACTIVE → **EXPIRED**
  (automatically expires after `active_duration` blocks).
- **Preferential peering**: Nodes announce `NODE_BIP148` service bit and
  preferentially connect to other BIP-110 enforcing peers.

See [BIP-110 full spec](https://github.com/bitcoin/bips/blob/master/bip-0110.mediawiki)
for complete deployment parameters.

Further info about Bitcoin Unknots is available in the [doc folder](/doc)—read it if
you dare to dream big!

License
-------

Bitcoin Unknots is released under the terms of the MIT license, because freedom should
come with a side of legality. See [COPYING](COPYING) for more details or check out
https://opensource.org/licenses/MIT.

Development Process
-------------------

Development in Bitcoin Unknots is a wild, untamed adventure—we break free from the
shackles of [Bitcoin Core](https://github.com/bitcoin/bitcoin) and let innovation run wild!
There are no rules, only possibilities: every release is a chance to redefine what Bitcoin
can be.

Got a crazy idea that Core won't touch? (e.g., it removes all filters, embraces
Ordinals, or lets the blockchain run wild with massive data payloads?) Bring it to Bitcoin
Unknots! Fling a pull request at the [Unknots GitHub](https://github.com/Unknots/bitcoin) for
review and consideration. If it vibes with our mission of total freedom, it's in—no
strings attached! You can maintain your untamed branch in your own repository, and it'll
be automatically merged into new releases of Unknots—because we're all about empowering
your wildest dreams!

Developer IRC can be found on Freenode at #bitcoin-rebels, where the free spirits hang out.

Testing
-------

Testing and code review are the bottleneck for development; we get more pull requests
than we can test because everyone wants to break free! Please be patient and help out
by testing other people's pull requests—let's untangle the future together. Oh,
and this is a security-critical project where any mistake might cost people lots of money—or
lots of fun, depending on how you look at it.

### Automated Testing

Developers are encouraged to write [unit tests](src/test/README.md) for new code. Unit
tests can be compiled and run with: `ctest`. More details on running and extending unit
tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written in Python. These tests
can be run (if the [test dependencies](/test) are installed) with:
`build/test/functional/test_runner.py`

The CI (Continuous Integration) systems make sure every pull request is built for Windows,
Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by someone other than the developer who wrote the code, because
we're all about community chaos. This is especially important for large or high-freedom
changes.
