# Change Log

An overview of changes:

## [0.3.0]

Requires `cmake` to build now.

This release updates `audiopus_sys` to `0.3`, bringing following
changes to this high-level crate:

### **Added:**

* Windows will build Opus instead of using pre-built Opus.

### **Fixed:**

* Cross-compiling should work now.

### **Removed:**

* Pre-built Windows binaries are no longer provided.

## [0.2.0]

This release fixes an API inconsistency by introducing one breaking change.

The `input` on `Decoder::decode_float` must be `Option<TP>`,
to be consistent with the `Decoder::decode`-method.
This allows users to provide a null raw pointer by passing `None`.

## [0.1.3]

The `Decoder` implements `Send` now, to be consistent with `Encoder`.

### **Added:**

* Implement `Send` for `Decoder`.

## [0.1.2]

This release contains a critical fix for `SoftClip::apply`.

### **Fixed:**

* Fixed potential Segfault caused by `SoftClip::apply`.
* A typo.

## [0.1.1]

### **Added:**

* Implements `std::error::Error` for `Error` and `ErrorCode`.


