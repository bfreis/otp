# otp - One Time Password generation with Bash

This script generates Hash-based One Time Passwords (HOTP) and Time-based One Time Passwords (TOTP).

It's written in bash, and has a minimal set of dependencies.

HMACs are calculated with OpenSSL, and date/string manipulation is done with GNU coreutils.

## Installation

To install, simply put the `otp` script in your `$PATH`.

Make sure to install the required dependencies. This has been tested with dependencies installed by Homebrew on Mac and Linuxbrew on Amazon Linux.

After installing Homebrew or Linuxbrew, simply run:

    brew install coreutils openssl bash

## Status

The script implements HOTP and TOTP, with arbitrary number of digits, and supports multiple hashing algorithms. It passes all the tests from the specs, including sha1, sha256, and sha512 TOTPs.

The script parses cmd line arguments, and generates HOTP and TOTP values according to the otp options specified.

To see what options are available, try:

    ./otp --help

## Roadmap

- Implement generating a few past and future TOTP codes (to help with sync)

- Implement URI parsing

- Implement STDIN processing

The stdin use case is intended to allow easy integration with command-line based secret storage, such as https://www.passwordstore.org/, or https://github.com/lastpass/lastpass-cli.

## Specs

- HOTP: https://tools.ietf.org/html/rfc4226

- TOTP: https://tools.ietf.org/html/rfc6238



