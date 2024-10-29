yeslogic-unicode-blocks
=======================

<div align="center">
  <a href="https://github.com/yeslogic/unicode-blocks/actions/workflows/ci.yml">
  <img src="https://github.com/yeslogic/unicode-blocks/actions/workflows/ci.yml/badge.svg" alt="Build Status"></a>
  <a href="https://docs.rs/yeslogic-unicode-blocks">
  <img src="https://docs.rs/yeslogic-unicode-blocks/badge.svg" alt="Documentation">
  </a>
  <a href="https://crates.io/crates/yeslogic-unicode-blocks">
    <img src="https://img.shields.io/crates/v/yeslogic-unicode-blocks.svg" alt="Version">
  </a>
  <img src="https://img.shields.io/badge/unicode-16.0-informational" alt="Unicode Version">
  <a href="https://github.com/yeslogic/unicode-blocks/blob/master/LICENSE">
    <img src="https://img.shields.io/crates/l/unicode-blocks.svg" alt="License">
  </a>
</div>

<br>

This is fork of [unicode-blocks](https://github.com/magiclen/unicode-blocks)
maintained by YesLogic. Differences from upstream: updated Unicode data, script
to regenerate Rust source. Original README follows:

----

This crate contains a list of all unicode blocks and provides some functions to search across them.

## Examples

#### Given a character, determine what unicode block contains it.

```rust
assert_eq!(yeslogic_unicode_blocks::BASIC_LATIN, yeslogic_unicode_blocks::find_unicode_block('A').unwrap());
```

#### Given a unicode block, determine whether it is used in CJK.

```rust
assert!(yeslogic_unicode_blocks::is_cjk_block(yeslogic_unicode_blocks::CJK_UNIFIED_IDEOGRAPHS));
```

#### Given a character, determine whether it is in CJK.

```rust
assert!(yeslogic_unicode_blocks::is_cjk('。'));
```
